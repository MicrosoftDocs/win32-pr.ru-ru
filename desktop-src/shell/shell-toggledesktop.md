---
description: Shell. Тоггледесктоп-метод — отображает или скрывает Рабочий стол.
title: Метод Shell. Тоггледесктоп (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ToggleDesktop
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: BD07F7F2-A588-4189-95F4-3A8E2905E8F5
ms.openlocfilehash: c0d6c1e03db960c6abc8abc28ba8e79755fce639
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083682"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="87179-103">Shell. Тоггледесктоп, метод</span><span class="sxs-lookup"><span data-stu-id="87179-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="87179-104">Отображает или скрывает Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="87179-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="87179-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87179-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="87179-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87179-106">Parameters</span></span>

<span data-ttu-id="87179-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="87179-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87179-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87179-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="87179-109">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="87179-109">JScript</span></span>

<span data-ttu-id="87179-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="87179-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="87179-111">VB</span><span class="sxs-lookup"><span data-stu-id="87179-111">VB</span></span>

<span data-ttu-id="87179-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="87179-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="87179-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="87179-113">Remarks</span></span>

<span data-ttu-id="87179-114">Этот метод действует так же, как кнопка " **Свернуть Рабочий стол** " на панели задач.</span><span class="sxs-lookup"><span data-stu-id="87179-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="87179-115">Он либо скрывает все открытые окна для отображения рабочего стола, либо скрывает Рабочий стол, отображая все открытые окна.</span><span class="sxs-lookup"><span data-stu-id="87179-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="87179-116">Метод **тоггледесктоп** не отображает пользовательский интерфейс, он просто вызывает действие Toggle.</span><span class="sxs-lookup"><span data-stu-id="87179-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="87179-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="87179-117">Examples</span></span>

<span data-ttu-id="87179-118">В следующих примерах показано правильное использование **тоггледесктоп** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="87179-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="87179-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="87179-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="87179-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="87179-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellDispatch4ToggleDesktopVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
            objShell.ToggleDesktop
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="87179-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="87179-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="87179-122">Требования</span><span class="sxs-lookup"><span data-stu-id="87179-122">Requirements</span></span>



| <span data-ttu-id="87179-123">Требование</span><span class="sxs-lookup"><span data-stu-id="87179-123">Requirement</span></span> | <span data-ttu-id="87179-124">Значение</span><span class="sxs-lookup"><span data-stu-id="87179-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87179-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87179-125">Minimum supported client</span></span><br/> | <span data-ttu-id="87179-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87179-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="87179-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87179-127">Minimum supported server</span></span><br/> | <span data-ttu-id="87179-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87179-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="87179-129">Header</span><span class="sxs-lookup"><span data-stu-id="87179-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="87179-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="87179-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="87179-131">IDL</span><span class="sxs-lookup"><span data-stu-id="87179-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87179-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87179-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="87179-133">DLL</span><span class="sxs-lookup"><span data-stu-id="87179-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87179-134"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="87179-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




