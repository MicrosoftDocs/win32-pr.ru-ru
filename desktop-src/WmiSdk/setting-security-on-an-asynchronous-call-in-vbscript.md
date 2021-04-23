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
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a><span data-ttu-id="5f15c-103">Настройка безопасности при асинхронном вызове в VBScript</span><span class="sxs-lookup"><span data-stu-id="5f15c-103">Setting Security on an Asynchronous Call in VBScript</span></span>

<span data-ttu-id="5f15c-104">Производительность вызовов [*семисинчронаус*](gloss-s.md) обычно достаточно важна для большинства ситуаций.</span><span class="sxs-lookup"><span data-stu-id="5f15c-104">The performance of [*semisynchronous*](gloss-s.md) calls is usually adequate for most situations.</span></span> <span data-ttu-id="5f15c-105">Обычно асинхронные вызовы не рекомендуются для сценариев.</span><span class="sxs-lookup"><span data-stu-id="5f15c-105">Asynchronous calls are generally not a recommended practice for scripts.</span></span> <span data-ttu-id="5f15c-106">Однако если необходимо выполнить асинхронные вызовы, можно задать значение реестра, чтобы принудительно использовать WMI для проверки доступа при асинхронных вызовах.</span><span class="sxs-lookup"><span data-stu-id="5f15c-106">However, if asynchronous calls must be made, a registry value can be set to force WMI to perform access checks on asynchronous calls.</span></span>


<span data-ttu-id="5f15c-107">Значение реестра **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **унсекаппакцессконтролдефаулт** определяет, будет ли Инструментарий WMI проверять наличие приемлемого уровня проверки подлинности при возврате данных для асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="5f15c-107">The **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**UnsecAppAccessControlDefault** registry value controls whether WMI checks for an acceptable authentication level when returning data for an asynchronous call.</span></span> <span data-ttu-id="5f15c-108">Обратный вызов может быть возвращен на более низком уровне проверки подлинности по сравнению с исходным асинхронным вызовом.</span><span class="sxs-lookup"><span data-stu-id="5f15c-108">The callback can be returned at a lower authentication level than that of the original asynchronous call.</span></span> <span data-ttu-id="5f15c-109">По умолчанию это значение равно нулю, поэтому обратные вызовы не проверяются.</span><span class="sxs-lookup"><span data-stu-id="5f15c-109">By default, this value is set to zero so that callbacks are not checked.</span></span> <span data-ttu-id="5f15c-110">Для защиты асинхронных вызовов в скриптах необходимо задать для раздела реестра значение 1 (один).</span><span class="sxs-lookup"><span data-stu-id="5f15c-110">To secure asynchronous calls in scripting, you must set the registry key to 1 (one).</span></span>

<span data-ttu-id="5f15c-111">Скрипты могут использовать методы [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) и [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) объекта реестра [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) для изменения значения параметра реестра **унсекаппакцессконтролдефаулт** .</span><span class="sxs-lookup"><span data-stu-id="5f15c-111">Scripts can use the [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) methods of the registry object [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) to change the setting of the **UnsecAppAccessControlDefault** registry value.</span></span> <span data-ttu-id="5f15c-112">Дополнительные сведения о проверке подлинности и уровнях олицетворения, необходимых для удаленного доступа, см. в разделе [Подключение к WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="5f15c-112">For more information about authentication and impersonation levels required for remote access, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

## <a name="to-set-asynchronous-call-security-in-vbscript"></a><span data-ttu-id="5f15c-113">Настройка безопасности асинхронного вызова в VBScript</span><span class="sxs-lookup"><span data-stu-id="5f15c-113">To set asynchronous call security in VBScript</span></span>

<span data-ttu-id="5f15c-114">В следующем примере кода VBScript показано, как изменить значение реестра для управления проверкой подлинности WMI для обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="5f15c-114">The following VBScript code example shows you how to change the registry value to control WMI authentication of callbacks.</span></span>

<span data-ttu-id="5f15c-115">Сценарий изменяет значение **унсекаппакцессконтролдефаулт** с нуля на единицу или значение, если оно уже задано, от одного до нуля.</span><span class="sxs-lookup"><span data-stu-id="5f15c-115">The script changes the value of **UnsecAppAccessControlDefault** from zero to one, or if the value is already set, from one to zero.</span></span> <span data-ttu-id="5f15c-116">Нуль является значением по умолчанию для недавно установленной системы.</span><span class="sxs-lookup"><span data-stu-id="5f15c-116">Zero is the default on a newly installed system.</span></span> <span data-ttu-id="5f15c-117">После установки флага параметр сохраняется во время перезагрузки или перезапуска WMI.</span><span class="sxs-lookup"><span data-stu-id="5f15c-117">Once the flag is set, the setting persists across reboot or WMI restart.</span></span>

<span data-ttu-id="5f15c-118">Скрипт использует объект [**свбеммесод. unparameters**](swbemmethod-inparameters.md) и [**SWbemObject.ExeКмесод**](swbemobject-execmethod-.md) для вызова [**стдрегпров. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) и [**стдрегпров. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="5f15c-118">The script uses a [**SWbemMethod.InParameters**](swbemmethod-inparameters.md) object and [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) to call [**StdRegProv.GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) and [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span> <span data-ttu-id="5f15c-119">Дополнительные сведения о задании значений в объекте **параметров** см. в разделе [Создание объектов параметров и анализ объектов параметров](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5f15c-119">For more information about setting the values in an **InParameters** object, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span> <span data-ttu-id="5f15c-120">Пример вызова в реестре с помощью [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)см. в разделе [**стдрегпров. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="5f15c-120">For an example of a registry call using [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), see [**StdRegProv.SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).</span></span>


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



 

 
