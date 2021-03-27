---
description: Извлекает сведения об элементе в папке. Например, его размер, тип или время последнего изменения.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Метод Folder. Жетдетаилсоф (Шлобж \_ Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990830"
---
# <a name="foldergetdetailsof-method"></a><span data-ttu-id="c8391-104">Folder. Жетдетаилсоф, метод</span><span class="sxs-lookup"><span data-stu-id="c8391-104">Folder.GetDetailsOf method</span></span>

<span data-ttu-id="c8391-105">Извлекает сведения об элементе в папке.</span><span class="sxs-lookup"><span data-stu-id="c8391-105">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="c8391-106">Например, его размер, тип или время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="c8391-106">For example, its size, type, or the time of its last modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8391-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8391-107">Syntax</span></span>


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a><span data-ttu-id="c8391-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c8391-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8391-109">*витем*</span><span class="sxs-lookup"><span data-stu-id="c8391-109">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="c8391-110">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c8391-110">Type: **Variant**</span></span>

<span data-ttu-id="c8391-111">Элемент, для которого необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="c8391-111">The item for which to retrieve the information.</span></span> <span data-ttu-id="c8391-112">Это должен быть объект [**FolderItem**](folderitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c8391-112">This must be a [**FolderItem**](folderitem.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="c8391-113">*иколумн*</span><span class="sxs-lookup"><span data-stu-id="c8391-113">*iColumn*</span></span> 
</dt> <dd>

<span data-ttu-id="c8391-114">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="c8391-114">Type: **Integer**</span></span>

<span data-ttu-id="c8391-115">**Целочисленное** значение, указывающее извлекаемую информацию.</span><span class="sxs-lookup"><span data-stu-id="c8391-115">An **Integer** value that specifies the information to be retrieved.</span></span> <span data-ttu-id="c8391-116">Сведения, доступные для элемента, зависят от папки, в которой он отображается.</span><span class="sxs-lookup"><span data-stu-id="c8391-116">The information available for an item depends on the folder in which it is displayed.</span></span> <span data-ttu-id="c8391-117">Это значение соответствует номеру столбца, начинающегося с нуля, который отображается в представлении оболочки.</span><span class="sxs-lookup"><span data-stu-id="c8391-117">This value corresponds to the zero-based column number that is displayed in a Shell view.</span></span> <span data-ttu-id="c8391-118">Для элемента в файловой системе это может быть одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="c8391-118">For an item in the file system, this can be one of the following values:</span></span>

<dt>



 <span data-ttu-id="c8391-119"> (0)</span><span class="sxs-lookup"><span data-stu-id="c8391-119">(0)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-120">Возвращает имя элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-120">Retrieves the name of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="c8391-121">(1)</span><span class="sxs-lookup"><span data-stu-id="c8391-121">(1)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-122">Возвращает размер элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-122">Retrieves the size of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="c8391-123">(2)</span><span class="sxs-lookup"><span data-stu-id="c8391-123">(2)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-124">Возвращает тип элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-124">Retrieves the type of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="c8391-125">(3)</span><span class="sxs-lookup"><span data-stu-id="c8391-125">(3)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-126">Извлекает дату и время последнего изменения элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-126">Retrieves the date and time that the item was last modified.</span></span>

</dd> <dt>



 <span data-ttu-id="c8391-127">(4)</span><span class="sxs-lookup"><span data-stu-id="c8391-127">(4)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-128">Извлекает атрибуты элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-128">Retrieves the attributes of the item.</span></span>

</dd> <dt>



 <span data-ttu-id="c8391-129">(-1)</span><span class="sxs-lookup"><span data-stu-id="c8391-129">(-1)</span></span>


</dt> <dd>

<span data-ttu-id="c8391-130">Извлекает сведения о подсказке для элемента.</span><span class="sxs-lookup"><span data-stu-id="c8391-130">Retrieves the info tip information for the item.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8391-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c8391-131">Return value</span></span>

<span data-ttu-id="c8391-132">Тип: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="c8391-132">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="c8391-133">Строка, содержащая извлеченные сведения.</span><span class="sxs-lookup"><span data-stu-id="c8391-133">String containing the retrieved detail.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8391-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="c8391-134">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c8391-135">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="c8391-135">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="c8391-136">Например, метод [_ *PARSENAME* \*](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="c8391-136">For example, the [_ *ParseName*\*](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="c8391-137">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="c8391-137">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="c8391-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="c8391-138">Examples</span></span>

<span data-ttu-id="c8391-139">В следующем примере **жетдетаилсоф** используется для получения типа файла с именем Clock.avi.</span><span class="sxs-lookup"><span data-stu-id="c8391-139">The following example uses **GetDetailsOf** to retrieve the type of the file named Clock.avi.</span></span> <span data-ttu-id="c8391-140">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c8391-140">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="c8391-141">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c8391-141">JScript:</span></span>


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



<span data-ttu-id="c8391-142">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c8391-142">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="c8391-143">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="c8391-143">Visual Basic:</span></span>


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="c8391-144">Требования</span><span class="sxs-lookup"><span data-stu-id="c8391-144">Requirements</span></span>



| <span data-ttu-id="c8391-145">Требование</span><span class="sxs-lookup"><span data-stu-id="c8391-145">Requirement</span></span> | <span data-ttu-id="c8391-146">Значение</span><span class="sxs-lookup"><span data-stu-id="c8391-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8391-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8391-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c8391-148">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c8391-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c8391-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8391-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c8391-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c8391-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8391-151">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c8391-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8391-152"><dt>Шлобж \_ Core. h (включение шлдисп. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c8391-152"><dt>Shlobj\_core.h (include Shldisp.h)</dt></span></span> </dl>  |
| <span data-ttu-id="c8391-153">IDL</span><span class="sxs-lookup"><span data-stu-id="c8391-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8391-154"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8391-154"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c8391-155">DLL</span><span class="sxs-lookup"><span data-stu-id="c8391-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8391-156"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c8391-156"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
