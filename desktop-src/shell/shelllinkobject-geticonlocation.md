---
description: Возвращает расположение значка, назначенного ссылке.
ms.assetid: 3bb7f0f0-7ab9-41e6-b738-274efbcd52ab
title: Метод Шелллинкобжект. Жетиконлокатион (Шлобж \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.GetIconLocation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ef2f502d30116def68aa43269b3020d404ce177d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265684"
---
# <a name="shelllinkobjectgeticonlocation-method"></a><span data-ttu-id="ee99a-103">Шелллинкобжект. Жетиконлокатион, метод</span><span class="sxs-lookup"><span data-stu-id="ee99a-103">ShellLinkObject.GetIconLocation method</span></span>

<span data-ttu-id="ee99a-104">Возвращает расположение значка, назначенного ссылке.</span><span class="sxs-lookup"><span data-stu-id="ee99a-104">Gets the location of the icon assigned to the link.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee99a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee99a-105">Syntax</span></span>


```JScript
iRetVal = ShellLinkObject.GetIconLocation(
  sPath
)
```



## <a name="parameters"></a><span data-ttu-id="ee99a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee99a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee99a-107">*спас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ee99a-107">*sPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee99a-108">Тип: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="ee99a-108">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="ee99a-109">При возврате из этого метода он содержит полный путь к файлу, содержащему значок.</span><span class="sxs-lookup"><span data-stu-id="ee99a-109">When this method returns, it holds the fully qualified path of the file that contains the icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee99a-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee99a-110">Return value</span></span>

<span data-ttu-id="ee99a-111">Тип: _*Integer \**_</span><span class="sxs-lookup"><span data-stu-id="ee99a-111">Type: _*Integer\**_</span></span>

<span data-ttu-id="ee99a-112">Возвращает индекс значка в файле, указанном параметром _sPath \*.</span><span class="sxs-lookup"><span data-stu-id="ee99a-112">Returns the icon's index in the file specified by _sPath\*.</span></span>

## <a name="examples"></a><span data-ttu-id="ee99a-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="ee99a-113">Examples</span></span>

<span data-ttu-id="ee99a-114">В следующем примере показано правильное использование этого метода для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ee99a-114">The following example shows the proper usage of this method for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ee99a-115">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ee99a-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellShellLinkObjectGetIconLocationJ()
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
                    var nIcon;
                    
                    nIcon = objShellLink.GetIconLocation(objFolderItem.Path);
                    alert(nIcon);
                }
            }
        }
    }
</script>
```



<span data-ttu-id="ee99a-116">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ee99a-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellLinkObjectGetIconLocationVB()
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
                                dim nIcon
                                
                                nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                                alert(nIcon)
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



<span data-ttu-id="ee99a-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ee99a-117">Visual Basic:</span></span>


```VB
Private Sub fnShellLinkObjectGetIconLocationVB()
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
                            Dim nIcon As Integer
                            
                            nIcon = objShellLink.GetIconLocation(objFolderItem.Path)
                            Debug.Print nIcon
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ee99a-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ee99a-118">Requirements</span></span>



| <span data-ttu-id="ee99a-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ee99a-119">Requirement</span></span> | <span data-ttu-id="ee99a-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ee99a-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee99a-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee99a-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ee99a-122">Windows 2000 Professional с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee99a-122">Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ee99a-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee99a-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ee99a-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ee99a-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ee99a-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ee99a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee99a-126"><dt>Шлобж \_ Core. h (включение шлдисп. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee99a-126"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl> |
| <span data-ttu-id="ee99a-127">IDL</span><span class="sxs-lookup"><span data-stu-id="ee99a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ee99a-128"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ee99a-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="ee99a-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ee99a-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee99a-130"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ee99a-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee99a-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee99a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee99a-132">**шелллинкобжект**</span><span class="sxs-lookup"><span data-stu-id="ee99a-132">**ShellLinkObject**</span></span>](shelllinkobject-object.md)
</dt> <dt>

[<span data-ttu-id="ee99a-133">**сетиконлокатион**</span><span class="sxs-lookup"><span data-stu-id="ee99a-133">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md)
</dt> </dl>

 

 
