---
description: 'Класс поставщика системного реестра Стдрегпров для WMI имеет методы, которые выполняют следующие действия:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Изменение данных реестра
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105713243"
---
# <a name="changing-registry-data"></a>Изменение данных реестра

Класс [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) для WMI имеет методы, которые выполняют следующие действия:

-   Создание или удаление разделов реестра.

    Используйте [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) или [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).

-   Создание или удаление именованных значений, которые называются записями, если они находятся под ключами.

    Для создания именованного значения используйте имя нового значения, [**сетбинаривалуе**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**сетдвордвалуе**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**сетекспандедстрингвалуе**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)или [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) . Используйте [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) для удаления именованного значения.

-   Измените именованные значения.

    Для изменения существующих именованных значений в разделе используйте имя значения и методы набора (определенные в предыдущем маркированном элементе). Необходимо иметь имя значения, чтобы изменить его. Если вы не знакомы с именами значений в ключе, используйте метод [**енумвалуес**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) для получения имен.

В этом разделе обсуждаются следующие разделы:

-   [Создание раздела реестра с помощью VBScript](#creating-a-registry-key-using-vbscript)
-   [Создание именованного значения реестра с помощью PowerShell и VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Создание раздела реестра с помощью VBScript

Поскольку реестр является центральной базой данных конфигурации для операционной системы, приложений и служб, будьте внимательны при записи изменений в значения реестра или удалении ключей.

> [!Note]  
> Нельзя отслеживать **\_ \_ корневой подраздел classes для классов hKey** **\_ Current \_ User (HKCU)**. Мониторинг **\_ пользователей hKey** не рекомендуется, так как подразделы появляются и исчезают при загрузке Hive.

 

В следующих примерах кода показано, как создать новый раздел реестра и подраздел.


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Создание именованного значения реестра с помощью PowerShell и VBScript

В следующем примере кода показано, как создать именованное значение с именем **мултистрингвалуе** в **разделе \_ \_** \\ **программное обеспечение** \\ **MyKey** \\ **мисубкэй** , которое создает предыдущий сценарий. Скрипт вызывает [**стдрегпров. сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) для записи строковых значений в новое именованное значение.


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

С помощью инструментария WMI нельзя установить параметры безопасности доступа к разделу реестра. Однако метод [**стдрегпров. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) сравнивает параметры безопасности текущего пользователя с дескриптором безопасности раздела реестра, чтобы определить, имеет ли пользователь определенное разрешение, например **\_ \_ значение набора ключей**.
