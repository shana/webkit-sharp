
TARGETS = \
	dom.exe

EXTRA_DIST = \
	Dom.cs

DEBUGS = $(addsuffix .mdb, $(TARGETS))

assembly=$(ASSEMBLY_NAME).dll

CLEANFILES = $(TARGETS) $(DEBUGS) $(assembly)

references=-r:../../sources/$(assembly) -pkg:gtk-sharp-2.0

all: $(TARGETS)

$(assembly): ../../sources/$(assembly)
	cp ../../sources/$(ASSEMBLY_NAME).dll $(srcdir)

dom.exe: $(assembly) $(srcdir)/Dom.cs
	$(CSC) -debug /out:$@ $(references) $(srcdir)/Dom.cs

