---
description: Метод Реадрекорд конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая считывает либо содержимое указанных записей, либо начальную часть одной записи простейшего файла.
ms.assetid: b00a3242-93bc-4779-8c62-89157fbcb5d1
title: 'Метод ISCardISO7816:: Реадрекорд (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 0cb9697315a6f9dd2436cd7a64d54fa6b44e00f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080752"
---
# <a name="iscardiso7816readrecord-method"></a><span data-ttu-id="3ac41-103">Метод ISCardISO7816:: Реадрекорд</span><span class="sxs-lookup"><span data-stu-id="3ac41-103">ISCardISO7816::ReadRecord method</span></span>

<span data-ttu-id="3ac41-104">\[Метод **реадрекорд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3ac41-104">\[The **ReadRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3ac41-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="3ac41-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3ac41-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3ac41-107">Метод **реадрекорд** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая считывает либо содержимое указанных записей, либо начальную часть одной записи простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="3ac41-107">The **ReadRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that reads either the contents of the specified records or the beginning part of one record of an elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ac41-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3ac41-108">Syntax</span></span>


```C++
HRESULT ReadRecord(
  [in]      BYTE       byRecordId,
  [in]      BYTE       byRefCtrl,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="3ac41-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ac41-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ac41-110">*бирекордид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-110">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac41-111">Номер записи или идентификатор первой записи для чтения (00 указывает текущую запись).</span><span class="sxs-lookup"><span data-stu-id="3ac41-111">Record number or ID of the first record to be read (00 indicates the current record).</span></span>

</dd> <dt>

<span data-ttu-id="3ac41-112">*бирефктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-112">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac41-113">Кодирование элемента управления ссылки.</span><span class="sxs-lookup"><span data-stu-id="3ac41-113">Coding of the reference control.</span></span>



| <span data-ttu-id="3ac41-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac41-114">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="3ac41-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac41-115">Meaning</span></span>                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="3ac41-116"><dt>**Текущая ссылка EF**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-116"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="3ac41-117">Битовое расположение: 00000---</span><span class="sxs-lookup"><span data-stu-id="3ac41-117">Bit position: 00000---</span></span><br/> <span data-ttu-id="3ac41-118">Текущее выбранное EF.</span><span class="sxs-lookup"><span data-stu-id="3ac41-118">Currently selected EF.</span></span><br/>                    |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="3ac41-119"><dt>**Краткий идентификатор EF**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-119"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="3ac41-120">Разрядное расположение: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="3ac41-120">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="3ac41-121">Короткий идентификатор EF.</span><span class="sxs-lookup"><span data-stu-id="3ac41-121">Short EF identifier.</span></span><br/>                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="3ac41-122"><dt>**рфу**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-122"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="3ac41-123">Битовое расположение: 11111---</span><span class="sxs-lookup"><span data-stu-id="3ac41-123">Bit position: 11111---</span></span><br/>                                                      |
| <span id="Record__"></span><span id="record__"></span><span id="RECORD__"></span><dl> <span data-ttu-id="3ac41-124"><dt>**Записать \#**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-124"><dt>**Record \#**</dt></span></span> </dl>            | <span data-ttu-id="3ac41-125">Битовое расположение:-----1XX</span><span class="sxs-lookup"><span data-stu-id="3ac41-125">Bit position: -----1xx</span></span><br/> <span data-ttu-id="3ac41-126">Использование номера записи в P1.</span><span class="sxs-lookup"><span data-stu-id="3ac41-126">Usage of record number in P1.</span></span><br/>             |
| <span id="Read_Record"></span><span id="read_record"></span><span id="READ_RECORD"></span><dl> <span data-ttu-id="3ac41-127"><dt>**Чтение записи**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-127"><dt>**Read Record**</dt></span></span> </dl> | <span data-ttu-id="3ac41-128">Битовое расположение:-----100</span><span class="sxs-lookup"><span data-stu-id="3ac41-128">Bit position: -----100</span></span><br/> <span data-ttu-id="3ac41-129">Чтение записи P1.</span><span class="sxs-lookup"><span data-stu-id="3ac41-129">Read record P1.</span></span><br/>                           |
| <span id="Up_to_Last"></span><span id="up_to_last"></span><span id="UP_TO_LAST"></span><dl> <span data-ttu-id="3ac41-130"><dt>**До последней**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-130"><dt>**Up to Last**</dt></span></span> </dl>     | <span data-ttu-id="3ac41-131">Битовое расположение:-----101</span><span class="sxs-lookup"><span data-stu-id="3ac41-131">Bit position: -----101</span></span><br/> <span data-ttu-id="3ac41-132">Чтение всех записей из P1 вплоть до последней.</span><span class="sxs-lookup"><span data-stu-id="3ac41-132">Read all records from P1 up to the last.</span></span> <br/> |
| <span id="Up_to_P1"></span><span id="up_to_p1"></span><span id="UP_TO_P1"></span><dl> <span data-ttu-id="3ac41-133"><dt>**До P1**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-133"><dt>**Up to P1**</dt></span></span> </dl>             | <span data-ttu-id="3ac41-134">Битовое расположение:-----110</span><span class="sxs-lookup"><span data-stu-id="3ac41-134">Bit position: -----110</span></span><br/> <span data-ttu-id="3ac41-135">Чтение всех записей из последней до P1.</span><span class="sxs-lookup"><span data-stu-id="3ac41-135">Read all records from the last up to P1.</span></span> <br/> |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="3ac41-136"><dt>**рфу**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-136"><dt>**RFU**</dt></span></span> </dl>                                                       | <span data-ttu-id="3ac41-137">Битовое расположение:-----111</span><span class="sxs-lookup"><span data-stu-id="3ac41-137">Bit position: -----111</span></span><br/>                                                      |
| <span id="Record_ID"></span><span id="record_id"></span><span id="RECORD_ID"></span><dl> <span data-ttu-id="3ac41-138"><dt>**Идентификатор записи**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-138"><dt>**Record ID**</dt></span></span> </dl>         | <span data-ttu-id="3ac41-139">Битовое расположение:-----0XX</span><span class="sxs-lookup"><span data-stu-id="3ac41-139">Bit position: -----0xx</span></span><br/> <span data-ttu-id="3ac41-140">Использование номера записи в P1.</span><span class="sxs-lookup"><span data-stu-id="3ac41-140">Usage of record number in P1.</span></span><br/>             |
| <span id="First_Occur"></span><span id="first_occur"></span><span id="FIRST_OCCUR"></span><dl> <span data-ttu-id="3ac41-141"><dt>**Первый появление**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-141"><dt>**First Occur**</dt></span></span> </dl> | <span data-ttu-id="3ac41-142">Битовое расположение:-----000</span><span class="sxs-lookup"><span data-stu-id="3ac41-142">Bit position: -----000</span></span><br/> <span data-ttu-id="3ac41-143">Чтение первого вхождения.</span><span class="sxs-lookup"><span data-stu-id="3ac41-143">Read first occurrence.</span></span> <br/>                   |
| <span id="Last_Occur"></span><span id="last_occur"></span><span id="LAST_OCCUR"></span><dl> <span data-ttu-id="3ac41-144"><dt>**Последняя ошибка**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-144"><dt>**Last Occur**</dt></span></span> </dl>     | <span data-ttu-id="3ac41-145">Битовое расположение:-----001</span><span class="sxs-lookup"><span data-stu-id="3ac41-145">Bit position: -----001</span></span><br/> <span data-ttu-id="3ac41-146">Прочитать последнее вхождение.</span><span class="sxs-lookup"><span data-stu-id="3ac41-146">Read last occurrence.</span></span> <br/>                    |
| <span id="Next_Occur"></span><span id="next_occur"></span><span id="NEXT_OCCUR"></span><dl> <span data-ttu-id="3ac41-147"><dt>**Следующая ситуация**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-147"><dt>**Next Occur**</dt></span></span> </dl>     | <span data-ttu-id="3ac41-148">Разрядное расположение:-----010</span><span class="sxs-lookup"><span data-stu-id="3ac41-148">Bit position: -----010</span></span><br/> <span data-ttu-id="3ac41-149">Прочитать следующее вхождение.</span><span class="sxs-lookup"><span data-stu-id="3ac41-149">Read next occurrence.</span></span> <br/>                    |
| <span id="Previous"></span><span id="previous"></span><span id="PREVIOUS"></span><dl> <span data-ttu-id="3ac41-150"><dt>**Назад**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-150"><dt>**Previous**</dt></span></span> </dl>             | <span data-ttu-id="3ac41-151">Битовое расположение:-----011</span><span class="sxs-lookup"><span data-stu-id="3ac41-151">Bit position: -----011</span></span><br/> <span data-ttu-id="3ac41-152">Прочитать предыдущее вхождение.</span><span class="sxs-lookup"><span data-stu-id="3ac41-152">Read previous occurrence.</span></span> <br/>                |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="3ac41-153"><dt>**Владел**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-153"><dt>**Secret**</dt></span></span> </dl>                     | <span data-ttu-id="3ac41-154">Разрядное расположение:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="3ac41-154">Bit position: ---xxxxx</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="3ac41-155">*лбитестореад* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-155">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac41-156">Число байтов для чтения из прозрачной EF.</span><span class="sxs-lookup"><span data-stu-id="3ac41-156">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="3ac41-157">Если поле Le содержит только нули, то в зависимости от b3b2b1 P2 и с ограничением в 256 для короткой длины или 65536 для расширенной длины команда должна читать либо единственную запрошенную запись, либо запрошенную последовательность записей.</span><span class="sxs-lookup"><span data-stu-id="3ac41-157">If the Le field contains only zeros, then depending on b3b2b1 of P2 and within the limit of 256 for short length or 65536 for extended length, the command should read completely either the single requested record or the requested sequence of records.</span></span>

</dd> <dt>

<span data-ttu-id="3ac41-158">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-158">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ac41-159">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3ac41-159">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="3ac41-160">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="3ac41-160">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="3ac41-161">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="3ac41-161">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ac41-162">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ac41-162">Return value</span></span>

<span data-ttu-id="3ac41-163">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="3ac41-163">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3ac41-164">Код возврата</span><span class="sxs-lookup"><span data-stu-id="3ac41-164">Return code</span></span>                                                                                   | <span data-ttu-id="3ac41-165">Описание</span><span class="sxs-lookup"><span data-stu-id="3ac41-165">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3ac41-166"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-166"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3ac41-167">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="3ac41-167">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3ac41-168"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-168"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3ac41-169">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="3ac41-169">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3ac41-170"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-170"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3ac41-171">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="3ac41-171">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3ac41-172"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-172"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3ac41-173">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="3ac41-173">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3ac41-174">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ac41-174">Remarks</span></span>

<span data-ttu-id="3ac41-175">Инкапсулированная команда может быть выполнена, только если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) удовлетворяет атрибутам безопасности простейшего считываемого файла.</span><span class="sxs-lookup"><span data-stu-id="3ac41-175">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span>

<span data-ttu-id="3ac41-176">Если в момент выполнения этой команды в настоящее время выбран другой простейший файл, он может быть обработан без идентификации текущего выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="3ac41-176">If another elementary file is currently selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="3ac41-177">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="3ac41-177">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="3ac41-178">Невозможно прочитать простейшие файлы без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="3ac41-178">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="3ac41-179">Инкапсулированная команда прерывается, если применяется к простейшему файлу без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="3ac41-179">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="3ac41-180">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="3ac41-180">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="3ac41-181">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="3ac41-181">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3ac41-182">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3ac41-182">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3ac41-183">Требования</span><span class="sxs-lookup"><span data-stu-id="3ac41-183">Requirements</span></span>



| <span data-ttu-id="3ac41-184">Требование</span><span class="sxs-lookup"><span data-stu-id="3ac41-184">Requirement</span></span> | <span data-ttu-id="3ac41-185">Значение</span><span class="sxs-lookup"><span data-stu-id="3ac41-185">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ac41-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ac41-186">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac41-187">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-187">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ac41-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ac41-188">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac41-189">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3ac41-189">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ac41-190">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3ac41-190">End of client support</span></span><br/>    | <span data-ttu-id="3ac41-191">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3ac41-191">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3ac41-192">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="3ac41-192">End of server support</span></span><br/>    | <span data-ttu-id="3ac41-193">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3ac41-193">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3ac41-194">Header</span><span class="sxs-lookup"><span data-stu-id="3ac41-194">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ac41-195"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-195"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ac41-196">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="3ac41-196">Type library</span></span><br/>             | <dl> <span data-ttu-id="3ac41-197"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-197"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3ac41-198">DLL</span><span class="sxs-lookup"><span data-stu-id="3ac41-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ac41-199"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ac41-199"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ac41-200">IID</span><span class="sxs-lookup"><span data-stu-id="3ac41-200">IID</span></span><br/>                      | <span data-ttu-id="3ac41-201">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="3ac41-201">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="3ac41-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ac41-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ac41-203">**аппендрекорд**</span><span class="sxs-lookup"><span data-stu-id="3ac41-203">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="3ac41-204">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="3ac41-204">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="3ac41-205">**упдатерекорд**</span><span class="sxs-lookup"><span data-stu-id="3ac41-205">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="3ac41-206">**вритерекорд**</span><span class="sxs-lookup"><span data-stu-id="3ac41-206">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
