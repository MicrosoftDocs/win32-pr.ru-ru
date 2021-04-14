---
description: Отображает пользовательский интерфейс по умолчанию для создания элемента избранного. Пользовательский интерфейс инициализируется с указанными параметрами.
title: Шеллуихелпер. Аддфаворите, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986021"
---
# <a name="shelluihelperaddfavorite-method"></a>Шеллуихелпер. Аддфаворите, метод

Отображает пользовательский интерфейс по умолчанию для создания элемента избранного. Пользовательский интерфейс инициализируется с указанными параметрами.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*СУРЛ* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строковое** значение, указывающее URL-адрес элемента, добавляемого в папку **"Избранное"** .

</dd> <dt>

*втитле* \[ в необязательное\]
</dt> <dd>

Тип: **Variant \** _

Значение _ *Variant**, указывающее имя элемента.

</dd> </dl>

## <a name="examples"></a>Примеры

В следующем примере показано правильное использование этого метода для JScript Embedded в HTML и Visual Basic.

Присутствовал


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
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
