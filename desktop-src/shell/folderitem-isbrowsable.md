---
description: Указывает, может ли элемент размещаться в кадре браузера или проводника Windows.
ms.assetid: 472e0906-9561-4390-a503-c5e490245ea0
title: Свойство FolderItem. Property (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsBrowsable
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d7c5f7a9cbde54647c299646bb6350c3be6aa2a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423514"
---
# <a name="folderitemisbrowsable-property"></a><span data-ttu-id="e2f15-103">FolderItem. свойство с возможностью просмотра</span><span class="sxs-lookup"><span data-stu-id="e2f15-103">FolderItem.IsBrowsable property</span></span>

<span data-ttu-id="e2f15-104">Указывает, может ли элемент размещаться в кадре браузера или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="e2f15-104">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span>

<span data-ttu-id="e2f15-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e2f15-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f15-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2f15-106">Syntax</span></span>


```JScript
bIsBrowsable = FolderItem.IsBrowsable
```



## <a name="property-value"></a><span data-ttu-id="e2f15-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e2f15-107">Property value</span></span>

<span data-ttu-id="e2f15-108">**Логическое** значение, которое получает **значение true** , если элемент может быть просмотрен, или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e2f15-108">A **Boolean** that receives **true** if the item can be browsed or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="e2f15-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="e2f15-109">Examples</span></span>

<span data-ttu-id="e2f15-110">В следующем примере для определения отображаемого состояния папки Windows используется параметр «с **возможностью** просмотра».</span><span class="sxs-lookup"><span data-stu-id="e2f15-110">The following example uses **IsBrowsable** to determine the browsable state of the Windows folder.</span></span> <span data-ttu-id="e2f15-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="e2f15-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="e2f15-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="e2f15-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsBrowsableJ()
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
                
                bReturn = objFolderItem.IsBrowsable;
            }
        }
    }
</script>
```



<span data-ttu-id="e2f15-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="e2f15-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsBrowsableVB()
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
                                
                    bReturn = objFolderItem.IsBrowsable
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="e2f15-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="e2f15-114">Visual Basic:</span></span>


```VB
Private Sub fnIsBrowsableVB()
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
                    
                    bReturn = objFolderItem.IsBrowsable
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



## <a name="requirements"></a><span data-ttu-id="e2f15-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e2f15-115">Requirements</span></span>



| <span data-ttu-id="e2f15-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e2f15-116">Requirement</span></span> | <span data-ttu-id="e2f15-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e2f15-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f15-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2f15-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f15-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e2f15-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2f15-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2f15-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f15-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e2f15-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="e2f15-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e2f15-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f15-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2f15-123"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="e2f15-124">IDL</span><span class="sxs-lookup"><span data-stu-id="e2f15-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2f15-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2f15-125"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="e2f15-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e2f15-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2f15-127"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="e2f15-127"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




