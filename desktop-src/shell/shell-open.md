---
description: Shell. Open метод — открывает указанную папку.
ms.assetid: 96ed9360-fb8f-4f7e-aefb-4a63ec95df07
title: Метод Shell. Open (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Open
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 36f8914be3fce6b461e5267562e6f3ef40aa5fef
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104232"
---
# <a name="shellopen-method"></a><span data-ttu-id="edbdc-103">Shell. Open, метод</span><span class="sxs-lookup"><span data-stu-id="edbdc-103">Shell.Open method</span></span>

<span data-ttu-id="edbdc-104">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="edbdc-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbdc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edbdc-105">Syntax</span></span>


```JScript
iRetVal = Shell.Open(
  vDir
)
```


```VB

Shell.Open( _
  ByVal vDir As Variant _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="edbdc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edbdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbdc-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="edbdc-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edbdc-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="edbdc-108">Type: **Variant**</span></span>

<span data-ttu-id="edbdc-109">Строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="edbdc-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="edbdc-110">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="edbdc-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="edbdc-111">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="edbdc-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="edbdc-112">Если для *vDir* задан один из [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) , а специальная папка не существует, эта функция создаст папку.</span><span class="sxs-lookup"><span data-stu-id="edbdc-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="edbdc-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="edbdc-113">Examples</span></span>

<span data-ttu-id="edbdc-114">В следующем примере показано использование **открытого** .</span><span class="sxs-lookup"><span data-stu-id="edbdc-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="edbdc-115">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="edbdc-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="edbdc-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="edbdc-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellOpenJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36
        
        objShell.Shell.Open(ssfWINDOWS);
    }
</script>
```



<span data-ttu-id="edbdc-117">Сценариев</span><span class="sxs-lookup"><span data-stu-id="edbdc-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellOpenVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        objShell.Shell.Open("C:\\")

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="edbdc-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="edbdc-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="edbdc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="edbdc-119">Requirements</span></span>



| <span data-ttu-id="edbdc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="edbdc-120">Requirement</span></span> | <span data-ttu-id="edbdc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="edbdc-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="edbdc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="edbdc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="edbdc-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="edbdc-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="edbdc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="edbdc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="edbdc-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="edbdc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="edbdc-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="edbdc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="edbdc-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="edbdc-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="edbdc-128">IDL</span><span class="sxs-lookup"><span data-stu-id="edbdc-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="edbdc-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="edbdc-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="edbdc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="edbdc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edbdc-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="edbdc-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbdc-132">См. также</span><span class="sxs-lookup"><span data-stu-id="edbdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbdc-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="edbdc-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="edbdc-134">**Анализ**</span><span class="sxs-lookup"><span data-stu-id="edbdc-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




