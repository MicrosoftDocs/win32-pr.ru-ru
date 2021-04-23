---
description: Отображает диалоговое окно Дата и время. Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра настроить дату и время.
ms.assetid: D4B949F6-5508-4624-9706-491184703DC6
title: Ишеллдиспатч. SetTime, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9c9e687ea89cad4715aeacf72a2a33792fba9f7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897910"
---
# <a name="ishelldispatchsettime-method"></a><span data-ttu-id="7f511-104">Ишеллдиспатч. SetTime, метод</span><span class="sxs-lookup"><span data-stu-id="7f511-104">IShellDispatch.SetTime method</span></span>

<span data-ttu-id="7f511-105">Отображает диалоговое окно **Дата и время** .</span><span class="sxs-lookup"><span data-stu-id="7f511-105">Displays the **Date and Time** dialog box.</span></span> <span data-ttu-id="7f511-106">Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра **настроить дату и время**.</span><span class="sxs-lookup"><span data-stu-id="7f511-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust date/time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f511-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7f511-107">Syntax</span></span>


```JScript
IShellDispatch.SetTime()
```


```VB

IShellDispatch.SetTime()
```





## <a name="parameters"></a><span data-ttu-id="7f511-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f511-108">Parameters</span></span>

<span data-ttu-id="7f511-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="7f511-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f511-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f511-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="7f511-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="7f511-111">JScript</span></span>

<span data-ttu-id="7f511-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f511-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="7f511-113">VB</span><span class="sxs-lookup"><span data-stu-id="7f511-113">VB</span></span>

<span data-ttu-id="7f511-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7f511-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f511-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7f511-115">Remarks</span></span>

<span data-ttu-id="7f511-116">Этот метод реализован и доступен через метод [**Shell. setTime**](shell-settime.md) .</span><span class="sxs-lookup"><span data-stu-id="7f511-116">This method is implemented and accessed through the [**Shell.SetTime**](shell-settime.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="7f511-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="7f511-117">Examples</span></span>

<span data-ttu-id="7f511-118">В следующих примерах показано использование **setTime** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="7f511-118">The following examples show the use of **SetTime** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="7f511-119">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="7f511-119">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.SetTime();
    }
</script>
```



<span data-ttu-id="7f511-120">Сценариев</span><span class="sxs-lookup"><span data-stu-id="7f511-120">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.SetTime
 
        set objShell = nothing
    end function
```



<span data-ttu-id="7f511-121">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="7f511-121">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.SetTime
 
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="7f511-122">Требования</span><span class="sxs-lookup"><span data-stu-id="7f511-122">Requirements</span></span>



| <span data-ttu-id="7f511-123">Требование</span><span class="sxs-lookup"><span data-stu-id="7f511-123">Requirement</span></span> | <span data-ttu-id="7f511-124">Значение</span><span class="sxs-lookup"><span data-stu-id="7f511-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f511-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f511-125">Minimum supported client</span></span><br/> | <span data-ttu-id="7f511-126">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7f511-126">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7f511-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f511-127">Minimum supported server</span></span><br/> | <span data-ttu-id="7f511-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f511-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7f511-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f511-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f511-130"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f511-130"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="7f511-131">IDL</span><span class="sxs-lookup"><span data-stu-id="7f511-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7f511-132"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7f511-132"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="7f511-133">DLL</span><span class="sxs-lookup"><span data-stu-id="7f511-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f511-134"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="7f511-134"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




