
TARGETS = \
	dom.exe

EXTRA_DIST = \
	Dom.cs

DEBUGS = $(addsuffix .mdb, $(TARGETS))

assembly=$(ASSEMBLY_NAME).dll

CLEANFILES = $(TARGETS) $(DEBUGS) $(assembly)

references=-r:../../out/$(assembly) -pkg:gtk-sharp-3.0

all: $(TARGETS)

$(assembly): ../../out/$(assembly)
	cp ../../out/$(ASSEMBLY_NAME).dll $(srcdir)

dom.exe: $(assembly) $(srcdir)/Dom.cs
	$(CSC) -debug /out:$@ $(references) $(srcdir)/Dom.cs

