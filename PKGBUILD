pkgbase=ttf-office
pkgname=($pkgbase)
pkgver=v0.1
pkgrel=1
arch=(any)
url='http://www.fonts.net.cn/fonts-zh/tag-huawen-1.html','http://www.foundertype.com/'
license=(custom)
depends=(fontconfig xorg-fonts-encodings xorg-mkfontscale xorg-mkfontdir)
provides=($pkgbase)
conflicts=($pkgbase)

_ttf_office=(
#########################################################################################
# Normal         Bold          Italic        Bold+Italic    #  Full name                #
#########################################################################################
LiSu.ttf                                                    # 隶书
YouYuan.ttf                                                 # 幼圆
STXihei.ttf                                                 # 华文细黑
STKaiti.ttf                                                 # 华文楷体
STSong.ttf                                                  # 华文宋体
STZhongsong.ttf  STZhongsong-Bold.ttf                       # 华文中宋
STFangsong.ttf                                              # 华文仿宋
FZShuTi.ttf                                                 # 方正舒体
FZNewShuTi.ttf                                              # 方正新舒体
FZYaoTi.ttf                                                 # 方正姚体
STCaiyun.ttf                                                # 华文彩云
STHupo.ttf                                                  # 华文琥珀
STLiti.ttf                                                  # 华文隶书
STXingkai.ttf                                               # 华文行楷
STXinwei.ttf                                                # 华文新魏
)

DLAGENTS=("file::/usr/bin/echo ${BOLD}${RED} Unable to find %u, please read the PKGBUILD ${ALL_OFF}" $DLAGENTS[@])

source=(${_ttf_office[@]/#/file://})

md5sums=('a13e19f9c580682ce540f955ff662b83'
         '1bebe226bbad0bdae5b6f0957927a2ca'
         'f351fefd9707a0730c884f47694e4265'
         '1ee9941f1b8c128110ca4307dda59917'
         '456f6968af7fdbde28970967bfdc4d12'
         '33b6cc8f9995f2770dcf959eaa6757a5'
         'c5bb075b764f234ca36c7d3de2331a2c'
         '071c5637d1d3d870af3f50de0c72bf24'
         '24e3b9450bd501d611c1c54c5f400208'
         '7e65d94081116e762626e7fac4bf4ed7'
         'bdf788eefae7450198e3943ab515a231'
         '71eaacb7c100911a2acca6547fa6520a'
         '818f863b08f06842d555e8d6257884a5'
         '61affead7e371b5f62990eca801af587'
         '8ad1406b369731411a475f98c57609b8'
         '7785d8ad927b9138cf250302d39ac719')

_package() {
    conflicts+=(${pkgname})
    install -Dm644 $@ -t "$pkgdir/usr/share/fonts/TTF"
}

package_ttf-office() {
    pkgdesc='HuaWen TrueType fonts'
    provides+=(${pkgname})
    conflicts+=(${pkgname})
    _package ${_ttf_office[@]}
}
