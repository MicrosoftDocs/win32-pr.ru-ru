---
description: Отображает центр справки и поддержки Windows. Этот метод действует так же, как и при щелчке меню Пуск и выбрав пункт Справка и поддержка.
ms.assetid: fc13fef8-dac8-4c59-936d-8da0e63e06d4
title: Метод Shell. Help (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Help
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bfb4e9b3272355c41d13526d2e526515ff65d42b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264545"
---
# <a name="shellhelp-method"></a><span data-ttu-id="0ea18-104">Shell. Help, метод</span><span class="sxs-lookup"><span data-stu-id="0ea18-104">Shell.Help method</span></span>

<span data-ttu-id="0ea18-105">Отображает центр справки и поддержки Windows.</span><span class="sxs-lookup"><span data-stu-id="0ea18-105">Displays the Windows Help and Support Center.</span></span> <span data-ttu-id="0ea18-106">Этот метод действует так же, как и при щелчке меню **Пуск** и выбрав пункт **Справка и поддержка**.</span><span class="sxs-lookup"><span data-stu-id="0ea18-106">This method has the same effect as clicking the **Start** menu and selecting **Help and Support**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea18-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ea18-107">Syntax</span></span>


```JScript
Shell.Help()
```


```VB

Shell.Help()
```





## <a name="parameters"></a><span data-ttu-id="0ea18-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ea18-108">Parameters</span></span>

<span data-ttu-id="0ea18-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ea18-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ea18-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ea18-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="0ea18-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="0ea18-111">JScript</span></span>

<span data-ttu-id="0ea18-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0ea18-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="0ea18-113">VB</span><span class="sxs-lookup"><span data-stu-id="0ea18-113">VB</span></span>

<span data-ttu-id="0ea18-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0ea18-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="0ea18-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ea18-115">Examples</span></span>

<span data-ttu-id="0ea18-116">В следующем примере показана **Справка** по использованию.</span><span class="sxs-lookup"><span data-stu-id="0ea18-116">The following example shows **Help** in use.</span></span> <span data-ttu-id="0ea18-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="0ea18-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="0ea18-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="0ea18-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellHelpJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Help();
    }
</script>
```



<span data-ttu-id="0ea18-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="0ea18-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellHelpVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Help

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="0ea18-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="0ea18-120">Visual Basic:</span></span>


```VB
Private Sub fnShellHelpVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Help

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="0ea18-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0ea18-121">Requirements</span></span>



| <span data-ttu-id="0ea18-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0ea18-122">Requirement</span></span> | <span data-ttu-id="0ea18-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0ea18-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea18-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ea18-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea18-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0ea18-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0ea18-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ea18-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea18-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0ea18-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0ea18-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0ea18-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ea18-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea18-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="0ea18-130">IDL</span><span class="sxs-lookup"><span data-stu-id="0ea18-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0ea18-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0ea18-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="0ea18-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0ea18-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ea18-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="0ea18-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




