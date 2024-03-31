# dinhanhthi.com

Next.js 14+ 🤝 Tailwind CSS 🤝 Notion as CMS 🤝 [notion-x](https://github.com/dinhanhthi/notion-x).

🎉 The step-by-step tutorial to create a website like this is [HERE](https://dinhanhthi.com/note/how-to-create-a-site-like-this/) (🚨 This tut is corresponding to [**v6.1.3**](https://github.com/dinhanhthi/dinhanhthi.com/releases/tag/v6.1.3))! Feel free to mention my assistance when you embark on creating your unique site. Appreciate it!

🧡 If what I do is helpful to you for some reason, please consider [supporting me](https://dinhanhthi.com/support-me/). Thank you!

> 🪖 I can duplicate my site for you at a cost of **\$20 + \$15/hour for any additional requests** (we can discuss this over a call if you prefer). Please be aware that this is a **one-time service** and does not include ongoing maintenance. If you're interested, please [email me](me@dinhanhthi.com).

🚨 There are individuals who have forked my repository and published their confidential information directly in the `.env.local` or `example.env.local` files. I urge you to please **STOP DOING THIS**, as it will expose your secret information to the world!

## Previous versions

👉 Version 1 (Jekyll): [v1.dinhanhthi.com](https://v1.dinhanhthi.com) -- [source](https://github.com/dinhanhthi/dinhanhthi.com-v1).<br />
👉 Version 2 (Jekyll): [v2.dinhanhthi.com](https://v2.dinhanhthi.com) -- [source](https://github.com/dinhanhthi/dinhanhthi.com-v2).<br />
👉 Version 3 (Jekyll): [v3.dinhanhthi.com](https://v3.dinhanhthi.com) -- [source](https://github.com/dinhanhthi/dinhanhthi.com-v3).<br />
👉 Version 4 (Gatsby, canceled at 60%): [demo of what I did](https://v4.dinhanhthi.com) -- [source](https://github.com/dinhanhthi/dinhanhthi.com-v4-gatsby).<br />
👉 Version 5 (11ty): [v5.dinhanhthi.com](https://v5.dinhanhthi.com) -- [source](https://github.com/dinhanhthi/dinhanhthi.com-v5).

## Dev

🚨 You have to install **globally** [Nodejs >=18](https://nodejs.org/en) (recommend using [nvm](https://github.com/nvm-sh/nvm)) and [Yarn](https://yarnpkg.com/) first.

```bash
# install
yarn

# clone submodule notion-x (when installing only)
git submodule update --init --recursive

# ud notion-x
git submodule update --recursive --remote
# or yarn getlib

# dev
yarn dev # port 3003

# build
yarn build

# serve (need to build first)
yarn start # port 3003

# reinstall all
yarn reinstall

# clean
yarn clean

# prettier
yarn prettier

# clear yarn cache (helpful sometimes)
yarn cache clean
```

Deploy to vercel,

```bash
vercel dev # like yarn dev

vercel build

# preview only
vercel deploy

# production
vercel --prod
```

## Update something new (for me only)

- Modify directly notion-x's components inside this repo.
- Overwrite modified files from this repo to notion-x's repo.
- Push changes from notion-x.
- On dat, make a script and run `ud_submodules`

  ```bash
  # Make sure notion-x and this repo are cloned to the same parent folder.
  alias checkout_notion-x="cd notion-x && git checkout * && cd -"
  alias ud_submodules='checkout_notion-x && git submodule update --recursive --remote'
  ```

- If there are changes from notion-x, cannot merge branch from `main` to `dev` or vice verso. We have to force reset one branch to the other!
