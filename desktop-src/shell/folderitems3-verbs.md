---
description: Возвращает список команд, общих для всех элементов папки.
ms.assetid: f72f5dcc-35e0-4a23-ae4c-355da2858aab
title: Свойство FolderItems3. Verbs (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Verbs
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7e07da0b4901b4d4ba7a1bda1f20d3f58298f9d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808002"
---
# <a name="folderitems3verbs-property"></a><span data-ttu-id="399c1-103">FolderItems3. Verbs, свойство</span><span class="sxs-lookup"><span data-stu-id="399c1-103">FolderItems3.Verbs property</span></span>

<span data-ttu-id="399c1-104">Возвращает список команд, общих для всех элементов папки.</span><span class="sxs-lookup"><span data-stu-id="399c1-104">Gets the list of verbs common to all the folder items.</span></span>

<span data-ttu-id="399c1-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="399c1-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="399c1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="399c1-106">Syntax</span></span>


```JScript
Verbs = FolderItems3.Verbs
```



## <a name="property-value"></a><span data-ttu-id="399c1-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="399c1-107">Property value</span></span>

<span data-ttu-id="399c1-108">Адрес указателя на коллекцию команд.</span><span class="sxs-lookup"><span data-stu-id="399c1-108">Address of a pointer to the collection of verbs.</span></span> <span data-ttu-id="399c1-109">См. [**фолдеритемвербс**](folderitemverbs.md).</span><span class="sxs-lookup"><span data-stu-id="399c1-109">See [**FolderItemVerbs**](folderitemverbs.md).</span></span>

## <a name="examples"></a><span data-ttu-id="399c1-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="399c1-110">Examples</span></span>

<span data-ttu-id="399c1-111">В следующем примере показано правильное использование **глаголов** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="399c1-111">The following example shows the proper usage of **Verbs** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="399c1-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="399c1-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems3VerbsJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 17;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var objFolderItemVerbs;
                
                objFolderItemVerbs = objFolderItems3.Verbs;
                alert(objFolderItemVerbs.Item(0));
            }
        }
    }
</script>
```



<span data-ttu-id="399c1-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="399c1-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems3VerbsVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim objFolderItemVerbs
                    
                    set objFolderItemVerbs = objFolderItems3.Verbs
                        if (not objFolderItemVerbs is nothing) then
                            alert(objFolderItemVerbs.Item(0))
                        end if
                    set objFolderItemVerbs = nothing
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="399c1-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="399c1-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems3VerbsVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim objFolderItemVerbs As FolderItemVerbs
                    
                    Set objFolderItemVerbs = objFolderItems3.Verbs
                        If (Not objFolderItemVerbs Is Nothing) Then
                            Debug.Print objFolderItemVerbs.Item(0)
                        End If
                    Set objFolderItemVerbs = Nothing
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="399c1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="399c1-115">Requirements</span></span>



| <span data-ttu-id="399c1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="399c1-116">Requirement</span></span> | <span data-ttu-id="399c1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="399c1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="399c1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="399c1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="399c1-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="399c1-119">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="399c1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="399c1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="399c1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="399c1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="399c1-122">Header</span><span class="sxs-lookup"><span data-stu-id="399c1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="399c1-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="399c1-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="399c1-124">IDL</span><span class="sxs-lookup"><span data-stu-id="399c1-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="399c1-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="399c1-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="399c1-126">DLL</span><span class="sxs-lookup"><span data-stu-id="399c1-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="399c1-127"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="399c1-127"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 




