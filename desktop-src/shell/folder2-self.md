---
description: Содержит объект FolderItem папки.
ms.assetid: 0964505d-4138-4444-91d4-46c707c45688
title: Свойство folder2. Self (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.Self
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f49666096f35f9871f8a3b3c141d4bc169dea0c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262781"
---
# <a name="folder2self-property"></a><span data-ttu-id="987a5-103">Folder2. Self, свойство</span><span class="sxs-lookup"><span data-stu-id="987a5-103">Folder2.Self property</span></span>

<span data-ttu-id="987a5-104">Содержит объект [**FolderItem**](folderitem.md) папки.</span><span class="sxs-lookup"><span data-stu-id="987a5-104">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span>

<span data-ttu-id="987a5-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="987a5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="987a5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="987a5-106">Syntax</span></span>


```JScript
Self = Folder2.Self
```



## <a name="property-value"></a><span data-ttu-id="987a5-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="987a5-107">Property value</span></span>

<span data-ttu-id="987a5-108">Объект, результатом которого является объект [**FolderItem**](folderitem.md) папки.</span><span class="sxs-lookup"><span data-stu-id="987a5-108">The object that evaluates to the folder's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="987a5-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="987a5-109">Examples</span></span>

<span data-ttu-id="987a5-110">В следующем примере **Self** используется для получения [**FolderItem**](folderitem.md) для папки C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="987a5-110">The following example uses **Self** to retrieve the [**FolderItem**](folderitem.md) for the C:\\Windows folder.</span></span> <span data-ttu-id="987a5-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="987a5-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="987a5-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="987a5-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectSelfJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="987a5-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="987a5-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectSelfVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder2.Self

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="987a5-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="987a5-114">Visual Basic:</span></span>


```VB
Private Sub btnFolder2Self_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder2.Self()

        If (Not objFolderItem Is Nothing) Then
            'Add code here.
        End If

        Set objFolderItem = Nothing
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="987a5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="987a5-115">Requirements</span></span>



| <span data-ttu-id="987a5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="987a5-116">Requirement</span></span> | <span data-ttu-id="987a5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="987a5-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="987a5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="987a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="987a5-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="987a5-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="987a5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="987a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="987a5-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="987a5-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="987a5-122">Header</span><span class="sxs-lookup"><span data-stu-id="987a5-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="987a5-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="987a5-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="987a5-124">IDL</span><span class="sxs-lookup"><span data-stu-id="987a5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="987a5-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="987a5-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="987a5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="987a5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="987a5-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="987a5-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="987a5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="987a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="987a5-129">**Folder2**</span><span class="sxs-lookup"><span data-stu-id="987a5-129">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="987a5-130">**Папка**</span><span class="sxs-lookup"><span data-stu-id="987a5-130">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




