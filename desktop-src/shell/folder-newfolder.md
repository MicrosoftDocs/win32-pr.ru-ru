---
description: Создает новую папку.
ms.assetid: 7a552e5a-e9a3-4fcf-bc6b-17e8bc39af87
title: Метод Folder. NewFolder (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.NewFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 86784aa071be22cd16a06d9d4516970d2924079a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998459"
---
# <a name="foldernewfolder-method"></a><span data-ttu-id="458a5-103">Folder. NewFolder, метод</span><span class="sxs-lookup"><span data-stu-id="458a5-103">Folder.NewFolder method</span></span>

<span data-ttu-id="458a5-104">Создает новую папку.</span><span class="sxs-lookup"><span data-stu-id="458a5-104">Creates a new folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="458a5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="458a5-105">Syntax</span></span>


```JScript
Folder.NewFolder(
  bName,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="458a5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="458a5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="458a5-107">*бнаме*</span><span class="sxs-lookup"><span data-stu-id="458a5-107">*bName*</span></span> 
</dt> <dd>

<span data-ttu-id="458a5-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="458a5-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="458a5-109">Строка, указывающая имя новой папки.</span><span class="sxs-lookup"><span data-stu-id="458a5-109">A string that specifies the name of the new folder.</span></span>

</dd> <dt>

<span data-ttu-id="458a5-110">*воптионс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="458a5-110">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="458a5-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="458a5-111">Type: **Variant**</span></span>

<span data-ttu-id="458a5-112">В настоящее время это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="458a5-112">This value is not currently used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="458a5-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="458a5-113">Return value</span></span>

<span data-ttu-id="458a5-114">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="458a5-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="458a5-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="458a5-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="458a5-116">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="458a5-116">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="458a5-117">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="458a5-117">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="458a5-118">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="458a5-118">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="458a5-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="458a5-119">Examples</span></span>

<span data-ttu-id="458a5-120">В следующем примере используется **NewFolder** для создания новой папки C: \\ testFolder.</span><span class="sxs-lookup"><span data-stu-id="458a5-120">The following example uses **NewFolder** to create the new folder C:\\TestFolder.</span></span> <span data-ttu-id="458a5-121">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="458a5-121">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="458a5-122">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="458a5-122">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderObjectNewFolderJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\");
        if (objFolder != null)
        {
            objFolder.NewFolder("TestFolder");
        }
    }
</script>
```



<span data-ttu-id="458a5-123">Сценариев</span><span class="sxs-lookup"><span data-stu-id="458a5-123">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderObjectNewFolderVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            objFolder.NewFolder("TestFolder")
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="458a5-124">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="458a5-124">Visual Basic:</span></span>


```VB
Private Sub btnNewFolder_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\")

    If (Not objFolder Is Nothing) Then
        objFolder.NewFolder ("TestFolder")
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="458a5-125">Требования</span><span class="sxs-lookup"><span data-stu-id="458a5-125">Requirements</span></span>



| <span data-ttu-id="458a5-126">Требование</span><span class="sxs-lookup"><span data-stu-id="458a5-126">Requirement</span></span> | <span data-ttu-id="458a5-127">Значение</span><span class="sxs-lookup"><span data-stu-id="458a5-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="458a5-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="458a5-128">Minimum supported client</span></span><br/> | <span data-ttu-id="458a5-129">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="458a5-129">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="458a5-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="458a5-130">Minimum supported server</span></span><br/> | <span data-ttu-id="458a5-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="458a5-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="458a5-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="458a5-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="458a5-133"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="458a5-133"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="458a5-134">IDL</span><span class="sxs-lookup"><span data-stu-id="458a5-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="458a5-135"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="458a5-135"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="458a5-136">DLL</span><span class="sxs-lookup"><span data-stu-id="458a5-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="458a5-137"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="458a5-137"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
