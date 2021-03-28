---
description: Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора окна каскадом.
ms.assetid: f73d2066-4626-455b-8ee6-f7004cc9e699
title: Метод Shell. Каскадевиндовс (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 751182ec53e0495021f4a6e2fad355c2c700ad66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545914"
---
# <a name="shellcascadewindows-method"></a><span data-ttu-id="03a33-104">Shell. Каскадевиндовс, метод</span><span class="sxs-lookup"><span data-stu-id="03a33-104">Shell.CascadeWindows method</span></span>

<span data-ttu-id="03a33-105">Каскадное расположение всех окон на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="03a33-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="03a33-106">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора **окна каскадом**.</span><span class="sxs-lookup"><span data-stu-id="03a33-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade Windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="03a33-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03a33-107">Syntax</span></span>


```JScript
Shell.CascadeWindows()
```


```VB

Shell.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="03a33-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="03a33-108">Parameters</span></span>

<span data-ttu-id="03a33-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="03a33-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03a33-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03a33-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="03a33-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="03a33-111">JScript</span></span>

<span data-ttu-id="03a33-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03a33-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="03a33-113">VB</span><span class="sxs-lookup"><span data-stu-id="03a33-113">VB</span></span>

<span data-ttu-id="03a33-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03a33-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="03a33-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="03a33-115">Examples</span></span>

<span data-ttu-id="03a33-116">В следующем примере показано использование **каскадевиндовс** .</span><span class="sxs-lookup"><span data-stu-id="03a33-116">The following example shows **CascadeWindows** in use.</span></span> <span data-ttu-id="03a33-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="03a33-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="03a33-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="03a33-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="03a33-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="03a33-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="03a33-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="03a33-120">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="03a33-121">Требования</span><span class="sxs-lookup"><span data-stu-id="03a33-121">Requirements</span></span>



| <span data-ttu-id="03a33-122">Требование</span><span class="sxs-lookup"><span data-stu-id="03a33-122">Requirement</span></span> | <span data-ttu-id="03a33-123">Значение</span><span class="sxs-lookup"><span data-stu-id="03a33-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03a33-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03a33-124">Minimum supported client</span></span><br/> | <span data-ttu-id="03a33-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="03a33-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03a33-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03a33-126">Minimum supported server</span></span><br/> | <span data-ttu-id="03a33-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="03a33-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="03a33-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="03a33-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="03a33-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="03a33-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="03a33-130">IDL</span><span class="sxs-lookup"><span data-stu-id="03a33-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03a33-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03a33-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="03a33-132">DLL</span><span class="sxs-lookup"><span data-stu-id="03a33-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03a33-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="03a33-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




