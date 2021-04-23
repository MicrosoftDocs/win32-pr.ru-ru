---
description: Отображает диалоговое окно запуска для пользователя.
ms.assetid: BC7C4C26-593D-4467-A2AA-4F2DF835C989
title: Ишеллдиспатч. Филерун, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 56806edf06d334d90ad038886d955c00876f8f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810972"
---
# <a name="ishelldispatchfilerun-method"></a><span data-ttu-id="aadc2-103">Ишеллдиспатч. Филерун, метод</span><span class="sxs-lookup"><span data-stu-id="aadc2-103">IShellDispatch.FileRun method</span></span>

<span data-ttu-id="aadc2-104">Отображает диалоговое окно **запуска** для пользователя.</span><span class="sxs-lookup"><span data-stu-id="aadc2-104">Displays the **Run** dialog to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="aadc2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aadc2-105">Syntax</span></span>


```JScript
IShellDispatch.FileRun()
```


```VB

IShellDispatch.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="aadc2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aadc2-106">Parameters</span></span>

<span data-ttu-id="aadc2-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="aadc2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aadc2-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aadc2-108">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="aadc2-109">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="aadc2-109">JScript</span></span>

<span data-ttu-id="aadc2-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="aadc2-110">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="aadc2-111">VB</span><span class="sxs-lookup"><span data-stu-id="aadc2-111">VB</span></span>

<span data-ttu-id="aadc2-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="aadc2-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aadc2-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="aadc2-113">Remarks</span></span>

<span data-ttu-id="aadc2-114">Этот метод реализован и доступен через метод [**Shell. филерун**](shell-filerun.md) .</span><span class="sxs-lookup"><span data-stu-id="aadc2-114">This method is implemented and accessed through the [**Shell.FileRun**](shell-filerun.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="aadc2-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="aadc2-115">Examples</span></span>

<span data-ttu-id="aadc2-116">В следующих примерах показано использование **филерун** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="aadc2-116">The following examples show the use of **FileRun** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="aadc2-117">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="aadc2-117">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FileRun();
    }
</script>
```



<span data-ttu-id="aadc2-118">Сценариев</span><span class="sxs-lookup"><span data-stu-id="aadc2-118">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="aadc2-119">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="aadc2-119">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="aadc2-120">Требования</span><span class="sxs-lookup"><span data-stu-id="aadc2-120">Requirements</span></span>



| <span data-ttu-id="aadc2-121">Требование</span><span class="sxs-lookup"><span data-stu-id="aadc2-121">Requirement</span></span> | <span data-ttu-id="aadc2-122">Значение</span><span class="sxs-lookup"><span data-stu-id="aadc2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aadc2-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aadc2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="aadc2-124">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aadc2-124">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aadc2-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aadc2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="aadc2-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aadc2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="aadc2-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="aadc2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="aadc2-128"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="aadc2-128"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="aadc2-129">IDL</span><span class="sxs-lookup"><span data-stu-id="aadc2-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="aadc2-130"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="aadc2-130"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="aadc2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="aadc2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aadc2-132"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="aadc2-132"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




