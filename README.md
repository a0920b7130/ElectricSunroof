class ElectricSunroof:
    def __init__(self):
        self.is_open = False  # 天窗的狀態，是否打開
        self.tilt_angle = 0  # 傾斜角度，0 表示完全閉合

    def open_sunroof(self):
        if not self.is_open:
            self.is_open = True
            self.tilt_angle = 100  # 打開天窗，設置到全開位置
            print("Sunroof is fully opened.")
        else:
            print("Sunroof is already open.")

    def close_sunroof(self):
        if self.is_open:
            self.is_open = False
            self.tilt_angle = 0  # 關閉天窗，設置到全閉位置
            print("Sunroof is closed.")
        else:
            print("Sunroof is already closed.")

    def tilt_sunroof(self, angle):
        if 0 <= angle <= 100:
            self.tilt_angle = angle
            print(f"Sunroof tilted to {angle} degrees.")
        else:
            print("Invalid angle. Please set an angle between 0 and 100.")

    def status(self):
        if self.is_open:
            print(f"Sunroof is open, tilted at {self.tilt_angle} degrees.")
        else:
            print("Sunroof is closed.")

# 使用範例
sunroof = ElectricSunroof()
sunroof.open_sunroof()
sunroof.tilt_sunroof(50)
sunroof.status()
sunroof.close_sunroof()
# ElectricSunroof
