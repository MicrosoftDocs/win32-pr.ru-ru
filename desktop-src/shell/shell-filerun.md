---
description: Отображает диалоговое окно запуска для пользователя. Этот метод оказывает тот же результат, что и при щелчке меню Пуск и выборе Run.
ms.assetid: bb984777-e09f-41e6-8359-51c5291654f7
title: Метод Shell. Филерун (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FileRun
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ebccf11ea21fdd4ceba2563a6110c1eb2494947b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985988"
---
# <a name="shellfilerun-method"></a><span data-ttu-id="d675e-104">Shell. Филерун, метод</span><span class="sxs-lookup"><span data-stu-id="d675e-104">Shell.FileRun method</span></span>

<span data-ttu-id="d675e-105">Отображает диалоговое окно **запуска** для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d675e-105">Displays the **Run** dialog to the user.</span></span> <span data-ttu-id="d675e-106">Этот метод оказывает тот же результат, что и при щелчке меню **Пуск** и выборе **Run**.</span><span class="sxs-lookup"><span data-stu-id="d675e-106">This method has the same effect as clicking the **Start** menu and selecting **Run**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d675e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d675e-107">Syntax</span></span>


```JScript
Shell.FileRun()
```


```VB

Shell.FileRun()
```





## <a name="parameters"></a><span data-ttu-id="d675e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d675e-108">Parameters</span></span>

<span data-ttu-id="d675e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="d675e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d675e-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d675e-110">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d675e-111">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="d675e-111">JScript</span></span>

<span data-ttu-id="d675e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d675e-112">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d675e-113">VB</span><span class="sxs-lookup"><span data-stu-id="d675e-113">VB</span></span>

<span data-ttu-id="d675e-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d675e-114">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d675e-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="d675e-115">Examples</span></span>

<span data-ttu-id="d675e-116">В следующем примере показано использование **филерун** .</span><span class="sxs-lookup"><span data-stu-id="d675e-116">The following example shows **FileRun** in use.</span></span> <span data-ttu-id="d675e-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d675e-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d675e-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="d675e-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFileRunJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FileRun();
    }
</script>
```



<span data-ttu-id="d675e-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="d675e-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFileRunVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.FileRun

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d675e-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d675e-120">Visual Basic:</span></span>


```VB
Private Sub fnShellFileRunVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FileRun

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d675e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d675e-121">Requirements</span></span>



| <span data-ttu-id="d675e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d675e-122">Requirement</span></span> | <span data-ttu-id="d675e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d675e-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d675e-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d675e-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d675e-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d675e-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d675e-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d675e-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d675e-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d675e-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d675e-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d675e-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d675e-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="d675e-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d675e-130">IDL</span><span class="sxs-lookup"><span data-stu-id="d675e-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d675e-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d675e-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d675e-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d675e-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d675e-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="d675e-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




