---
description: Производительность вызовов семисинчронаус обычно достаточно важна для большинства ситуаций.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Настройка безопасности при асинхронном вызове в VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712947"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Настройка безопасности при асинхронном вызове в VBScript

Производительность вызовов [*семисинчронаус*](gloss-s.md) обычно достаточно важна для большинства ситуаций. Обычно асинхронные вызовы не рекомендуются для сценариев. Однако если необходимо выполнить асинхронные вызовы, можно задать значение реестра, чтобы принудительно использовать WMI для проверки доступа при асинхронных вызовах.


Значение реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **унсекаппакцессконтролдефаулт** определяет, будет ли Инструментарий WMI проверять наличие приемлемого уровня проверки подлинности при возврате данных для асинхронного вызова. Обратный вызов может быть возвращен на более низком уровне проверки подлинности по сравнению с исходным асинхронным вызовом. По умолчанию это значение равно нулю, поэтому обратные вызовы не проверяются. Для защиты асинхронных вызовов в скриптах необходимо задать для раздела реестра значение 1 (один).

Скрипты могут использовать методы [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) и [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) объекта реестра [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) для изменения значения параметра реестра **унсекаппакцессконтролдефаулт** . Дополнительные сведения о проверке подлинности и уровнях олицетворения, необходимых для удаленного доступа, см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>Настройка безопасности асинхронного вызова в VBScript

В следующем примере кода VBScript показано, как изменить значение реестра для управления проверкой подлинности WMI для обратных вызовов.

Сценарий изменяет значение **унсекаппакцессконтролдефаулт** с нуля на единицу или значение, если оно уже задано, от одного до нуля. Нуль является значением по умолчанию для недавно установленной системы. После установки флага параметр сохраняется во время перезагрузки или перезапуска WMI.

Скрипт использует объект [**свбеммесод. unparameters**](swbemmethod-inparameters.md) и [**SWbemObject.ExeКмесод**](swbemobject-execmethod-.md) для вызова [**стдрегпров. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) и [**стдрегпров. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov). Дополнительные сведения о задании значений в объекте **параметров** см. в разделе [Создание объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Пример вызова в реестре с помощью [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)см. в разделе [**стдрегпров. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
