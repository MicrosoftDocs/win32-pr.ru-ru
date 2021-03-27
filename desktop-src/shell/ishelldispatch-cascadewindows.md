---
description: Каскадное расположение всех окон на рабочем столе. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора окна каскадом.
ms.assetid: 6A957D70-D6A3-4485-8DF3-7FD2C6DEFF78
title: Ишеллдиспатч. Каскадевиндовс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.CascadeWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4252e4df579bc73e9f082630f9f98b83e3b57f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154946"
---
# <a name="ishelldispatchcascadewindows-method"></a><span data-ttu-id="11517-104">Ишеллдиспатч. Каскадевиндовс, метод</span><span class="sxs-lookup"><span data-stu-id="11517-104">IShellDispatch.CascadeWindows method</span></span>

<span data-ttu-id="11517-105">Каскадное расположение всех окон на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="11517-105">Cascades all of the windows on the desktop.</span></span> <span data-ttu-id="11517-106">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбора **окна каскадом**.</span><span class="sxs-lookup"><span data-stu-id="11517-106">This method has the same effect as right-clicking the taskbar and selecting **Cascade windows**.</span></span>

## <a name="syntax"></a><span data-ttu-id="11517-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="11517-107">Syntax</span></span>


```JScript
IShellDispatch.CascadeWindows()
```


```VB

IShellDispatch.CascadeWindows()
```





## <a name="parameters"></a><span data-ttu-id="11517-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11517-108">Parameters</span></span>

<span data-ttu-id="11517-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="11517-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="11517-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11517-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="11517-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="11517-111">JScript</span></span>

<span data-ttu-id="11517-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11517-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="11517-113">VB</span><span class="sxs-lookup"><span data-stu-id="11517-113">VB</span></span>

<span data-ttu-id="11517-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="11517-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="11517-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="11517-115">Remarks</span></span>

<span data-ttu-id="11517-116">Этот метод реализован и доступен через метод [**Shell. каскадевиндовс**](shell-cascadewindows.md) .</span><span class="sxs-lookup"><span data-stu-id="11517-116">This method is implemented and accessed through the [**Shell.CascadeWindows**](shell-cascadewindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="11517-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="11517-117">Examples</span></span>

<span data-ttu-id="11517-118">В следующих примерах показано использование **каскадевиндовс** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="11517-118">The following examples show the use of **CascadeWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="11517-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="11517-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellCascadeWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.CascadeWindows();
    }
</script>
```



<span data-ttu-id="11517-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="11517-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellCascadeWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.CascadeWindows
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="11517-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="11517-121">Visual Basic:</span></span>


```VB
Private Sub fnShellCascadeWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.CascadeWindows
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="11517-122">Требования</span><span class="sxs-lookup"><span data-stu-id="11517-122">Requirements</span></span>



| <span data-ttu-id="11517-123">Требование</span><span class="sxs-lookup"><span data-stu-id="11517-123">Requirement</span></span> | <span data-ttu-id="11517-124">Значение</span><span class="sxs-lookup"><span data-stu-id="11517-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11517-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11517-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11517-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="11517-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="11517-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11517-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11517-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="11517-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="11517-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="11517-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="11517-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="11517-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="11517-131">IDL</span><span class="sxs-lookup"><span data-stu-id="11517-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11517-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11517-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="11517-133">DLL</span><span class="sxs-lookup"><span data-stu-id="11517-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11517-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="11517-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




