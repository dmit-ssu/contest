SOURCES := $(wildcard *.java)
SOLUTIONS := $(patsubst %.java,%.dir/Solution.class,$(SOURCES))
SOLUTIONS_SRCS := $(patsubst %.java,%.dir/Solution.java,$(SOURCES))
SOLUTIONS_DIRS := $(patsubst %.java,%.dir,$(SOURCES))
JAVAC := javac
JAVA := java

.PHONY: clean

all: $(SOLUTIONS)

%.dir/Solution.java: %.java
	mkdir -p $(patsubst %.java,%.dir,$<)
	cp -f $< $@

%.dir/Solution.class: %.dir/Solution.java
	${JAVAC} $<

%: %.dir/Solution.class
	@${JAVA} -cp $@.dir Solution

clean:
	rm -rf $(SOLUTIONS_DIRS)
