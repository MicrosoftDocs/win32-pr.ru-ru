---
description: Располагает все окна на рабочем столе по вертикали. Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор окон мозаики по вертикали.
ms.assetid: 7d0f6dbe-b5a6-431b-954f-7ef2c62c68ea
title: Метод Shell. Тилевертикалли (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.TileVertically
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8ecea9df2bcbb2e410841231ed7eca170872e015
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985964"
---
# <a name="shelltilevertically-method"></a><span data-ttu-id="7f4c2-104">Shell. Тилевертикалли, метод</span><span class="sxs-lookup"><span data-stu-id="7f4c2-104">Shell.TileVertically method</span></span>

<span data-ttu-id="7f4c2-105">Располагает все окна на рабочем столе по вертикали.</span><span class="sxs-lookup"><span data-stu-id="7f4c2-105">Tiles all of the windows on the desktop vertically.</span></span> <span data-ttu-id="7f4c2-106">Этот метод действует так же, как и щелчок правой кнопкой мыши панели задач и выбор **окон мозаики по вертикали**.</span><span class="sxs-lookup"><span data-stu-id="7f4c2-106">This method has the same effect as right-clicking the taskbar and selecting **Tile Windows Vertically**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f4c2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f4c2-107">Syntax</span></span>


```JScript
iRetVal = Shell.TileVertically()
```


```VB

Shell.TileVertically() As Integer
```





## <a name="parameters"></a><span data-ttu-id="7f4c2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f4c2-108">Parameters</span></span>

<span data-ttu-id="7f4c2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7f4c2-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="7f4c2-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="7f4c2-110">Examples</span></span>

<span data-ttu-id="7f4c2-111">В следующем примере показано использование **тилевертикалли** .</span><span class="sxs-lookup"><span data-stu-id="7f4c2-111">The following example shows **TileVertically** in use.</span></span> <span data-ttu-id="7f4c2-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7f4c2-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7f4c2-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7f4c2-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellTileVerticallyJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.TileVertically();
    }
</script>
```



<span data-ttu-id="7f4c2-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7f4c2-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellTileVerticallyVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.TileVertically

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7f4c2-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7f4c2-115">Visual Basic:</span></span>


```VB
Private Sub fnShellTileVerticallyVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.TileVertically

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7f4c2-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7f4c2-116">Requirements</span></span>



| <span data-ttu-id="7f4c2-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7f4c2-117">Requirement</span></span> | <span data-ttu-id="7f4c2-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7f4c2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f4c2-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f4c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f4c2-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f4c2-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f4c2-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f4c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f4c2-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f4c2-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f4c2-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f4c2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f4c2-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f4c2-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7f4c2-125">IDL</span><span class="sxs-lookup"><span data-stu-id="7f4c2-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f4c2-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f4c2-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7f4c2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f4c2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f4c2-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7f4c2-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




