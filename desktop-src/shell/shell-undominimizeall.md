---
description: Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды Минимизеалл.
ms.assetid: dcedfa18-6dde-4fb8-9679-4d6ff80249e4
title: Метод Shell. Ундоминимизеалл (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4a5010e4ac6b4fca42689f7c80db50c55ab2cb4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265074"
---
# <a name="shellundominimizeall-method"></a><span data-ttu-id="55df7-103">Shell. Ундоминимизеалл, метод</span><span class="sxs-lookup"><span data-stu-id="55df7-103">Shell.UndoMinimizeALL method</span></span>

<span data-ttu-id="55df7-104">Восстанавливает все настольные компьютеры в том же состоянии, в котором они находились до последней команды [**минимизеалл**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="55df7-104">Restores all desktop windows to the same state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="55df7-105">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды **отменить свернуть все окна** в старых системах или второй щелчок значка Свернуть **Рабочий стол** в области Быстрый запуск панели задач в Windows 2000 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="55df7-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** on older systems or a second clicking of the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="55df7-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55df7-106">Syntax</span></span>


```JScript
iRetVal = Shell.UndoMinimizeALL()
```


```VB

Shell.UndoMinimizeALL() As Integer
```





## <a name="parameters"></a><span data-ttu-id="55df7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="55df7-107">Parameters</span></span>

<span data-ttu-id="55df7-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="55df7-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="55df7-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="55df7-109">Examples</span></span>

<span data-ttu-id="55df7-110">В следующем примере показано использование **ундоминимизеалл** .</span><span class="sxs-lookup"><span data-stu-id="55df7-110">The following example shows **UndoMinimizeALL** in use.</span></span> <span data-ttu-id="55df7-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55df7-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="55df7-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="55df7-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="55df7-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="55df7-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="55df7-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="55df7-114">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="55df7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="55df7-115">Requirements</span></span>



| <span data-ttu-id="55df7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="55df7-116">Requirement</span></span> | <span data-ttu-id="55df7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="55df7-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55df7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55df7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="55df7-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55df7-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55df7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55df7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="55df7-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55df7-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55df7-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55df7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="55df7-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="55df7-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="55df7-124">IDL</span><span class="sxs-lookup"><span data-stu-id="55df7-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55df7-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55df7-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="55df7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="55df7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55df7-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="55df7-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




