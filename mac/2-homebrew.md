# Homebrew

Homebrew is a tool that simplifies installing applications on your machine. Think of it like an app store for your computer.

---

## Verify if Homebrew is already installed

**_If this is your first time going through the setup guide on your current machine, skip this "Verify" section and move on to the "Install" section below_**

In your terminal, run:

- `brew --version`

> **IF** the output is similar to:
>
> ```text
> Homebrew 3.4.11
> ```
>
> Run the command:
>>
> - `brew update`
>
> to get latest updates, and move on to the [next page](./3-git.md)
>
> ---
> **else if** the output is not similar to the above:
>
> Continue with instructions on this page.

---

## Install Homebrew

In your terminal, run the following command:

- `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

You will be prompted several times along the way.

Enter your password when prompted, accept all the defaults, say "Yes" if prompted. (**_Note:_** _You will not have any visual feedback on your screen as you type your password. It is protecting your password by not displaying ANYTHING at all to the screen, but it is registering your key strokes._)

You will likely be prompted to install XCode command line tools. Select "Yes".

Once the main installation finishes (could take up to 30 minutes), **look at the output at the bottom of your terminal.** You may see an arrow pointing to **"Next steps:"** instructions. They would look similar to the image below.

![Homebrew No Next Steps example](../images/homebrew-next-steps.png)

Run the commands shown in your terminal one at a time - they should produce no errors, and do not produce success messages.

Once that step is completed, **run:**

- `brew doctor`

> **IF** the return output is:
>
> ```text
> Your system is ready to brew
> ```
>
> **OR** the return output is:
>
> ```text
> Please note that these warnings are just used to help the Homebrew maintainers with debugging if you file an issue. If everything you use Homebrew for is working fine: please don't worry or file an issue; just ignore this. Thanks!
> ```
>
> **then**  run the command:
>
> - `brew update`
>
> ---
> **else if** the return output is:
>
> ```text
> brew: command not found
> ```
>
> **then** run these commands
>
> - `` echo 'eval "$(`which brew` shellenv)"' >> $HOME/.zshrc ``
> - `` eval "$(`which brew` shellenv)" ``
> - `reset`
>
> and start the sequence over from the `brew doctor` step one more time

**If `brew doctor` still fails to run, [click here](../../error/error.md) and do not continue with the following steps until you have Homebrew properly installed**

When that completes, you will be returned to the command prompt and can move on to the next steps.

---

### [⇐ Previous](./1-environment.md) | [Next ⇒](./3-git.md)
