ROFF=groff
SORT=sort

frl.pdf: frl.ps
	ps2pdf frl.ps

frl.ps: frl.n
	echo ".Ib" > frl.index
	${ROFF} -fT -mpapersize -dpaper=a4 -P-pa4 -me -w mac -step -mpdfmark -mlmacs -M. frl.n >frl.ps 2>>frl.index
	${SORT} -k 3 frl.index | grep '^\.I' > frl.bindex
	${ROFF} -fT -mpapersize -dpaper=a4 -P-pa4 -me -w mac -step -mpdfmark -mlmacs -M. frl.n frl.bindex >frl.ps

frl.bookmarks.pdf: frl.n
	echo ".Ib" > frl.index
	${ROFF} -Tpdf -fT -mpapersize -mpdfmark -dpaper=a4 -P-pa4 -me -w mac -step -mlmacs -M. frl.n >frl.bookmarks.pdf 2>>frl.index
	${SORT} -k 3 frl.index | grep '^\.I' > frl.bindex
	${ROFF} -Tpdf -fT -mpapersize -dpaper=a4 -P-pa4 -me -mpdfmark -w mac -step -mlmacs -M. frl.n frl.bindex >frl.bookmarks.pdf

clean:
	rm -f frl.ps
	rm -f frl.pdf
	rm -f frl.bookmarks.pdf
	rm -f frl.bindex
	rm -f frl.index
