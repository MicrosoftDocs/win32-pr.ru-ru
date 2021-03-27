---
description: Содержит объект родительской папки.
ms.assetid: b832948c-f599-4ada-8760-9280b86abfed
title: Свойство Folder. Парентфолдер (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParentFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 200d8f8c931bd81015f52226bed5a4e584951e20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998458"
---
# <a name="folderparentfolder-property"></a><span data-ttu-id="9228c-103">Свойство Folder. Парентфолдер</span><span class="sxs-lookup"><span data-stu-id="9228c-103">Folder.ParentFolder property</span></span>

<span data-ttu-id="9228c-104">Содержит объект родительской [**папки**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="9228c-104">Contains the parent [**Folder**](folder.md) object.</span></span>

<span data-ttu-id="9228c-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9228c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9228c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9228c-106">Syntax</span></span>


```JScript
ParentFolder = Folder.ParentFolder
```



## <a name="property-value"></a><span data-ttu-id="9228c-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9228c-107">Property value</span></span>

<span data-ttu-id="9228c-108">Ссылка на объект Парентфолдер.</span><span class="sxs-lookup"><span data-stu-id="9228c-108">An object reference to the ParentFolder object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9228c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="9228c-109">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9228c-110">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="9228c-110">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="9228c-111">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="9228c-111">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="9228c-112">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="9228c-112">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="9228c-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="9228c-113">Examples</span></span>

<span data-ttu-id="9228c-114">В следующем примере показано правильное использование **парентфолдер** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9228c-114">The following example shows the proper usage of **ParentFolder** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="9228c-115">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="9228c-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderParentFolderJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objParentFolder;
                
            objParentFolder = objFolder.ParentFolder;
            if (objParentFolder != null)
            {
                alert(objParentFolder.Title);
            }
        }
    }
</script>
```



<span data-ttu-id="9228c-116">Сценариев</span><span class="sxs-lookup"><span data-stu-id="9228c-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderParentFolderVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objParentFolder
                        
                set objParentFolder = objFolder.ParentFolder
                if (not objParentFolder is nothing) then
                    alert(objParentFolder.Title)
                end if
                set objParentFolder = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="9228c-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="9228c-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderParentFolderVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objParentFolder As Folder
                
        Set objParentFolder = objFolder.ParentFolder
        If (Not objParentFolder Is Nothing) Then
            Debug.Print objParentFolder.Title
        End If
        Set objParentFolder = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="9228c-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9228c-118">Requirements</span></span>



| <span data-ttu-id="9228c-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9228c-119">Requirement</span></span> | <span data-ttu-id="9228c-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9228c-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9228c-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9228c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9228c-122">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9228c-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9228c-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9228c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9228c-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9228c-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9228c-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9228c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9228c-126"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9228c-126"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9228c-127">IDL</span><span class="sxs-lookup"><span data-stu-id="9228c-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9228c-128"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9228c-128"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9228c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9228c-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9228c-130"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="9228c-130"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




