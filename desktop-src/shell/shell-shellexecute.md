---
description: Shell. ShellExecute-метод выполняет указанную операцию с указанным файлом.
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
ms.openlocfilehash: 0fd31f0859fff5a1c94d5586f287e4a8980ddc02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104132"
---
# <a name="shellshellexecute-method"></a><span data-ttu-id="c7cfa-103">Shell. ShellExecute, метод</span><span class="sxs-lookup"><span data-stu-id="c7cfa-103">Shell.ShellExecute method</span></span>

<span data-ttu-id="c7cfa-104">Выполняет указанную операцию с указанным файлом.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-104">Performs a specified operation on a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7cfa-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7cfa-105">Syntax</span></span>

<span data-ttu-id="c7cfa-106">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c7cfa-106">JScript:</span></span>

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

<span data-ttu-id="c7cfa-107">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c7cfa-107">VBScript:</span></span>

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

<span data-ttu-id="c7cfa-108">VB:</span><span class="sxs-lookup"><span data-stu-id="c7cfa-108">VB:</span></span>

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a><span data-ttu-id="c7cfa-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7cfa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7cfa-110">*сфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-110">*sFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cfa-111">Тип: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="c7cfa-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="c7cfa-112">**Строка** , содержащая имя файла, в котором **ShellExecute** будет выполнять действие, заданное параметром *воператион*.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-112">A **String** that contains the name of the file on which **ShellExecute** will perform the action specified by *vOperation*.</span></span>

</dd> <dt>

<span data-ttu-id="c7cfa-113">*варгументс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-113">*vArguments* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cfa-114">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c7cfa-114">Type: **Variant**</span></span>

<span data-ttu-id="c7cfa-115">Строка, содержащая значения параметров для операции.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-115">A string that contains parameter values for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="c7cfa-116">*вдиректори* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-116">*vDirectory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cfa-117">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c7cfa-117">Type: **Variant**</span></span>

<span data-ttu-id="c7cfa-118">Полный путь к каталогу, содержащему файл, указанный параметром *сфиле*.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-118">The fully qualified path of the directory that contains the file specified by *sFile*.</span></span> <span data-ttu-id="c7cfa-119">Если этот параметр не указан, используется текущий рабочий каталог.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-119">If this parameter is not specified, the current working directory is used.</span></span>

</dd> <dt>

<span data-ttu-id="c7cfa-120">*воператион* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-120">*vOperation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cfa-121">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c7cfa-121">Type: **Variant**</span></span>

<span data-ttu-id="c7cfa-122">Операция, которая выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-122">The operation to be performed.</span></span> <span data-ttu-id="c7cfa-123">Это значение устанавливается равным одной из строк команд, поддерживаемых файлом.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-123">This value is set to one of the verb strings that is supported by the file.</span></span> <span data-ttu-id="c7cfa-124">Описание команд см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="c7cfa-124">For a discussion of verbs, see the Remarks section.</span></span> <span data-ttu-id="c7cfa-125">Если этот параметр не указан, выполняется операция по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-125">If this parameter is not specified, the default operation is performed.</span></span>

</dd> <dt>

<span data-ttu-id="c7cfa-126">*вшов* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-126">*vShow* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c7cfa-127">Тип: **Variant**</span><span class="sxs-lookup"><span data-stu-id="c7cfa-127">Type: **Variant**</span></span>

<span data-ttu-id="c7cfa-128">Рекомендации относительно того, как окно приложения должно отображаться изначально.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-128">A recommendation as to how the application window should be displayed initially.</span></span> <span data-ttu-id="c7cfa-129">Приложение может игнорировать эту рекомендацию.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-129">The application can ignore this recommendation.</span></span> <span data-ttu-id="c7cfa-130">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-130">This parameter can be one of the following values.</span></span> <span data-ttu-id="c7cfa-131">Если этот параметр не указан, приложение использует значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-131">If this parameter is not specified, the application uses its default value.</span></span>



| <span data-ttu-id="c7cfa-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c7cfa-132">Value</span></span>                                                                                                                               | <span data-ttu-id="c7cfa-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c7cfa-133">Meaning</span></span>                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c7cfa-134"><dt></dt>значение <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-134"><dt></dt> <dt>0</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-135">Откройте приложение с помощью скрытого окна.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-135">Open the application with a hidden window.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="c7cfa-136"><dt></dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-136"><dt></dt> <dt>1</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-137">Откройте приложение в нормальном окне.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-137">Open the application with a normal window.</span></span> <span data-ttu-id="c7cfa-138">Если окно является сведенным или развернутым, система восстанавливает его исходный размер и расположение.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-138">If the window is minimized or maximized, the system restores it to its original size and position.</span></span><br/> |
| <dl> <span data-ttu-id="c7cfa-139"><dt></dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-139"><dt></dt> <dt>2</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-140">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-140">Open the application with a minimized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c7cfa-141"><dt></dt><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-141"><dt></dt> <dt>3</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-142">Откройте приложение с развернутым окном.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-142">Open the application with a maximized window.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="c7cfa-143"><dt></dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-143"><dt></dt> <dt>4</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-144">Откройте приложение со своим окном в последнем размере и позиции.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-144">Open the application with its window at its most recent size and position.</span></span> <span data-ttu-id="c7cfa-145">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-145">The active window remains active.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c7cfa-146"><dt></dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-146"><dt></dt> <dt>5</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-147">Откройте приложение с его текущим размером и положением в своем окне.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-147">Open the application with its window at its current size and position.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="c7cfa-148"><dt></dt><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-148"><dt></dt> <dt>7</dt></span></span> </dl>  | <span data-ttu-id="c7cfa-149">Откройте приложение с помощью сворачивания окна.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-149">Open the application with a minimized window.</span></span> <span data-ttu-id="c7cfa-150">Активное окно остается активным.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-150">The active window remains active.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="c7cfa-151"><dt></dt><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-151"><dt></dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="c7cfa-152">Откройте приложение со своим окном в состоянии по умолчанию, заданном приложением.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-152">Open the application with its window in the default state specified by the application.</span></span><br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7cfa-153">Remarks</span><span class="sxs-lookup"><span data-stu-id="c7cfa-153">Remarks</span></span>

<span data-ttu-id="c7cfa-154">Этот метод эквивалентен запуску одной из команд, связанных с контекстным меню файла.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-154">This method is equivalent to launching one of the commands associated with a file's shortcut menu.</span></span> <span data-ttu-id="c7cfa-155">Каждая команда представляется строкой команды.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-155">Each command is represented by a verb string.</span></span> <span data-ttu-id="c7cfa-156">Набор поддерживаемых команд отличается от файла к файлу.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-156">The set of supported verbs varies from file to file.</span></span> <span data-ttu-id="c7cfa-157">Наиболее часто поддерживаемая команда — "Open", которая также обычно является глаголом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-157">The most commonly supported verb is "open", which is also usually the default verb.</span></span> <span data-ttu-id="c7cfa-158">Другие команды могут поддерживаться только определенными типами файлов.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-158">Other verbs might be supported by only certain types of files.</span></span> <span data-ttu-id="c7cfa-159">Дополнительные сведения о командах оболочки см. в статье [Запуск приложений](launch.md) или [расширение контекстных меню](context.md).</span><span class="sxs-lookup"><span data-stu-id="c7cfa-159">For further discussion of Shell verbs, see [Launching Applications](launch.md) or [Extending Shortcut Menus](context.md).</span></span>

<span data-ttu-id="c7cfa-160">Этот метод в настоящее время недоступен в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-160">This method is not currently available in Microsoft Visual Basic.</span></span>

## <a name="examples"></a><span data-ttu-id="c7cfa-161">Примеры</span><span class="sxs-lookup"><span data-stu-id="c7cfa-161">Examples</span></span>

<span data-ttu-id="c7cfa-162">В следующих примерах показано использование **ShellExecute** для открытия блокнота.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-162">The following examples show the use of **ShellExecute** to open Notepad.</span></span> <span data-ttu-id="c7cfa-163">Для JScript и VBScript отображается использование.</span><span class="sxs-lookup"><span data-stu-id="c7cfa-163">Usage is shown for JScript and VBScript.</span></span>

<span data-ttu-id="c7cfa-164">Присутствовал</span><span class="sxs-lookup"><span data-stu-id="c7cfa-164">JScript:</span></span>


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

<span data-ttu-id="c7cfa-165">Сценариев</span><span class="sxs-lookup"><span data-stu-id="c7cfa-165">VBScript:</span></span>

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a><span data-ttu-id="c7cfa-166">Требования</span><span class="sxs-lookup"><span data-stu-id="c7cfa-166">Requirements</span></span>



| <span data-ttu-id="c7cfa-167">Требование</span><span class="sxs-lookup"><span data-stu-id="c7cfa-167">Requirement</span></span> | <span data-ttu-id="c7cfa-168">Значение</span><span class="sxs-lookup"><span data-stu-id="c7cfa-168">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7cfa-169">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7cfa-169">Minimum supported client</span></span><br/> | <span data-ttu-id="c7cfa-170">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-170">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7cfa-171">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7cfa-171">Minimum supported server</span></span><br/> | <span data-ttu-id="c7cfa-172">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7cfa-172">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c7cfa-173">Header</span><span class="sxs-lookup"><span data-stu-id="c7cfa-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7cfa-174"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-174"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c7cfa-175">IDL</span><span class="sxs-lookup"><span data-stu-id="c7cfa-175">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7cfa-176"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-176"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c7cfa-177">DLL</span><span class="sxs-lookup"><span data-stu-id="c7cfa-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7cfa-178"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="c7cfa-178"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
