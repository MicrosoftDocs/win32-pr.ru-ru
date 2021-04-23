---
description: Извлекает объект Фолдеритемс, представляющий коллекцию элементов в папке.
ms.assetid: ef2965ec-c8ab-4108-8e5e-b4fd5370521a
title: Метод Folder. Items (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Items
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c3cfa0fcd2d8e2e51a67a362b33af34abf5b1427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345405"
---
# <a name="folderitems-method"></a><span data-ttu-id="4dd6a-103">Метод Folder. Items</span><span class="sxs-lookup"><span data-stu-id="4dd6a-103">Folder.Items method</span></span>

<span data-ttu-id="4dd6a-104">Извлекает объект [**фолдеритемс**](folderitems.md) , представляющий коллекцию элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="4dd6a-104">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dd6a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dd6a-105">Syntax</span></span>


```JScript
retVal = Folder.Items()
```



## <a name="parameters"></a><span data-ttu-id="4dd6a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4dd6a-106">Parameters</span></span>

<span data-ttu-id="4dd6a-107">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="4dd6a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4dd6a-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4dd6a-108">Return value</span></span>

<span data-ttu-id="4dd6a-109">Тип: **[ **фолдеритемс**](folderitems.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="4dd6a-109">Type: **[**FolderItems**](folderitems.md)\*\***</span></span>

<span data-ttu-id="4dd6a-110">Ссылка на объект [**фолдеритемс**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="4dd6a-110">An object reference to the [**FolderItems**](folderitems.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4dd6a-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4dd6a-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4dd6a-112">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="4dd6a-112">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="4dd6a-113">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="4dd6a-113">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="4dd6a-114">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="4dd6a-114">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4dd6a-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="4dd6a-115">Examples</span></span>

<span data-ttu-id="4dd6a-116">В следующем примере **элементы** используются для определения количества элементов в папке C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="4dd6a-116">The following example uses **Items** to determine the number of items in the C:\\Windows folder.</span></span> <span data-ttu-id="4dd6a-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="4dd6a-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="4dd6a-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="4dd6a-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectItemsJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItems = new Object;
            
            objFolderItems = objFolder.Items();
            if (objFolderItems != null)
            {
                document.write (objFolderItems.Count);
            }
        }
    }
</script>
```



<span data-ttu-id="4dd6a-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="4dd6a-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectItemsVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItems

            set objFolderItems = objFolder.Items

            if (not objFolderItems Is Nothing) then
                document.write objFolderItems.Count
            end if

            set objFolderItem = nothing
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="4dd6a-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="4dd6a-120">Visual Basic:</span></span>


```VB
Private Sub btnFolderObjectItems_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItems As FolderItems

        Set objFolderItems = objFolder.Items()

        If (Not objFolderItems Is Nothing) Then
            Dim vCount As Variant

            vCount = objFolderItems.Count
        End If

        Set objFolderItems = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="4dd6a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="4dd6a-121">Requirements</span></span>



| <span data-ttu-id="4dd6a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="4dd6a-122">Requirement</span></span> | <span data-ttu-id="4dd6a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="4dd6a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dd6a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dd6a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="4dd6a-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4dd6a-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4dd6a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dd6a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="4dd6a-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4dd6a-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4dd6a-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4dd6a-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4dd6a-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4dd6a-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="4dd6a-130">IDL</span><span class="sxs-lookup"><span data-stu-id="4dd6a-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4dd6a-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4dd6a-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="4dd6a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="4dd6a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dd6a-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="4dd6a-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




