---
description: Ишеллдиспатч. Open метод — открывает указанную папку.
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
ms.openlocfilehash: 4b5301e030926b9bcfdc18949b6a04706c22bb71
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086632"
---
# <a name="ishelldispatchopen-method"></a><span data-ttu-id="b1722-103">Ишеллдиспатч. Open, метод</span><span class="sxs-lookup"><span data-stu-id="b1722-103">IShellDispatch.Open method</span></span>

<span data-ttu-id="b1722-104">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="b1722-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1722-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1722-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="b1722-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1722-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1722-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1722-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1722-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="b1722-108">Type: **Variant**</span></span>

<span data-ttu-id="b1722-109">Строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="b1722-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="b1722-110">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="b1722-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="b1722-111">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="b1722-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="b1722-112">Если для *vDir* задан один из [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) , а специальная папка не существует, эта функция создаст папку.</span><span class="sxs-lookup"><span data-stu-id="b1722-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1722-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1722-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="b1722-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="b1722-114">JScript</span></span>

<span data-ttu-id="b1722-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b1722-115">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="b1722-116">VB</span><span class="sxs-lookup"><span data-stu-id="b1722-116">VB</span></span>

<span data-ttu-id="b1722-117">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b1722-117">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1722-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="b1722-118">Remarks</span></span>

<span data-ttu-id="b1722-119">Этот метод реализован и доступен через метод [**Shell. Open**](shell-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b1722-119">This method is implemented and accessed through the [**Shell.Open**](shell-open.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="b1722-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="b1722-120">Examples</span></span>

<span data-ttu-id="b1722-121">В следующих примерах показано использование **Open** в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b1722-121">The following examples show the use of **Open** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="b1722-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="b1722-122">JScript:</span></span>


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



<span data-ttu-id="b1722-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="b1722-123">VBScript:</span></span>


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



<span data-ttu-id="b1722-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="b1722-124">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objshell.Open (ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="b1722-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b1722-125">Requirements</span></span>



| <span data-ttu-id="b1722-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b1722-126">Requirement</span></span> | <span data-ttu-id="b1722-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b1722-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1722-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1722-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b1722-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1722-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b1722-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1722-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b1722-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b1722-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b1722-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b1722-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1722-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="b1722-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b1722-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1722-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="b1722-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b1722-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1722-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b1722-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1722-138">См. также</span><span class="sxs-lookup"><span data-stu-id="b1722-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1722-139">**ишеллдиспатч**</span><span class="sxs-lookup"><span data-stu-id="b1722-139">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="b1722-140">**Анализ**</span><span class="sxs-lookup"><span data-stu-id="b1722-140">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




