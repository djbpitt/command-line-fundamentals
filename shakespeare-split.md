# Separate Shakespeare sonnets into individual files

```bash
gcsplit --suppress-matched shakespeare-sonnets.txt '/^$/' '{*}'
for file in xx[0-9]*; do mv $file  `printf sonnet%03d.txt $((10#${file#xx}+1))`; done
```

```bash
for file in sonnet*; do if [ `wc -l $file | sed 's/^ *//' | cut -d " " -f 1` -ne 15 ] ; then echo $file; fi; done
```