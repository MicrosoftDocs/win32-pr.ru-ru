---
description: Добавляет новый канал в список каналов в меню Избранное Windows Internet Explorer и на панель каналов на рабочем столе.
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
ms.openlocfilehash: d08c1360cb2a96fbc7b87daecb650bbf46aa6ad9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841205"
---
# <a name="shelluihelperaddchannel-method"></a>Шеллуихелпер. Аддчаннел, метод

Добавляет новый канал в список каналов в меню **Избранное** Windows Internet Explorer и на панель **каналов** на рабочем столе.

> [!Note]  
> Этот метод больше не поддерживается в Windows Vista. В этой операционной системе возвращается E \_ нотимпл.

 

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
