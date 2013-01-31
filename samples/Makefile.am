SUBDIRS = dom

TARGETS = \
	funnybrowser.exe

EXTRA_DIST = \
	FunnyBrowser.cs

DEBUGS = $(addsuffix .mdb, $(TARGETS))

assembly=$(ASSEMBLY_NAME).dll

CLEANFILES = $(TARGETS) $(DEBUGS) $(assembly)

references=-r:../out/$(assembly) -pkg:gtk-sharp-3.0

all: $(TARGETS)

$(assembly): ../out/$(assembly)
	cp ../out/$(ASSEMBLY_NAME).dll $(srcdir)

funnybrowser.exe: $(assembly) $(srcdir)/FunnyBrowser.cs
	$(CSC)  /out:$@ $(references) $(srcdir)/FunnyBrowser.cs

