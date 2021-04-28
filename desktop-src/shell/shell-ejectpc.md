---
description: Shell. Ежектпк метод — извлекает компьютер из стыковочного узла. Это то же самое, что и при нажатии кнопки "Пуск" и выборе пункта "извлечь компьютер", если компьютер поддерживает эту команду.
ms.assetid: eaba3dce-8fea-453f-90c2-4a9b5cb05ecc
title: Метод Shell. Ежектпк (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.EjectPC
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5ec08aaa82d2f752fa06537434adede86b9d5a3a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104352"
---
# <a name="shellejectpc-method"></a><span data-ttu-id="55405-104">Shell. Ежектпк, метод</span><span class="sxs-lookup"><span data-stu-id="55405-104">Shell.EjectPC method</span></span>

<span data-ttu-id="55405-105">Извлекает компьютер из стыковочного узла.</span><span class="sxs-lookup"><span data-stu-id="55405-105">Ejects the computer from its docking station.</span></span> <span data-ttu-id="55405-106">Это то же самое, что и при нажатии кнопки " **Пуск** " и выборе пункта " **извлечь компьютер**", если компьютер поддерживает эту команду.</span><span class="sxs-lookup"><span data-stu-id="55405-106">This is the same as clicking the **Start** menu and selecting **Eject PC**, if your computer supports this command.</span></span>

## <a name="syntax"></a><span data-ttu-id="55405-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55405-107">Syntax</span></span>


```JScript
Shell.EjectPC()
```


```VB

Shell.EjectPC()
```





## <a name="parameters"></a><span data-ttu-id="55405-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="55405-108">Parameters</span></span>

<span data-ttu-id="55405-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="55405-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55405-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55405-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="55405-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="55405-111">JScript</span></span>

<span data-ttu-id="55405-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="55405-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="55405-113">VB</span><span class="sxs-lookup"><span data-stu-id="55405-113">VB</span></span>

<span data-ttu-id="55405-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="55405-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="55405-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="55405-115">Examples</span></span>

<span data-ttu-id="55405-116">В следующем примере показано использование **ежектпк** .</span><span class="sxs-lookup"><span data-stu-id="55405-116">The following example shows **EjectPC** in use.</span></span> <span data-ttu-id="55405-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="55405-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="55405-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="55405-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellEjectPCJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.EjectPC();
    }
</script>
```



<span data-ttu-id="55405-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="55405-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellEjectPCVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.EjectPC

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="55405-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="55405-120">Visual Basic:</span></span>


```VB
Private Sub fnShellEjectPCVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.EjectPC

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="55405-121">Требования</span><span class="sxs-lookup"><span data-stu-id="55405-121">Requirements</span></span>



| <span data-ttu-id="55405-122">Требование</span><span class="sxs-lookup"><span data-stu-id="55405-122">Requirement</span></span> | <span data-ttu-id="55405-123">Значение</span><span class="sxs-lookup"><span data-stu-id="55405-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55405-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55405-124">Minimum supported client</span></span><br/> | <span data-ttu-id="55405-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="55405-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="55405-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55405-126">Minimum supported server</span></span><br/> | <span data-ttu-id="55405-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="55405-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="55405-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="55405-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="55405-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="55405-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="55405-130">IDL</span><span class="sxs-lookup"><span data-stu-id="55405-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="55405-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="55405-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="55405-132">DLL</span><span class="sxs-lookup"><span data-stu-id="55405-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55405-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="55405-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




