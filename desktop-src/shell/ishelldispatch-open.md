---
description: Открывает указанную папку.
ms.assetid: 30FE669A-4AFD-4dfa-9F62-E62E744469C7
title: Метод Ишеллдиспатч. Open (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d794020313ad776c1d538dc2acb909d562d32f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810966"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="cb6cf-103">Ишеллдиспатч. Open, метод</span><span class="sxs-lookup"><span data-stu-id="cb6cf-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="cb6cf-104">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb6cf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb6cf-105">Syntax</span></span>


```JScript
IShellDispatch.Open(
  vDir
)
```


```VB

IShellDispatch.Open( _
  ByVal vDir As Variant _
)
```





## <a name="parameters"></a><span data-ttu-id="cb6cf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb6cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6cf-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb6cf-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb6cf-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="cb6cf-108">Type: **Variant**</span></span>

<span data-ttu-id="cb6cf-109">Строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="cb6cf-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="cb6cf-110">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="cb6cf-111">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="cb6cf-112">Если для *vDir* задан один из [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) , а специальная папка не существует, эта функция создаст папку.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6cf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb6cf-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="cb6cf-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="cb6cf-114">JScript</span></span>

<span data-ttu-id="cb6cf-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="cb6cf-116">VB</span><span class="sxs-lookup"><span data-stu-id="cb6cf-116">VB</span></span>

<span data-ttu-id="cb6cf-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6cf-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="cb6cf-118">Remarks</span></span>

<span data-ttu-id="cb6cf-119">Этот метод реализован и доступен через метод [**Shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="cb6cf-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="cb6cf-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="cb6cf-120">Examples</span></span>

<span data-ttu-id="cb6cf-121">В следующих примерах показано использование **Open** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="cb6cf-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="cb6cf-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="cb6cf-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objshell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="cb6cf-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="cb6cf-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objshell.Open("C:\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="cb6cf-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="cb6cf-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="cb6cf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="cb6cf-125">Requirements</span></span>



| <span data-ttu-id="cb6cf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="cb6cf-126">Requirement</span></span> | <span data-ttu-id="cb6cf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="cb6cf-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6cf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb6cf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6cf-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cb6cf-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cb6cf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb6cf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6cf-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cb6cf-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cb6cf-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cb6cf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6cf-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6cf-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="cb6cf-134">IDL</span><span class="sxs-lookup"><span data-stu-id="cb6cf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb6cf-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb6cf-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="cb6cf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cb6cf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb6cf-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="cb6cf-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb6cf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb6cf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6cf-139">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="cb6cf-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="cb6cf-140">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="cb6cf-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




