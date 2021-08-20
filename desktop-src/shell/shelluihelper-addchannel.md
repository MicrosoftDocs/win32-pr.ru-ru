---
description: добавляет новый канал в список каналов в меню "избранное" Windows Internet Explorer и на панель каналов на рабочем столе.
title: Шеллуихелпер. Аддчаннел, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddChannel
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b62e6e82-429a-4d41-96d4-cba639b611f5
ms.openlocfilehash: 6be928a7cae9d9349bb39fc3a27a49a16495a8609c8e1cb448de888ac190619b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047517"
---
# <a name="shelluihelperaddchannel-method"></a>Шеллуихелпер. Аддчаннел, метод

добавляет новый канал в список каналов в меню **"избранное"** Windows Internet Explorer и на панель **каналов** на рабочем столе.

> [!Note]  
> этот метод больше не поддерживается в Windows Vista. В этой операционной системе возвращается E \_ нотимпл.

 

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellUIHelper.AddChannel(
  sURL
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*СУРЛ* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строковое** значение, указывающее URL-адрес файла CDF.

> [!Note]  
> Ссылки в файле CDF должны использовать протоколы HTTP, HTTPS или FTP. Если в файле CDF содержится любой другой протокол, добавление канала завершается сбоем и диалоговое окно не появляется.

 

</dd> </dl>

## <a name="examples"></a>Примеры

в следующем примере показано правильное использование этого метода для JScript, внедренного в HTML и Visual Basic.

JScript:


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddChannelJ()
    {
        ShellUIHelper.AddChannel("https://www.microsoft.com/windows/cdf/g_stock.cdf");
    }
</script>

</head>
<body onload=fnShellUIHelperAddChannelJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddChannelVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddChannel ("https://www.microsoft.com/windows/cdf/g_stock.cdf")
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
