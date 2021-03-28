---
description: Выполняет указанную операцию с указанным файлом.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Метод IShellDispatch2. ShellExecute (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed5a8a2732f8ca358a0582d1da23aa7ffa7a98df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984672"
---
# <a name="ishelldispatch2shellexecute-method"></a><span data-ttu-id="51da2-103">IShellDispatch2. ShellExecute, метод</span><span class="sxs-lookup"><span data-stu-id="51da2-103">IShellDispatch2.ShellExecute method</span></span>

<span data-ttu-id="51da2-104">Выполняет указанную операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="51da2-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="51da2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51da2-105">Syntax</span></span>


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a><span data-ttu-id="51da2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51da2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51da2-107">*сфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="51da2-107">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51da2-108">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="51da2-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="51da2-109">**Строка** , содержащая имя файла, в котором **ShellExecute** будет выполнять действие, заданное параметром *воператион*.</span><span class="sxs-lookup"><span data-stu-id="51da2-109">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="51da2-110">*варгументс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="51da2-110">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51da2-111">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="51da2-111">Type: **Variant**</span></span>

<span data-ttu-id="51da2-112">Строка, содержащая значения параметров для операции.</span><span class="sxs-lookup"><span data-stu-id="51da2-112">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="51da2-113">*вдиректори* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="51da2-113">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51da2-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="51da2-114">Type: **Variant**</span></span>

<span data-ttu-id="51da2-115">Полный путь к каталогу, содержащему файл, указанный параметром *сфиле*.</span><span class="sxs-lookup"><span data-stu-id="51da2-115">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="51da2-116">Если этот параметр не указан, используется текущий рабочий каталог.</span><span class="sxs-lookup"><span data-stu-id="51da2-116">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="51da2-117">*воператион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="51da2-117">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51da2-118">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="51da2-118">Type: **Variant**</span></span>

<span data-ttu-id="51da2-119">Операция, которая выполняется.</span><span class="sxs-lookup"><span data-stu-id="51da2-119">The operation to be performed.</span></span> <span data-ttu-id="51da2-120">Это значение устанавливается равным одной из строк команд, поддерживаемых файлом.</span><span class="sxs-lookup"><span data-stu-id="51da2-120">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="51da2-121">Описание команд см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="51da2-121">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="51da2-122">Если этот параметр не указан, выполняется операция по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51da2-122">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="51da2-123">*вшов* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="51da2-123">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51da2-124">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="51da2-124">Type: **Variant**</span></span>

<span data-ttu-id="51da2-125">Рекомендации относительно того, как окно приложения должно отображаться изначально.</span><span class="sxs-lookup"><span data-stu-id="51da2-125">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="51da2-126">Приложение может игнорировать эту рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="51da2-126">The application can ignore this recommendation.</span></span> <span data-ttu-id="51da2-127">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="51da2-127">This parameter can be one of the following values.</span></span> <span data-ttu-id="51da2-128">Если этот параметр не указан, приложение использует значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51da2-128">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="51da2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="51da2-129">Value</span></span>                                                                                                                               | <span data-ttu-id="51da2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="51da2-130">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="51da2-131"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-131"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="51da2-132">Откройте приложение с помощью скрытого окна.</span><span class="sxs-lookup"><span data-stu-id="51da2-132">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="51da2-133"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-133"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="51da2-134">Откройте приложение в нормальном окне.</span><span class="sxs-lookup"><span data-stu-id="51da2-134">Open the application with a normal window.</span></span> <span data-ttu-id="51da2-135">Если окно является сведенным или развернутым, система восстанавливает его исходный размер и расположение.</span><span class="sxs-lookup"><span data-stu-id="51da2-135">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="51da2-136"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-136"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="51da2-137">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="51da2-137">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="51da2-138"><dt></dt><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-138"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="51da2-139">Откройте приложение с развернутым окном.</span><span class="sxs-lookup"><span data-stu-id="51da2-139">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="51da2-140"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-140"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="51da2-141">Откройте приложение со своим окном в последнем размере и позиции.</span><span class="sxs-lookup"><span data-stu-id="51da2-141">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="51da2-142">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="51da2-142">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="51da2-143"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-143"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="51da2-144">Откройте приложение с его текущим размером и положением в своем окне.</span><span class="sxs-lookup"><span data-stu-id="51da2-144">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="51da2-145"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-145"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="51da2-146">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="51da2-146">Open the application with a minimized window.</span></span> <span data-ttu-id="51da2-147">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="51da2-147">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="51da2-148"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-148"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="51da2-149">Откройте приложение со своим окном в состоянии по умолчанию, заданном приложением.</span><span class="sxs-lookup"><span data-stu-id="51da2-149">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51da2-150">Примечания</span><span class="sxs-lookup"><span data-stu-id="51da2-150">Remarks</span></span>

<span data-ttu-id="51da2-151">Этот метод реализован и доступен через метод [**Shell. ShellExecute**](./shell-shellexecute.md) .</span><span class="sxs-lookup"><span data-stu-id="51da2-151">This method is implemented and accessed through the [**Shell.ShellExecute**](./shell-shellexecute.md) method.</span></span>

<span data-ttu-id="51da2-152">Этот метод эквивалентен запуску одной из команд, связанных с контекстным меню файла.</span><span class="sxs-lookup"><span data-stu-id="51da2-152">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="51da2-153">Каждая команда представляется строкой команды.</span><span class="sxs-lookup"><span data-stu-id="51da2-153">Each command is represented by a verb string.</span></span> <span data-ttu-id="51da2-154">Набор поддерживаемых команд отличается от файла к файлу.</span><span class="sxs-lookup"><span data-stu-id="51da2-154">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="51da2-155">Наиболее часто поддерживаемая команда — "Open", которая также обычно является глаголом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51da2-155">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="51da2-156">Другие команды могут поддерживаться только определенными типами файлов.</span><span class="sxs-lookup"><span data-stu-id="51da2-156">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="51da2-157">Дополнительные сведения о командах оболочки см. в статье [Запуск приложений](launch.md) или [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="51da2-157">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="51da2-158">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="51da2-158">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="51da2-159">Примеры</span><span class="sxs-lookup"><span data-stu-id="51da2-159">Examples</span></span>

<span data-ttu-id="51da2-160">В следующих примерах показано использование **ShellExecute** для открытия блокнота.</span><span class="sxs-lookup"><span data-stu-id="51da2-160">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="51da2-161">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="51da2-161">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="51da2-162">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="51da2-162">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



<span data-ttu-id="51da2-163">Сценариев</span><span class="sxs-lookup"><span data-stu-id="51da2-163">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a><span data-ttu-id="51da2-164">Требования</span><span class="sxs-lookup"><span data-stu-id="51da2-164">Requirements</span></span>



| <span data-ttu-id="51da2-165">Требование</span><span class="sxs-lookup"><span data-stu-id="51da2-165">Requirement</span></span> | <span data-ttu-id="51da2-166">Значение</span><span class="sxs-lookup"><span data-stu-id="51da2-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51da2-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51da2-167">Minimum supported client</span></span><br/> | <span data-ttu-id="51da2-168">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="51da2-168">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="51da2-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51da2-169">Minimum supported server</span></span><br/> | <span data-ttu-id="51da2-170">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="51da2-170">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="51da2-171">Header</span><span class="sxs-lookup"><span data-stu-id="51da2-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="51da2-172"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-172"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="51da2-173">IDL</span><span class="sxs-lookup"><span data-stu-id="51da2-173">IDL</span></span><br/>                      | <dl> <span data-ttu-id="51da2-174"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-174"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="51da2-175">DLL</span><span class="sxs-lookup"><span data-stu-id="51da2-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51da2-176"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="51da2-176"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
