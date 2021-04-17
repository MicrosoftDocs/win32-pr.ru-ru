---
description: Синхронизирует все автономные файлы в папке.
ms.assetid: b149df96-0c8e-47b9-b71e-2ad5dcfdeb8f
title: Метод folder2. Synchronize (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Synchronize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e9c39c37ff0e44e58aa71c69496dec8bee2745bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423518"
---
# <a name="folder2synchronize-method"></a><span data-ttu-id="61623-103">Folder2. Synchronize, метод</span><span class="sxs-lookup"><span data-stu-id="61623-103">Folder2.Synchronize method</span></span>

<span data-ttu-id="61623-104">Синхронизирует все автономные файлы в папке.</span><span class="sxs-lookup"><span data-stu-id="61623-104">Synchronizes all offline files in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="61623-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61623-105">Syntax</span></span>


```JScript
iRetVal = Folder2.Synchronize()
```



## <a name="parameters"></a><span data-ttu-id="61623-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61623-106">Parameters</span></span>

<span data-ttu-id="61623-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="61623-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="61623-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="61623-108">Remarks</span></span>

<span data-ttu-id="61623-109">Чтобы использовать этот метод, необходимо включить функцию автономные файлы.</span><span class="sxs-lookup"><span data-stu-id="61623-109">To use this method, the Offline Files feature must be enabled.</span></span>

## <a name="examples"></a><span data-ttu-id="61623-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="61623-110">Examples</span></span>

<span data-ttu-id="61623-111">В следующем примере показано правильное использование **Synchronize** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="61623-111">The following example shows the proper use of **Synchronize** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="61623-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="61623-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnSynchronizeJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            objFolder2.Synchronize();
        }
    }
</script>
```



<span data-ttu-id="61623-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="61623-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnSynchronizeVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            objFolder2.Synchronize
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="61623-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="61623-114">Visual Basic:</span></span>


```VB
Private Sub fnSynchronizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.Synchronize
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="61623-115">Требования</span><span class="sxs-lookup"><span data-stu-id="61623-115">Requirements</span></span>



| <span data-ttu-id="61623-116">Требование</span><span class="sxs-lookup"><span data-stu-id="61623-116">Requirement</span></span> | <span data-ttu-id="61623-117">Значение</span><span class="sxs-lookup"><span data-stu-id="61623-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61623-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61623-118">Minimum supported client</span></span><br/> | <span data-ttu-id="61623-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="61623-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="61623-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61623-120">Minimum supported server</span></span><br/> | <span data-ttu-id="61623-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="61623-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="61623-122">Header</span><span class="sxs-lookup"><span data-stu-id="61623-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="61623-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="61623-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="61623-124">IDL</span><span class="sxs-lookup"><span data-stu-id="61623-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="61623-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="61623-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="61623-126">DLL</span><span class="sxs-lookup"><span data-stu-id="61623-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61623-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="61623-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61623-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61623-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61623-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="61623-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="61623-130">**Папка**</span><span class="sxs-lookup"><span data-stu-id="61623-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




