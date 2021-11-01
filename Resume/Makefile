.PHONY: src

CC = xelatex
SRC_DIR = src
RESUME_DIR = resume
#CV_DIR = examples/cv
RESUME_SRCS = $(shell find $(RESUME_DIR) -name '*.tex')
#CV_SRCS = $(shell find $(CV_DIR) -name '*.tex')

src: $(foreach x,resume, $x.pdf)

resume.pdf: $(SRC_DIR)/resume.tex $(RESUME_SRCS)
	$(CC) -output-directory=$(SRC_DIR) $<

#cv.pdf: $(EXAMPLES_DIR)/cv.tex $(CV_SRCS)
#	$(CC) -output-directory=$(SRC_DIR) $<
#
#coverletter.pdf: $(EXAMPLES_DIR)/coverletter.tex
#	$(CC) -output-directory=$(SRC_DIR) $<

clean:
	rm -rf $(SRC_DIR)/*.pdf
