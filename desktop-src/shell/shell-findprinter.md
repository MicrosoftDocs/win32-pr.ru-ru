---
description: Отображает диалоговое окно Поиск принтера.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Метод Shell. Финдпринтер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1286bb7247359ea91d29a53f8f0eaa13b55be5e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985977"
---
# <a name="shellfindprinter-method"></a>Shell. Финдпринтер, метод

Отображает диалоговое окно **Поиск принтера** .

## <a name="syntax"></a>Синтаксис


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*sName* \[ в необязательное\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая имя принтера.

</dd> <dt>

*слокатион* \[ в необязательное\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая расположение принтера.

</dd> <dt>

*смодел* \[ в необязательное\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая модель принтера.

</dd> </dl>

## <a name="remarks"></a>Примечания

Если вы назначаете строки одному или нескольким необязательным параметрам, они отображаются как значения по умолчанию в связанном элементе управления "поле ввода" при отображении диалогового окна " **Найти принтер** ". Пользователь может либо принять, либо переопределить эти значения. Если параметру не присвоено значение, соответствующее поле редактирования будет пустым и пользователь должен ввести значение.

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **финдпринтер** для отображения диалогового окна **Найти принтер** для конкретного приложения. Сведения об использовании представлены для JScript, VBScript и Visual Basic.

Присутствовал


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional, только для \[ классических приложений Windows XP\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Шлдисп. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Шлдисп. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (версия 5,0 или более поздняя)</dt> </dl> |



 

 
