---
description: Содержит размер элемента.
ms.assetid: 0eda405e-d54f-48d2-a060-a1fdcdb23785
title: Свойство FolderItem. size (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Size
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5d44d1c1ddd9b46f768f218250802562f9a36312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539503"
---
# <a name="folderitemsize-property"></a><span data-ttu-id="afac0-103">FolderItem. size, свойство</span><span class="sxs-lookup"><span data-stu-id="afac0-103">FolderItem.Size property</span></span>

<span data-ttu-id="afac0-104">Содержит размер элемента.</span><span class="sxs-lookup"><span data-stu-id="afac0-104">Contains the item's size.</span></span>

<span data-ttu-id="afac0-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="afac0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="afac0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afac0-106">Syntax</span></span>


```JScript
iSize = FolderItem.Size
```



## <a name="property-value"></a><span data-ttu-id="afac0-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="afac0-107">Property value</span></span>

<span data-ttu-id="afac0-108">**Целое число** , получающее размер элемента.</span><span class="sxs-lookup"><span data-stu-id="afac0-108">An **Integer** that receives the item's size.</span></span>

## <a name="examples"></a><span data-ttu-id="afac0-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="afac0-109">Examples</span></span>

<span data-ttu-id="afac0-110">В следующем примере **Размер** используется для получения размера исполняемого файла Notepad.</span><span class="sxs-lookup"><span data-stu-id="afac0-110">The following example uses **Size** to retrieve the size of the Notepad executable file.</span></span> <span data-ttu-id="afac0-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="afac0-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="afac0-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="afac0-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemSizeJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                var szReturn;
                
                szReturn = objFolderItem.Size;
            }
        }
    }
</script>
```



<span data-ttu-id="afac0-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="afac0-113">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnFolderItemSizeVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    szReturn = objFolderItem.Size
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="afac0-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="afac0-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemSizeVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    szReturn = objFolderItem.Size
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



## <a name="requirements"></a><span data-ttu-id="afac0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="afac0-115">Requirements</span></span>



| <span data-ttu-id="afac0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="afac0-116">Requirement</span></span> | <span data-ttu-id="afac0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="afac0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afac0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="afac0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="afac0-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="afac0-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="afac0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="afac0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="afac0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="afac0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="afac0-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="afac0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="afac0-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="afac0-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="afac0-124">IDL</span><span class="sxs-lookup"><span data-stu-id="afac0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afac0-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afac0-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="afac0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="afac0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afac0-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="afac0-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




