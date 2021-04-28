---
description: Ишеллдиспатч. Ежектпк метод — извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки "Пуск" и выборе пункта "извлечь компьютер", если компьютер поддерживает эту команду.
ms.assetid: 34448D82-187C-40aa-90B4-A4111B33048B
title: Ишеллдиспатч. Ежектпк, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ac42e1a4331a553a03bac3da50a187e06c90859c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086642"
---
# <a name="ishelldispatchejectpc-method"></a><span data-ttu-id="582af-104">Ишеллдиспатч. Ежектпк, метод</span><span class="sxs-lookup"><span data-stu-id="582af-104">IShellDispatch.EjectPC method</span></span>

<span data-ttu-id="582af-105">Извлекает компьютер из стыковочного узла.</span><span class="sxs-lookup"><span data-stu-id="582af-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="582af-106">Это то же самое, что и при нажатии кнопки " **Пуск** " и выборе пункта " **извлечь компьютер**", если компьютер поддерживает эту команду.</span><span class="sxs-lookup"><span data-stu-id="582af-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="582af-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="582af-107">Syntax</span></span>


```JScript
IShellDispatch.EjectPC()
```


```VB

IShellDispatch.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="582af-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="582af-108">Parameters</span></span>

<span data-ttu-id="582af-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="582af-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="582af-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="582af-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="582af-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="582af-111">JScript</span></span>

<span data-ttu-id="582af-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="582af-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="582af-113">VB</span><span class="sxs-lookup"><span data-stu-id="582af-113">VB</span></span>

<span data-ttu-id="582af-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="582af-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="582af-115">Remarks</span><span class="sxs-lookup"><span data-stu-id="582af-115">Remarks</span></span>

<span data-ttu-id="582af-116">Этот метод реализован и доступен через метод [**Shell. ежектпк**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="582af-116">This method is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="582af-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="582af-117">Examples</span></span>

<span data-ttu-id="582af-118">В следующих примерах показано использование **ежектпк** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="582af-118">The following examples show the use of **EjectPC** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="582af-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="582af-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.EjectPC();
    }
</script>
```



<span data-ttu-id="582af-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="582af-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="582af-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="582af-121">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="582af-122">Требования</span><span class="sxs-lookup"><span data-stu-id="582af-122">Requirements</span></span>



| <span data-ttu-id="582af-123">Требование</span><span class="sxs-lookup"><span data-stu-id="582af-123">Requirement</span></span> | <span data-ttu-id="582af-124">Значение</span><span class="sxs-lookup"><span data-stu-id="582af-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="582af-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="582af-125">Minimum supported client</span></span><br/> | <span data-ttu-id="582af-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="582af-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="582af-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="582af-127">Minimum supported server</span></span><br/> | <span data-ttu-id="582af-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="582af-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="582af-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="582af-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="582af-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="582af-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="582af-131">IDL</span><span class="sxs-lookup"><span data-stu-id="582af-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="582af-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="582af-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="582af-133">DLL</span><span class="sxs-lookup"><span data-stu-id="582af-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="582af-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="582af-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




