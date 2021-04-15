---
description: Выполняет указанную операцию с указанным файлом.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Метод Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985604"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="17766-103">Shell. ShellExecute, метод</span><span class="sxs-lookup"><span data-stu-id="17766-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="17766-104">Выполняет указанную операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="17766-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="17766-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17766-105">Syntax</span></span>

<span data-ttu-id="17766-106">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="17766-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="17766-107">Сценариев</span><span class="sxs-lookup"><span data-stu-id="17766-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="17766-108">VB:</span><span class="sxs-lookup"><span data-stu-id="17766-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="17766-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="17766-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17766-110">*сфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17766-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17766-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="17766-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="17766-112">**Строка** , содержащая имя файла, в котором **ShellExecute** будет выполнять действие, заданное параметром *воператион*.</span><span class="sxs-lookup"><span data-stu-id="17766-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="17766-113">*варгументс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="17766-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17766-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17766-114">Type: **Variant**</span></span>

<span data-ttu-id="17766-115">Строка, содержащая значения параметров для операции.</span><span class="sxs-lookup"><span data-stu-id="17766-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="17766-116">*вдиректори* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="17766-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17766-117">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17766-117">Type: **Variant**</span></span>

<span data-ttu-id="17766-118">Полный путь к каталогу, содержащему файл, указанный параметром *сфиле*.</span><span class="sxs-lookup"><span data-stu-id="17766-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="17766-119">Если этот параметр не указан, используется текущий рабочий каталог.</span><span class="sxs-lookup"><span data-stu-id="17766-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="17766-120">*воператион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="17766-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17766-121">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17766-121">Type: **Variant**</span></span>

<span data-ttu-id="17766-122">Операция, которая выполняется.</span><span class="sxs-lookup"><span data-stu-id="17766-122">The operation to be performed.</span></span> <span data-ttu-id="17766-123">Это значение устанавливается равным одной из строк команд, поддерживаемых файлом.</span><span class="sxs-lookup"><span data-stu-id="17766-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="17766-124">Описание команд см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="17766-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="17766-125">Если этот параметр не указан, выполняется операция по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17766-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="17766-126">*вшов* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="17766-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17766-127">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="17766-127">Type: **Variant**</span></span>

<span data-ttu-id="17766-128">Рекомендации относительно того, как окно приложения должно отображаться изначально.</span><span class="sxs-lookup"><span data-stu-id="17766-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="17766-129">Приложение может игнорировать эту рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="17766-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="17766-130">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="17766-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="17766-131">Если этот параметр не указан, приложение использует значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17766-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="17766-132">Значение</span><span class="sxs-lookup"><span data-stu-id="17766-132">Value</span></span>                                                                                                                               | <span data-ttu-id="17766-133">Значение</span><span class="sxs-lookup"><span data-stu-id="17766-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="17766-134"><dt></dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="17766-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="17766-135">Откройте приложение с помощью скрытого окна.</span><span class="sxs-lookup"><span data-stu-id="17766-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="17766-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="17766-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="17766-137">Откройте приложение в нормальном окне.</span><span class="sxs-lookup"><span data-stu-id="17766-137">Open the application with a normal window.</span></span> <span data-ttu-id="17766-138">Если окно является сведенным или развернутым, система восстанавливает его исходный размер и расположение.</span><span class="sxs-lookup"><span data-stu-id="17766-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="17766-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="17766-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="17766-140">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="17766-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="17766-141"><dt></dt><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="17766-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="17766-142">Откройте приложение с развернутым окном.</span><span class="sxs-lookup"><span data-stu-id="17766-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="17766-143"><dt></dt><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="17766-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="17766-144">Откройте приложение со своим окном в последнем размере и позиции.</span><span class="sxs-lookup"><span data-stu-id="17766-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="17766-145">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="17766-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="17766-146"><dt></dt><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="17766-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="17766-147">Откройте приложение с его текущим размером и положением в своем окне.</span><span class="sxs-lookup"><span data-stu-id="17766-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="17766-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="17766-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="17766-149">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="17766-149">Open the application with a minimized window.</span></span> <span data-ttu-id="17766-150">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="17766-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="17766-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="17766-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="17766-152">Откройте приложение со своим окном в состоянии по умолчанию, заданном приложением.</span><span class="sxs-lookup"><span data-stu-id="17766-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="17766-153">Примечания</span><span class="sxs-lookup"><span data-stu-id="17766-153">Remarks</span></span>

<span data-ttu-id="17766-154">Этот метод эквивалентен запуску одной из команд, связанных с контекстным меню файла.</span><span class="sxs-lookup"><span data-stu-id="17766-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="17766-155">Каждая команда представляется строкой команды.</span><span class="sxs-lookup"><span data-stu-id="17766-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="17766-156">Набор поддерживаемых команд отличается от файла к файлу.</span><span class="sxs-lookup"><span data-stu-id="17766-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="17766-157">Наиболее часто поддерживаемая команда — "Open", которая также обычно является глаголом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="17766-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="17766-158">Другие команды могут поддерживаться только определенными типами файлов.</span><span class="sxs-lookup"><span data-stu-id="17766-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="17766-159">Дополнительные сведения о командах оболочки см. в статье [Запуск приложений](launch.md) или [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="17766-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="17766-160">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="17766-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="17766-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="17766-161">Examples</span></span>

<span data-ttu-id="17766-162">В следующих примерах показано использование **ShellExecute** для открытия блокнота.</span><span class="sxs-lookup"><span data-stu-id="17766-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="17766-163">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="17766-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="17766-164">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="17766-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="17766-165">Сценариев</span><span class="sxs-lookup"><span data-stu-id="17766-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="17766-166">Требования</span><span class="sxs-lookup"><span data-stu-id="17766-166">Requirements</span></span>



| <span data-ttu-id="17766-167">Требование</span><span class="sxs-lookup"><span data-stu-id="17766-167">Requirement</span></span> | <span data-ttu-id="17766-168">Значение</span><span class="sxs-lookup"><span data-stu-id="17766-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17766-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17766-169">Minimum supported client</span></span><br/> | <span data-ttu-id="17766-170">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="17766-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="17766-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17766-171">Minimum supported server</span></span><br/> | <span data-ttu-id="17766-172">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="17766-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="17766-173">Header</span><span class="sxs-lookup"><span data-stu-id="17766-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="17766-174"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="17766-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="17766-175">IDL</span><span class="sxs-lookup"><span data-stu-id="17766-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="17766-176"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="17766-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="17766-177">DLL</span><span class="sxs-lookup"><span data-stu-id="17766-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17766-178"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="17766-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
