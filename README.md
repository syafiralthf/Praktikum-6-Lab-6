# Biodata

Nama: Syafira Luthfi Azzahra

Kelas: TI.24.A.4

NIM: 312410353

# Latihan 1

![Screenshot from 2024-11-26 14-22-32](https://github.com/user-attachments/assets/7671aac1-384f-4cbb-af9f-42165a4e20fb)

## Latihan 1.py

```python
import math

a = lambda x: x**2
b = lambda x, y: math.sqrt(x*2 + y*2)
c = lambda *args: sum(args)/len(args) if args else 0
d = lambda s: "".join(set(s)) 

print("lambda a(5):", a(5))
print("lambda b(3, 4):", b(3, 4))
print("lambda c(1, 2, 3, 4, 5):", c(1, 2, 3, 4, 5))
print("lambda d('hello Syafira'):", d("Syafira"))
```

![image](https://github.com/user-attachments/assets/8261d24d-29b4-4746-9d77-f27f22f867e1)
