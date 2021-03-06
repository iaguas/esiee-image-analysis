EXE=$(BDIR)/addconst $(BDIR)/avgfilter $(BDIR)/avgfilter_color $(BDIR)/deriche $(BDIR)/diffimage $(BDIR)/equalize \
	$(BDIR)/gammac $(BDIR)/log $(BDIR)/normalize $(BDIR)/pixelwisefilter $(BDIR)/pixelwisefilter_color $(BDIR)/power \
	$(BDIR)/ppm2pgm $(BDIR)/pgm2ppm $(BDIR)/threshold $(BDIR)/weightavg $(BDIR)/windowwisefilter

DOC=$(DOCDIR)/tutorialEnglish.html

REP=$(DOCDIR)/report/report.pdf

CCFLAGS = -g -DUNIXIO -Wall -std=c99 -O2
CCINCLUDE = -lm

IDIR = ./include
ODIR = ./obj
BDIR = ./bin
CDIR = ./src/com
LDIR = ./src/lib
DOCDIR = ./doc
CC = cc

# Documentation, if not already comiled, can be compiled thanks to 'make doc'
# You can also do a 'make clean' if you want

all:	$(EXE)
doc:    $(DOC)
report: $(REP)	

pruebas: $(CDIR)/pruebas.c $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/pruebas.c $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/pruebas


# ===============================================================
# shell commands
# ===============================================================

$(BDIR)/addconst:	$(CDIR)/addconst.c $(IDIR)/laddconst.h $(IDIR)/mcimage.h $(ODIR)/mcimage.o $(ODIR)/laddconst.o
	mkdir -p bin
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/addconst.c $(ODIR)/laddconst.o $(ODIR)/mcimage.o -o $(BDIR)/addconst

$(BDIR)/avgfilter:	$(CDIR)/avgfilter.c $(IDIR)/lavgfilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lavgfilter.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/avgfilter.c $(ODIR)/lavgfilter.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/avgfilter

$(BDIR)/avgfilter_color:	$(CDIR)/avgfilter_color.c $(IDIR)/lavgfilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lavgfilter.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/avgfilter_color.c $(ODIR)/lavgfilter.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/avgfilter_color

$(BDIR)/deriche:	$(CDIR)/deriche.c $(IDIR)/lderiche.h $(IDIR)/mcimage.h $(ODIR)/mcimage.o $(ODIR)/lderiche.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/deriche.c $(ODIR)/lderiche.o $(ODIR)/mcimage.o -lm -o $(BDIR)/deriche

$(BDIR)/diffimage:	$(CDIR)/diffimage.c $(IDIR)/ldiffimage.h $(IDIR)/mcimage.h $(ODIR)/mcimage.o $(ODIR)/ldiffimage.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/diffimage.c $(ODIR)/ldiffimage.o $(ODIR)/mcimage.o -o $(BDIR)/diffimage

$(BDIR)/equalize:	$(CDIR)/equalize.c $(IDIR)/lequalize.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lequalize.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/equalize.c $(ODIR)/lequalize.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/equalize

$(BDIR)/gammac:	$(CDIR)/gammac.c $(IDIR)/lgammac.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lgammac.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/gammac.c $(ODIR)/lgammac.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/gammac

$(BDIR)/log:	$(CDIR)/log.c $(IDIR)/llog.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/llog.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/log.c $(ODIR)/llog.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/log

$(BDIR)/normalize:	$(CDIR)/normalize.c $(IDIR)/lnormalize.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lnormalize.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/normalize.c $(ODIR)/lnormalize.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/normalize

$(BDIR)/pixelwisefilter:	$(CDIR)/pixelwisefilter.c $(IDIR)/lpixelwisefilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lpixelwisefilter.o
	$(CC) $(CCFLAGS) $(CCINCLUDE) -I$(IDIR) $(CDIR)/pixelwisefilter.c $(ODIR)/lpixelwisefilter.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/pixelwisefilter

$(BDIR)/pixelwisefilter_color:	$(CDIR)/pixelwisefilter_color.c $(IDIR)/lpixelwisefilter_color.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lpixelwisefilter_color.o
	$(CC) $(CCFLAGS) $(CCINCLUDE) -I$(IDIR) $(CDIR)/pixelwisefilter_color.c $(ODIR)/lpixelwisefilter_color.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/pixelwisefilter_color

$(BDIR)/power:	$(CDIR)/power.c $(IDIR)/lpower.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lpower.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/power.c $(ODIR)/lpower.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/power

$(BDIR)/threshold:	$(CDIR)/threshold.c $(IDIR)/lthreshold.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lthreshold.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/threshold.c $(ODIR)/lthreshold.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/threshold

$(BDIR)/weightavg:	$(CDIR)/weightavg.c $(IDIR)/lweightavg.h $(IDIR)/lfilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lweightavg.o $(ODIR)/lfilter.o
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/weightavg.c $(ODIR)/lweightavg.o $(ODIR)/lfilter.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/weightavg

$(BDIR)/windowwisefilter:	$(CDIR)/windowwisefilter.c $(IDIR)/lwindowwisefilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h $(ODIR)/mcimage.o $(ODIR)/tools.o $(ODIR)/lwindowwisefilter.o
	$(CC) $(CCFLAGS) $(CCINCLUDE) -I$(IDIR) $(CDIR)/windowwisefilter.c $(ODIR)/lwindowwisefilter.o $(ODIR)/mcimage.o $(ODIR)/tools.o -o $(BDIR)/windowwisefilter


# ===============================================================
# Library functions 
# ===============================================================

# Basic ones:
# ===============================================================

$(ODIR)/mcimage.o:	$(LDIR)/mcimage.c $(IDIR)/mcimage.h
	mkdir -p obj
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/mcimage.c -o $(ODIR)/mcimage.o
	
$(ODIR)/tools.o:	$(LDIR)/tools.c $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/tools.c -o $(ODIR)/tools.o

# Operators:
# ===============================================================

$(ODIR)/laddconst.o:	$(LDIR)/laddconst.c $(IDIR)/laddconst.h $(IDIR)/mcimage.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/laddconst.c -o $(ODIR)/laddconst.o

$(ODIR)/lavgfilter.o:	$(LDIR)/lavgfilter.c $(IDIR)/lavgfilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lavgfilter.c -o $(ODIR)/lavgfilter.o

$(ODIR)/lderiche.o:	$(LDIR)/lderiche.c $(IDIR)/lderiche.h $(IDIR)/mcimage.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lderiche.c -o $(ODIR)/lderiche.o

$(ODIR)/ldiffimage.o:	$(LDIR)/ldiffimage.c $(IDIR)/ldiffimage.h $(IDIR)/mcimage.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/ldiffimage.c -o $(ODIR)/ldiffimage.o

$(ODIR)/lequalize.o:	$(LDIR)/lequalize.c $(IDIR)/lequalize.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lequalize.c -o $(ODIR)/lequalize.o

$(ODIR)/lfilter.o:	$(LDIR)/lfilter.c $(IDIR)/lfilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lfilter.c -o $(ODIR)/lfilter.o

$(ODIR)/lgammac.o:	$(LDIR)/lgammac.c $(IDIR)/lgammac.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lgammac.c -o $(ODIR)/lgammac.o

$(ODIR)/llog.o:	$(LDIR)/llog.c $(IDIR)/llog.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/llog.c -o $(ODIR)/llog.o

$(ODIR)/lnormalize.o:	$(LDIR)/lnormalize.c $(IDIR)/lnormalize.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lnormalize.c -o $(ODIR)/lnormalize.o

$(ODIR)/lpixelwisefilter.o:	$(LDIR)/lpixelwisefilter.c $(IDIR)/lpixelwisefilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lpixelwisefilter.c -o $(ODIR)/lpixelwisefilter.o

$(ODIR)/lpixelwisefilter_color.o:	$(LDIR)/lpixelwisefilter_color.c $(IDIR)/lpixelwisefilter_color.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lpixelwisefilter_color.c -o $(ODIR)/lpixelwisefilter_color.o

$(ODIR)/lpower.o:	$(LDIR)/lpower.c $(IDIR)/lpower.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lpower.c -o $(ODIR)/lpower.o

$(ODIR)/lthreshold.o:	$(LDIR)/lthreshold.c $(IDIR)/lthreshold.h $(IDIR)/mcimage.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lthreshold.c -o $(ODIR)/lthreshold.o

$(ODIR)/lweightavg.o:	$(LDIR)/lweightavg.c $(IDIR)/lweightavg.h $(IDIR)/lfilter.h $(IDIR)/mcimage.h 
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lweightavg.c -o $(ODIR)/lweightavg.o

$(ODIR)/lwindowwisefilter.o:	$(LDIR)/lwindowwisefilter.c $(IDIR)/lwindowwisefilter.h $(IDIR)/mcimage.h $(IDIR)/tools.h
	$(CC) -c $(CCFLAGS) -I$(IDIR) $(LDIR)/lwindowwisefilter.c -o $(ODIR)/lwindowwisefilter.o


$(BDIR)/ppm2pgm:	$(CDIR)/ppm2pgm.c $(IDIR)/mcimage.h $(LDIR)/mcimage.c
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/ppm2pgm.c  $(ODIR)/mcimage.o -o $(BDIR)/ppm2pgm

$(BDIR)/pgm2ppm:	$(CDIR)/pgm2ppm.c $(IDIR)/mcimage.h $(LDIR)/mcimage.c
	$(CC) $(CCFLAGS) -I$(IDIR) $(CDIR)/pgm2ppm.c $(ODIR)/mcimage.o -o $(BDIR)/pgm2ppm

# Documentation
# ===============================================================
$(DOCDIR)/tutorialEnglish.html: $(DOCDIR)/tutorialEnglish.tex
	cd $(DOCDIR); htlatex ./tutorialEnglish; cd ..

$(DOCDIR)/report/report.pdf: $(DOCDIR)/report/report.tex
	cd $(DOCDIR)/report; latexmk -pdf report.tex


clean:
	rm -rf *~ $(ODIR)/* $(IDIR)/*~ $(CDIR)/*~ $(LDIR)/*~ $(DOCDIR)/*~ 
	cd $(DOCDIR); rm -rf *.4ct *.4tc *.aux *.dvi *.idv *.lg *.log *.tmp *.xref

cleanall: 
	rm -rf *~ $(BDIR)/* $(ODIR)/* $(IDIR)/*~ $(CDIR)/*~ $(LDIR)/*~ $(DOCDIR)/*~ 
	cd $(DOCDIR); rm -rf *.4ct *.4tc *.aux *.dvi *.idv *.lg *.log *.tmp *.xref