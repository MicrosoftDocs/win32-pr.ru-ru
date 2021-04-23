---
description: Создает и возвращает новый объект Шеллвиндовс, являющийся копией этого объекта Шеллвиндовс.
title: Метод ShellWindows._NewEnum (Ексдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows._NewEnum
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 85e84c13-62aa-4502-b642-ca55273a800d
ms.openlocfilehash: ded5ae2c337e80359c012fb63a37aa13cc43b5fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272322"
---
# <a name="shellwindows_newenum-method"></a><span data-ttu-id="8c8b0-103">Шеллвиндовс. \_ Метод NewEnum</span><span class="sxs-lookup"><span data-stu-id="8c8b0-103">ShellWindows.\_NewEnum method</span></span>

<span data-ttu-id="8c8b0-104">Создает и возвращает новый объект [**шеллвиндовс**](shellwindows.md) , являющийся копией этого объекта **шеллвиндовс** .</span><span class="sxs-lookup"><span data-stu-id="8c8b0-104">Creates and returns a new [**ShellWindows**](shellwindows.md) object that is a copy of this **ShellWindows** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c8b0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c8b0-105">Syntax</span></span>


```JScript
retVal = ShellWindows._NewEnum()
```



## <a name="parameters"></a><span data-ttu-id="8c8b0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c8b0-106">Parameters</span></span>

<span data-ttu-id="8c8b0-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8c8b0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8c8b0-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8c8b0-108">Return value</span></span>

<span data-ttu-id="8c8b0-109">Тип: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="8c8b0-109">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="8c8b0-110">Ссылка на объект для копирования объекта [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="8c8b0-110">An object reference to the [**ShellWindows**](shellwindows.md) object copy.</span></span>

## <a name="examples"></a><span data-ttu-id="8c8b0-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="8c8b0-111">Examples</span></span>

<span data-ttu-id="8c8b0-112">В следующем примере показано использование **\_ NewEnum** .</span><span class="sxs-lookup"><span data-stu-id="8c8b0-112">The following example shows **\_NewEnum** in use.</span></span> <span data-ttu-id="8c8b0-113">Для VBScript и Visual Basic отображается правильное использование.</span><span class="sxs-lookup"><span data-stu-id="8c8b0-113">Proper usage is shown for VBScript and Visual Basic.</span></span> <span data-ttu-id="8c8b0-114">Этот метод нельзя использовать с JScript.</span><span class="sxs-lookup"><span data-stu-id="8c8b0-114">This method cannot be used with JScript.</span></span>

<span data-ttu-id="8c8b0-115">Сценариев</span><span class="sxs-lookup"><span data-stu-id="8c8b0-115">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsNewEnumVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Shell_Windows

        if (not objShellWindows is nothing) then
            dim objEnumItems
            
            for each objEnumItems in objShellWindows
                alert(objEnumItems.Type)
            next
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="8c8b0-116">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8c8b0-116">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsNewEnumVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Shell_Windows

    If (Not objShellWindows Is Nothing) Then
        Dim vEnumItem As Variant
        
        For Each vEnumItem In objShellWindows
            Debug.Print vEnumItem.Type
        Next vEnumItem
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="8c8b0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8c8b0-117">Requirements</span></span>



| <span data-ttu-id="8c8b0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8c8b0-118">Requirement</span></span> | <span data-ttu-id="8c8b0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8c8b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c8b0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8c8b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c8b0-121">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8c8b0-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c8b0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8c8b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c8b0-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8c8b0-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c8b0-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8c8b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c8b0-125"><dt>Ексдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c8b0-125"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="8c8b0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="8c8b0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c8b0-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="8c8b0-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
