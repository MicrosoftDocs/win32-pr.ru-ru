---
description: Содержит аргументы ссылки.
ms.assetid: 938db958-4b59-4dd6-ac56-f21db05ec989
title: Свойство Шелллинкобжект. Arguments (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Arguments
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c9b8a32eb4b935b5164ef91bf299777b36d7e53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266166"
---
# <a name="shelllinkobjectarguments-property"></a><span data-ttu-id="f34d0-103">Шелллинкобжект. Arguments, свойство</span><span class="sxs-lookup"><span data-stu-id="f34d0-103">ShellLinkObject.Arguments property</span></span>

<span data-ttu-id="f34d0-104">Содержит аргументы ссылки.</span><span class="sxs-lookup"><span data-stu-id="f34d0-104">Contains a link's arguments.</span></span>

<span data-ttu-id="f34d0-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="f34d0-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f34d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f34d0-106">Syntax</span></span>


```JScript
strArguments = ShellLinkObject.Arguments
ShellLinkObject.Arguments(sArguments) = strArguments
```



## <a name="property-value"></a><span data-ttu-id="f34d0-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f34d0-107">Property value</span></span>

<span data-ttu-id="f34d0-108">аргументы ссылки.</span><span class="sxs-lookup"><span data-stu-id="f34d0-108">the link's arguments.</span></span>

## <a name="examples"></a><span data-ttu-id="f34d0-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="f34d0-109">Examples</span></span>

<span data-ttu-id="f34d0-110">В следующем примере **аргументы** используются для получения аргументов для ссылки на Internet Explorer, найденного в меню "Пуск" пользователя.</span><span class="sxs-lookup"><span data-stu-id="f34d0-110">The following example uses **Arguments** to retrieve the arguments for a link to Internet Explorer found in the user's Start menu.</span></span> <span data-ttu-id="f34d0-111">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f34d0-111">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="f34d0-112">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="f34d0-112">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectArgumentJ()
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
                    var szArguments;
                    
                    // Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments;
                    alert(szArguments);
                    
                    // Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                }
            }
        }
    }
</script>
```



<span data-ttu-id="f34d0-113">Сценариев</span><span class="sxs-lookup"><span data-stu-id="f34d0-113">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectArgumentVB()
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
                    dim szArguments
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    alert(szArguments)
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
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



<span data-ttu-id="f34d0-114">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="f34d0-114">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectArgumentsVB()
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
                    Dim szArguments As String
                    
                    'Get the arguments for the ShellLinkObject
                    szArguments = objShellLink.Arguments
                    Debug.Print szArguments
                    
                    'Set the arguments for the ShellLinkObject
                    objShellLink.Arguments = "/s"
                End If

                Set objShellLink = Nothing
            End If

            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="f34d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="f34d0-115">Requirements</span></span>



| <span data-ttu-id="f34d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="f34d0-116">Requirement</span></span> | <span data-ttu-id="f34d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f34d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f34d0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f34d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f34d0-119">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f34d0-119">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f34d0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f34d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f34d0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f34d0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f34d0-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f34d0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f34d0-123"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f34d0-123"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f34d0-124">IDL</span><span class="sxs-lookup"><span data-stu-id="f34d0-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f34d0-125"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f34d0-125"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f34d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f34d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f34d0-127"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f34d0-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




