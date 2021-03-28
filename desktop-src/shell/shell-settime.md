---
description: Отображает диалоговое окно Свойства даты и времени. Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра настроить дату и время.
ms.assetid: 01694607-3fc2-4d0d-ba48-5bdbb40da000
title: Метод Shell. SetTime (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.SetTime
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b610effe87bd9e4ab33a6e8396e90f79e7bbbe9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985541"
---
# <a name="shellsettime-method"></a><span data-ttu-id="ccb2e-104">Shell. SetTime, метод</span><span class="sxs-lookup"><span data-stu-id="ccb2e-104">Shell.SetTime method</span></span>

<span data-ttu-id="ccb2e-105">Отображает диалоговое окно **Свойства даты и времени** .</span><span class="sxs-lookup"><span data-stu-id="ccb2e-105">Displays the **Date and Time Properties** dialog box.</span></span> <span data-ttu-id="ccb2e-106">Этот метод действует так же, как и щелчок правой кнопкой мыши по часам в области состояние панели задач и выбор параметра **настроить дату и время**.</span><span class="sxs-lookup"><span data-stu-id="ccb2e-106">This method has the same effect as right-clicking the clock in the taskbar status area and selecting **Adjust Date/Time**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccb2e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccb2e-107">Syntax</span></span>


```JScript
iRetVal = Shell.SetTime()
```


```VB

Shell.SetTime() As Integer
```





## <a name="parameters"></a><span data-ttu-id="ccb2e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccb2e-108">Parameters</span></span>

<span data-ttu-id="ccb2e-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="ccb2e-109">This method has no parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="ccb2e-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="ccb2e-110">Examples</span></span>

<span data-ttu-id="ccb2e-111">В следующем примере показано использование **setTime** .</span><span class="sxs-lookup"><span data-stu-id="ccb2e-111">The following example shows **SetTime** in use.</span></span> <span data-ttu-id="ccb2e-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ccb2e-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ccb2e-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ccb2e-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellSetTimeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.SetTime();
    }
</script>
```



<span data-ttu-id="ccb2e-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ccb2e-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellSetTimeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.SetTime
 
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ccb2e-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ccb2e-115">Visual Basic:</span></span>


```VB
Private Sub fnShellSetTimeVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.SetTime
 
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ccb2e-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ccb2e-116">Requirements</span></span>



| <span data-ttu-id="ccb2e-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ccb2e-117">Requirement</span></span> | <span data-ttu-id="ccb2e-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ccb2e-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccb2e-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccb2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ccb2e-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ccb2e-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ccb2e-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccb2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ccb2e-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ccb2e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ccb2e-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ccb2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccb2e-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ccb2e-125">IDL</span><span class="sxs-lookup"><span data-stu-id="ccb2e-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ccb2e-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ccb2e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ccb2e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccb2e-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ccb2e-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




