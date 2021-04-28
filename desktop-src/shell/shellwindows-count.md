---
description: Шеллвиндовс. Count, свойство содержит количество элементов в коллекции.
ms.assetid: 0113cc32-2197-4004-99a1-89fe10828e5f
title: Свойство Шеллвиндовс. Count (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b2b33dc11e6bf909043ac5391965e1ebd225d376
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103942"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="1e3ea-103">Шеллвиндовс. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="1e3ea-103">ShellWindows.Count property</span></span>

<span data-ttu-id="1e3ea-104">Содержит число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="1e3ea-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="1e3ea-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1e3ea-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e3ea-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e3ea-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="1e3ea-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1e3ea-107">Property value</span></span>

<span data-ttu-id="1e3ea-108">**Целое число** , содержащее значение для свойства **Count** .</span><span class="sxs-lookup"><span data-stu-id="1e3ea-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="1e3ea-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="1e3ea-109">Examples</span></span>

<span data-ttu-id="1e3ea-110">В следующем примере показано использование **счетчика** .</span><span class="sxs-lookup"><span data-stu-id="1e3ea-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="1e3ea-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1e3ea-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1e3ea-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="1e3ea-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Shell_Windows();
        if (objShellWindows != null)
        {
            var nCount;
            
            nCount = objShellWindows.Count;
            alert(nCount);
        }
    }
</script>
```



<span data-ttu-id="1e3ea-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="1e3ea-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsCountVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim nCount
            nCount = objShellWindows.Count

            alert(nCount)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1e3ea-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1e3ea-114">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsCountVB()
    Dim objShell         As Shell
    Dim objShellWindows  As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1e3ea-115">Требования</span><span class="sxs-lookup"><span data-stu-id="1e3ea-115">Requirements</span></span>



| <span data-ttu-id="1e3ea-116">Требование</span><span class="sxs-lookup"><span data-stu-id="1e3ea-116">Requirement</span></span> | <span data-ttu-id="1e3ea-117">Значение</span><span class="sxs-lookup"><span data-stu-id="1e3ea-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e3ea-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e3ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e3ea-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1e3ea-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1e3ea-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e3ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e3ea-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1e3ea-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1e3ea-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1e3ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e3ea-123"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e3ea-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="1e3ea-124">DLL</span><span class="sxs-lookup"><span data-stu-id="1e3ea-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e3ea-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1e3ea-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




