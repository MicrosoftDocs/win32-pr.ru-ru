---
description: Вызывается в ответ на веб-представление баррикаде, закрытое пользователем.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Folder2. Дисмисседвебвиевбаррикаде, метод (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156479"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="6e1fa-103">Folder2. Дисмисседвебвиевбаррикаде, метод</span><span class="sxs-lookup"><span data-stu-id="6e1fa-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="6e1fa-104">Вызывается в ответ на веб-представление баррикаде, закрытое пользователем.</span><span class="sxs-lookup"><span data-stu-id="6e1fa-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e1fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e1fa-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="6e1fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6e1fa-106">Parameters</span></span>

<span data-ttu-id="6e1fa-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="6e1fa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e1fa-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6e1fa-108">Return value</span></span>

<span data-ttu-id="6e1fa-109">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6e1fa-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e1fa-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="6e1fa-110">Remarks</span></span>

<span data-ttu-id="6e1fa-111">Приложение вызывает этот метод после того, как пользователь закрывает баррикаде веб-представления.</span><span class="sxs-lookup"><span data-stu-id="6e1fa-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="6e1fa-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="6e1fa-112">Examples</span></span>

<span data-ttu-id="6e1fa-113">В следующем примере используется **дисмисседвебвиевбаррикаде** , чтобы указать, что веб-представление баррикаде для папки C: Windows было закрыто \\ .</span><span class="sxs-lookup"><span data-stu-id="6e1fa-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="6e1fa-114">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6e1fa-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6e1fa-115">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="6e1fa-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="6e1fa-116">Сценариев</span><span class="sxs-lookup"><span data-stu-id="6e1fa-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6e1fa-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6e1fa-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6e1fa-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6e1fa-118">Requirements</span></span>



| <span data-ttu-id="6e1fa-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6e1fa-119">Requirement</span></span> | <span data-ttu-id="6e1fa-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6e1fa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e1fa-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6e1fa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6e1fa-122">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6e1fa-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6e1fa-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6e1fa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6e1fa-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6e1fa-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6e1fa-125">Header</span><span class="sxs-lookup"><span data-stu-id="6e1fa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e1fa-126"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6e1fa-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6e1fa-127">IDL</span><span class="sxs-lookup"><span data-stu-id="6e1fa-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6e1fa-128"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6e1fa-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6e1fa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6e1fa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e1fa-130"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="6e1fa-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e1fa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6e1fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e1fa-132">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="6e1fa-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="6e1fa-133">**Папка**</span><span class="sxs-lookup"><span data-stu-id="6e1fa-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




