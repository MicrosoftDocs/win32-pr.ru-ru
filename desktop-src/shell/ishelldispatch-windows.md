---
description: Метод Ишеллдиспатч. Windows — создает и возвращает объект Шеллвиндовс. Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.
ms.assetid: 788E2106-3534-4e22-801F-677FD02BDFE0
title: Метод Ишеллдиспатч. Windows (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Windows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 16991d6a251909e8f3b277894a96e6ad08a7f9a4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117172"
---
# <a name="ishelldispatchwindows-method"></a><span data-ttu-id="3ed5e-104">Ишеллдиспатч. Windows, метод</span><span class="sxs-lookup"><span data-stu-id="3ed5e-104">IShellDispatch.Windows method</span></span>

<span data-ttu-id="3ed5e-105">Создает и возвращает объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed5e-105">Creates and returns a [**ShellWindows**](shellwindows.md) object.</span></span> <span data-ttu-id="3ed5e-106">Этот объект представляет коллекцию всех открытых окон, принадлежащих оболочке.</span><span class="sxs-lookup"><span data-stu-id="3ed5e-106">This object represents a collection of all of the open windows that belong to the Shell.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed5e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ed5e-107">Syntax</span></span>


```JScript
retVal = IShellDispatch.Windows()
```


```VB

IShellDispatch.Windows() As IDispatch
```





## <a name="parameters"></a><span data-ttu-id="3ed5e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ed5e-108">Parameters</span></span>

<span data-ttu-id="3ed5e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3ed5e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3ed5e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ed5e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="3ed5e-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="3ed5e-111">JScript</span></span>

<span data-ttu-id="3ed5e-112">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ed5e-112">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="3ed5e-113">Ссылка на объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed5e-113">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

### <a name="vb"></a><span data-ttu-id="3ed5e-114">VB</span><span class="sxs-lookup"><span data-stu-id="3ed5e-114">VB</span></span>

<span data-ttu-id="3ed5e-115">Тип: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="3ed5e-115">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="3ed5e-116">Ссылка на объект [**шеллвиндовс**](shellwindows.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed5e-116">An object reference to the [**ShellWindows**](shellwindows.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ed5e-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="3ed5e-117">Remarks</span></span>

<span data-ttu-id="3ed5e-118">Этот метод реализован и доступен через метод [**Shell. Windows**](shell-windows.md) .</span><span class="sxs-lookup"><span data-stu-id="3ed5e-118">This method is implemented and accessed through the [**Shell.Windows**](shell-windows.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="3ed5e-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ed5e-119">Examples</span></span>

<span data-ttu-id="3ed5e-120">В следующих примерах используется **Windows** для извлечения объекта [**шеллвиндовс**](shellwindows.md) и отображается количество содержащихся в нем элементов.</span><span class="sxs-lookup"><span data-stu-id="3ed5e-120">The following examples use **Windows** to retrieve the [**ShellWindows**](shellwindows.md) object and display a count of the number of items that it contains.</span></span> <span data-ttu-id="3ed5e-121">Сведения об использовании представлены для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3ed5e-121">Usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="3ed5e-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="3ed5e-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellWindowsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();

        if (objShellWindows != null)
        {
            alert(objShellWindows.Count);
        }
    }
</script>
```



<span data-ttu-id="3ed5e-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="3ed5e-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows

        if (not objShellWindows is nothing) then
            alert(objShellWindows.Count)
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="3ed5e-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="3ed5e-124">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows

    If (Not objShellWindows Is Nothing) Then
        Debug.Print objShellWindows.Count
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="3ed5e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3ed5e-125">Requirements</span></span>



| <span data-ttu-id="3ed5e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3ed5e-126">Requirement</span></span> | <span data-ttu-id="3ed5e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3ed5e-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ed5e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ed5e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3ed5e-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ed5e-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="3ed5e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ed5e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3ed5e-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3ed5e-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ed5e-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3ed5e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ed5e-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ed5e-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="3ed5e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="3ed5e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ed5e-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ed5e-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="3ed5e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3ed5e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ed5e-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3ed5e-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
