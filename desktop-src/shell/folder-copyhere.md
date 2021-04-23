---
description: Копирует элемент или элементы в папку.
title: Метод Folder. Копихере (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997735"
---
# <a name="foldercopyhere-method"></a><span data-ttu-id="66d7c-103">Folder. Копихере, метод</span><span class="sxs-lookup"><span data-stu-id="66d7c-103">Folder.CopyHere method</span></span>

<span data-ttu-id="66d7c-104">Копирует элемент или элементы в папку.</span><span class="sxs-lookup"><span data-stu-id="66d7c-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d7c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66d7c-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="66d7c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="66d7c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66d7c-107">*витем*</span><span class="sxs-lookup"><span data-stu-id="66d7c-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="66d7c-108">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="66d7c-108">Type: **Variant**</span></span>

<span data-ttu-id="66d7c-109">Копируемый элемент или элементы.</span><span class="sxs-lookup"><span data-stu-id="66d7c-109">The item or items to copy.</span></span> <span data-ttu-id="66d7c-110">Это может быть строка, представляющая имя файла, объект [**FolderItem**](folderitem.md) или объект [**фолдеритемс**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="66d7c-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="66d7c-111">*воптионс* \[ используемых\]</span><span class="sxs-lookup"><span data-stu-id="66d7c-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66d7c-112">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="66d7c-112">Type: **Variant**</span></span>

<span data-ttu-id="66d7c-113">Параметры для операции копирования.</span><span class="sxs-lookup"><span data-stu-id="66d7c-113">Options for the copy operation.</span></span> <span data-ttu-id="66d7c-114">Это значение может быть нулевым или иметь сочетание следующих значений.</span><span class="sxs-lookup"><span data-stu-id="66d7c-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="66d7c-115">Эти значения основаны на флагах, определенных для использования с элементом **ффлагс** структуры C++ [**шфилеопструкт**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="66d7c-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="66d7c-116">Каждое пространство имен оболочки должно предоставлять собственную реализацию этих флагов, и каждое пространство имен может игнорировать некоторые или даже все эти флаги.</span><span class="sxs-lookup"><span data-stu-id="66d7c-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="66d7c-117">Эти флаги не определяются по имени для Visual Basic, VBScript или JScript, поэтому их необходимо определить самостоятельно или использовать их числовые эквиваленты.</span><span class="sxs-lookup"><span data-stu-id="66d7c-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="66d7c-118">В некоторых случаях, например сжатых ZIP-файлах, некоторые флаги параметров могут игнорироваться конструкцией.</span><span class="sxs-lookup"><span data-stu-id="66d7c-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="66d7c-119">(4)</span><span class="sxs-lookup"><span data-stu-id="66d7c-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-120">Не отображать диалоговое окно хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="66d7c-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-121">(8)</span><span class="sxs-lookup"><span data-stu-id="66d7c-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-122">Если файл с таким именем уже существует, присвойте файлу новое имя в операции перемещения, копирования или переименования.</span><span class="sxs-lookup"><span data-stu-id="66d7c-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-123">(16)</span><span class="sxs-lookup"><span data-stu-id="66d7c-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-124">Ответьте "Да для всех" для любого отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="66d7c-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-125">(64)</span><span class="sxs-lookup"><span data-stu-id="66d7c-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-126">По возможности сохраняйте сведения об отмене.</span><span class="sxs-lookup"><span data-stu-id="66d7c-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-127">(128)</span><span class="sxs-lookup"><span data-stu-id="66d7c-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-128">Выполнить операцию с файлами следует только в том случае, если указано имя файла с подстановочным знаком ( \* . \* ).</span><span class="sxs-lookup"><span data-stu-id="66d7c-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-129">(256)</span><span class="sxs-lookup"><span data-stu-id="66d7c-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-130">Отображает диалоговое окно хода выполнения, но не отображает имена файлов.</span><span class="sxs-lookup"><span data-stu-id="66d7c-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-131">(512)</span><span class="sxs-lookup"><span data-stu-id="66d7c-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-132">Не подтверждайте создание нового каталога, если для операции требуется создать один.</span><span class="sxs-lookup"><span data-stu-id="66d7c-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="66d7c-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-134">Не отображать пользовательский интерфейс при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="66d7c-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="66d7c-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="66d7c-136">Версия 4,71.</span><span class="sxs-lookup"><span data-stu-id="66d7c-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="66d7c-137">Не копируйте атрибуты безопасности файла.</span><span class="sxs-lookup"><span data-stu-id="66d7c-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="66d7c-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="66d7c-139">Работают только в локальном каталоге.</span><span class="sxs-lookup"><span data-stu-id="66d7c-139">Only operate in the local directory.</span></span> <span data-ttu-id="66d7c-140">Не работают рекурсивно в подкаталогах.</span><span class="sxs-lookup"><span data-stu-id="66d7c-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="66d7c-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="66d7c-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="66d7c-142">Версия 5,0.</span><span class="sxs-lookup"><span data-stu-id="66d7c-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="66d7c-143">Не копируйте подключенные файлы в группу.</span><span class="sxs-lookup"><span data-stu-id="66d7c-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="66d7c-144">Копировать только указанные файлы.</span><span class="sxs-lookup"><span data-stu-id="66d7c-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66d7c-145">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66d7c-145">Return value</span></span>

<span data-ttu-id="66d7c-146">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="66d7c-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66d7c-147">Примечания</span><span class="sxs-lookup"><span data-stu-id="66d7c-147">Remarks</span></span>

<span data-ttu-id="66d7c-148">В вызывающей программе не выдается уведомление о том, что копирование завершено.</span><span class="sxs-lookup"><span data-stu-id="66d7c-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="66d7c-149">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="66d7c-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="66d7c-150">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="66d7c-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="66d7c-151">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="66d7c-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="66d7c-152">Примеры</span><span class="sxs-lookup"><span data-stu-id="66d7c-152">Examples</span></span>

<span data-ttu-id="66d7c-153">В следующем примере используется **копихере** для копирования файла Autoexec.bat из корневого каталога в каталог C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="66d7c-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="66d7c-154">Правильное использование показано в JScript, VBScript и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="66d7c-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="66d7c-155">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="66d7c-155">JScript:</span></span>


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



<span data-ttu-id="66d7c-156">Сценариев</span><span class="sxs-lookup"><span data-stu-id="66d7c-156">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



<span data-ttu-id="66d7c-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="66d7c-157">Visual Basic:</span></span>


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="66d7c-158">Требования</span><span class="sxs-lookup"><span data-stu-id="66d7c-158">Requirements</span></span>



| <span data-ttu-id="66d7c-159">Требование</span><span class="sxs-lookup"><span data-stu-id="66d7c-159">Requirement</span></span> | <span data-ttu-id="66d7c-160">Значение</span><span class="sxs-lookup"><span data-stu-id="66d7c-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d7c-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66d7c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="66d7c-162">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="66d7c-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="66d7c-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66d7c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="66d7c-164">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66d7c-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="66d7c-165">Заголовок</span><span class="sxs-lookup"><span data-stu-id="66d7c-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="66d7c-166"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d7c-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="66d7c-167">IDL</span><span class="sxs-lookup"><span data-stu-id="66d7c-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66d7c-168"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66d7c-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="66d7c-169">DLL</span><span class="sxs-lookup"><span data-stu-id="66d7c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66d7c-170"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="66d7c-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d7c-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66d7c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d7c-172">**Папка**</span><span class="sxs-lookup"><span data-stu-id="66d7c-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




