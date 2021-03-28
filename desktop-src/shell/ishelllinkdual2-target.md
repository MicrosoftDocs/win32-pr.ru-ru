---
description: Содержит целевой объект объекта Link.
ms.assetid: 26da562b-a1d6-4150-9d9a-05b11e3972d9
title: Свойство IShellLinkDual2. Target (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellLinkDual2.Target
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8e5f29623cf94ef5f17f06e52337928c0c345e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984613"
---
# <a name="ishelllinkdual2target-property"></a><span data-ttu-id="a6f70-103">IShellLinkDual2. Target, свойство</span><span class="sxs-lookup"><span data-stu-id="a6f70-103">IShellLinkDual2.Target property</span></span>

<span data-ttu-id="a6f70-104">Содержит целевой объект объекта Link.</span><span class="sxs-lookup"><span data-stu-id="a6f70-104">Contains the link object's target.</span></span>

<span data-ttu-id="a6f70-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a6f70-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6f70-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6f70-106">Syntax</span></span>


```JScript
Target = IShellLinkDual2.Target
```



## <a name="property-value"></a><span data-ttu-id="a6f70-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="a6f70-107">Property value</span></span>

<span data-ttu-id="a6f70-108">Выражение объекта, результатом которого является объект [**FolderItem**](folderitem.md) целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="a6f70-108">An object expression that evaluates to the target's [**FolderItem**](folderitem.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="a6f70-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="a6f70-109">Examples</span></span>

<span data-ttu-id="a6f70-110">В следующем примере используется **целевой объект** для получения цели ярлыка к Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a6f70-110">The following example uses **Target** to retrieve the target of a shortcut to Internet Explorer.</span></span> <span data-ttu-id="a6f70-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a6f70-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="a6f70-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="a6f70-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellLinkDual2TargetJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
                
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                        
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    var objTargetItem;
                            
                    objTargetItem = objShellLink.Target;
                    if (objTargetItem != null)
                    {
                        // Add code here.
                    }
                }
            }
        }
    }
</script>
```



<span data-ttu-id="a6f70-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="a6f70-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIShellLinkDual2TargetVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim objShellLink
                    
                    set objShellLink = objFolderItem.GetLink
                        if (not objShellLink is nothing) then
                            dim objTargetItem
                            
                            set objTargetItem = objShellLink.Target
                                if (not objTargetItem is nothing) then
                                    'Add code here.
                                end if
                            set objTargetItem = nothing
                        end if
                    set objShellLink = nothing
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="a6f70-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="a6f70-114">Visual Basic:</span></span>


```VB
Private Sub fnIShellLinkDual2TargetVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfPROGRAMS
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
                
        Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
        If (Not objFolderItem Is Nothing) Then
            Dim objShellLink As ShellLinkObject
            
            Set objShellLink = objFolderItem.GetLink
                If (Not objShellLink Is Nothing) Then
                    Dim objTargetItem As FolderItem
                    
                    Set objTargetItem = objShellLink.Target
                        If (Not objTargetItem Is Nothing) Then
                            'Add code here
                        End If
                    Set objTargetItem = Nothing
                End If
            Set objShellLink = Nothing
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="a6f70-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a6f70-115">Requirements</span></span>



| <span data-ttu-id="a6f70-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a6f70-116">Requirement</span></span> | <span data-ttu-id="a6f70-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a6f70-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6f70-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a6f70-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6f70-119">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a6f70-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6f70-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a6f70-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6f70-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a6f70-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a6f70-122">Header</span><span class="sxs-lookup"><span data-stu-id="a6f70-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6f70-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a6f70-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="a6f70-124">IDL</span><span class="sxs-lookup"><span data-stu-id="a6f70-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a6f70-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a6f70-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="a6f70-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a6f70-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a6f70-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a6f70-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6f70-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6f70-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6f70-129">**IShellLinkDual2**</span><span class="sxs-lookup"><span data-stu-id="a6f70-129">**IShellLinkDual2**</span></span>](ishelllinkdual2-object.md)
</dt> <dt>

[<span data-ttu-id="a6f70-130">**шелллинкобжект**</span><span class="sxs-lookup"><span data-stu-id="a6f70-130">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> </dl>

 

 




