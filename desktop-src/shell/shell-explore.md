---
description: Shell. исследовать метод — открывает указанную папку в окне проводника Windows.
ms.assetid: a788a3c4-f316-4fae-9294-3872eee8f46a
title: Метод Shell. reисследовать (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Explore
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 9ec1756ad6743c5bbac36f56087e6f3820cbb624
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104332"
---
# <a name="shellexplore-method"></a><span data-ttu-id="beb4c-103">Метод Shell. исследовать</span><span class="sxs-lookup"><span data-stu-id="beb4c-103">Shell.Explore method</span></span>

<span data-ttu-id="beb4c-104">Открывает указанную папку в окне проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="beb4c-104">Opens a specified folder in a Windows Explorer window.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="beb4c-105">Syntax</span></span>


```JScript
Shell.Explore(
  vDir
)
```


```VB

Shell.Explore( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="beb4c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="beb4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb4c-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="beb4c-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb4c-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="beb4c-108">Type: **Variant**</span></span>

<span data-ttu-id="beb4c-109">Отображаемая папка.</span><span class="sxs-lookup"><span data-stu-id="beb4c-109">The folder to be displayed.</span></span> <span data-ttu-id="beb4c-110">Это может быть строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="beb4c-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="beb4c-111">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="beb4c-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="beb4c-112">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="beb4c-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb4c-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="beb4c-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="beb4c-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="beb4c-114">JScript</span></span>

<span data-ttu-id="beb4c-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="beb4c-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="beb4c-116">VB</span><span class="sxs-lookup"><span data-stu-id="beb4c-116">VB</span></span>

<span data-ttu-id="beb4c-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="beb4c-117">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="beb4c-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="beb4c-118">Examples</span></span>

<span data-ttu-id="beb4c-119">**В следующем примере показано использование** .</span><span class="sxs-lookup"><span data-stu-id="beb4c-119">The following example shows **Explore** in use.</span></span> <span data-ttu-id="beb4c-120">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="beb4c-120">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="beb4c-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="beb4c-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExploreJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.Explore("C:\\");
    }
</script>]]>
```



<span data-ttu-id="beb4c-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="beb4c-122">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExploreVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.Explore(ssfWINDOWS)

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="beb4c-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="beb4c-123">Visual Basic:</span></span>


```VB
Private Sub fnShellExploreVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.Explore (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="beb4c-124">Требования</span><span class="sxs-lookup"><span data-stu-id="beb4c-124">Requirements</span></span>



| <span data-ttu-id="beb4c-125">Требование</span><span class="sxs-lookup"><span data-stu-id="beb4c-125">Requirement</span></span> | <span data-ttu-id="beb4c-126">Значение</span><span class="sxs-lookup"><span data-stu-id="beb4c-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4c-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="beb4c-127">Minimum supported client</span></span><br/> | <span data-ttu-id="beb4c-128">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="beb4c-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="beb4c-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="beb4c-129">Minimum supported server</span></span><br/> | <span data-ttu-id="beb4c-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="beb4c-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="beb4c-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="beb4c-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="beb4c-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb4c-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="beb4c-133">IDL</span><span class="sxs-lookup"><span data-stu-id="beb4c-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="beb4c-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="beb4c-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="beb4c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="beb4c-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="beb4c-136"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="beb4c-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




