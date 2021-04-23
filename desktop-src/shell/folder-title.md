---
description: Содержит заголовок папки.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Свойство Folder. Title (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8fc66d231d49d724749ae79b248b4dca9d917acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985501"
---
# <a name="foldertitle-property"></a><span data-ttu-id="818a0-103">Свойство Folder. Title</span><span class="sxs-lookup"><span data-stu-id="818a0-103">Folder.Title property</span></span>

<span data-ttu-id="818a0-104">Содержит заголовок папки.</span><span class="sxs-lookup"><span data-stu-id="818a0-104">Contains the title of the folder.</span></span>

<span data-ttu-id="818a0-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="818a0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="818a0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="818a0-106">Syntax</span></span>


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a><span data-ttu-id="818a0-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="818a0-107">Property value</span></span>

<span data-ttu-id="818a0-108">Строка, содержащая заголовок объекта.</span><span class="sxs-lookup"><span data-stu-id="818a0-108">A string containing the object's title.</span></span>

## <a name="remarks"></a><span data-ttu-id="818a0-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="818a0-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="818a0-110">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="818a0-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="818a0-111">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="818a0-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="818a0-112">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="818a0-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="818a0-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="818a0-113">Examples</span></span>

<span data-ttu-id="818a0-114">В следующем примере используется **заголовок** для получения заголовка папки, содержащей группы программ пользователя (обычно это «Programs»).</span><span class="sxs-lookup"><span data-stu-id="818a0-114">The following example uses **Title** to retrieve the title of the folder holding the user's program groups (usually "Programs").</span></span> <span data-ttu-id="818a0-115">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="818a0-115">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="818a0-116">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="818a0-116">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="818a0-117">Сценариев</span><span class="sxs-lookup"><span data-stu-id="818a0-117">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="818a0-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="818a0-118">Visual Basic:</span></span>


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="818a0-119">Требования</span><span class="sxs-lookup"><span data-stu-id="818a0-119">Requirements</span></span>



| <span data-ttu-id="818a0-120">Требование</span><span class="sxs-lookup"><span data-stu-id="818a0-120">Requirement</span></span> | <span data-ttu-id="818a0-121">Значение</span><span class="sxs-lookup"><span data-stu-id="818a0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="818a0-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="818a0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="818a0-123">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="818a0-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="818a0-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="818a0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="818a0-125">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="818a0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="818a0-126">Заголовок</span><span class="sxs-lookup"><span data-stu-id="818a0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="818a0-127"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="818a0-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="818a0-128">IDL</span><span class="sxs-lookup"><span data-stu-id="818a0-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="818a0-129"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="818a0-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="818a0-130">DLL</span><span class="sxs-lookup"><span data-stu-id="818a0-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="818a0-131"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="818a0-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




