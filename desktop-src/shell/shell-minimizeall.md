---
description: Свертывает все окна на рабочем столе.
ms.assetid: 3af98a16-27d1-4c93-ac72-7c9e24e68c23
title: Метод Shell. Минимизеалл (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.MinimizeAll
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 55b615cfed8813f5567b13d58648fef36aaedda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985972"
---
# <a name="shellminimizeall-method"></a><span data-ttu-id="42737-103">Shell. Минимизеалл, метод</span><span class="sxs-lookup"><span data-stu-id="42737-103">Shell.MinimizeAll method</span></span>

<span data-ttu-id="42737-104">Свертывает все окна на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="42737-104">Minimizes all of the windows on the desktop.</span></span> <span data-ttu-id="42737-105">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора пункта **Свернуть все окна** в старых системах или нажатия значка **Показывать Рабочий стол** в области Быстрый запуск панели задач в Windows 2000 или Windows XP.</span><span class="sxs-lookup"><span data-stu-id="42737-105">This method has the same effect as right-clicking the taskbar and selecting **Minimize All Windows** on older systems or clicking the **Show Desktop** icon in the Quick Launch area of the taskbar in Windows 2000 or Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="42737-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42737-106">Syntax</span></span>


```JScript
iRetVal = Shell.MinimizeAll()
```


```VB

Shell.MinimizeAll() As Integer
```





## <a name="parameters"></a><span data-ttu-id="42737-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="42737-107">Parameters</span></span>

<span data-ttu-id="42737-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="42737-108">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="42737-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="42737-109">Examples</span></span>

<span data-ttu-id="42737-110">В следующем примере показано использование **минимизеалл** .</span><span class="sxs-lookup"><span data-stu-id="42737-110">The following example shows **MinimizeAll** in use.</span></span> <span data-ttu-id="42737-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="42737-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="42737-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="42737-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellMinimizeAllJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.MinimizeAll();
    }
</script>
```



<span data-ttu-id="42737-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="42737-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellMinimizeAllVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.MinimizeAll

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="42737-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="42737-114">Visual Basic:</span></span>


```VB
Private Sub fnShellMinimizeAllVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.MinimizeAll

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="42737-115">Требования</span><span class="sxs-lookup"><span data-stu-id="42737-115">Requirements</span></span>



| <span data-ttu-id="42737-116">Требование</span><span class="sxs-lookup"><span data-stu-id="42737-116">Requirement</span></span> | <span data-ttu-id="42737-117">Значение</span><span class="sxs-lookup"><span data-stu-id="42737-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42737-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42737-118">Minimum supported client</span></span><br/> | <span data-ttu-id="42737-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="42737-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="42737-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42737-120">Minimum supported server</span></span><br/> | <span data-ttu-id="42737-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="42737-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="42737-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="42737-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="42737-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="42737-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="42737-124">IDL</span><span class="sxs-lookup"><span data-stu-id="42737-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="42737-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="42737-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="42737-126">DLL</span><span class="sxs-lookup"><span data-stu-id="42737-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="42737-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="42737-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42737-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42737-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42737-129">**Shell**</span><span class="sxs-lookup"><span data-stu-id="42737-129">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="42737-130">**ундоминимизеалл**</span><span class="sxs-lookup"><span data-stu-id="42737-130">**UndoMinimizeALL**</span></span>](shell-undominimizeall.md)
</dt> </dl>

 

 




