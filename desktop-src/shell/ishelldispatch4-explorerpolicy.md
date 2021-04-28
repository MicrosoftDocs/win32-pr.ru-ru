---
description: IShellDispatch4. Експлорерполици, метод возвращает значение для указанной политики Windows Internet Explorer.
ms.assetid: 490c3e18-b606-456a-9016-dc4f7bad2bc3
title: IShellDispatch4. Експлорерполици, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a03d61905bdb1f2b16de11cc604625d8e71a7ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116834"
---
# <a name="ishelldispatch4explorerpolicy-method"></a><span data-ttu-id="04cc4-103">IShellDispatch4. Експлорерполици, метод</span><span class="sxs-lookup"><span data-stu-id="04cc4-103">IShellDispatch4.ExplorerPolicy method</span></span>

<span data-ttu-id="04cc4-104">Возвращает значение для указанной политики Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="04cc4-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="04cc4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04cc4-105">Syntax</span></span>


```JScript
retVal = IShellDispatch4.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

IShellDispatch4.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="04cc4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04cc4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04cc4-107">*бстрполицинаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04cc4-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04cc4-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="04cc4-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="04cc4-109">**Строка** , указывающая имя политики.</span><span class="sxs-lookup"><span data-stu-id="04cc4-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04cc4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04cc4-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="04cc4-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="04cc4-111">JScript</span></span>

<span data-ttu-id="04cc4-112">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="04cc4-112">Type: **Variant\***</span></span>

<span data-ttu-id="04cc4-113">Значение, связанное с указанным именем политики.</span><span class="sxs-lookup"><span data-stu-id="04cc4-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="04cc4-114">VB</span><span class="sxs-lookup"><span data-stu-id="04cc4-114">VB</span></span>

<span data-ttu-id="04cc4-115">Тип: **Variant \***</span><span class="sxs-lookup"><span data-stu-id="04cc4-115">Type: **Variant\***</span></span>

<span data-ttu-id="04cc4-116">Значение, связанное с указанным именем политики.</span><span class="sxs-lookup"><span data-stu-id="04cc4-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="04cc4-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="04cc4-117">Remarks</span></span>

<span data-ttu-id="04cc4-118">Сетевые администраторы могут управлять вычислительной средой пользователей и управлять ею, настроив политики.</span><span class="sxs-lookup"><span data-stu-id="04cc4-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="04cc4-119">Указанное имя значения должно **находиться в \_ \_** \\  \\  \\  \\  \\  \\  подразделе раздела реестра "Microsoft Windows CurrentVersion Policies.</span><span class="sxs-lookup"><span data-stu-id="04cc4-119">The specified value name must be within the **HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Policies**\\**Explorer** subkey.</span></span> <span data-ttu-id="04cc4-120">Если имя параметра не существует, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="04cc4-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="04cc4-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="04cc4-121">Examples</span></span>

<span data-ttu-id="04cc4-122">В следующих примерах показано правильное использование **експлорерполици** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="04cc4-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="04cc4-123">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="04cc4-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objshell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="04cc4-124">Сценариев</span><span class="sxs-lookup"><span data-stu-id="04cc4-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objshell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="04cc4-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="04cc4-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objshell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="04cc4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="04cc4-126">Requirements</span></span>



| <span data-ttu-id="04cc4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="04cc4-127">Requirement</span></span> | <span data-ttu-id="04cc4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="04cc4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04cc4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04cc4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="04cc4-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="04cc4-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="04cc4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04cc4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="04cc4-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="04cc4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="04cc4-133">Header</span><span class="sxs-lookup"><span data-stu-id="04cc4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="04cc4-134"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="04cc4-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="04cc4-135">IDL</span><span class="sxs-lookup"><span data-stu-id="04cc4-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04cc4-136"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04cc4-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="04cc4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="04cc4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04cc4-138"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="04cc4-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
