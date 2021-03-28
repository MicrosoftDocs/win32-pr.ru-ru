---
description: Создает и возвращает объект Folder для указанной папки.
ms.assetid: CEA73705-1C27-4138-86C4-1715016E2ED8
title: Метод Ишеллдиспатч. NameSpace (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 069752a5e81949889dce5539e3f23960a12c9736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543151"
---
# <a name="ishelldispatchnamespace-method"></a><span data-ttu-id="705ff-103">Ишеллдиспатч. NameSpace, метод</span><span class="sxs-lookup"><span data-stu-id="705ff-103">IShellDispatch.NameSpace method</span></span>

<span data-ttu-id="705ff-104">Создает и возвращает объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="705ff-104">Creates and returns a [**Folder**](folder.md) object for the specified folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="705ff-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="705ff-105">Syntax</span></span>


```JScript
retVal = IShellDispatch.NameSpace(
  vDir
)
```


```VB

IShellDispatch.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a><span data-ttu-id="705ff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="705ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="705ff-107">*vDir* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="705ff-107">*vDir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="705ff-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="705ff-108">Type: **Variant**</span></span>

<span data-ttu-id="705ff-109">Папка, для которой создается объект [**папки**](folder.md) .</span><span class="sxs-lookup"><span data-stu-id="705ff-109">The folder for which to create the [**Folder**](folder.md) object.</span></span> <span data-ttu-id="705ff-110">Это может быть строка, указывающая путь к папке или одно из значений [**шеллспеЦиалфолдерконстантс**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .</span><span class="sxs-lookup"><span data-stu-id="705ff-110">This can be a string that specifies the path of the folder or one of the [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) values.</span></span> <span data-ttu-id="705ff-111">Обратите внимание, что имена констант, найденные в **шеллспеЦиалфолдерконстантс** , доступны в Visual Basic, но не в VBScript или JScript.</span><span class="sxs-lookup"><span data-stu-id="705ff-111">Note that the constant names found in **ShellSpecialFolderConstants** are available in Visual Basic, but not in VBScript or JScript.</span></span> <span data-ttu-id="705ff-112">В таких случаях необходимо использовать числовые значения на своем месте.</span><span class="sxs-lookup"><span data-stu-id="705ff-112">In those cases, the numeric values must be used in their place.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="705ff-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="705ff-113">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="705ff-114">Язык JScript</span><span class="sxs-lookup"><span data-stu-id="705ff-114">JScript</span></span>

<span data-ttu-id="705ff-115">Тип: **[ **Папка**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="705ff-115">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="705ff-116">Ссылка на объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="705ff-116">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="705ff-117">Если папка не была создана, это значение возвращает значение **null**.</span><span class="sxs-lookup"><span data-stu-id="705ff-117">If the folder is not successfully created, this value returns **null**.</span></span>

### <a name="vb"></a><span data-ttu-id="705ff-118">VB</span><span class="sxs-lookup"><span data-stu-id="705ff-118">VB</span></span>

<span data-ttu-id="705ff-119">Тип: **[ **Папка**](folder.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="705ff-119">Type: **[**Folder**](folder.md)\*\***</span></span>

<span data-ttu-id="705ff-120">Ссылка на объект [**Folder**](folder.md) для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="705ff-120">Object reference to the [**Folder**](folder.md) object for the specified folder.</span></span> <span data-ttu-id="705ff-121">Если папка не была создана, это значение возвращает значение **null**.</span><span class="sxs-lookup"><span data-stu-id="705ff-121">If the folder is not successfully created, this value returns **null**.</span></span>

## <a name="remarks"></a><span data-ttu-id="705ff-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="705ff-122">Remarks</span></span>

<span data-ttu-id="705ff-123">Этот метод реализован и доступен через метод [**Shell. Namespace**](shell-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="705ff-123">This method is implemented and accessed through the [**Shell.NameSpace**](shell-namespace.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="705ff-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="705ff-124">Examples</span></span>

<span data-ttu-id="705ff-125">В следующих примерах показано использование [**пространства имен**](shell-namespace.md) в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="705ff-125">The following examples show the use of [**NameSpace**](shell-namespace.md) in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="705ff-126">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="705ff-126">JScript:</span></span>


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



<span data-ttu-id="705ff-127">Сценариев</span><span class="sxs-lookup"><span data-stu-id="705ff-127">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="705ff-128">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="705ff-128">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="705ff-129">Требования</span><span class="sxs-lookup"><span data-stu-id="705ff-129">Requirements</span></span>



| <span data-ttu-id="705ff-130">Требование</span><span class="sxs-lookup"><span data-stu-id="705ff-130">Requirement</span></span> | <span data-ttu-id="705ff-131">Значение</span><span class="sxs-lookup"><span data-stu-id="705ff-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="705ff-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="705ff-132">Minimum supported client</span></span><br/> | <span data-ttu-id="705ff-133">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="705ff-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="705ff-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="705ff-134">Minimum supported server</span></span><br/> | <span data-ttu-id="705ff-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="705ff-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="705ff-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="705ff-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="705ff-137"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="705ff-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="705ff-138">IDL</span><span class="sxs-lookup"><span data-stu-id="705ff-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="705ff-139"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="705ff-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="705ff-140">DLL</span><span class="sxs-lookup"><span data-stu-id="705ff-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="705ff-141"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="705ff-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




