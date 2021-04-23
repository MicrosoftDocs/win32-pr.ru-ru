---
description: 'Отображает диалоговое окно Результаты поиска: компьютеры. В диалоговом окне отображается результат поиска указанного компьютера.'
ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257
title: Ишеллдиспатч. Финдкомпутер, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FindComputer
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ad928b6860a85126a714a08f3bc3df9d4aff67c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984716"
---
# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="7ee28-104">Ишеллдиспатч. Финдкомпутер, метод</span><span class="sxs-lookup"><span data-stu-id="7ee28-104">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="7ee28-105">Отображает диалоговое окно **Результаты поиска: компьютеры** .</span><span class="sxs-lookup"><span data-stu-id="7ee28-105">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="7ee28-106">В диалоговом окне отображается результат поиска указанного компьютера.</span><span class="sxs-lookup"><span data-stu-id="7ee28-106">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee28-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ee28-107">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="7ee28-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ee28-108">Parameters</span></span>

<span data-ttu-id="7ee28-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7ee28-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ee28-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ee28-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7ee28-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="7ee28-111">JScript</span></span>

<span data-ttu-id="7ee28-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ee28-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7ee28-113">VB</span><span class="sxs-lookup"><span data-stu-id="7ee28-113">VB</span></span>

<span data-ttu-id="7ee28-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ee28-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ee28-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ee28-115">Remarks</span></span>

<span data-ttu-id="7ee28-116">Этот метод реализован и доступен через метод [**Shell. финдкомпутер**](shell-findcomputer.md) .</span><span class="sxs-lookup"><span data-stu-id="7ee28-116">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7ee28-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="7ee28-117">Examples</span></span>

<span data-ttu-id="7ee28-118">В следующих примерах показано использование **финдкомпутер** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7ee28-118">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7ee28-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7ee28-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="7ee28-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7ee28-120">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="7ee28-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7ee28-121">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="7ee28-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7ee28-122">Requirements</span></span>



| <span data-ttu-id="7ee28-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7ee28-123">Requirement</span></span> | <span data-ttu-id="7ee28-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7ee28-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee28-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ee28-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee28-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7ee28-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7ee28-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ee28-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee28-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7ee28-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7ee28-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7ee28-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ee28-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ee28-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7ee28-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7ee28-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ee28-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ee28-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7ee28-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7ee28-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ee28-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee28-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




