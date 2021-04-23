---
description: Отображает диалоговое окно Завершение работы Windows. Это то же самое, что и при нажатии кнопки «Пуск», и при выборе «завершение работы».
ms.assetid: 6fa8e2e0-a58f-4837-89f5-898cece2d80a
title: Метод Shell. Шутдовнвиндовс (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShutdownWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 804a1e211e191206d20f83d85dee2202492bfd27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265077"
---
# <a name="shellshutdownwindows-method"></a><span data-ttu-id="2a12e-104">Shell. Шутдовнвиндовс, метод</span><span class="sxs-lookup"><span data-stu-id="2a12e-104">Shell.ShutdownWindows method</span></span>

<span data-ttu-id="2a12e-105">Отображает диалоговое окно **Завершение работы Windows** .</span><span class="sxs-lookup"><span data-stu-id="2a12e-105">Displays the **Shut Down Windows** dialog box.</span></span> <span data-ttu-id="2a12e-106">Это то же самое, что и при нажатии кнопки « **Пуск** », и при выборе « **Завершение работы**».</span><span class="sxs-lookup"><span data-stu-id="2a12e-106">This is the same as clicking the **Start** menu and selecting **Shut Down**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a12e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a12e-107">Syntax</span></span>


```JScript
iRetVal = Shell.ShutdownWindows()
```


```VB

Shell.ShutdownWindows() As Integer
```





## <a name="parameters"></a><span data-ttu-id="2a12e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a12e-108">Parameters</span></span>

<span data-ttu-id="2a12e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2a12e-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="2a12e-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="2a12e-110">Examples</span></span>

<span data-ttu-id="2a12e-111">В следующем примере показано использование **шутдовнвиндовс** .</span><span class="sxs-lookup"><span data-stu-id="2a12e-111">The following example shows **ShutdownWindows** in use.</span></span> <span data-ttu-id="2a12e-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2a12e-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2a12e-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="2a12e-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShutdownWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShutdownWindows();
    }
</script>
```



<span data-ttu-id="2a12e-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="2a12e-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellShutdownWindowsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.ShutdownWindows

        set objShell = nothing
    end function
```



<span data-ttu-id="2a12e-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2a12e-115">Visual Basic:</span></span>


```VB
Private Sub fnShellShutdownWindowsVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.ShutdownWindows

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2a12e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2a12e-116">Requirements</span></span>



| <span data-ttu-id="2a12e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2a12e-117">Requirement</span></span> | <span data-ttu-id="2a12e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2a12e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a12e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2a12e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2a12e-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2a12e-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2a12e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2a12e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2a12e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2a12e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a12e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2a12e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a12e-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a12e-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2a12e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="2a12e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a12e-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a12e-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2a12e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2a12e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a12e-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="2a12e-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




