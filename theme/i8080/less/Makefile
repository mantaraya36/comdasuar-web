FINAL_CSS = ../static/css/main.css
SOURCE_LESS = master.less
DATE=$(shell date +%I:%M%p)
CHECK=\033[32m✔\033[39m
HR=\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#\#


build:
	@echo "\n${HR}"
	@echo "Building less file..."
	@echo "${HR}\n"
	@lessc  --yui-compress  ${SOURCE_LESS} > ${FINAL_CSS}
	@echo "Compiling LESS with Recess...               ${CHECK} Done"

watch:
	echo "Watching less files..."; \
	watchr -e "watch('.*\.less') { system 'make'}"