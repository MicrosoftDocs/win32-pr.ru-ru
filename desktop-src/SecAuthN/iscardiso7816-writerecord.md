---
description: Конструирует команду КАТЕГОРИЯХ APDU, которая инициирует одну из перечисленных операций.
ms.assetid: 2ce313b9-ccd7-4be0-a91f-d0747e35fab8
title: 'Метод ISCardISO7816:: Вритерекорд (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 30bfdb9ff8779633d81da89bbf7ac8e69a617d04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143714"
---
# <a name="iscardiso7816writerecord-method"></a><span data-ttu-id="367a6-103">Метод ISCardISO7816:: Вритерекорд</span><span class="sxs-lookup"><span data-stu-id="367a6-103">ISCardISO7816::WriteRecord method</span></span>

<span data-ttu-id="367a6-104">\[Метод **вритерекорд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="367a6-104">\[The **WriteRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="367a6-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="367a6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="367a6-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="367a6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="367a6-107">Метод **вритерекорд** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая инициирует одну из следующих операций:</span><span class="sxs-lookup"><span data-stu-id="367a6-107">The **WriteRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates one of the following operations:</span></span>

-   <span data-ttu-id="367a6-108">Запись один раз для записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-108">The write once of a record.</span></span>
-   <span data-ttu-id="367a6-109">Логический **или** из байтов данных записи, уже присутствующей в карточке с байтами данных записи, указанной в команде категориях APDU.</span><span class="sxs-lookup"><span data-stu-id="367a6-109">The logical **OR** of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>
-   <span data-ttu-id="367a6-110">Логический и по байтам данных записи, уже присутствующим в карточке с байтами данных записи, указанной в команде КАТЕГОРИЯХ APDU.</span><span class="sxs-lookup"><span data-stu-id="367a6-110">The logical AND of the data bytes of a record already present in the card with the data bytes of the record given in the command APDU.</span></span>

<span data-ttu-id="367a6-111">Если в байте кода данных не указаны никакие указания, применяется логическое поведение или.</span><span class="sxs-lookup"><span data-stu-id="367a6-111">When no indication is given in the data coding byte, the logical OR behavior applies.</span></span>

> [!Note]  
> <span data-ttu-id="367a6-112">При использовании адресации текущей записи команда устанавливает указатель на запись об успешно обновленной записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-112">When using current record addressing, the command sets the record pointer on the successfully updated record.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="367a6-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="367a6-113">Syntax</span></span>


```C++
HRESULT WriteRecord(
  [in]      BYTE         byRecordId,
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="367a6-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="367a6-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="367a6-115">*бирекордид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="367a6-115">*byRecordId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367a6-116">Идентификация записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-116">Record identification.</span></span> <span data-ttu-id="367a6-117">Это значение P1:</span><span class="sxs-lookup"><span data-stu-id="367a6-117">This is the P1 value:</span></span>

<span data-ttu-id="367a6-118">P1 = ' 00 ' обозначает текущую запись.</span><span class="sxs-lookup"><span data-stu-id="367a6-118">P1 = '00' designates the current record.</span></span>

<span data-ttu-id="367a6-119">P1! = ' 00 ' — номер указанной записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-119">P1 != '00' is the number of the specified record.</span></span>

</dd> <dt>

<span data-ttu-id="367a6-120">*бирефктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="367a6-120">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367a6-121">Программирование ссылочного элемента управления P2.</span><span class="sxs-lookup"><span data-stu-id="367a6-121">Coding of the reference control P2.</span></span>



| <span data-ttu-id="367a6-122">Значение</span><span class="sxs-lookup"><span data-stu-id="367a6-122">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="367a6-123">Значение</span><span class="sxs-lookup"><span data-stu-id="367a6-123">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="367a6-124"><dt>**Текущая ссылка EF**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-124"><dt>**Current EF**</dt></span></span> </dl>                     | <span data-ttu-id="367a6-125">Битовое расположение: 00000---</span><span class="sxs-lookup"><span data-stu-id="367a6-125">Bit position: 00000---</span></span><br/> <span data-ttu-id="367a6-126">Текущее выбранное EF.</span><span class="sxs-lookup"><span data-stu-id="367a6-126">Currently selected EF.</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="367a6-127"><dt>**Краткий идентификатор EF**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-127"><dt>**Short EF ID**</dt></span></span> </dl>                 | <span data-ttu-id="367a6-128">Разрядное расположение: XXXXX---</span><span class="sxs-lookup"><span data-stu-id="367a6-128">Bit position: xxxxx---</span></span><br/> <span data-ttu-id="367a6-129">Короткий идентификатор EF.</span><span class="sxs-lookup"><span data-stu-id="367a6-129">Short EF identifier.</span></span><br/>   |
| <span id="First_Record"></span><span id="first_record"></span><span id="FIRST_RECORD"></span><dl> <span data-ttu-id="367a6-130"><dt>**Первая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-130"><dt>**First Record**</dt></span></span> </dl>             | <span data-ttu-id="367a6-131">Битовое расположение:-----000</span><span class="sxs-lookup"><span data-stu-id="367a6-131">Bit position: -----000</span></span><br/>                                   |
| <span id="Last_Record"></span><span id="last_record"></span><span id="LAST_RECORD"></span><dl> <span data-ttu-id="367a6-132"><dt>**Последняя запись**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-132"><dt>**Last Record**</dt></span></span> </dl>                 | <span data-ttu-id="367a6-133">Битовое расположение:-----001</span><span class="sxs-lookup"><span data-stu-id="367a6-133">Bit position: -----001</span></span><br/>                                   |
| <span id="Next_Record"></span><span id="next_record"></span><span id="NEXT_RECORD"></span><dl> <span data-ttu-id="367a6-134"><dt>**Следующая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-134"><dt>**Next Record**</dt></span></span> </dl>                 | <span data-ttu-id="367a6-135">Разрядное расположение:-----010</span><span class="sxs-lookup"><span data-stu-id="367a6-135">Bit position: -----010</span></span><br/>                                   |
| <span id="Previous_Record"></span><span id="previous_record"></span><span id="PREVIOUS_RECORD"></span><dl> <span data-ttu-id="367a6-136"><dt>**Предыдущая запись**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-136"><dt>**Previous Record**</dt></span></span> </dl> | <span data-ttu-id="367a6-137">Битовое расположение:-----011</span><span class="sxs-lookup"><span data-stu-id="367a6-137">Bit position: -----011</span></span><br/>                                   |
| <span id="Record___in_P1"></span><span id="record___in_p1"></span><span id="RECORD___IN_P1"></span><dl> <span data-ttu-id="367a6-138"><dt>**Запись \# в P1**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-138"><dt>**Record \# in P1**</dt></span></span> </dl>    | <span data-ttu-id="367a6-139">Битовое расположение:-----100</span><span class="sxs-lookup"><span data-stu-id="367a6-139">Bit position: -----100</span></span><br/>                                   |



 

</dd> <dt>

<span data-ttu-id="367a6-140">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="367a6-140">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="367a6-141">Указатель на запись, которую необходимо записать.</span><span class="sxs-lookup"><span data-stu-id="367a6-141">Pointer to the record to be written.</span></span>

</dd> <dt>

<span data-ttu-id="367a6-142">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="367a6-142">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="367a6-143">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="367a6-143">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="367a6-144">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="367a6-144">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="367a6-145">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается через указатель *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="367a6-145">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned via the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="367a6-146">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="367a6-146">Return value</span></span>

<span data-ttu-id="367a6-147">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="367a6-147">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="367a6-148">Код возврата</span><span class="sxs-lookup"><span data-stu-id="367a6-148">Return code</span></span>                                                                                   | <span data-ttu-id="367a6-149">Описание</span><span class="sxs-lookup"><span data-stu-id="367a6-149">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="367a6-150"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-150"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="367a6-151">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="367a6-151">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="367a6-152"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-152"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="367a6-153">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="367a6-153">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="367a6-154"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-154"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="367a6-155">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="367a6-155">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="367a6-156"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-156"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="367a6-157">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="367a6-157">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="367a6-158">Комментарии</span><span class="sxs-lookup"><span data-stu-id="367a6-158">Remarks</span></span>

<span data-ttu-id="367a6-159">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) соответствует атрибутам безопасности для обрабатываемого простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="367a6-159">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="367a6-160">Если команда содержит допустимый краткий простой идентификатор, она устанавливает файл в качестве текущего простейшего файла.</span><span class="sxs-lookup"><span data-stu-id="367a6-160">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span> <span data-ttu-id="367a6-161">Если в момент выполнения этой команды в настоящее время выбран другой простейший файл, эта команда может быть обработана без определения текущего выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="367a6-161">If another elementary file is currently selected at the time of issuing this command, this command may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="367a6-162">Если Инкапсулированная команда применяется к элементарному файлу с линейной или циклической структурой, он будет прерван, если длина записи отличается от длины существующей записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-162">If the encapsulated command applies to a linear-fixed or cyclic-structured elementary file, it will abort if the record length is different from the length of the existing record.</span></span> <span data-ttu-id="367a6-163">Если он применяется к структурированному элементарному файлу с линейной переменной, он может выполняться, если длина записи отличается от длины существующей записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-163">If it applies to a linear-variable structured elementary file, it may be carried out when the record length is different from the length of the existing record.</span></span>

<span data-ttu-id="367a6-164">Если P2 = xxxxx011 и простейший файл является циклической, эта команда имеет то же поведение, что и команда, созданная с помощью [**аппендрекорд**](iscardiso7816-appendrecord.md).</span><span class="sxs-lookup"><span data-stu-id="367a6-164">If P2=xxxxx011 and the elementary file is cyclic file, this command has the same behavior a command constructed using [**AppendRecord**](iscardiso7816-appendrecord.md).</span></span>

<span data-ttu-id="367a6-165">В невозможно записать простейшие файлы без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-165">Elementary files without a record structure cannot be written to.</span></span> <span data-ttu-id="367a6-166">Созданная команда прерывается при применении к простейшему файлу без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="367a6-166">The constructed command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="367a6-167">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="367a6-167">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="367a6-168">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="367a6-168">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="367a6-169">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="367a6-169">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="367a6-170">Требования</span><span class="sxs-lookup"><span data-stu-id="367a6-170">Requirements</span></span>



| <span data-ttu-id="367a6-171">Требование</span><span class="sxs-lookup"><span data-stu-id="367a6-171">Requirement</span></span> | <span data-ttu-id="367a6-172">Значение</span><span class="sxs-lookup"><span data-stu-id="367a6-172">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="367a6-173">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="367a6-173">Minimum supported client</span></span><br/> | <span data-ttu-id="367a6-174">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="367a6-174">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="367a6-175">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="367a6-175">Minimum supported server</span></span><br/> | <span data-ttu-id="367a6-176">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="367a6-176">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="367a6-177">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="367a6-177">End of client support</span></span><br/>    | <span data-ttu-id="367a6-178">Windows XP</span><span class="sxs-lookup"><span data-stu-id="367a6-178">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="367a6-179">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="367a6-179">End of server support</span></span><br/>    | <span data-ttu-id="367a6-180">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="367a6-180">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="367a6-181">Header</span><span class="sxs-lookup"><span data-stu-id="367a6-181">Header</span></span><br/>                   | <dl> <span data-ttu-id="367a6-182"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-182"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="367a6-183">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="367a6-183">Type library</span></span><br/>             | <dl> <span data-ttu-id="367a6-184"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-184"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="367a6-185">DLL</span><span class="sxs-lookup"><span data-stu-id="367a6-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="367a6-186"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="367a6-186"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="367a6-187">IID</span><span class="sxs-lookup"><span data-stu-id="367a6-187">IID</span></span><br/>                      | <span data-ttu-id="367a6-188">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="367a6-188">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="367a6-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="367a6-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="367a6-190">**аппендрекорд**</span><span class="sxs-lookup"><span data-stu-id="367a6-190">**AppendRecord**</span></span>](iscardiso7816-appendrecord.md)
</dt> <dt>

[<span data-ttu-id="367a6-191">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="367a6-191">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="367a6-192">**реадрекорд**</span><span class="sxs-lookup"><span data-stu-id="367a6-192">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="367a6-193">**упдатерекорд**</span><span class="sxs-lookup"><span data-stu-id="367a6-193">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> </dl>

 

 
