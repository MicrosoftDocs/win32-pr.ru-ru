---
description: Создает и возвращает объект FolderItem, представляющий указанный элемент.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Метод Folder. ParseName (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808032"
---
# <a name="folderparsename-method"></a><span data-ttu-id="c6256-103">Folder. ParseName, метод</span><span class="sxs-lookup"><span data-stu-id="c6256-103">Folder.ParseName method</span></span>

<span data-ttu-id="c6256-104">Создает и возвращает объект [**FolderItem**](folderitem.md) , представляющий указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="c6256-104">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6256-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6256-105">Syntax</span></span>


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a><span data-ttu-id="c6256-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6256-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6256-107">*бнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6256-107">*bName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6256-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c6256-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c6256-109">Строка, указывающая имя элемента.</span><span class="sxs-lookup"><span data-stu-id="c6256-109">A string that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6256-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6256-110">Return value</span></span>

<span data-ttu-id="c6256-111">Тип: **[ **FolderItem**](folderitem.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="c6256-111">Type: **[**FolderItem**](folderitem.md)\*\***</span></span>

<span data-ttu-id="c6256-112">Ссылка на объект [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c6256-112">An object reference to the [**FolderItem**](folderitem.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6256-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="c6256-113">Remarks</span></span>

<span data-ttu-id="c6256-114">**PARSENAME** не следует использовать для таких виртуальных папок, как "Мои документы".</span><span class="sxs-lookup"><span data-stu-id="c6256-114">**ParseName** should not be used for virtual folders such as My Documents.</span></span>

## <a name="examples"></a><span data-ttu-id="c6256-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="c6256-115">Examples</span></span>

<span data-ttu-id="c6256-116">В следующем примере используется **PARSENAME** для создания объекта, представляющего элемент папки, Clock.avi в папке C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="c6256-116">The following example uses **ParseName** to create an object representing the folder item Clock.avi in the C:\\Windows folder.</span></span> <span data-ttu-id="c6256-117">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c6256-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c6256-118">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c6256-118">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



<span data-ttu-id="c6256-119">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c6256-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="c6256-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c6256-120">Visual Basic:</span></span>


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c6256-121">Требования</span><span class="sxs-lookup"><span data-stu-id="c6256-121">Requirements</span></span>



| <span data-ttu-id="c6256-122">Требование</span><span class="sxs-lookup"><span data-stu-id="c6256-122">Requirement</span></span> | <span data-ttu-id="c6256-123">Значение</span><span class="sxs-lookup"><span data-stu-id="c6256-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6256-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6256-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c6256-125">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c6256-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c6256-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6256-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c6256-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c6256-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c6256-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c6256-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6256-129"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6256-129"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c6256-130">IDL</span><span class="sxs-lookup"><span data-stu-id="c6256-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6256-131"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6256-131"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c6256-132">DLL</span><span class="sxs-lookup"><span data-stu-id="c6256-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6256-133"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c6256-133"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
