---
description: Содержит число элементов в коллекции.
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
ms.openlocfilehash: a8d5b9e605650ba7d3cb6036e8abfac58c0b8597
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986017"
---
# <a name="shellwindowscount-property"></a><span data-ttu-id="588ae-103">Шеллвиндовс. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="588ae-103">ShellWindows.Count property</span></span>

<span data-ttu-id="588ae-104">Содержит число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="588ae-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="588ae-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="588ae-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="588ae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="588ae-106">Syntax</span></span>


```JScript
iCount = ShellWindows.Count
```



## <a name="property-value"></a><span data-ttu-id="588ae-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="588ae-107">Property value</span></span>

<span data-ttu-id="588ae-108">**Целое число** , содержащее значение для свойства **Count** .</span><span class="sxs-lookup"><span data-stu-id="588ae-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="588ae-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="588ae-109">Examples</span></span>

<span data-ttu-id="588ae-110">В следующем примере показано использование **счетчика** .</span><span class="sxs-lookup"><span data-stu-id="588ae-110">The following example shows **Count** in use.</span></span> <span data-ttu-id="588ae-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="588ae-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="588ae-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="588ae-112">JScript:</span></span>


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



<span data-ttu-id="588ae-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="588ae-113">VBScript:</span></span>


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



<span data-ttu-id="588ae-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="588ae-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="588ae-115">Требования</span><span class="sxs-lookup"><span data-stu-id="588ae-115">Requirements</span></span>



| <span data-ttu-id="588ae-116">Требование</span><span class="sxs-lookup"><span data-stu-id="588ae-116">Requirement</span></span> | <span data-ttu-id="588ae-117">Значение</span><span class="sxs-lookup"><span data-stu-id="588ae-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="588ae-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="588ae-118">Minimum supported client</span></span><br/> | <span data-ttu-id="588ae-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="588ae-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="588ae-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="588ae-120">Minimum supported server</span></span><br/> | <span data-ttu-id="588ae-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="588ae-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="588ae-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="588ae-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="588ae-123"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="588ae-123"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="588ae-124">DLL</span><span class="sxs-lookup"><span data-stu-id="588ae-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="588ae-125"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="588ae-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




