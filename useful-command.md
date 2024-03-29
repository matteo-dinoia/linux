# Useful Commands

## Speed up
### Blaming startup times
systemd-analyze blame
Other command at: [tecmint](https://www.tecmint.com/systemd-analyze-monitor-linux-bootup-performance)


## Media
### REMOVING METADATA
```sh
mat2 * --inplace
```
### ROTATING ALL IMAGES -> need imagemagick
```sh
for photo in *.jpg ;do
    convert $photo -rotate 90 $photo;
done
```
### COMPRESSING PHOTO
```sh
jpegoptim *
```
### COMPRESSING PDF -> need ghostscript
gs -sDEVICE=pdfwrite -dCompatibilityLevel=1.4 -dPDFSETTINGS=/ebook -dNOPAUSE -dBATCH -dColorImageResolution=150 -sOutputFile=output.pdf 17_grafi_albero_minimo_ricoprente.pdf
### BATCH RENAMING
```sh
i=1
for fi in *.jpg; do
    mv "$fi" "$(printf "book-v1-p%03d.jpg" "$i")"
    i=$((i+1))
done
```

### IMAGE DOWNLOAD AND RESIZING
```sh
curl "link" --output "name";
convert -resize <size> "name" "name";
```

### SPLITTING PDF (2x2) -> need mupdf-tools
mutool poster -x 2 -y 2 input.pdf output.pdf
#### Alternative
convert -quality 100 -density 300 a.pdf +repage -crop 2x2@  +repage b.pdf
