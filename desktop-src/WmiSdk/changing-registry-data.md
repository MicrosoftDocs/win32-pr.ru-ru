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
# <a name="changing-registry-data"></a><span data-ttu-id="5b1ec-103">Изменение данных реестра</span><span class="sxs-lookup"><span data-stu-id="5b1ec-103">Changing Registry Data</span></span>

<span data-ttu-id="5b1ec-104">Класс [поставщика системного реестра](/previous-versions/windows/desktop/regprov/system-registry-provider) [**стдрегпров**](/previous-versions/windows/desktop/regprov/stdregprov) для WMI имеет методы, которые выполняют следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5b1ec-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="5b1ec-105">Создание или удаление разделов реестра.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="5b1ec-106">Используйте [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) или [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="5b1ec-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="5b1ec-107">Создание или удаление именованных значений, которые называются записями, если они находятся под ключами.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="5b1ec-108">Для создания именованного значения используйте имя нового значения, [**сетбинаривалуе**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**сетдвордвалуе**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**сетекспандедстрингвалуе**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)или [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) .</span><span class="sxs-lookup"><span data-stu-id="5b1ec-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="5b1ec-109">Используйте [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) для удаления именованного значения.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="5b1ec-110">Измените именованные значения.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-110">Change named values.</span></span>

    <span data-ttu-id="5b1ec-111">Для изменения существующих именованных значений в разделе используйте имя значения и методы набора (определенные в предыдущем маркированном элементе).</span><span class="sxs-lookup"><span data-stu-id="5b1ec-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="5b1ec-112">Необходимо иметь имя значения, чтобы изменить его.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="5b1ec-113">Если вы не знакомы с именами значений в ключе, используйте метод [**енумвалуес**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) для получения имен.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="5b1ec-114">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="5b1ec-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="5b1ec-115">Создание раздела реестра с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="5b1ec-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="5b1ec-116">Создание именованного значения реестра с помощью PowerShell и VBScript</span><span class="sxs-lookup"><span data-stu-id="5b1ec-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="5b1ec-117">Создание раздела реестра с помощью VBScript</span><span class="sxs-lookup"><span data-stu-id="5b1ec-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="5b1ec-118">Поскольку реестр является центральной базой данных конфигурации для операционной системы, приложений и служб, будьте внимательны при записи изменений в значения реестра или удалении ключей.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="5b1ec-119">Нельзя отслеживать **\_ \_ корневой подраздел classes для классов hKey** **\_ Current \_ User (HKCU)**.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="5b1ec-120">Мониторинг **\_ пользователей hKey** не рекомендуется, так как подразделы появляются и исчезают при загрузке Hive.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="5b1ec-121">В следующих примерах кода показано, как создать новый раздел реестра и подраздел.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-121">The following code examples show how to create a new registry key and a subkey.</span></span>


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="5b1ec-122">Создание именованного значения реестра с помощью PowerShell и VBScript</span><span class="sxs-lookup"><span data-stu-id="5b1ec-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="5b1ec-123">В следующем примере кода показано, как создать именованное значение с именем **мултистрингвалуе** в **разделе \_ \_** \\ **программное обеспечение** \\ **MyKey** \\ **мисубкэй** , которое создает предыдущий сценарий.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="5b1ec-124">Скрипт вызывает [**стдрегпров. сетмултистрингвалуе**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) для записи строковых значений в новое именованное значение.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


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

<span data-ttu-id="5b1ec-125">С помощью инструментария WMI нельзя установить параметры безопасности доступа к разделу реестра.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="5b1ec-126">Однако метод [**стдрегпров. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) сравнивает параметры безопасности текущего пользователя с дескриптором безопасности раздела реестра, чтобы определить, имеет ли пользователь определенное разрешение, например **\_ \_ значение набора ключей**.</span><span class="sxs-lookup"><span data-stu-id="5b1ec-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
