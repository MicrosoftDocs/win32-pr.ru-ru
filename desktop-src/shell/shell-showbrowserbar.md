---
description: Shell. Шовбровсербар-метод — отображает панель браузера.
ms.assetid: 203636D2-54D3-4163-B9AC-39213D6F4203
title: Метод Shell. Шовбровсербар (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShowBrowserBar
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d19cd5b98ce39470860cc481ab05e4bb41adc9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083732"
---
# <a name="shellshowbrowserbar-method"></a>Shell. Шовбровсербар, метод

Отображает панель браузера.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = Shell.ShowBrowserBar(
  sCLSID,
  vShow
)
```


```VB

Shell.ShowBrowserBar( _
  ByVal sCLSID As BSTR, _
  ByVal vShow As Variant _
) As Variant
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*склсид* \[ окне\]
</dt> <dd>

Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Строка** , содержащая форму строки CLSID отображаемой панели браузера. Объект должен быть зарегистрирован в качестве объекта панели обозревателя с \_ категорией компонента CATID инфобанд. Дополнительные сведения см. в разделе [Создание настраиваемых панелей обозревателя, панелей инструментов и полос рабочего стола](band-objects.md).

</dd> <dt>

*вшов* \[ окне\]
</dt> <dd>

Тип: **Variant**

Задайте значение **true** , чтобы отобразить панель браузера, или **значение false** , чтобы скрыть ее.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="jscript"></a>Язык JScript

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

### <a name="vb"></a>VB

Тип: **Variant \***

Возвращает **значение true** в случае успешного выполнения. в противном случае — **значение false**.

## <a name="remarks"></a>Remarks

Можно отобразить одну из стандартных панелей обозревателя, задав для параметра *склсид* значение CLSID этой панели обозревателя. Ниже перечислены стандартные панели обозревателя и их строки CLSID.



| Панель обозревателя | Строка CLSID                           |
|--------------|----------------------------------------|
| Избранное    | {EFA24E61-B078-11d0-89E4-00C04FC9E26E} |
| Папки      | {EFA24E64-B078-11d0-89E4-00C04FC9E26E} |
| Журнал      | {EFA24E62-B078-11d0-89E4-00C04FC9E26E} |
| Поиск       | {30D02401-6A81-11d0-8274-00C04FD5AE38} |



 

Этот метод в настоящее время недоступен в Microsoft Visual Basic.

## <a name="examples"></a>Примеры

В следующих примерах показано использование **оболочки. шовбровсербар** для отображения панели браузера **избранного** . Для JScript и VBScript отображается использование.

Присутствовал


```JScript
<script language="JavaScript">
    function fnShowBrowserBarJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var bReturn;
        
        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true);
    }
</script>
```



Сценариев


```VB
<script language="VBScript">
    function fnShowBrowserBarVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")

        bReturn = objShell.ShowBrowserBar("{EFA24E61-B078-11d0-89E4-00C04FC9E26E}", true)

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



 

 
