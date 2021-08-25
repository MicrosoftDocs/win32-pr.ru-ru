---
description: Добавляет элемент в Microsoft Active Desktop.
title: Шеллуихелпер. Адддесктопкомпонент, метод (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: 5141b35b9fb71b09b9b269016d0b38cdb0b9f01ec88a02070a0f936934159930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941504"
---
# <a name="shelluihelperadddesktopcomponent-method"></a>Шеллуихелпер. Адддесктопкомпонент, метод

Добавляет элемент в Microsoft Active Desktop.

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*СУРЛ* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строковое** значение, указывающее URL-адрес нового элемента избранного.

</dd> <dt>

*Стипе* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строковое** значение, указывающее тип добавляемого элемента. Это может быть одно из следующих значений.

<dt>



 Эскиз


</dt> <dd>

Компонент является изображением.

</dd> <dt>



 веб


</dt> <dd>

Компонент является веб-сайтом.

</dd> </dl> </dd> <dt>

По *левому краю* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Расположение левого края компонента в экранных координатах.

</dd> <dt>

В *Начало* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Расположение верхнего края компонента в экранных координатах.

</dd> <dt>

*Ширина* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Ширина компонента в единицах экрана.

</dd> <dt>

*Высота* \[ в необязательное\]
</dt> <dd>

Тип: **Variant**

Высота компонента в единицах экрана.

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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



Visual Basic:


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ настольных приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                           |
| Заголовок<br/>                   | <dl> <dt>Ексдисп. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 4,71 или более поздняя)</dt> </dl> |



 

 
