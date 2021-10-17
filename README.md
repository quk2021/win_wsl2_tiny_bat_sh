- Examine the content of the repo (or, just blindly trust me!)

- Then, clone the repo as a folder (directory -- we use both linux and win terms interchangeably) 
    - that is on the $PATH.
        - For exaample: $HOME/bin , 
            - which often is already set on the PATH in .profile.
                - See below "use default" rule.
- Then, you can enjoy those tiny tools.
    - Note that they are self-documenting -- which is very important.  
        - See below "self-documenting" rule.

# AI, Big-data, and Cloud perspective
 
- AI, Big-data, and Cloud (ABC) shows that "developers" should be re-invented or re-imagined. 

- First, let's take away those so-called "applications", 
    - regardless web, desktop, or phone ones,
    - let us focus on markdown and csv files. 
        - As a reslt, all are async events or micro-batchs. 
    - As a result, "developers" are the same as "data engineers" and "data scientists". 
        - So, "spark" and "notebooks" are our main tools.
            - All developers should know those tools, just as they must know RDB in the past.  
    - After we have done the prototype with markdown and csv files,
        - then, we can go back to those "applications".
      
- Second, let's think command line are just a simple "chat" application, 
    - "CLI" (scripting) is just the precursor of "chat". 
        - "Mouse clicking" is and should always be the seconary tool. 
            - In the future, because of AI, it will be less important. 
                - But "CLI" will be mixed with natural language tools.       
   
- Third -- that is, only after the first and the second, 
    - then, we have "programming", which is just more structured "chat". 
        - The structure is always "composability" or "modularity". 
            - As a result, "progrmaming" -- if it is good -- is just 
                - well-structured "chatting".   

    - With enough and the right data, all good programming should have an element of 
        - "AI engineering".  

# About "use default" and "self documenting"

- "Use default" can make us more open to the community, and, to changes and new environments. 
    - If every time you do 'pair programming', you have to configure the environment ...

- "Self documenting" is to use the folder structure and simple scripting to document. 
    - Here, the word "simple" is VERY important.
        - Complex scripting is serious programming, not "scripting per se".
            - Even "serious programming", we have "modularity" and "composability". 
- Those two contradict each other; so, balance is the key. 
    - "Default" can change and after they are changed, they are forgotten; 
        - so, not "self documenting". 
    - Also, "use default" needs many ad hoc techniques; 
        - so, even more not "self documenting".
    
- For example, the way I used to set up vim, 
    - is to use consecutive 'j' 'k' to switch to 'normal mode'.
    - And a few other config, e.g., use 'z' to save, 
    - and using advanced 'one letter' search and 'two letter' search.   
    - But then I realized that those techniques/habits actually had been prevent me 
        - from using vim everywhere productively!!
        - So, I gave them up and learned a few less productive but more portable habits, 
            - e.g., using 'arrow keys' more often, which reduces the frequency to use 'escape'.               
- Another vim example: recently, on vim, I have to get used to "set spell" on the fly! 
    - Sometimes, it is easier and healthier to 'just adapt to the default' than to 'configure'.
    - But github can help also: that is the reason I put those tiny tools here. 

- One more vim example: for less critical configuration, I will configure it to my like. 
    - After "set spell", on the PC I use often, I will put below in the .vimrc
        - Of course, first: cp .vimrc from /usr/share/vim/vim81 to ~

```
set ic
"""""""""""""""""""""""
" set wrap! go+=b
set spell
highlight clear SpellBad
" highlight SpellBad ctermfg=011 ctermbg=022 guifg=#ff0000 guibg=#ffff00
highlight SpellBad ctermfg=011 ctermbg=088 guifg=#ff0000 guibg=#ffff00

``` 

# About git-github connection: 

- Why use non-default location ~/.ssh?
    - It is b/c of "use folder structure and scripting for 'self-documenting'".
        - Changing ssh keys is "often but not everyday",  
            - a category that needs "self-documenting" the most. 
    - So, we need a directory at ~ with a hint, e.g., 3_ssh_keygen.ssh

- How to use a non-default key name 
    - By redirection, i.e., put below lines in a file, config, in ~/.ssh directory, 
 
```
Host github.com
    IdentityFile ~/3_ssh_keygen.ssh/.ssh/id_rsa_github_quk2021
    User git
```

- Git URL:
    - Git protocol  (i.e. git@xxxxxxxx, note it is @ ) uses ":" 
        - "@" is "user"; the protocol is "git+ssh" but is ommited. 
    - Https protocol (i.e. https://xxxx, note it is //) uses "/"
            
- How to test connection: 
    - ssh -T git@github.com 


