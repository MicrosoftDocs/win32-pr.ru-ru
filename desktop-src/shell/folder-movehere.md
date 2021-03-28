---
description: Перемещает элемент или элементы в эту папку.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Метод Folder. Мовехере (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808033"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="ff1fe-103">Folder. Мовехере, метод</span><span class="sxs-lookup"><span data-stu-id="ff1fe-103">Folder.MoveHere method</span></span>

<span data-ttu-id="ff1fe-104">Перемещает элемент или элементы в эту папку.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff1fe-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff1fe-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="ff1fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff1fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1fe-107">*витем* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ff1fe-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff1fe-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ff1fe-108">Type: **Variant**</span></span>

<span data-ttu-id="ff1fe-109">Перемещаемый элемент или элементы.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-109">The item or items to move.</span></span> <span data-ttu-id="ff1fe-110">Это может быть строка, представляющая имя файла, объект [**FolderItem**](folderitem.md) или объект [**фолдеритемс**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="ff1fe-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="ff1fe-111">*воптионс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ff1fe-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ff1fe-112">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ff1fe-112">Type: **Variant**</span></span>

<span data-ttu-id="ff1fe-113">Параметры для операции перемещения.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-113">Options for the move operation.</span></span> <span data-ttu-id="ff1fe-114">Это значение может быть нулевым или иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="ff1fe-115">Эти значения основаны на флагах, определенных для использования с элементом **ффлагс** структуры C++ [**шфилеопструкт**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="ff1fe-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="ff1fe-116">Эти флаги не определены для Visual Basic, VBScript или JScript, поэтому их необходимо определить самостоятельно или использовать их числовые эквиваленты.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="ff1fe-117">(4)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-118">Не отображать диалоговое окно хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-119">(8)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-120">Если файл с таким именем уже существует, присвойте файлу новое имя в операции перемещения, копирования или переименования.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-121">(16)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-122">Ответьте "Да для всех" для любого отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-123">(64)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-124">По возможности сохраняйте сведения об отмене.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-125">(128)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-126">Выполнить операцию с файлами следует только в том случае, если указано имя файла с подстановочным знаком ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="ff1fe-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-127">(256)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-128">Отображает диалоговое окно хода выполнения, но не отображает имена файлов.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-129">(512)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-130">Не подтверждайте создание нового каталога, если для операции требуется создать один.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-132">Не отображать пользовательский интерфейс при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="ff1fe-134">Версия 4,71.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="ff1fe-135">Не копируйте атрибуты безопасности файла.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="ff1fe-137">Работают только в локальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-137">Only operate in the local directory.</span></span> <span data-ttu-id="ff1fe-138">Не работают рекурсивно в подкаталогах.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="ff1fe-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="ff1fe-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="ff1fe-140">Версия 5,0.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="ff1fe-141">Не переносите подключенные файлы как группу.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-141">Do not move connected files as a group.</span></span> <span data-ttu-id="ff1fe-142">Переместить только указанные файлы.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1fe-143">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff1fe-143">Return value</span></span>

<span data-ttu-id="ff1fe-144">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff1fe-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff1fe-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff1fe-146">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="ff1fe-147">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="ff1fe-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="ff1fe-148">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="ff1fe-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ff1fe-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff1fe-149">Examples</span></span>

<span data-ttu-id="ff1fe-150">В следующем примере **мовехере** используется для перемещения файла Temp.txt из корневого каталога диска c в папку c: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="ff1fe-151">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="ff1fe-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="ff1fe-152">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="ff1fe-152">JScript:</span></span>


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



<span data-ttu-id="ff1fe-153">Сценариев</span><span class="sxs-lookup"><span data-stu-id="ff1fe-153">VBScript:</span></span>


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="ff1fe-154">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="ff1fe-154">Visual Basic:</span></span>


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="ff1fe-155">Требования</span><span class="sxs-lookup"><span data-stu-id="ff1fe-155">Requirements</span></span>



| <span data-ttu-id="ff1fe-156">Требование</span><span class="sxs-lookup"><span data-stu-id="ff1fe-156">Requirement</span></span> | <span data-ttu-id="ff1fe-157">Значение</span><span class="sxs-lookup"><span data-stu-id="ff1fe-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff1fe-158">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff1fe-158">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1fe-159">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ff1fe-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ff1fe-160">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff1fe-160">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1fe-161">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff1fe-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ff1fe-162">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ff1fe-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff1fe-163"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff1fe-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ff1fe-164">IDL</span><span class="sxs-lookup"><span data-stu-id="ff1fe-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff1fe-165"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff1fe-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ff1fe-166">DLL</span><span class="sxs-lookup"><span data-stu-id="ff1fe-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff1fe-167"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ff1fe-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




