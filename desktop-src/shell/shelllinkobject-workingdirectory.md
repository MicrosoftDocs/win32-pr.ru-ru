---
description: Возвращает или задает рабочий каталог, указанный в ссылке.
ms.assetid: c3820deb-9f00-42a9-ab0e-c0f6389e9f29
title: Свойство Шелллинкобжект. WorkingDirectory (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.WorkingDirectory
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d8788899a06179056cd871b68e4e64566bcd5ee6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346125"
---
# <a name="shelllinkobjectworkingdirectory-property"></a><span data-ttu-id="04775-103">Шелллинкобжект. WorkingDirectory, свойство</span><span class="sxs-lookup"><span data-stu-id="04775-103">ShellLinkObject.WorkingDirectory property</span></span>

<span data-ttu-id="04775-104">Возвращает или задает рабочий каталог, указанный в ссылке.</span><span class="sxs-lookup"><span data-stu-id="04775-104">Gets or sets the working directory specified in the link.</span></span>

<span data-ttu-id="04775-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="04775-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="04775-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04775-106">Syntax</span></span>


```JScript
strWorkingDirectory = ShellLinkObject.WorkingDirectory
ShellLinkObject.WorkingDirectory(sWorkingDirectory) = strWorkingDirectory
```



## <a name="property-value"></a><span data-ttu-id="04775-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="04775-107">Property value</span></span>

<span data-ttu-id="04775-108">полный путь к рабочему каталогу ссылки.</span><span class="sxs-lookup"><span data-stu-id="04775-108">the fully qualified path of the link's working directory.</span></span>

## <a name="examples"></a><span data-ttu-id="04775-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="04775-109">Examples</span></span>

<span data-ttu-id="04775-110">В следующем примере показано правильное использование этого свойства в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="04775-110">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="04775-111">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="04775-111">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectWorkingDirectoryJ()
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
                    var szDirectory;
                    
                    // Get the working directory for the ShellLinkObject.
                    szDirectory = objShellLink.WorkingDirectory;
                    alert(szDirectory);
                    
                    // Set the working directory for the ShellLinkObject.
                    objShellLink.WorkingDirectory = "";
                }
            }
        }
    }
</script>
```



<span data-ttu-id="04775-112">Сценариев</span><span class="sxs-lookup"><span data-stu-id="04775-112">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectWorkingDirectoryVB()
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
                                dim szDirectory
                                
                                'Get the working directory.
                                szDirectory = objShellLink.WorkingDirectory
                                alert(szDirectory)
                                
                                'Set the working directory.
                                objShellLink.WorkingDirectory = ""
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



<span data-ttu-id="04775-113">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="04775-113">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectWorkingDirectoryVB()
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
                            Dim szDirectory As String
                            
                            'Get the working directory.
                            szDirectory = objShellLink.WorkingDirectory
                            Debug.Print szDirectory
                            
                            'Set the working directory.
                            objShellLink.WorkingDirectory = ""
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
```



## <a name="requirements"></a><span data-ttu-id="04775-114">Требования</span><span class="sxs-lookup"><span data-stu-id="04775-114">Requirements</span></span>



| <span data-ttu-id="04775-115">Требование</span><span class="sxs-lookup"><span data-stu-id="04775-115">Requirement</span></span> | <span data-ttu-id="04775-116">Значение</span><span class="sxs-lookup"><span data-stu-id="04775-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04775-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04775-117">Minimum supported client</span></span><br/> | <span data-ttu-id="04775-118">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04775-118">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="04775-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04775-119">Minimum supported server</span></span><br/> | <span data-ttu-id="04775-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="04775-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="04775-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="04775-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="04775-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="04775-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="04775-123">IDL</span><span class="sxs-lookup"><span data-stu-id="04775-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04775-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04775-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="04775-125">DLL</span><span class="sxs-lookup"><span data-stu-id="04775-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04775-126"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="04775-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




