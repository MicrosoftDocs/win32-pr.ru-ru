---
description: Задает фильтр с подстановочными знаками, применяемый к возвращаемым элементам.
ms.assetid: 19ca82c5-16ff-46c7-8ea1-ddbfc2ce3ac9
title: Метод FolderItems3. Filter (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems3.Filter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 26a24dc3ef1f4d0de09dbd97a5dce4c8ed8c783b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808003"
---
# <a name="folderitems3filter-method"></a><span data-ttu-id="2b6fa-103">FolderItems3. Filter, метод</span><span class="sxs-lookup"><span data-stu-id="2b6fa-103">FolderItems3.Filter method</span></span>

<span data-ttu-id="2b6fa-104">Задает фильтр с подстановочными знаками, применяемый к возвращаемым элементам.</span><span class="sxs-lookup"><span data-stu-id="2b6fa-104">Sets a wildcard filter to apply to the items returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b6fa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b6fa-105">Syntax</span></span>


```JScript
iRetVal = FolderItems3.Filter(
  grfFlags,
  bstrFilter
)
```



## <a name="parameters"></a><span data-ttu-id="2b6fa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b6fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b6fa-107">*грффлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b6fa-107">*grfFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6fa-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="2b6fa-108">Type: **Integer**</span></span>

<span data-ttu-id="2b6fa-109">Этот параметр может быть одним из флагов, перечисленных в [**шконтф**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span><span class="sxs-lookup"><span data-stu-id="2b6fa-109">This parameter can be one of the flags listed in [**SHCONTF**](/windows/win32/api/shobjidl_core/ne-shobjidl_core-_shcontf).</span></span>

</dd> <dt>

<span data-ttu-id="2b6fa-110">*бстрфилтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2b6fa-110">*bstrFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b6fa-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="2b6fa-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="2b6fa-112">Строка фильтра, указывающая, что должно быть указано в коллекции [**фолдеритемс**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="2b6fa-112">A filter string that specifies what should be listed in the [**FolderItems**](folderitems.md) collection.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="2b6fa-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b6fa-113">Examples</span></span>

<span data-ttu-id="2b6fa-114">В следующем примере показано правильное использование **фильтра** для JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2b6fa-114">The following example shows the proper usage of **Filter** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2b6fa-115">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="2b6fa-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItems3FilterJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItems3;
            
            objFolderItems3 = objFolder.Items();
            if (objFolderItems3 != null)
            {
                var SHCONTF_NONFOLDERS = 64;
                
                alert(objFolderItems3.Count);
                objFolderItems3.Filter(SHCONTF_NONFOLDERS, "*.txt");
                alert(objFolderItems3.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="2b6fa-116">Сценариев</span><span class="sxs-lookup"><span data-stu-id="2b6fa-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItems3FilterVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems3
                        
                set objFolderItems3 = objFolder.Items()
                if (not objFolderItems3 is nothing) then
                    dim SHCONTF_NONFOLDERS
                
                    SHCONTF_NONFOLDERS = 64
                    alert(objFolderItems3.Count)
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.txt"
                    alert(objFolderItems3.Count)
                end if
                set objFolderItems3 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2b6fa-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2b6fa-117">Visual Basic:</span></span>


```VB
Private Sub fnFolderItems3FilterVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems3 As FolderItems3
            
            Set objFolderItems3 = objFolder.Items
                If (Not objFolderItems3 Is Nothing) Then
                    Dim SHCONTF_NONFOLDERS As Long
                    
                    SHCONTF_NONFOLDERS = 64
                    Debug.Print objFolderItems3.Count
                    objFolderItems3.Filter SHCONTF_NONFOLDERS, "*.exe"
                    Debug.Print objFolderItems3.Count
                End If
            Set objFolderItems3 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2b6fa-118">Требования</span><span class="sxs-lookup"><span data-stu-id="2b6fa-118">Requirements</span></span>



| <span data-ttu-id="2b6fa-119">Требование</span><span class="sxs-lookup"><span data-stu-id="2b6fa-119">Requirement</span></span> | <span data-ttu-id="2b6fa-120">Значение</span><span class="sxs-lookup"><span data-stu-id="2b6fa-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b6fa-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b6fa-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2b6fa-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b6fa-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b6fa-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b6fa-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2b6fa-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="2b6fa-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2b6fa-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="2b6fa-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b6fa-126"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fa-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2b6fa-127">IDL</span><span class="sxs-lookup"><span data-stu-id="2b6fa-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b6fa-128"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fa-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2b6fa-129">DLL</span><span class="sxs-lookup"><span data-stu-id="2b6fa-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b6fa-130"><dt>Shell32.dll (версия 6,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="2b6fa-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b6fa-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b6fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b6fa-132">**FolderItems3**</span><span class="sxs-lookup"><span data-stu-id="2b6fa-132">**FolderItems3**</span></span>](folderitems3-object.md)
</dt> <dt>

[<span data-ttu-id="2b6fa-133">**FolderItems2**</span><span class="sxs-lookup"><span data-stu-id="2b6fa-133">**FolderItems2**</span></span>](folderitems2-object.md)
</dt> <dt>

[<span data-ttu-id="2b6fa-134">**FolderItem**</span><span class="sxs-lookup"><span data-stu-id="2b6fa-134">**FolderItem**</span></span>](folderitem.md)
</dt> </dl>

 

 
