---
description: Возвращает или задает описание ссылки.
ms.assetid: d3a95281-fb1f-4fd4-9d26-2a6e10a36a86
title: Свойство Шелллинкобжект. Description (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Description
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: aff08831bf194da5c7ce958e5a0746abdd533dc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985576"
---
# <a name="shelllinkobjectdescription-property"></a><span data-ttu-id="97022-103">Шелллинкобжект. Description, свойство</span><span class="sxs-lookup"><span data-stu-id="97022-103">ShellLinkObject.Description property</span></span>

<span data-ttu-id="97022-104">Возвращает или задает описание ссылки.</span><span class="sxs-lookup"><span data-stu-id="97022-104">Gets or sets the description of the link.</span></span>

<span data-ttu-id="97022-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="97022-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="97022-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97022-106">Syntax</span></span>


```JScript
strDescription = ShellLinkObject.Description
ShellLinkObject.Description(sDescription) = strDescription
```



## <a name="property-value"></a><span data-ttu-id="97022-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="97022-107">Property value</span></span>

<span data-ttu-id="97022-108">Описание ссылки.</span><span class="sxs-lookup"><span data-stu-id="97022-108">the link's description.</span></span>

## <a name="examples"></a><span data-ttu-id="97022-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="97022-109">Examples</span></span>

<span data-ttu-id="97022-110">В следующем примере показано правильное использование этого свойства в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="97022-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="97022-111">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="97022-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectDescriptionJ()
    {
        var objShell = new ActiveXObject("shell.application");
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
                    var szDescription;
                    
                    // Get the description for the ShellLinkObject.
                    szDescription = objShellLink.Description;
                    alert(szDescription);
                    
                    // Set the description for the ShellLinkObject.
                    objShellLink.Description = "Test"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="97022-112">Сценариев</span><span class="sxs-lookup"><span data-stu-id="97022-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectDescriptionVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                dim szDescription
                                
                                'Get the description for the ShellLinkObject.
                                szDescription = objShellLink.Description
                                alert(szDescription)
                                
                                'Set the description for the ShellLinkObject.
                                objShellLink.Description = "Test"
                            end if
                        set objShellLink = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="97022-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="97022-113">Visual Basic:</span></span>


```VB
rivate Sub fnShellLinkObjectDescriptionVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            Dim szDescription As String
                            
                            'Get the description for the ShellLinkObject.
                            szDescription = objShellLink.Description
                            Debug.Print szDescription
                            
                            'Set the description for the ShellLinkObject.
                            objShellLink.Description = "Test"
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="97022-114">Требования</span><span class="sxs-lookup"><span data-stu-id="97022-114">Requirements</span></span>



| <span data-ttu-id="97022-115">Требование</span><span class="sxs-lookup"><span data-stu-id="97022-115">Requirement</span></span> | <span data-ttu-id="97022-116">Значение</span><span class="sxs-lookup"><span data-stu-id="97022-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97022-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97022-117">Minimum supported client</span></span><br/> | <span data-ttu-id="97022-118">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97022-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97022-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97022-119">Minimum supported server</span></span><br/> | <span data-ttu-id="97022-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="97022-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="97022-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="97022-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="97022-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="97022-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="97022-123">IDL</span><span class="sxs-lookup"><span data-stu-id="97022-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97022-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97022-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="97022-125">DLL</span><span class="sxs-lookup"><span data-stu-id="97022-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97022-126"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="97022-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




