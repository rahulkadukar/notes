# Notes
These are just notes that I took and if you like them feel free to 
use them. The first thing that I recommend is that you configure 
vi (a real text editor). I use the following settings for my vi as 
found in the config folder in this repository. These settings also
need the color theme Lucius (although this is a personal preference)
and you should change it to whatever you prefer.

## Format
The notes contain a lot of mathematical formulae and hence I have
decided to use latex instead of markdown for writing the notes. There
is a tex file in the repository called notes.tex and this can be used
to produce a file in any format using something like **pandoc**

After doing more research I have found that you can use MathML in the
Markdown directly and this can then be converted into any format 
including HTML that renders the equations perfectly.

## vim and tmux setup
```bash
git clone https://github.com/rahulkadukar/notes.git 0d0bb8cd1f6c3851ad90bceb8978b86b424209373818a81e782ffdcb6e2a91ea4332cbf9ab3415eb932979cac14e2c3a82872667d35b39641fb35a66b448d1eb && \
mkdir -p ~/.vim/colors && \
cp 0d0bb8cd1f6c3851ad90bceb8978b86b424209373818a81e782ffdcb6e2a91ea4332cbf9ab3415eb932979cac14e2c3a82872667d35b39641fb35a66b448d1eb/config/.vim/colors/lucius.vim ~/.vim/colors/lucius.vim && \
cp 0d0bb8cd1f6c3851ad90bceb8978b86b424209373818a81e782ffdcb6e2a91ea4332cbf9ab3415eb932979cac14e2c3a82872667d35b39641fb35a66b448d1eb/config/.vimrc ~/.vimrc && \
cp  0d0bb8cd1f6c3851ad90bceb8978b86b424209373818a81e782ffdcb6e2a91ea4332cbf9ab3415eb932979cac14e2c3a82872667d35b39641fb35a66b448d1eb/config/.tmux.conf ~/.tmux.conf && \
rm -rf 0d0bb8cd1f6c3851ad90bceb8978b86b424209373818a81e782ffdcb6e2a91ea4332cbf9ab3415eb932979cac14e2c3a82872667d35b39641fb35a66b448d1eb/
```
