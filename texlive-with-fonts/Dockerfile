FROM listx/texlive:2020

MAINTAINER Linus Arver <linus@ucla.edu>

# Add all known font packages on official Arch Linux repos (not AUR). This is
# done with a regex for more automation.
RUN \
	# Sync package databases.
	pacman -Syw \
	# Install fonts.
	&& pacman -S --noconfirm \
		adobe-source-code-pro-fonts \
		adobe-source-han-sans-cn-fonts \
		adobe-source-han-sans-hk-fonts \
		adobe-source-han-sans-jp-fonts \
		adobe-source-han-sans-kr-fonts \
		adobe-source-han-sans-otc-fonts \
		adobe-source-han-sans-tw-fonts \
		adobe-source-han-serif-cn-fonts \
		adobe-source-han-serif-jp-fonts \
		adobe-source-han-serif-kr-fonts \
		adobe-source-han-serif-otc-fonts \
		adobe-source-han-serif-tw-fonts \
		adobe-source-sans-pro-fonts \
		adobe-source-serif-pro-fonts \
		awesome-terminal-fonts \
		bdf-unifont \
		cantarell-fonts \
		dina-font \
		font-bh-ttf \
		gentium-plus-font \
		gnu-free-fonts \
		gsfonts \
		inter-font \
		noto-fonts \
		noto-fonts-cjk \
		noto-fonts-emoji \
		noto-fonts-extra \
		opendesktop-fonts \
		otf-cascadia-code \
		otf-cormorant \
		otf-fantasque-sans-mono \
		otf-fira-mono \
		otf-fira-sans \
		otf-font-awesome \
		otf-hermit \
		otf-ipaexfont \
		otf-ipafont \
		otf-ipamjfont \
		otf-latin-modern \
		otf-latinmodern-math \
		otf-overpass \
		powerline-fonts \
		tamsyn-font \
		terminus-font \
		terminus-font-otb \
		tex-gyre-fonts \
		ttf-anonymous-pro \
		ttf-arphic-ukai \
		ttf-arphic-uming \
		ttf-baekmuk \
		ttf-bitstream-vera \
		ttf-caladea \
		ttf-carlito \
		ttf-cascadia-code \
		ttf-cormorant \
		ttf-croscore \
		ttf-dejavu \
		ttf-droid \
		ttf-eurof \
		ttf-fantasque-sans-mono \
		ttf-fira-code \
		ttf-fira-mono \
		ttf-fira-sans \
		ttf-font-awesome \
		ttf-hack \
		ttf-hanazono \
		ttf-hannom \
		ttf-ibm-plex \
		ttf-inconsolata \
		ttf-indic-otf \
		ttf-ionicons \
		ttf-jetbrains-mono \
		ttf-joypixels \
		ttf-junicode \
		ttf-khmer \
		ttf-lato \
		ttf-liberation \
		ttf-linux-libertine \
		ttf-linux-libertine-g \
		ttf-monofur \
		ttf-nerd-fonts-symbols \
		ttf-opensans \
		ttf-proggy-clean \
		ttf-roboto \
		ttf-roboto-mono \
		ttf-sarasa-gothic \
		ttf-sazanami \
		ttf-tibetan-machine \
		ttf-ubuntu-font-family \
		woff2-cascadia-code \
		woff2-fira-code \
		woff-fira-code \
		wqy-bitmapfont \
		wqy-microhei \
		wqy-microhei-lite \
		wqy-zenhei \
		xorg-fonts-100dpi \
		xorg-fonts-75dpi \
		xorg-fonts-alias-100dpi \
		xorg-fonts-alias-75dpi \
		xorg-fonts-alias-cyrillic \
		xorg-fonts-alias-misc \
		xorg-fonts-cyrillic \
		xorg-fonts-encodings \
		xorg-fonts-misc \
		xorg-fonts-type1 \
		xorg-xlsfonts \
	# Clean up pacman package cache.
	&& pacman -Scc --noconfirm \
	# Make TeX pick up newly-installed fonts from above.
	&& texhash \
	&& luaotfload-tool --update
