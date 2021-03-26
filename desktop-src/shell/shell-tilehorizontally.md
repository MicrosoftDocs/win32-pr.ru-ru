---
description: Мозаичное отображение всех окон на рабочем столе по горизонтали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор окон мозаики по горизонтали.
ms.assetid: b0e06766-1bd4-4744-81f3-139b018aa72c
title: Метод Shell. Тилехоризонталли (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileHorizontally
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e295d0a7847afc0cb405f3ab9141e54ae424e9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265075"
---
# <a name="shelltilehorizontally-method"></a><span data-ttu-id="72ce1-104">Shell. Тилехоризонталли, метод</span><span class="sxs-lookup"><span data-stu-id="72ce1-104">Shell.TileHorizontally method</span></span>

<span data-ttu-id="72ce1-105">Мозаичное отображение всех окон на рабочем столе по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="72ce1-105">Tiles all of the windows on the desktop horizontally.</span></span> <span data-ttu-id="72ce1-106">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор **окон мозаики по горизонтали**.</span><span class="sxs-lookup"><span data-stu-id="72ce1-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Horizontally**.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ce1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72ce1-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileHorizontally()
```


```VB

Shell.TileHorizontally() As Integer
```





## <a name="parameters"></a><span data-ttu-id="72ce1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="72ce1-108">Parameters</span></span>

<span data-ttu-id="72ce1-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="72ce1-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="72ce1-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="72ce1-110">Examples</span></span>

<span data-ttu-id="72ce1-111">В следующем примере показано использование **тилехоризонталли** .</span><span class="sxs-lookup"><span data-stu-id="72ce1-111">The following example shows **TileHorizontally** in use.</span></span> <span data-ttu-id="72ce1-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="72ce1-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="72ce1-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="72ce1-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileHorizontallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileHorizontally();
    }
</script>
```



<span data-ttu-id="72ce1-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="72ce1-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileHorizontallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileHorizontally

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="72ce1-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="72ce1-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileHorizontallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileHorizontally

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="72ce1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="72ce1-116">Requirements</span></span>



| <span data-ttu-id="72ce1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="72ce1-117">Requirement</span></span> | <span data-ttu-id="72ce1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="72ce1-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ce1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72ce1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="72ce1-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="72ce1-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="72ce1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72ce1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="72ce1-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="72ce1-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="72ce1-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="72ce1-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="72ce1-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="72ce1-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="72ce1-125">IDL</span><span class="sxs-lookup"><span data-stu-id="72ce1-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72ce1-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72ce1-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="72ce1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="72ce1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72ce1-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="72ce1-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




