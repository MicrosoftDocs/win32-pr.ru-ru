---
description: Восстанавливает все настольные окна до состояния, в котором они были до последней команды Минимизеалл.
ms.assetid: 32BDE544-C4FF-4a64-99AF-F8960AEC4690
title: Ишеллдиспатч. Ундоминимизеалл, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.UndoMinimizeALL
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1b11fdd7a0a82a11baa20b0f3a63a31a8a46b701
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543135"
---
# <a name="ishelldispatchundominimizeall-method"></a><span data-ttu-id="6d2a0-103">Ишеллдиспатч. Ундоминимизеалл, метод</span><span class="sxs-lookup"><span data-stu-id="6d2a0-103">IShellDispatch.UndoMinimizeALL method</span></span>

<span data-ttu-id="6d2a0-104">Восстанавливает все настольные окна до состояния, в котором они были до последней команды [**минимизеалл**](shell-minimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2a0-104">Restores all desktop windows to the state they were in before the last [**MinimizeAll**](shell-minimizeall.md) command.</span></span> <span data-ttu-id="6d2a0-105">Этот метод действует аналогично щелчку правой кнопкой мыши панели задач и выбора команды **отменить свернуть все окна** (в старых системах) или второй щелчок значка Свернуть **Рабочий стол** на панели задач.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-105">This method has the same effect as right-clicking the taskbar and selecting **Undo Minimize All Windows** (on older systems) or a second clicking of the **Show Desktop** icon in the taskbar.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d2a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d2a0-106">Syntax</span></span>


```JScript
IShellDispatch.UndoMinimizeALL()
```


```VB

IShellDispatch.UndoMinimizeALL()
```





## <a name="parameters"></a><span data-ttu-id="6d2a0-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d2a0-107">Parameters</span></span>

<span data-ttu-id="6d2a0-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d2a0-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d2a0-109">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="6d2a0-110">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="6d2a0-110">JScript</span></span>

<span data-ttu-id="6d2a0-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-111">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="6d2a0-112">VB</span><span class="sxs-lookup"><span data-stu-id="6d2a0-112">VB</span></span>

<span data-ttu-id="6d2a0-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d2a0-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d2a0-114">Remarks</span></span>

<span data-ttu-id="6d2a0-115">Этот метод реализован и доступен через метод [**Shell. ундоминимизеалл**](./shell-undominimizeall.md) .</span><span class="sxs-lookup"><span data-stu-id="6d2a0-115">This method is implemented and accessed through the [**Shell.UndoMinimizeAll**](./shell-undominimizeall.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="6d2a0-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d2a0-116">Examples</span></span>

<span data-ttu-id="6d2a0-117">В следующих примерах показано использование **ундоминимизеалл** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-117">The following examples show the use of **UndoMinimizeALL** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6d2a0-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="6d2a0-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellUndoMinimizeALLJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.UndoMinimizeALL();
    }
</script>
```



<span data-ttu-id="6d2a0-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="6d2a0-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellUndoMinimizeALLVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.UndoMinimizeALL

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="6d2a0-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6d2a0-120">Visual Basic:</span></span>


```VB
Private Sub fnShellUndoMinimizeAllVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.UndoMinimizeALL

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6d2a0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6d2a0-121">Requirements</span></span>



| <span data-ttu-id="6d2a0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6d2a0-122">Requirement</span></span> | <span data-ttu-id="6d2a0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6d2a0-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d2a0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d2a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6d2a0-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d2a0-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6d2a0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d2a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6d2a0-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6d2a0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6d2a0-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6d2a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d2a0-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d2a0-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="6d2a0-130">IDL</span><span class="sxs-lookup"><span data-stu-id="6d2a0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6d2a0-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6d2a0-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="6d2a0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="6d2a0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d2a0-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6d2a0-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
