---
description: Сохраняет все изменения в ссылке.
ms.assetid: 4c776c82-8eca-4c9b-9487-4a835affd2d8
title: Метод Шелллинкобжект. Save (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Save
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0283b839069464a1a059bd11ef52b522f7ec7072
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997939"
---
# <a name="shelllinkobjectsave-method"></a><span data-ttu-id="dc5bc-103">Шелллинкобжект. Save, метод</span><span class="sxs-lookup"><span data-stu-id="dc5bc-103">ShellLinkObject.Save method</span></span>

<span data-ttu-id="dc5bc-104">Сохраняет все изменения в ссылке.</span><span class="sxs-lookup"><span data-stu-id="dc5bc-104">Saves all changes to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc5bc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc5bc-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.Save(
  [ sFile ]
)
```



## <a name="parameters"></a><span data-ttu-id="dc5bc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc5bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc5bc-107">*сфиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="dc5bc-107">*sFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5bc-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="dc5bc-108">Type: **Variant**</span></span>

<span data-ttu-id="dc5bc-109">Строковое значение, содержащее полный путь к файлу, в который должны быть сохранены сведения о новых ссылках.</span><span class="sxs-lookup"><span data-stu-id="dc5bc-109">A string value that contains the fully qualified path of the file where the new link information is to be saved.</span></span> <span data-ttu-id="dc5bc-110">Если файл не указан, используется текущий файл.</span><span class="sxs-lookup"><span data-stu-id="dc5bc-110">If no file is specified, the current file is used.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="dc5bc-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="dc5bc-111">Examples</span></span>

<span data-ttu-id="dc5bc-112">В следующем примере показано правильное использование этого метода для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dc5bc-112">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="dc5bc-113">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="dc5bc-113">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellLinkObjectSaveJ()
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
                    // Making a change to the ShellLinkObject.
                    objShellLink.Description = "New Description";
                    
                    // Saving the changes.
                    objShellLink.Save();
                }
            }
        }
    }
</script>
```



<span data-ttu-id="dc5bc-114">Сценариев</span><span class="sxs-lookup"><span data-stu-id="dc5bc-114">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectSaveVB()
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
                                'Making a change to the ShellLinkObject.
                                objShellLink.Description = "New Description"
                                
                                'Saving the changes.
                                objShellLink.Save()
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



<span data-ttu-id="dc5bc-115">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="dc5bc-115">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectSaveVB()
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
                            'Making a change to the ShellLinkObject.
                            objShellLink.Description = "New Description"
                            'Saving the changes
                            objShellLink.Save
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="dc5bc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dc5bc-116">Requirements</span></span>



| <span data-ttu-id="dc5bc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dc5bc-117">Requirement</span></span> | <span data-ttu-id="dc5bc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dc5bc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5bc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc5bc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5bc-120">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc5bc-120">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc5bc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc5bc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5bc-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dc5bc-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="dc5bc-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dc5bc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc5bc-124"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc5bc-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="dc5bc-125">IDL</span><span class="sxs-lookup"><span data-stu-id="dc5bc-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc5bc-126"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc5bc-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="dc5bc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dc5bc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc5bc-128"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="dc5bc-128"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 




