---
description: Содержит число элементов в коллекции.
ms.assetid: 383382d5-7e3f-4b27-bebf-6b79dbe677b8
title: Свойство Фолдеритемс. Count (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 814a8248a54c5b58624a721f006bc8d4f974ba92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984181"
---
# <a name="folderitemscount-property"></a><span data-ttu-id="bb0b8-103">Фолдеритемс. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="bb0b8-103">FolderItems.Count property</span></span>

<span data-ttu-id="bb0b8-104">Содержит число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="bb0b8-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="bb0b8-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bb0b8-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb0b8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb0b8-106">Syntax</span></span>


```JScript
iCount = FolderItems.Count
```



## <a name="property-value"></a><span data-ttu-id="bb0b8-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bb0b8-107">Property value</span></span>

<span data-ttu-id="bb0b8-108">**Целое число** , содержащее значение для свойства **Count** .</span><span class="sxs-lookup"><span data-stu-id="bb0b8-108">An **Integer** that contains a value for the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="bb0b8-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="bb0b8-109">Examples</span></span>

<span data-ttu-id="bb0b8-110">В следующем примере функция **Count** используется для получения числа элементов в папке Windows.</span><span class="sxs-lookup"><span data-stu-id="bb0b8-110">The following example uses **Count** to retrieve the count of items in the Windows folder.</span></span> <span data-ttu-id="bb0b8-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bb0b8-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bb0b8-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="bb0b8-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                var nCount;
                
                nCount = objFolderItems.Count;
                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="bb0b8-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="bb0b8-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bb0b8-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bb0b8-114">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bb0b8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bb0b8-115">Requirements</span></span>



| <span data-ttu-id="bb0b8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bb0b8-116">Requirement</span></span> | <span data-ttu-id="bb0b8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bb0b8-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb0b8-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bb0b8-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bb0b8-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bb0b8-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bb0b8-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bb0b8-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bb0b8-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bb0b8-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb0b8-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bb0b8-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb0b8-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb0b8-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bb0b8-124">IDL</span><span class="sxs-lookup"><span data-stu-id="bb0b8-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bb0b8-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bb0b8-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bb0b8-126">DLL</span><span class="sxs-lookup"><span data-stu-id="bb0b8-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb0b8-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="bb0b8-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




