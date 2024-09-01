import qrcode

qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=10,
    border=4,
)
qr.add_data("https://github.com/karunarajak?tab=repositories")
qr.make(fit=True)
img = qr.make_image(fill_color="black", backgnd_color="white")
img.save("karuna.png")
