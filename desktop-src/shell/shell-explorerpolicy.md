---
description: Возвращает значение для указанной политики Windows Internet Explorer.
ms.assetid: 47E17F6A-ED43-44cd-AF77-A6E49865E1B5
title: Метод Shell. Експлорерполици (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ExplorerPolicy
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fea5192990b8c19c8ddfe8ffad6efe21b98625c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986092"
---
# <a name="shellexplorerpolicy-method"></a><span data-ttu-id="a79cc-103">Shell. Експлорерполици, метод</span><span class="sxs-lookup"><span data-stu-id="a79cc-103">Shell.ExplorerPolicy method</span></span>

<span data-ttu-id="a79cc-104">Возвращает значение для указанной политики Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a79cc-104">Gets the value for a specified Windows Internet Explorer policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="a79cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a79cc-105">Syntax</span></span>


```JScript
retVal = Shell.ExplorerPolicy(
  bstrPolicyName
)
```


```VB

Shell.ExplorerPolicy( _
  ByVal bstrPolicyName As BSTR _
) As Variant
```





## <a name="parameters"></a><span data-ttu-id="a79cc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a79cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a79cc-107">*бстрполицинаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a79cc-107">*bstrPolicyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a79cc-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="a79cc-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="a79cc-109">**Строка** , указывающая имя политики.</span><span class="sxs-lookup"><span data-stu-id="a79cc-109">A **String** that specifies the name of the policy.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a79cc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a79cc-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a79cc-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="a79cc-111">JScript</span></span>

<span data-ttu-id="a79cc-112">Тип: \**Variant \** _</span><span class="sxs-lookup"><span data-stu-id="a79cc-112">Type: \**Variant\** _</span></span>

<span data-ttu-id="a79cc-113">Значение, связанное с указанным именем политики.</span><span class="sxs-lookup"><span data-stu-id="a79cc-113">The value associated with the specified policy name.</span></span>

### <a name="vb"></a><span data-ttu-id="a79cc-114">VB</span><span class="sxs-lookup"><span data-stu-id="a79cc-114">VB</span></span>

<span data-ttu-id="a79cc-115">Тип: _*Variant \**_</span><span class="sxs-lookup"><span data-stu-id="a79cc-115">Type: _*Variant\**_</span></span>

<span data-ttu-id="a79cc-116">Значение, связанное с указанным именем политики.</span><span class="sxs-lookup"><span data-stu-id="a79cc-116">The value associated with the specified policy name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a79cc-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="a79cc-117">Remarks</span></span>

<span data-ttu-id="a79cc-118">Сетевые администраторы могут управлять вычислительной средой пользователей и управлять ею, настроив политики.</span><span class="sxs-lookup"><span data-stu-id="a79cc-118">Network Administrators can control and manage the computing environment of their users by setting policies.</span></span>

<span data-ttu-id="a79cc-119">Указанное имя значения должно находиться в подразделе "_,\*\_ текущее \_ пользовательское **\\** программное обеспечение **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** политики **\\** обозревателя\*\*".</span><span class="sxs-lookup"><span data-stu-id="a79cc-119">The specified value name must be within the _ *HKEY\_CURRENT\_USER **\\** Software **\\** Microsoft **\\** Windows **\\** CurrentVersion **\\** Policies **\\** Explorer*\* subkey.</span></span> <span data-ttu-id="a79cc-120">Если имя параметра не существует, метод возвращает **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="a79cc-120">If the value name does not exist then the method returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="a79cc-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="a79cc-121">Examples</span></span>

<span data-ttu-id="a79cc-122">В следующих примерах показано правильное использование **експлорерполици** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a79cc-122">The following examples show the proper use of **ExplorerPolicy** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a79cc-123">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a79cc-123">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ExplorerPolicyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;
        
        vReturn = objShell.ExplorerPolicy("ValueName");
        alert(vReturn);
    }
</script>
```



<span data-ttu-id="a79cc-124">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a79cc-124">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch4ExplorerPolicyVB()
        dim objShell
        dim vReturn
        
        set objShell = CreateObject("shell.application")
            vReturn = objShell.ExplorerPolicy("ValueName")
            alert(vReturn)
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a79cc-125">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a79cc-125">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ExplorerPolicyVB()
    Dim objShell As Shell
    Dim vReturn  As Variant
    
    Set objShell = New Shell
        vReturn = objShell.ExplorerPolicy("ValueName")
        Debug.Print vReturn
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a79cc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a79cc-126">Requirements</span></span>



| <span data-ttu-id="a79cc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a79cc-127">Requirement</span></span> | <span data-ttu-id="a79cc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a79cc-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a79cc-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a79cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a79cc-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a79cc-130">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a79cc-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a79cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a79cc-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a79cc-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a79cc-133">Header</span><span class="sxs-lookup"><span data-stu-id="a79cc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a79cc-134"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a79cc-134"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a79cc-135">IDL</span><span class="sxs-lookup"><span data-stu-id="a79cc-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a79cc-136"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a79cc-136"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a79cc-137">DLL</span><span class="sxs-lookup"><span data-stu-id="a79cc-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a79cc-138"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a79cc-138"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
