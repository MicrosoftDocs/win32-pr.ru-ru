---
description: Указывает, является ли элемент частью файловой системы.
ms.assetid: 321a2109-88b5-4a41-9a67-dab3e82e95d8
title: Свойство FolderItem. a FileSystem (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsFileSystem
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 852f022e1c24fa24c158ee4eb68dca44e6f010a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984189"
---
# <a name="folderitemisfilesystem-property"></a><span data-ttu-id="14eb8-103">FolderItem. для свойства FileSystem</span><span class="sxs-lookup"><span data-stu-id="14eb8-103">FolderItem.IsFileSystem property</span></span>

<span data-ttu-id="14eb8-104">Указывает, является ли элемент частью файловой системы.</span><span class="sxs-lookup"><span data-stu-id="14eb8-104">Indicates if the item is part of the file system.</span></span>

<span data-ttu-id="14eb8-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="14eb8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="14eb8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14eb8-106">Syntax</span></span>


```JScript
bIsFileSystem = FolderItem.IsFileSystem
```



## <a name="property-value"></a><span data-ttu-id="14eb8-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="14eb8-107">Property value</span></span>

<span data-ttu-id="14eb8-108">**Логическое** значение, которое получает **значение true** , если элемент является частью файловой системы, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="14eb8-108">A **Boolean** that receives **true** if the item is part of the file system or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="14eb8-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="14eb8-109">Examples</span></span>

<span data-ttu-id="14eb8-110">В следующем примере с **помощью файла** «файл» определяется, является ли папка Windows частью файловой системы.</span><span class="sxs-lookup"><span data-stu-id="14eb8-110">The following example uses **IsFileSystem** to determine whether the Windows folder is a part of the file system.</span></span> <span data-ttu-id="14eb8-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="14eb8-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="14eb8-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="14eb8-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsFileSystemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsFileSystem;
            }
        }
    }
</script>
```



<span data-ttu-id="14eb8-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="14eb8-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsFileSystemVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsFileSystem
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="14eb8-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="14eb8-114">Visual Basic:</span></span>


```VB
Private Sub fnIsFileSystemVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsFileSystem
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="14eb8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="14eb8-115">Requirements</span></span>



| <span data-ttu-id="14eb8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="14eb8-116">Requirement</span></span> | <span data-ttu-id="14eb8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="14eb8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14eb8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="14eb8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="14eb8-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="14eb8-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="14eb8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="14eb8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="14eb8-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="14eb8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="14eb8-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="14eb8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="14eb8-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="14eb8-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="14eb8-124">IDL</span><span class="sxs-lookup"><span data-stu-id="14eb8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14eb8-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14eb8-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="14eb8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="14eb8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14eb8-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="14eb8-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




