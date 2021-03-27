---
description: Указывает, является ли элемент ярлыком.
ms.assetid: f3400f0b-5c7f-4d41-a162-1c35014082ac
title: Свойство FolderItem. a (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.IsLink
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: bd4357485dce3f3d236f31797d8b2df7028f3d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896557"
---
# <a name="folderitemislink-property"></a><span data-ttu-id="ab57d-103">FolderItem. свойство связи</span><span class="sxs-lookup"><span data-stu-id="ab57d-103">FolderItem.IsLink property</span></span>

<span data-ttu-id="ab57d-104">Указывает, является ли элемент ярлыком.</span><span class="sxs-lookup"><span data-stu-id="ab57d-104">Indicates whether the item is a shortcut.</span></span>

<span data-ttu-id="ab57d-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ab57d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab57d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ab57d-106">Syntax</span></span>


```JScript
bIsLink = FolderItem.IsLink
```



## <a name="property-value"></a><span data-ttu-id="ab57d-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ab57d-107">Property value</span></span>

<span data-ttu-id="ab57d-108">**Логическое** значение, которое получает **значение true** , если элемент является ярлыком, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ab57d-108">A **Boolean** that receives **true** if the item is a shortcut or **false** if not.</span></span>

## <a name="examples"></a><span data-ttu-id="ab57d-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab57d-109">Examples</span></span>

<span data-ttu-id="ab57d-110">В следующем примере с помощью « **onlink** » определяется, является ли определенный объект ссылкой.</span><span class="sxs-lookup"><span data-stu-id="ab57d-110">The following example uses **IsLink** to determine whether a particular object is a link.</span></span> <span data-ttu-id="ab57d-111">В этом случае объект является ярлыком Internet Explorer и поэтому должен возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ab57d-111">In this case, the object is a shortcut to Internet Explorer and so should return **true**.</span></span> <span data-ttu-id="ab57d-112">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ab57d-112">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ab57d-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ab57d-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIsLinkJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfPROGRAMS = 2;
        
        objFolder2 = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var bReturn;
                
                bReturn = objFolderItem.IsLink;
            }
        }
    }
</script>
```



<span data-ttu-id="ab57d-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ab57d-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnIsLinkVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfPROGRAMS
                
            ssfPROGRAMS = 2
            set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                if (not objFolderItem is nothing) then
                    dim bReturn
                                
                    bReturn = objFolderItem.IsLink
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="ab57d-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ab57d-115">Visual Basic:</span></span>


```VB
Private Sub fnIsLinkVB()
    Dim objShell    As Shell
    Dim objFolder2  As Folder2
    Dim ssfPROGRAMS As Long
    
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim bReturn As Boolean
                    
                    bReturn = objFolderItem.IsLink
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



## <a name="requirements"></a><span data-ttu-id="ab57d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ab57d-116">Requirements</span></span>



| <span data-ttu-id="ab57d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ab57d-117">Requirement</span></span> | <span data-ttu-id="ab57d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ab57d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab57d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab57d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab57d-120">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ab57d-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ab57d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab57d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab57d-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ab57d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab57d-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ab57d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab57d-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab57d-124"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ab57d-125">IDL</span><span class="sxs-lookup"><span data-stu-id="ab57d-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab57d-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab57d-126"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ab57d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ab57d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab57d-128"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ab57d-128"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




