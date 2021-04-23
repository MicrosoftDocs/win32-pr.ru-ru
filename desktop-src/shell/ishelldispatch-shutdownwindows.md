---
description: Отображает диалоговое окно Завершение работы Windows. Это то же самое, что и при нажатии кнопки «Пуск», и при выборе «завершение работы».
ms.assetid: 3C4F6579-6398-4af4-8911-FE22555B0ABC
title: Ишеллдиспатч. Шутдовнвиндовс, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c111e1b740857337953cdcdf81735a8c0568ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997287"
---
# <a name="ishelldispatchshutdownwindows-method"></a><span data-ttu-id="9a92c-104">Ишеллдиспатч. Шутдовнвиндовс, метод</span><span class="sxs-lookup"><span data-stu-id="9a92c-104">IShellDispatch.ShutdownWindows method</span></span>

<span data-ttu-id="9a92c-105">Отображает диалоговое окно **Завершение работы Windows** .</span><span class="sxs-lookup"><span data-stu-id="9a92c-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="9a92c-106">Это то же самое, что и при нажатии кнопки « **Пуск** », и при выборе « **Завершение работы**».</span><span class="sxs-lookup"><span data-stu-id="9a92c-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a92c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a92c-107">Syntax</span></span>


```JScript
IShellDispatch.ShutdownWindows()
```


```VB

IShellDispatch.ShutdownWindows()
```





## <a name="parameters"></a><span data-ttu-id="9a92c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a92c-108">Parameters</span></span>

<span data-ttu-id="9a92c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="9a92c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a92c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a92c-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="9a92c-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="9a92c-111">JScript</span></span>

<span data-ttu-id="9a92c-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a92c-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="9a92c-113">VB</span><span class="sxs-lookup"><span data-stu-id="9a92c-113">VB</span></span>

<span data-ttu-id="9a92c-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a92c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a92c-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="9a92c-115">Remarks</span></span>

<span data-ttu-id="9a92c-116">Этот метод реализован и доступен через метод [**Shell. шутдовнвиндовс**](shell-shutdownwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="9a92c-116">This method is implemented and accessed through the [**Shell.ShutdownWindows**](shell-shutdownwindows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="9a92c-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="9a92c-117">Examples</span></span>

<span data-ttu-id="9a92c-118">В следующем примере показано использование **шутдовнвиндовс** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9a92c-118">The following example shows the use of **ShutdownWindows** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9a92c-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="9a92c-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="9a92c-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="9a92c-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.ShutdownWindows

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9a92c-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9a92c-121">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9a92c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9a92c-122">Requirements</span></span>



| <span data-ttu-id="9a92c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9a92c-123">Requirement</span></span> | <span data-ttu-id="9a92c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9a92c-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a92c-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a92c-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9a92c-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9a92c-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9a92c-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a92c-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9a92c-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9a92c-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9a92c-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9a92c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a92c-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a92c-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9a92c-131">IDL</span><span class="sxs-lookup"><span data-stu-id="9a92c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a92c-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a92c-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9a92c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9a92c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a92c-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9a92c-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




