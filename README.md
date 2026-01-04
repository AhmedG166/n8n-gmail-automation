# نظام أتمتة Gmail
# Gmail Automation System

## العربية

### الوصف
نظام يراقب حساب Gmail ويحفظ الرسائل الواردة في Google Sheets مع إرسال إشعارات Slack.

### كيف يعمل
1. يفحص Gmail كل دقيقة للبحث عن رسائل جديدة
2. يستخرج معلومات المرسل والموضوع والمحتوى
3. ينظف البيانات من العلامات الزائدة
4. يحفظ البيانات في جدول منظم
5. يرسل إشعار فوري للفريق عبر Slack

### التقنيات
- n8n للأتمتة
- Gmail API
- Google Sheets API  
- Slack API
- JavaScript

### التثبيت

**الخطوة 1: Google Cloud**
- أنشئ مشروع جديد
- فعّل Gmail API وSheets API
- أنشئ OAuth credentials
- انسخ Client ID وSecret

**الخطوة 2: Slack**
- أنشئ بوت جديد على api.slack.com
- أضف صلاحيات: chat:write وchannels:read
- انسخ Bot Token

**الخطوة 3: Google Sheets**
- أنشئ جدول جديد
- أضف العناوين: Sender Email | Sender Name | Subject | Body | Received At | Processed At
- انسخ معرف الجدول من الرابط

**الخطوة 4: n8n**
- استورد ملف gmail-automation.json
- أضف بيانات الاعتماد الثلاثة
- استبدل معرف الجدول ورقم القناة
- فعّل الـ workflow

### التخصيص
يمكنك تعديل:
- تكرار الفحص من دقيقة إلى 5 أو 10 دقائق
- التسميات المراقبة في Gmail
- شكل الرسالة في Slack
- الأعمدة المحفوظة في Sheets

### ملاحظة
المشروع يحتاج بيانات اعتماد خاصة بك. الملف يحتوي على قيم تجريبية يجب استبدالها.

---

## English

### Description
A system that monitors Gmail and saves incoming messages to Google Sheets with Slack notifications.

### How It Works
1. Checks Gmail every minute for new messages
2. Extracts sender, subject, and body information
3. Cleans data from extra tags
4. Saves data to organized spreadsheet
5. Sends instant notification to team via Slack

### Technologies
- n8n for automation
- Gmail API
- Google Sheets API
- Slack API  
- JavaScript

### Installation

**Step 1: Google Cloud**
- Create new project
- Enable Gmail API and Sheets API
- Create OAuth credentials
- Copy Client ID and Secret

**Step 2: Slack**
- Create new bot at api.slack.com
- Add scopes: chat:write and channels:read
- Copy Bot Token

**Step 3: Google Sheets**
- Create new spreadsheet
- Add headers: Sender Email | Sender Name | Subject | Body | Received At | Processed At
- Copy sheet ID from URL

**Step 4: n8n**
- Import gmail-automation.json file
- Add three credentials
- Replace sheet ID and channel number
- Activate workflow

### Customization
You can modify:
- Check frequency from 1 to 5 or 10 minutes
- Monitored labels in Gmail
- Slack message format
- Saved columns in Sheets

### Note
Project requires your own credentials. File contains demo values that must be replaced.


## المطور | Developer
Ahmed Gaiter
