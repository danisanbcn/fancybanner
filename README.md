# fancybanner
Fancy random banner for linux terminal.

## Dependencies

If you want colored random banner install lolcat.

```bash
sudo apt get install lolcat
```

## Install

Clone this repo in your home directory. 
```bash
cd ~ && git clone https://github.com/danisanbcn/fancybanner.git
```

**Non colored**

```bash
echo 'BANNERLIST=$(ls -1 ~/fancybanner/banner* | wc -l)' >> ~/.bashrc
echo 'cat ~/fancybanner/banner$((RANDOM % $BANNERLIST + 1))' >> ~/.bashrc
```

**Colored**

```bash
echo 'BANNERLIST=$(ls -1 ~/fancybanner/banner* | wc -l) | lolcat' >> ~/.bashrc
echo 'cat ~/fancybanner/banner$((RANDOM % $BANNERLIST + 1)) | loclat' >> ~/.bashrc
```

Done!

## Optional: as hidden directory

Make it hidden
```bash
mv fancybanner .fancybanner
```
Replace *~/fancybanner* with *~/.fancybanner* in .bashrc lines
