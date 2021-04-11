---
description: Метод Упдатерекорд конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая обновляет определенную запись с помощью битов, заданных в команде КАТЕГОРИЯХ APDU.
ms.assetid: 66039afd-5d73-41b3-b87b-b5d598c6f3db
title: 'Метод ISCardISO7816:: Упдатерекорд (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.UpdateRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bf810594e623d58944f58d3b7671664b3be175f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264691"
---
# <a name="iscardiso7816updaterecord-method"></a><span data-ttu-id="dc8b1-103">Метод ISCardISO7816:: Упдатерекорд</span><span class="sxs-lookup"><span data-stu-id="dc8b1-103">ISCardISO7816::UpdateRecord method</span></span>

<span data-ttu-id="dc8b1-104">\[Метод **упдатерекорд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-104">\[The **UpdateRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dc8b1-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dc8b1-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="dc8b1-107">Метод **упдатерекорд** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая обновляет определенную запись с помощью битов, заданных в команде категориях APDU.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-107">The **UpdateRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that updates a specific record with the bits given in the APDU command.</span></span>

> [!Note]  
> <span data-ttu-id="dc8b1-108">При использовании адресации текущей записи команда устанавливает указатель на запись об успешно обновленной записи.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-108">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="dc8b1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc8b1-109">Syntax</span></span>


```C++
HRESULT UpdateRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="dc8b1-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc8b1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc8b1-111">*бирекордид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-111">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8b1-112">Значение P1:</span><span class="sxs-lookup"><span data-stu-id="dc8b1-112">P1 value:</span></span>

<span data-ttu-id="dc8b1-113">P1 = 00 обозначает текущую запись</span><span class="sxs-lookup"><span data-stu-id="dc8b1-113">P1 = 00 designates the current record</span></span>

<span data-ttu-id="dc8b1-114">P1! = ' 00 ' — номер указанной записи</span><span class="sxs-lookup"><span data-stu-id="dc8b1-114">P1 != '00' is the number of the specified record</span></span>

</dd> <dt>

<span data-ttu-id="dc8b1-115">*бирефктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-115">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8b1-116">Программирование ссылочного элемента управления P2:</span><span class="sxs-lookup"><span data-stu-id="dc8b1-116">Coding of the reference control P2:</span></span>



| <span data-ttu-id="dc8b1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dc8b1-117">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="dc8b1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dc8b1-118">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="dc8b1-119"><dt>**Текущая ссылка EF**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-119"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="dc8b1-120">Битовое расположение: 00000---</span><span class="sxs-lookup"><span data-stu-id="dc8b1-120">Bit position: 00000---</span></span><br/> <span data-ttu-id="dc8b1-121">Текущее выбранное EF.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-121">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="dc8b1-122"><dt>**Краткий идентификатор EF**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-122"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="dc8b1-123">Разрядное расположение: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="dc8b1-123">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="dc8b1-124">Короткий идентификатор EF.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-124">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="dc8b1-125"><dt>**Первая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-125"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="dc8b1-126">Битовое расположение:-----000</span><span class="sxs-lookup"><span data-stu-id="dc8b1-126">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="dc8b1-127"><dt>**Последняя запись**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-127"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="dc8b1-128">Битовое расположение:-----001</span><span class="sxs-lookup"><span data-stu-id="dc8b1-128">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="dc8b1-129"><dt>**Следующая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-129"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="dc8b1-130">Разрядное расположение:-----010</span><span class="sxs-lookup"><span data-stu-id="dc8b1-130">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="dc8b1-131"><dt>**Предыдущая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-131"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="dc8b1-132">Битовое расположение:-----011</span><span class="sxs-lookup"><span data-stu-id="dc8b1-132">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="dc8b1-133"><dt>**Запись \# в P1**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-133"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="dc8b1-134">Битовое расположение:-----100</span><span class="sxs-lookup"><span data-stu-id="dc8b1-134">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="dc8b1-135">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-135">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8b1-136">Указатель на обновляемую запись.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-136">Pointer to the record to be updated.</span></span>

</dd> <dt>

<span data-ttu-id="dc8b1-137">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-137">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc8b1-138">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-138">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="dc8b1-139">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-139">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="dc8b1-140">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="dc8b1-140">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc8b1-141">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc8b1-141">Return value</span></span>

<span data-ttu-id="dc8b1-142">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-142">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="dc8b1-143">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc8b1-143">Return code</span></span>                                                                                   | <span data-ttu-id="dc8b1-144">Описание</span><span class="sxs-lookup"><span data-stu-id="dc8b1-144">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="dc8b1-145"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-145"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dc8b1-146">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="dc8b1-146">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="dc8b1-147"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-147"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dc8b1-148">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-148">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="dc8b1-149"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-149"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="dc8b1-150">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-150">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="dc8b1-151"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-151"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dc8b1-152">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-152">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="dc8b1-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc8b1-153">Remarks</span></span>

<span data-ttu-id="dc8b1-154">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-154">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="dc8b1-155">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-155">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="dc8b1-156">Если в момент выполнения этой команды в настоящее время выбран другой простейший файл, эта команда может быть обработана без определения текущего выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-156">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="dc8b1-157">Если созданная команда применяется к элементарному файлу с линейной или циклической структурой, он будет прерван, если длина записи отличается от длины существующей записи.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-157">If the constructed command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="dc8b1-158">Если команда применяется к структурированному элементарному файлу с линейной переменной, она может быть выполнена, если длина записи отличается от длины существующей записи.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-158">If the command applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="dc8b1-159">Параметр "Previous" команды (P2 = xxxxx011), применяемый к циклу файла, имеет то же поведение, что и команда, созданная с помощью [**аппендрекорд**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="dc8b1-159">The "previous" option of the command (P2=xxxxx011), applied to a cyclic file, has the same behavior as a command constructed by [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="dc8b1-160">Невозможно прочитать простейшие файлы без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-160">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="dc8b1-161">Созданная команда прерывает работу при применении к простейшему файлу без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-161">The constructed command aborts if applied to an elementary file without record structure.</span></span>

<span data-ttu-id="dc8b1-162">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="dc8b1-162">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="dc8b1-163">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="dc8b1-163">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="dc8b1-164">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="dc8b1-164">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dc8b1-165">Требования</span><span class="sxs-lookup"><span data-stu-id="dc8b1-165">Requirements</span></span>



| <span data-ttu-id="dc8b1-166">Требование</span><span class="sxs-lookup"><span data-stu-id="dc8b1-166">Requirement</span></span> | <span data-ttu-id="dc8b1-167">Значение</span><span class="sxs-lookup"><span data-stu-id="dc8b1-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc8b1-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc8b1-168">Minimum supported client</span></span><br/> | <span data-ttu-id="dc8b1-169">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-169">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="dc8b1-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc8b1-170">Minimum supported server</span></span><br/> | <span data-ttu-id="dc8b1-171">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="dc8b1-171">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dc8b1-172">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="dc8b1-172">End of client support</span></span><br/>    | <span data-ttu-id="dc8b1-173">Windows XP</span><span class="sxs-lookup"><span data-stu-id="dc8b1-173">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="dc8b1-174">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="dc8b1-174">End of server support</span></span><br/>    | <span data-ttu-id="dc8b1-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="dc8b1-175">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="dc8b1-176">Header</span><span class="sxs-lookup"><span data-stu-id="dc8b1-176">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc8b1-177"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-177"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc8b1-178">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dc8b1-178">Type library</span></span><br/>             | <dl> <span data-ttu-id="dc8b1-179"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-179"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="dc8b1-180">DLL</span><span class="sxs-lookup"><span data-stu-id="dc8b1-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc8b1-181"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc8b1-181"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dc8b1-182">IID</span><span class="sxs-lookup"><span data-stu-id="dc8b1-182">IID</span></span><br/>                      | <span data-ttu-id="dc8b1-183">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="dc8b1-183">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="dc8b1-184">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc8b1-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc8b1-185">**аппендрекорд**</span><span class="sxs-lookup"><span data-stu-id="dc8b1-185">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="dc8b1-186">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="dc8b1-186">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="dc8b1-187">**реадрекорд**</span><span class="sxs-lookup"><span data-stu-id="dc8b1-187">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="dc8b1-188">**вритерекорд**</span><span class="sxs-lookup"><span data-stu-id="dc8b1-188">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
