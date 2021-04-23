---
description: Обновляет содержимое меню "Пуск". Используется только с системами, предшествующими Windows XP.
ms.assetid: 1269c66d-61df-432d-9220-5ac975e3ad58
title: Метод Shell. Рефрешмену (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.RefreshMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a5812312c846026f4e0c7d2a4f6a5f857a572a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985544"
---
# <a name="shellrefreshmenu-method"></a><span data-ttu-id="bfddd-104">Shell. Рефрешмену, метод</span><span class="sxs-lookup"><span data-stu-id="bfddd-104">Shell.RefreshMenu method</span></span>

<span data-ttu-id="bfddd-105">Обновляет содержимое меню " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="bfddd-105">Refreshes the contents of the **Start** menu.</span></span> <span data-ttu-id="bfddd-106">Используется только с системами, предшествующими Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bfddd-106">Used only with systems preceding Windows XP.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfddd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfddd-107">Syntax</span></span>


```JScript
iRetVal = Shell.RefreshMenu()
```


```VB

Shell.RefreshMenu() As Integer
```





## <a name="parameters"></a><span data-ttu-id="bfddd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfddd-108">Parameters</span></span>

<span data-ttu-id="bfddd-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="bfddd-109">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfddd-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="bfddd-110">Remarks</span></span>

<span data-ttu-id="bfddd-111">Функциональные возможности, предоставляемые **рефрешмену** , автоматически обрабатываются в Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="bfddd-111">The functionality that **RefreshMenu** provides is handled automatically under Windows XP or later.</span></span> <span data-ttu-id="bfddd-112">Не вызывайте этот метод в этой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="bfddd-112">Do not call this method under that operating system.</span></span>

## <a name="examples"></a><span data-ttu-id="bfddd-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="bfddd-113">Examples</span></span>

<span data-ttu-id="bfddd-114">В следующем примере показано использование **рефрешмену** .</span><span class="sxs-lookup"><span data-stu-id="bfddd-114">The following example shows **RefreshMenu** in use.</span></span> <span data-ttu-id="bfddd-115">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bfddd-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bfddd-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="bfddd-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellRefreshMenuJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.RefreshMenu();
    }
</script>
```



<span data-ttu-id="bfddd-117">Сценариев</span><span class="sxs-lookup"><span data-stu-id="bfddd-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellRefreshMenuVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.RefreshMenu

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bfddd-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bfddd-118">Visual Basic:</span></span>


```VB
Private Sub fnShellRefreshMenuVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.RefreshMenu

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bfddd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="bfddd-119">Requirements</span></span>



| <span data-ttu-id="bfddd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="bfddd-120">Requirement</span></span> | <span data-ttu-id="bfddd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="bfddd-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bfddd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfddd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bfddd-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bfddd-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bfddd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfddd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bfddd-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bfddd-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bfddd-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bfddd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfddd-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfddd-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bfddd-128">IDL</span><span class="sxs-lookup"><span data-stu-id="bfddd-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bfddd-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bfddd-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bfddd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="bfddd-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfddd-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="bfddd-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




