---
description: Отображает окно справки и поддержки Windows. Этот метод действует так же, как и при щелчке меню Пуск и выбрав пункт Справка и поддержка.
ms.assetid: 9460C87E-6703-4df6-A84C-8D394E0E6703
title: Метод Ишеллдиспатч. Help (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b58bcc97748cecf6ab4064ecccf3ba5bbe190b57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984709"
---
# <a name="ishelldispatchhelp-method"></a><span data-ttu-id="842ed-104">Ишеллдиспатч. Help, метод</span><span class="sxs-lookup"><span data-stu-id="842ed-104">IShellDispatch.Help method</span></span>

<span data-ttu-id="842ed-105">Отображает окно справки и поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="842ed-105">Displays the Windows Help and Support window.</span></span> <span data-ttu-id="842ed-106">Этот метод действует так же, как и при щелчке меню **Пуск** и выбрав пункт **Справка и поддержка**.</span><span class="sxs-lookup"><span data-stu-id="842ed-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="842ed-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="842ed-107">Syntax</span></span>


```JScript
IShellDispatch.Help()
```


```VB

IShellDispatch.Help()
```





## <a name="parameters"></a><span data-ttu-id="842ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="842ed-108">Parameters</span></span>

<span data-ttu-id="842ed-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="842ed-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="842ed-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="842ed-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="842ed-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="842ed-111">JScript</span></span>

<span data-ttu-id="842ed-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="842ed-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="842ed-113">VB</span><span class="sxs-lookup"><span data-stu-id="842ed-113">VB</span></span>

<span data-ttu-id="842ed-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="842ed-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="842ed-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="842ed-115">Remarks</span></span>

<span data-ttu-id="842ed-116">Этот метод реализован и доступен через метод [**Shell. Help**](shell-help.md) .</span><span class="sxs-lookup"><span data-stu-id="842ed-116">This method is implemented and accessed through the [**Shell.Help**](shell-help.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="842ed-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="842ed-117">Examples</span></span>

<span data-ttu-id="842ed-118">В следующих примерах показано использование **справки** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="842ed-118">The following examples show the use of **Help** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="842ed-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="842ed-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Help();
    }
</script>
```



<span data-ttu-id="842ed-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="842ed-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="842ed-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="842ed-121">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="842ed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="842ed-122">Requirements</span></span>



| <span data-ttu-id="842ed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="842ed-123">Requirement</span></span> | <span data-ttu-id="842ed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="842ed-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842ed-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="842ed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="842ed-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="842ed-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="842ed-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="842ed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="842ed-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="842ed-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="842ed-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="842ed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="842ed-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="842ed-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="842ed-131">IDL</span><span class="sxs-lookup"><span data-stu-id="842ed-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="842ed-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="842ed-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="842ed-133">DLL</span><span class="sxs-lookup"><span data-stu-id="842ed-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="842ed-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="842ed-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




