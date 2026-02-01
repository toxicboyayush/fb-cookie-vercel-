# Cookie Format Helper

## Single Cookie Format

Paste exactly as you copy from browser (JSON or cookie string):

```
c_user=1234567890; xs=1234567890:abcdef; ...
```

OR

```json
{
  "name": "c_user",
  "value": "1234567890",
  ...
}
```

---

## Multiple Cookies Format (cookies.txt)

One cookie per line:

```
c_user=1234567890; xs=1234567890:abcdef; fr=abc123;
c_user=9876543210; xs=9876543210:fedcba; fr=xyz456;
c_user=5555555555; xs=5555555555:gggggg; fr=hhh789;
```

---

## How to Get Cookies from Browser

### Method 1: EditThisCookie Extension (Chrome/Edge)
1. Install "EditThisCookie" from Chrome Web Store
2. Login to Facebook
3. Click extension icon
4. Click "Export" button
5. Copy all text
6. Paste in application

### Method 2: Developer Console
1. Login to Facebook
2. Press F12
3. Go to Application/Storage tab
4. Click Cookies → facebook.com
5. Copy cookie values
6. Format as: name=value; name2=value2;

---

## Example cookies.txt file:

```
c_user=100012345678901; xs=12:abc123def456:2:1234567890::-1; fr=0Abc123Def456.ABC.Xyz.123.1234567890; datr=xyz123; sb=abc456;
c_user=100087654321098; xs=34:fed987cba654:2:9876543210::-1; fr=0Fed987Cba654.FED.Zyx.987.9876543210; datr=zyx987; sb=fed654;
```

Save this as `cookies.txt` and upload in the app.

---

## Tips:
- Cookies expire, refresh them regularly
- Use fresh login cookies
- Don't share cookies publicly
- One cookie = One Facebook account
