---
description: Возвращает или задает сочетание клавиш для ссылки.
ms.assetid: edc65fe8-c7f3-46d0-86ca-1c0c93e7ca64
title: Свойство Шелллинкобжект. горячих клавиш (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Hotkey
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ab8615421eee7289e5f0bb58582bf8e0d48f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985957"
---
# <a name="shelllinkobjecthotkey-property"></a><span data-ttu-id="78609-103">Шелллинкобжект. Горячие, свойство</span><span class="sxs-lookup"><span data-stu-id="78609-103">ShellLinkObject.Hotkey property</span></span>

<span data-ttu-id="78609-104">Возвращает или задает сочетание клавиш для ссылки.</span><span class="sxs-lookup"><span data-stu-id="78609-104">Gets or sets the keyboard shortcut for the link.</span></span>

<span data-ttu-id="78609-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="78609-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78609-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78609-106">Syntax</span></span>


```JScript
iHotkey = ShellLinkObject.Hotkey
ShellLinkObject.Hotkey(iHotkey) = iHotkey
```



## <a name="property-value"></a><span data-ttu-id="78609-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="78609-107">Property value</span></span>

<span data-ttu-id="78609-108">сочетание клавиш для ссылки.</span><span class="sxs-lookup"><span data-stu-id="78609-108">the link's keyboard shortcut.</span></span> <span data-ttu-id="78609-109">Виртуальный клавиатурный ярлык находится в младших байтах, а флаги-модификаторы находятся в байте высокого порядка.</span><span class="sxs-lookup"><span data-stu-id="78609-109">The virtual keyboard shortcut is in the low-order byte, and the modifier flags are in the high-order byte.</span></span> <span data-ttu-id="78609-110">Флаги модификатора могут быть сочетанием следующих значений.</span><span class="sxs-lookup"><span data-stu-id="78609-110">The modifier flags can be a combination of the following values.</span></span>

<dt>



 <span data-ttu-id="78609-111">(1)</span><span class="sxs-lookup"><span data-stu-id="78609-111">(1)</span></span>


</dt> <dd>

<span data-ttu-id="78609-112">Клавиша SHIFT</span><span class="sxs-lookup"><span data-stu-id="78609-112">SHIFT key</span></span>

</dd> <dt>



 <span data-ttu-id="78609-113">(2)</span><span class="sxs-lookup"><span data-stu-id="78609-113">(2)</span></span>


</dt> <dd>

<span data-ttu-id="78609-114">Клавиша CTRL</span><span class="sxs-lookup"><span data-stu-id="78609-114">CTRL key</span></span>

</dd> <dt>



 <span data-ttu-id="78609-115">(4)</span><span class="sxs-lookup"><span data-stu-id="78609-115">(4)</span></span>


</dt> <dd>

<span data-ttu-id="78609-116">ALT - клавиша</span><span class="sxs-lookup"><span data-stu-id="78609-116">ALT key</span></span>

</dd> <dt>



 <span data-ttu-id="78609-117">(8)</span><span class="sxs-lookup"><span data-stu-id="78609-117">(8)</span></span>


</dt> <dd>

<span data-ttu-id="78609-118">Расширенный ключ</span><span class="sxs-lookup"><span data-stu-id="78609-118">Extended key</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="78609-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="78609-119">Examples</span></span>

<span data-ttu-id="78609-120">В следующем примере показано правильное использование этого свойства в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="78609-120">The following example shows the proper usage of this property in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="78609-121">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="78609-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectHotkeyJ()
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
                    var nHotkey;
                    
                    // Get the keyboard shortcut for the ShellLinkObject.
                    nHotkey = objShellLink.Hotkey;
                    alert(nHotkey);
                    
                    // Set the keyboard shortcut for the ShellLinkObject.
                    objShellLink.Hotkey = 4;
                }
            }
        }
    }
</script>
```



<span data-ttu-id="78609-122">Сценариев</span><span class="sxs-lookup"><span data-stu-id="78609-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnShellLinkObjectHotkeyVB()
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
                                dim nHotkey
                                
                                'Get the keyboard shortcut for the ShellLinkObject.
                                nHotkey = objShellLink.Hotkey
                                alert(nHotkey)
                                
                                'Set the keyboard shortcut for the ShellLinkObject.
                                objShellLink.Hotkey = 4
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



<span data-ttu-id="78609-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="78609-123">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectHotkeyVB()
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
                            Dim nHotkey As Integer
                            
                            'Get the keyboard shortcut for the ShellLinkObject.
                            nHotkey = objShellLink.Hotkey
                            Debug.Print nHotkey
                            
                            'Set the keyboard shortcut for the ShellLinkObject.
                            objShellLink.Hotkey = 4
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="78609-124">Требования</span><span class="sxs-lookup"><span data-stu-id="78609-124">Requirements</span></span>



| <span data-ttu-id="78609-125">Требование</span><span class="sxs-lookup"><span data-stu-id="78609-125">Requirement</span></span> | <span data-ttu-id="78609-126">Значение</span><span class="sxs-lookup"><span data-stu-id="78609-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78609-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78609-127">Minimum supported client</span></span><br/> | <span data-ttu-id="78609-128">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78609-128">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="78609-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78609-129">Minimum supported server</span></span><br/> | <span data-ttu-id="78609-130">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="78609-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="78609-131">Заголовок</span><span class="sxs-lookup"><span data-stu-id="78609-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="78609-132"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="78609-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="78609-133">IDL</span><span class="sxs-lookup"><span data-stu-id="78609-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="78609-134"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="78609-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="78609-135">DLL</span><span class="sxs-lookup"><span data-stu-id="78609-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78609-136"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="78609-136"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




