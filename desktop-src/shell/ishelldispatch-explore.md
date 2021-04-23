---
description: Открывает указанную папку в окне проводника Windows.
ms.assetid: DB434D02-56B2-4e8f-9E43-BBF47C7BE377
title: Метод Ишеллдиспатч. reисследовать (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1ae29b4962dcac1be0b7ea23808e36ce005cb62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984717"
---
# <a name="ishelldispatchexplore-method"></a><span data-ttu-id="f9402-103">Метод Ишеллдиспатч. исследовать</span><span class="sxs-lookup"><span data-stu-id="f9402-103">IShellDispatch.Explore method</span></span>

<span data-ttu-id="f9402-104">Открывает указанную папку в окне проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="f9402-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9402-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9402-105">Syntax</span></span>


```JScript
IShellDispatch.Explore(
  vDir
)
```


```VB

IShellDispatch.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="f9402-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9402-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9402-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9402-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9402-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="f9402-108">Type: **Variant**</span></span>

<span data-ttu-id="f9402-109">Отображаемая папка.</span><span class="sxs-lookup"><span data-stu-id="f9402-109">The folder to be displayed.</span></span> <span data-ttu-id="f9402-110">Это может быть строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="f9402-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="f9402-111">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="f9402-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="f9402-112">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="f9402-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9402-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9402-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="f9402-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="f9402-114">JScript</span></span>

<span data-ttu-id="f9402-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9402-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="f9402-116">VB</span><span class="sxs-lookup"><span data-stu-id="f9402-116">VB</span></span>

<span data-ttu-id="f9402-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9402-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9402-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="f9402-118">Remarks</span></span>

<span data-ttu-id="f9402-119">Этот метод реализован и доступен через метод [**Shell. исследовать**](shell-explore.md) .</span><span class="sxs-lookup"><span data-stu-id="f9402-119">This method is implemented and accessed through the [**Shell.Explore**](shell-explore.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="f9402-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="f9402-120">Examples</span></span>

<span data-ttu-id="f9402-121">В следующих примерах показано использование **исследования** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f9402-121">The following examples show the use of **Explore** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f9402-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="f9402-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.Explore("C:\\");
    }
</script>
```



<span data-ttu-id="f9402-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="f9402-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="f9402-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f9402-124">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f9402-125">Требования</span><span class="sxs-lookup"><span data-stu-id="f9402-125">Requirements</span></span>



| <span data-ttu-id="f9402-126">Требование</span><span class="sxs-lookup"><span data-stu-id="f9402-126">Requirement</span></span> | <span data-ttu-id="f9402-127">Значение</span><span class="sxs-lookup"><span data-stu-id="f9402-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9402-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9402-128">Minimum supported client</span></span><br/> | <span data-ttu-id="f9402-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9402-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f9402-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9402-130">Minimum supported server</span></span><br/> | <span data-ttu-id="f9402-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9402-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f9402-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f9402-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9402-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9402-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="f9402-134">IDL</span><span class="sxs-lookup"><span data-stu-id="f9402-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9402-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9402-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="f9402-136">DLL</span><span class="sxs-lookup"><span data-stu-id="f9402-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9402-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f9402-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




