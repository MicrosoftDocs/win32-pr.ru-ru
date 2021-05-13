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
ms.openlocfilehash: 472f6141b8aaed47ac05c8eaf670a0d039ce5561
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841015"
---
# <a name="shelltoggledesktop-method"></a><span data-ttu-id="a2e3a-103">Shell. Тоггледесктоп, метод</span><span class="sxs-lookup"><span data-stu-id="a2e3a-103">Shell.ToggleDesktop method</span></span>

<span data-ttu-id="a2e3a-104">Отображает или скрывает Рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-104">Displays or hides the desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2e3a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a2e3a-105">Syntax</span></span>


```JScript
Shell.ToggleDesktop()
```


```VB

Shell.ToggleDesktop()
```





## <a name="parameters"></a><span data-ttu-id="a2e3a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2e3a-106">Parameters</span></span>

<span data-ttu-id="a2e3a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a2e3a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a2e3a-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="a2e3a-109">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="a2e3a-109">JScript</span></span>

<span data-ttu-id="a2e3a-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="a2e3a-111">VB</span><span class="sxs-lookup"><span data-stu-id="a2e3a-111">VB</span></span>

<span data-ttu-id="a2e3a-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2e3a-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="a2e3a-113">Remarks</span></span>

<span data-ttu-id="a2e3a-114">Этот метод действует так же, как кнопка " **Свернуть Рабочий стол** " на панели задач.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-114">This method has the same effect as the **Show Desktop** button on the taskbar.</span></span> <span data-ttu-id="a2e3a-115">Он либо скрывает все открытые окна для отображения рабочего стола, либо скрывает Рабочий стол, отображая все открытые окна.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-115">It either hides all open windows to show the desktop or it hides the desktop by showing all open windows.</span></span> <span data-ttu-id="a2e3a-116">Метод **тоггледесктоп** не отображает пользовательский интерфейс, он просто вызывает действие Toggle.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-116">The **ToggleDesktop** method does not display a user interface, it just invokes the toggle action.</span></span>

## <a name="examples"></a><span data-ttu-id="a2e3a-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2e3a-117">Examples</span></span>

<span data-ttu-id="a2e3a-118">В следующих примерах показано правильное использование **тоггледесктоп** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a2e3a-118">The following examples show the proper use of **ToggleDesktop** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a2e3a-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a2e3a-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch4ToggleDesktopJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ToggleDesktop();
    }
</script>
```



<span data-ttu-id="a2e3a-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a2e3a-120">VBScript:</span></span>


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



<span data-ttu-id="a2e3a-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a2e3a-121">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch4ToggleDesktopVB()
    Dim objShell As Shell
            
    Set objShell = New Shell
        objShell.ToggleDesktop
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a2e3a-122">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a2e3a-122">Requirements</span></span>



| <span data-ttu-id="a2e3a-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a2e3a-123">Requirement</span></span> | <span data-ttu-id="a2e3a-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a2e3a-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2e3a-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2e3a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a2e3a-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a2e3a-126">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="a2e3a-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2e3a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a2e3a-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a2e3a-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a2e3a-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a2e3a-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2e3a-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2e3a-130"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a2e3a-131">IDL</span><span class="sxs-lookup"><span data-stu-id="a2e3a-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a2e3a-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a2e3a-132"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a2e3a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a2e3a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2e3a-134"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a2e3a-134"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




