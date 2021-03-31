---
description: Создает и возвращает объект Folder для указанной папки.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Метод Shell. NameSpace (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 856a86efb4aca6ae7c1d4c8a3a81b5bc722a3963
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264544"
---
# <a name="shellnamespace-method"></a><span data-ttu-id="bef3d-103">Метод Shell. NameSpace</span><span class="sxs-lookup"><span data-stu-id="bef3d-103">Shell.NameSpace method</span></span>

<span data-ttu-id="bef3d-104">Создает и возвращает объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="bef3d-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="bef3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bef3d-105">Syntax</span></span>


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="bef3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bef3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef3d-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bef3d-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bef3d-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="bef3d-108">Type: **Variant**</span></span>

<span data-ttu-id="bef3d-109">Папка, для которой создается объект [**папки**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="bef3d-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="bef3d-110">Это может быть строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="bef3d-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="bef3d-111">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="bef3d-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="bef3d-112">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="bef3d-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef3d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bef3d-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="bef3d-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="bef3d-114">JScript</span></span>

<span data-ttu-id="bef3d-115">Тип: **[ **Папка**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bef3d-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="bef3d-116">Ссылка на объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="bef3d-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="bef3d-117">Если папка не была создана, это значение возвращает значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bef3d-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="bef3d-118">VB</span><span class="sxs-lookup"><span data-stu-id="bef3d-118">VB</span></span>

<span data-ttu-id="bef3d-119">Тип: **[ **Папка**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bef3d-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="bef3d-120">Ссылка на объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="bef3d-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="bef3d-121">Если папка не была создана, это значение возвращает значение **null**.</span><span class="sxs-lookup"><span data-stu-id="bef3d-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="examples"></a><span data-ttu-id="bef3d-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="bef3d-122">Examples</span></span>

<span data-ttu-id="bef3d-123">В следующем примере показано используемое **пространство имен** .</span><span class="sxs-lookup"><span data-stu-id="bef3d-123">The following example shows **NameSpace** in use.</span></span> <span data-ttu-id="bef3d-124">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="bef3d-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="bef3d-125">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="bef3d-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



<span data-ttu-id="bef3d-126">Сценариев</span><span class="sxs-lookup"><span data-stu-id="bef3d-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="bef3d-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="bef3d-127">Visual Basic:</span></span>


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="bef3d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="bef3d-128">Requirements</span></span>



| <span data-ttu-id="bef3d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="bef3d-129">Requirement</span></span> | <span data-ttu-id="bef3d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="bef3d-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bef3d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bef3d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="bef3d-132">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bef3d-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bef3d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bef3d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="bef3d-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="bef3d-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bef3d-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="bef3d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="bef3d-136"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bef3d-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="bef3d-137">IDL</span><span class="sxs-lookup"><span data-stu-id="bef3d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bef3d-138"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bef3d-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="bef3d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="bef3d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef3d-140"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="bef3d-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




