---
description: Метод Message объекта Session выполняет все включенные операции ведения журнала и откладывает выполнение объекта обработчика пользовательского интерфейса, связанного с ядром. Ведение журнала может быть выборочно включено для различных типов сообщений. См. метод EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652252"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="78161-105">Session. Message, метод</span><span class="sxs-lookup"><span data-stu-id="78161-105">Session.Message method</span></span>

<span data-ttu-id="78161-106">Метод **Message** объекта [**Session**](session-object.md) выполняет все включенные операции ведения журнала и откладывает выполнение объекта обработчика пользовательского интерфейса, связанного с ядром.</span><span class="sxs-lookup"><span data-stu-id="78161-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="78161-107">Ведение журнала может быть выборочно включено для различных типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="78161-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="78161-108">См. метод [**EnableLog**](installer-enablelog.md) .</span><span class="sxs-lookup"><span data-stu-id="78161-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="78161-109">Если поле записи 0 содержит строку форматирования, оно используется для форматирования данных в других полях.</span><span class="sxs-lookup"><span data-stu-id="78161-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="78161-110">Иначе, если сообщение является ошибкой, предупреждением или пользовательским сообщением, предпринимается попытка найти в таблице ошибок шаблон сообщения для текущей базы данных, используя номер ошибки, найденный в поле 1 записи для типов сообщений и возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="78161-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="78161-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78161-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="78161-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="78161-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78161-113">*особого*</span><span class="sxs-lookup"><span data-stu-id="78161-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="78161-114">Параметр *Kind* должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="78161-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="78161-115">Чтобы отобразить окно сообщения с кнопками и значками, Вычислите значение *типа* , добавив стандартные стили окна сообщения, используемые [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) и [**мессажебоксекс**](/windows/win32/api/winuser/nf-winuser-messageboxexa) , в **мсимессажетипиррор**, **мсимессажетипеварнинг** или **мсимессажетипеусер**.</span><span class="sxs-lookup"><span data-stu-id="78161-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="78161-116">Дополнительные сведения см. в разделе "Примечания" ниже.</span><span class="sxs-lookup"><span data-stu-id="78161-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="78161-117">Константа</span><span class="sxs-lookup"><span data-stu-id="78161-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="78161-118">Значение</span><span class="sxs-lookup"><span data-stu-id="78161-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="78161-119"><dt>**мсимессажетипефаталексит**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="78161-120">Преждевременное завершение, возможно, Неустранимая память.</span><span class="sxs-lookup"><span data-stu-id="78161-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="78161-121"><dt>**мсимессажетипиррор**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="78161-122">Форматированное сообщение об ошибке, \[ 1 \] — номер сообщения в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="78161-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="78161-123"><dt>**мсимессажетипеварнинг**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="78161-124">Форматированное предупреждающее сообщение, \[ 1 \] — номер сообщения в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="78161-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="78161-125"><dt> **мсимессажетипеусер**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="78161-126">Сообщение запроса пользователя, \[ 1 \] — номер сообщения в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="78161-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="78161-127"><dt>**мсимессажетипеинфо**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="78161-128">Информативное сообщение для журнала, которое не должно отображаться.</span><span class="sxs-lookup"><span data-stu-id="78161-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="78161-129"><dt>**мсимессажетипефилесинусе**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="78161-130">Список используемых файлов, которые необходимо заменить.</span><span class="sxs-lookup"><span data-stu-id="78161-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="78161-131"><dt>**мсимессажетипересолвесаурце**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="78161-132">Запрос на определение допустимого исходного расположения.</span><span class="sxs-lookup"><span data-stu-id="78161-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="78161-133"><dt>**мсимессажетипеаутофдискспаце**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="78161-134">Недостаточно места для сообщения на диске.</span><span class="sxs-lookup"><span data-stu-id="78161-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="78161-135"><dt>**мсимессажетипеактионстарт**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="78161-136">Начало действия, \[ 1 \] имя действия, \[ 2 \] Описание, \[ 3 \] шаблона для сообщений актиондата.</span><span class="sxs-lookup"><span data-stu-id="78161-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="78161-137"><dt>**мсимессажетипеактиондата**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="78161-138">Данные действия.</span><span class="sxs-lookup"><span data-stu-id="78161-138">Action data.</span></span> <span data-ttu-id="78161-139">Поля записей соответствуют шаблону сообщения АКТИОНСТАРТ.</span><span class="sxs-lookup"><span data-stu-id="78161-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="78161-140"><dt>**мсимессажетипепрогресс**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="78161-141">Сведения о индикаторе выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-141">Progress bar information.</span></span> <span data-ttu-id="78161-142">См. Описание полей записи ниже.</span><span class="sxs-lookup"><span data-stu-id="78161-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="78161-143"><dt> **мсимессажетипекоммондата**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="78161-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="78161-144">Чтобы включить кнопку Cancel, установите \[ 1 \] – 2, а \[ 2 — \] 1.</span><span class="sxs-lookup"><span data-stu-id="78161-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="78161-145">Отключение кнопки "Отмена" с параметром \[ 1 \] на 2 и \[ 2 \] до 0</span><span class="sxs-lookup"><span data-stu-id="78161-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="78161-146">*record*</span><span class="sxs-lookup"><span data-stu-id="78161-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="78161-147">Обязательный объект [**Record**](record-object.md) , содержащий поле, относящееся к сообщению.</span><span class="sxs-lookup"><span data-stu-id="78161-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78161-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78161-148">Return value</span></span>



| <span data-ttu-id="78161-149">Константа</span><span class="sxs-lookup"><span data-stu-id="78161-149">Constant</span></span>                                                                                              | <span data-ttu-id="78161-150">Значение</span><span class="sxs-lookup"><span data-stu-id="78161-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="78161-151"><dt>**мсимессажестатусеррор**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="78161-152">-1</span><span class="sxs-lookup"><span data-stu-id="78161-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="78161-153"><dt>**мсимессажестатусноне**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="78161-154">0</span><span class="sxs-lookup"><span data-stu-id="78161-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="78161-155"><dt>**мсимессажестатусок**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="78161-156">1</span><span class="sxs-lookup"><span data-stu-id="78161-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="78161-157"><dt>**мсимессажестатусканцел**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="78161-158">2</span><span class="sxs-lookup"><span data-stu-id="78161-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="78161-159"><dt>**мсимессажестатусаборт**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="78161-160">3</span><span class="sxs-lookup"><span data-stu-id="78161-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="78161-161"><dt>**мсимессажестатусретри**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="78161-162">4</span><span class="sxs-lookup"><span data-stu-id="78161-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="78161-163"><dt>**мсимессажестатусигноре**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="78161-164">5</span><span class="sxs-lookup"><span data-stu-id="78161-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="78161-165"><dt>**мсимессажестатусес**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="78161-166">6</span><span class="sxs-lookup"><span data-stu-id="78161-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="78161-167"><dt>**мсимессажестатусно**</dt></span><span class="sxs-lookup"><span data-stu-id="78161-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="78161-168">7</span><span class="sxs-lookup"><span data-stu-id="78161-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="78161-169">Комментарии</span><span class="sxs-lookup"><span data-stu-id="78161-169">Remarks</span></span>

<span data-ttu-id="78161-170">**Поля записей сообщений**</span><span class="sxs-lookup"><span data-stu-id="78161-170">**Message Record Fields**</span></span>

<span data-ttu-id="78161-171">Ниже описаны определения полей записей, когда Мсимессажетипепрогресс передается как тип сообщений.</span><span class="sxs-lookup"><span data-stu-id="78161-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="78161-172">Поле 1 указывает тип сообщения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="78161-173">Значение других полей зависит от значения в этом поле.</span><span class="sxs-lookup"><span data-stu-id="78161-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="78161-174">Ниже приведены возможные значения, которые можно задать в поле 1.</span><span class="sxs-lookup"><span data-stu-id="78161-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="78161-175">Название сообщения</span><span class="sxs-lookup"><span data-stu-id="78161-175">Message name</span></span>     | <span data-ttu-id="78161-176">Значение</span><span class="sxs-lookup"><span data-stu-id="78161-176">Value</span></span> | <span data-ttu-id="78161-177">Описание поля 1</span><span class="sxs-lookup"><span data-stu-id="78161-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78161-178">мастерресет</span><span class="sxs-lookup"><span data-stu-id="78161-178">MasterReset</span></span>      | <span data-ttu-id="78161-179">0</span><span class="sxs-lookup"><span data-stu-id="78161-179">0</span></span>     | <span data-ttu-id="78161-180">Сбрасывает индикатор выполнения и устанавливает ожидаемое общее число тактов на полосе.</span><span class="sxs-lookup"><span data-stu-id="78161-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="78161-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="78161-181">ActionInfo</span></span>       | <span data-ttu-id="78161-182">1</span><span class="sxs-lookup"><span data-stu-id="78161-182">1</span></span>     | <span data-ttu-id="78161-183">Предоставляет сведения, связанные с сообщениями о ходе выполнения, которые должны быть отправлены текущим действием.</span><span class="sxs-lookup"><span data-stu-id="78161-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="78161-184">прогрессрепорт</span><span class="sxs-lookup"><span data-stu-id="78161-184">ProgressReport</span></span>   | <span data-ttu-id="78161-185">2</span><span class="sxs-lookup"><span data-stu-id="78161-185">2</span></span>     | <span data-ttu-id="78161-186">Увеличивает индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="78161-187">прогрессаддитион</span><span class="sxs-lookup"><span data-stu-id="78161-187">ProgressAddition</span></span> | <span data-ttu-id="78161-188">3</span><span class="sxs-lookup"><span data-stu-id="78161-188">3</span></span>     | <span data-ttu-id="78161-189">Позволяет действию (например, CustomAction) добавлять такты к ожидаемому общему количеству хода выполнения индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="78161-190">Значение поля 2 зависит от значения в поле 1, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="78161-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="78161-191">Значение поля 1</span><span class="sxs-lookup"><span data-stu-id="78161-191">Field 1 value</span></span> | <span data-ttu-id="78161-192">Описание поля 2</span><span class="sxs-lookup"><span data-stu-id="78161-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78161-193">0</span><span class="sxs-lookup"><span data-stu-id="78161-193">0</span></span>             | <span data-ttu-id="78161-194">Ожидаемое общее число тактов на индикаторе выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="78161-195">1</span><span class="sxs-lookup"><span data-stu-id="78161-195">1</span></span>             | <span data-ttu-id="78161-196">Число тактов, на которое перемещается индикатор выполнения для каждого сообщения Актиондата.</span><span class="sxs-lookup"><span data-stu-id="78161-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="78161-197">Это поле игнорируется, если поле 3 равно 0.</span><span class="sxs-lookup"><span data-stu-id="78161-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="78161-198">2</span><span class="sxs-lookup"><span data-stu-id="78161-198">2</span></span>             | <span data-ttu-id="78161-199">Число тактов, на которое переместился индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="78161-200">3</span><span class="sxs-lookup"><span data-stu-id="78161-200">3</span></span>             | <span data-ttu-id="78161-201">Число тактов, которое нужно добавить к общему ожидаемому прогрессу.</span><span class="sxs-lookup"><span data-stu-id="78161-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="78161-202">Значение поля 3 зависит от значения в поле 1, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="78161-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="78161-203">Значение поля 1</span><span class="sxs-lookup"><span data-stu-id="78161-203">Field 1 value</span></span> | <span data-ttu-id="78161-204">Значение поля 3</span><span class="sxs-lookup"><span data-stu-id="78161-204">Field 3 value</span></span> | <span data-ttu-id="78161-205">Описание поля 3</span><span class="sxs-lookup"><span data-stu-id="78161-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78161-206">0</span><span class="sxs-lookup"><span data-stu-id="78161-206">0</span></span>             | <span data-ttu-id="78161-207">0</span><span class="sxs-lookup"><span data-stu-id="78161-207">0</span></span>             | <span data-ttu-id="78161-208">Пересылка индикатора выполнения (слева направо)</span><span class="sxs-lookup"><span data-stu-id="78161-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="78161-209">1</span><span class="sxs-lookup"><span data-stu-id="78161-209">1</span></span>             | <span data-ttu-id="78161-210">Обратный индикатор выполнения (справа налево)</span><span class="sxs-lookup"><span data-stu-id="78161-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="78161-211">1</span><span class="sxs-lookup"><span data-stu-id="78161-211">1</span></span>             | <span data-ttu-id="78161-212">0</span><span class="sxs-lookup"><span data-stu-id="78161-212">0</span></span>             | <span data-ttu-id="78161-213">Текущее действие будет отсылать явные сообщения Прогрессрепорт.</span><span class="sxs-lookup"><span data-stu-id="78161-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="78161-214">1</span><span class="sxs-lookup"><span data-stu-id="78161-214">1</span></span>             | <span data-ttu-id="78161-215">Увеличение индикатора выполнения на число тактов, указанное в поле 2, каждый раз, когда отправляется сообщение Актиондата.</span><span class="sxs-lookup"><span data-stu-id="78161-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="78161-216">2</span><span class="sxs-lookup"><span data-stu-id="78161-216">2</span></span>             | <span data-ttu-id="78161-217">Не используется</span><span class="sxs-lookup"><span data-stu-id="78161-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="78161-218">3</span><span class="sxs-lookup"><span data-stu-id="78161-218">3</span></span>             | <span data-ttu-id="78161-219">Не используется</span><span class="sxs-lookup"><span data-stu-id="78161-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="78161-220">Значение поля 4 зависит от значения в поле 1, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="78161-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="78161-221">Значение поля 1</span><span class="sxs-lookup"><span data-stu-id="78161-221">Field 1 value</span></span> | <span data-ttu-id="78161-222">Значение поля 4</span><span class="sxs-lookup"><span data-stu-id="78161-222">Field 4 value</span></span> | <span data-ttu-id="78161-223">Описание поля 4</span><span class="sxs-lookup"><span data-stu-id="78161-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78161-224">0</span><span class="sxs-lookup"><span data-stu-id="78161-224">0</span></span>             | <span data-ttu-id="78161-225">0</span><span class="sxs-lookup"><span data-stu-id="78161-225">0</span></span>             | <span data-ttu-id="78161-226">Выполнение выполняется.</span><span class="sxs-lookup"><span data-stu-id="78161-226">Execution is in progress.</span></span> <span data-ttu-id="78161-227">В этом случае пользовательский интерфейс может вычислить и отобразить оставшееся время.</span><span class="sxs-lookup"><span data-stu-id="78161-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="78161-228">1</span><span class="sxs-lookup"><span data-stu-id="78161-228">1</span></span>             | <span data-ttu-id="78161-229">Создание скрипта выполнения.</span><span class="sxs-lookup"><span data-stu-id="78161-229">Creating the execution script.</span></span> <span data-ttu-id="78161-230">В этом случае пользовательский интерфейс может отобразить сообщение, в течение которого установщик завершит подготовку установки.</span><span class="sxs-lookup"><span data-stu-id="78161-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="78161-231">1</span><span class="sxs-lookup"><span data-stu-id="78161-231">1</span></span>             | <span data-ttu-id="78161-232">Не используется</span><span class="sxs-lookup"><span data-stu-id="78161-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="78161-233">2</span><span class="sxs-lookup"><span data-stu-id="78161-233">2</span></span>             | <span data-ttu-id="78161-234">Не используется</span><span class="sxs-lookup"><span data-stu-id="78161-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="78161-235">3</span><span class="sxs-lookup"><span data-stu-id="78161-235">3</span></span>             | <span data-ttu-id="78161-236">Не используется</span><span class="sxs-lookup"><span data-stu-id="78161-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="78161-237">**Отображение окон сообщений**</span><span class="sxs-lookup"><span data-stu-id="78161-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="78161-238">Чтобы отобразить окно сообщения с кнопками и значками, Вычислите значение *типа* , добавив стандартные стили окна сообщения, используемые **MessageBox** и **мессажебоксекс** , в **мсимессажетипиррор**, **мсимессажетипеварнинг** или **мситипеусер**.</span><span class="sxs-lookup"><span data-stu-id="78161-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="78161-239">Доступные параметры кнопки отправки для VBScript: Вбоконли (МБ \_ ОК), вбокканцел (МБ \_ окканцел), ВБАБОРТРЕТРИГНОРЕ (МБ \_ Абортретригноре), вбесноканцел (МБ \_ есноканцел), vbYesNo (МБ \_ ДАНЕТ) и vbRetryCancel (МБ \_ RETRYCANCEL).</span><span class="sxs-lookup"><span data-stu-id="78161-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="78161-240">Доступные варианты значков для VBScript: Вбкритикал (МБ \_ иконеррор), вбкуестион (МБ \_ иконкуестион), ВБЕКСКЛАМАТИОН (МБ \_ Иконварнинг) и вбинформатион (МБ \_ ICONINFORMATION).</span><span class="sxs-lookup"><span data-stu-id="78161-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="78161-241">Например, следующий вызов отправляет сообщение **мсимессажетипиррор** с помощью значка вбекскламатион и кнопок вбесно.</span><span class="sxs-lookup"><span data-stu-id="78161-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="78161-242">Если пользовательское действие вызывает метод **Message** , пользовательское действие должно уметь обрабатывать отмену пользователем и возвращать **мсидоактионстатусусерексит**.</span><span class="sxs-lookup"><span data-stu-id="78161-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="78161-243">Требования</span><span class="sxs-lookup"><span data-stu-id="78161-243">Requirements</span></span>



| <span data-ttu-id="78161-244">Требование</span><span class="sxs-lookup"><span data-stu-id="78161-244">Requirement</span></span> | <span data-ttu-id="78161-245">Значение</span><span class="sxs-lookup"><span data-stu-id="78161-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78161-246">Версия</span><span class="sxs-lookup"><span data-stu-id="78161-246">Version</span></span><br/> | <span data-ttu-id="78161-247">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="78161-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="78161-248">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="78161-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="78161-249">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="78161-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="78161-250">DLL</span><span class="sxs-lookup"><span data-stu-id="78161-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="78161-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78161-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="78161-252">IID</span><span class="sxs-lookup"><span data-stu-id="78161-252">IID</span></span><br/>     | <span data-ttu-id="78161-253">IID \_ ISession определяется как 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="78161-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
