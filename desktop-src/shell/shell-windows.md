---
description: Создает и возвращает объект Шеллвиндовс. Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.
title: Метод Shell. Windows (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ffa6311c-8bbe-45c4-9b06-069779d2306d
ms.openlocfilehash: a865109f926253215e5ad39227cfe3d480e9ccc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999346"
---
# <a name="shellwindows-method"></a><span data-ttu-id="827bb-104">Shell. Windows, метод</span><span class="sxs-lookup"><span data-stu-id="827bb-104">Shell.Windows method</span></span>

<span data-ttu-id="827bb-105">Создает и возвращает объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="827bb-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="827bb-106">Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="827bb-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="827bb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="827bb-107">Syntax</span></span>


```JScript
retVal = Shell.Windows()
```


```VB

Shell.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="827bb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="827bb-108">Parameters</span></span>

<span data-ttu-id="827bb-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="827bb-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="827bb-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="827bb-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="827bb-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="827bb-111">JScript</span></span>

<span data-ttu-id="827bb-112">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="827bb-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="827bb-113">Ссылка на объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="827bb-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="827bb-114">VB</span><span class="sxs-lookup"><span data-stu-id="827bb-114">VB</span></span>

<span data-ttu-id="827bb-115">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="827bb-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="827bb-116">Ссылка на объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="827bb-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="827bb-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="827bb-117">Examples</span></span>

<span data-ttu-id="827bb-118">В следующем примере **Windows** используется для получения объекта [**шеллвиндовс**](shellwindows.md) и отображает количество элементов, которые он содержит.</span><span class="sxs-lookup"><span data-stu-id="827bb-118">The following example uses **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="827bb-119">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="827bb-119">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="827bb-120">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="827bb-120">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objShell.Windows();

        if (objShellWindows != null)
        {
            var Shell = new ActiveXObject("WScript.Shell");
            Shell.Popup(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="827bb-121">Сценариев</span><span class="sxs-lookup"><span data-stu-id="827bb-121">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVBS()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objShell.Windows

        if (not objShellWindows is nothing) then
            WScript.Echo objShellWindows.Count
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="827bb-122">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="827bb-122">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objShell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="827bb-123">Требования</span><span class="sxs-lookup"><span data-stu-id="827bb-123">Requirements</span></span>



| <span data-ttu-id="827bb-124">Требование</span><span class="sxs-lookup"><span data-stu-id="827bb-124">Requirement</span></span> | <span data-ttu-id="827bb-125">Значение</span><span class="sxs-lookup"><span data-stu-id="827bb-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="827bb-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="827bb-126">Minimum supported client</span></span><br/> | <span data-ttu-id="827bb-127">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="827bb-127">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="827bb-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="827bb-128">Minimum supported server</span></span><br/> | <span data-ttu-id="827bb-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="827bb-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="827bb-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="827bb-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="827bb-131"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="827bb-131"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="827bb-132">IDL</span><span class="sxs-lookup"><span data-stu-id="827bb-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="827bb-133"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="827bb-133"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="827bb-134">DLL</span><span class="sxs-lookup"><span data-stu-id="827bb-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="827bb-135"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="827bb-135"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
