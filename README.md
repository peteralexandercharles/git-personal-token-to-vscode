# How to add github personal access token to visual studio code

> I received an email saying Github will require token authentication after August 13 2021. I want to ensure I don't have an interruption of service (push/pull) after this date.
So I logged into Gith...

I received an [email](https://github.blog/2020-12-15-token-authentication-requirements-for-git-operations/) saying Github will require token authentication after August 13 2021. I want to ensure I don't have an interruption of service (push/pull) after this date. So I logged into Github and [created a token](https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token) for my single repo.

Now I want to use the token to push/pull my repo from Github, in Visual Studio Code, which uses git and the command line, which I have installed on my Mac.

**QUESTION** - What do I do to add/replace the password from Github with the generated token I just created to push/pull from my repo? Can I do it from Visual Studio Code or does it get added from the terminal command line?


Tried these steps and can now check in code via VSCode error free (note this approach uses Microsoft Git Credential Manager Core - see [here](https://docs.github.com/en/get-started/getting-started-with-git/caching-your-github-credentials-in-git)):


![](https://www.gravatar.com/avatar/8266f1b38502046425bc1a947fec1721?s=64&d=identicon&r=PG)


[snowbound](chrome-extension://cjedbglnccaioiolemnfhjncicchinao/users/1175956/snowbound)snowbound

1,5522 gold badges17 silver badges27 bronze badges

copy following line and past it into your vs code terminal

    git remote set-url origin https://<TOKEN>@github.com/<USERNAME>/<REPOSITORYNAME>.git
    

replace TOKEN with your token USERNAME with username and REPOSITORYNAME with your repository this should work your final line should look something like

    git remote set-url origin https://asdlkuresdflj23433423lj234@github.com/brother/sampleapp.git
    

answered Sep 30 at 18:18


To create code blocks or other preformatted text, indent by four spaces or surround 
[Source](https://stackoverflow.com/questions/66231282/how-to-add-github-personal-access-token-to-visual-studio-code)