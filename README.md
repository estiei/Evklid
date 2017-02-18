
# Evklid

print('Enter the first integer number:')
a = int(input())
print('Thank you! Enter the second integer number:')
b = int(input())
if (a == b) or (a == 1) or (b == 1):
    print('gcd (', a, ',', b, ') = 1')
elif a > b:
    z0 = a
    z1 = b
else:
    z0 = b
    z1 = a
print(z0, z1)
x0 = 1
y0 = 0
x1 = 0
y1 = 1
z2 = 0
while z2 != 1:
    x2 = x0 - x1 * (z0//z1)
    y2 = y0 - y1 * (z0//z1)
    z2 = z0%z1
    print("%7d%7d%7d" % (x2, y2, z2), ' q = ', z0//z1)

    x0, x1 = x1, x2
    y0, y1 = y1, y2
    z0, z1 = z1, z2
