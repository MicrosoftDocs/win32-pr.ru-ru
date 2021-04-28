---
description: Фолдеритемвербс. Count, свойство содержит количество элементов в коллекции.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Свойство Фолдеритемвербс. Count (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5545ea64da914188226fbdabf7cc6301baa695af
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089552"
---
# <a name="folderitemverbscount-property"></a><span data-ttu-id="84c24-103">Фолдеритемвербс. Count, свойство</span><span class="sxs-lookup"><span data-stu-id="84c24-103">FolderItemVerbs.Count property</span></span>

<span data-ttu-id="84c24-104">Содержит число элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="84c24-104">Contains the number of items in the collection.</span></span>

<span data-ttu-id="84c24-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="84c24-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84c24-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84c24-106">Syntax</span></span>


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a><span data-ttu-id="84c24-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="84c24-107">Property value</span></span>

<span data-ttu-id="84c24-108">**Целое число** , принимающее свойство **Count** .</span><span class="sxs-lookup"><span data-stu-id="84c24-108">An **Integer** that receives the **Count** property.</span></span>

## <a name="examples"></a><span data-ttu-id="84c24-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="84c24-109">Examples</span></span>

<span data-ttu-id="84c24-110">В следующем примере функция **Count** используется для получения числа команд, доступных для папки панели управления.</span><span class="sxs-lookup"><span data-stu-id="84c24-110">The following example uses **Count** to retrieve the count of verbs available for the Control Panel folder.</span></span> <span data-ttu-id="84c24-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="84c24-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="84c24-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="84c24-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



<span data-ttu-id="84c24-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="84c24-113">VBScript:</span></span>


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



<span data-ttu-id="84c24-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="84c24-114">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="84c24-115">Требования</span><span class="sxs-lookup"><span data-stu-id="84c24-115">Requirements</span></span>



| <span data-ttu-id="84c24-116">Требование</span><span class="sxs-lookup"><span data-stu-id="84c24-116">Requirement</span></span> | <span data-ttu-id="84c24-117">Значение</span><span class="sxs-lookup"><span data-stu-id="84c24-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84c24-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84c24-118">Minimum supported client</span></span><br/> | <span data-ttu-id="84c24-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="84c24-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="84c24-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84c24-120">Minimum supported server</span></span><br/> | <span data-ttu-id="84c24-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="84c24-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="84c24-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="84c24-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="84c24-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="84c24-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="84c24-124">IDL</span><span class="sxs-lookup"><span data-stu-id="84c24-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84c24-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84c24-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="84c24-126">DLL</span><span class="sxs-lookup"><span data-stu-id="84c24-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84c24-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="84c24-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




