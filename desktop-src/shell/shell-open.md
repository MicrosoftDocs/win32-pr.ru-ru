---
description: Открывает указанную папку.
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
ms.openlocfilehash: 3572f48a7b129500c38c3c0227ba479ecb775067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910763"
---
# <a name="shellopen-method"></a><span data-ttu-id="97fd7-103">Shell. Open, метод</span><span class="sxs-lookup"><span data-stu-id="97fd7-103">Shell.Open method</span></span>

<span data-ttu-id="97fd7-104">Открывает указанную папку.</span><span class="sxs-lookup"><span data-stu-id="97fd7-104">Opens the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="97fd7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97fd7-105">Syntax</span></span>


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





## <a name="parameters"></a><span data-ttu-id="97fd7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="97fd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97fd7-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="97fd7-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97fd7-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="97fd7-108">Type: **Variant**</span></span>

<span data-ttu-id="97fd7-109">Строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="97fd7-109">A string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="97fd7-110">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="97fd7-110">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="97fd7-111">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="97fd7-111">In those cases, the numeric values must be used in their place.</span></span>

<span data-ttu-id="97fd7-112">Если для *vDir* задан один из [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) , а специальная папка не существует, эта функция создаст папку.</span><span class="sxs-lookup"><span data-stu-id="97fd7-112">If *vDir* is set to one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) and the special folder does not exist, this function will create the folder.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="97fd7-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="97fd7-113">Examples</span></span>

<span data-ttu-id="97fd7-114">В следующем примере показано использование **открытого** .</span><span class="sxs-lookup"><span data-stu-id="97fd7-114">The following example shows **Open** in use.</span></span> <span data-ttu-id="97fd7-115">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97fd7-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="97fd7-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="97fd7-116">JScript:</span></span>


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



<span data-ttu-id="97fd7-117">Сценариев</span><span class="sxs-lookup"><span data-stu-id="97fd7-117">VBScript:</span></span>


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



<span data-ttu-id="97fd7-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="97fd7-118">Visual Basic:</span></span>


```VB
Private Sub fnShellOpenVB()
    Dim objShell As Shell
    
    Set objShell = New Shell
    objShell.Shell.Open(ssfPERSONAL)

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="97fd7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="97fd7-119">Requirements</span></span>



| <span data-ttu-id="97fd7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="97fd7-120">Requirement</span></span> | <span data-ttu-id="97fd7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="97fd7-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97fd7-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97fd7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="97fd7-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="97fd7-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97fd7-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97fd7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="97fd7-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97fd7-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="97fd7-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="97fd7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="97fd7-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="97fd7-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="97fd7-128">IDL</span><span class="sxs-lookup"><span data-stu-id="97fd7-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97fd7-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97fd7-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="97fd7-130">DLL</span><span class="sxs-lookup"><span data-stu-id="97fd7-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97fd7-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="97fd7-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97fd7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="97fd7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97fd7-133">**Shell**</span><span class="sxs-lookup"><span data-stu-id="97fd7-133">**Shell**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="97fd7-134">**Обзор**</span><span class="sxs-lookup"><span data-stu-id="97fd7-134">**Explore**</span></span>](shell-explore.md)
</dt> </dl>

 

 




