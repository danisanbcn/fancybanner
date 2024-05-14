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
Optional: make it hidden
```bash
mv fancybanner .fancybanner
```

**Non colored**

```bash
echo 'BANNERLIST=$(ls -1 fancybanner | wc -l)' >> ~/.bashrc
echo 'cat ~/fancybanner/banner$((RANDOM % $BANNERLIST + 1))' >> ~/.bashrc
```

**Colored**

```bash
echo 'BANNERLIST=$(ls -1 fancybanner | wc -l)' >> ~/.bashrc
echo 'cat ~/fancybanner/banner$((RRANDOM % $BANNERLIST + 1)) | loclat' >> ~/.bashrc
```
