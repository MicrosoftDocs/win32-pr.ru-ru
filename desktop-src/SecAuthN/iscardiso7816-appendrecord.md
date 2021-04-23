---
description: Метод Аппендрекорд создает команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая либо добавляет запись в конец базового файла с линейной структурой (EF), либо записывает номер 1 в циклический простой файл.
ms.assetid: 4dd88661-41c4-4238-88c9-279b39afb206
title: 'Метод ISCardISO7816:: Аппендрекорд (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.AppendRecord
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28d1b6762e0a350bb87b673f21fa063ae2478e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263587"
---
# <a name="iscardiso7816appendrecord-method"></a><span data-ttu-id="6afc3-103">Метод ISCardISO7816:: Аппендрекорд</span><span class="sxs-lookup"><span data-stu-id="6afc3-103">ISCardISO7816::AppendRecord method</span></span>

<span data-ttu-id="6afc3-104">\[Метод **аппендрекорд** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="6afc3-104">\[The **AppendRecord** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6afc3-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="6afc3-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6afc3-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="6afc3-107">Метод **аппендрекорд** создает команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая либо добавляет запись в конец базового файла с линейной структурой (EF), либо записывает номер 1 в циклический простой файл.</span><span class="sxs-lookup"><span data-stu-id="6afc3-107">The **AppendRecord** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that either appends a record to the end of a linear-structured elementary file (EF) or writes record number 1 in a cyclic-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6afc3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6afc3-108">Syntax</span></span>


```C++
HRESULT AppendRecord(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="6afc3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6afc3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6afc3-110">*бирефктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6afc3-111">Определяет простейший файл, который необходимо добавить.</span><span class="sxs-lookup"><span data-stu-id="6afc3-111">Identifies the elementary file to be appended.</span></span>



| <span data-ttu-id="6afc3-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-112">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="6afc3-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-113">Meaning</span></span>                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="Current_EF"></span><span id="current_ef"></span><span id="CURRENT_EF"></span><dl> <span data-ttu-id="6afc3-114"><dt>**Текущая ссылка EF**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-114"><dt>**Current EF**</dt></span></span> </dl>     | <span data-ttu-id="6afc3-115">Разрядное расположение: 00000000</span><span class="sxs-lookup"><span data-stu-id="6afc3-115">Bit position: 00000000</span></span><br/> |
| <span id="Short_EF_ID"></span><span id="short_ef_id"></span><span id="SHORT_EF_ID"></span><dl> <span data-ttu-id="6afc3-116"><dt>**Краткий идентификатор EF**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-116"><dt>**Short EF ID**</dt></span></span> </dl> | <span data-ttu-id="6afc3-117">Битовое расположение: xxxxx000</span><span class="sxs-lookup"><span data-stu-id="6afc3-117">Bit position: xxxxx000</span></span><br/> |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <span data-ttu-id="6afc3-118"><dt>**Зарезервировано**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-118"><dt>**Reserved**</dt></span></span> </dl>             | <span data-ttu-id="6afc3-119">Разрядное расположение: XXXXXXXX</span><span class="sxs-lookup"><span data-stu-id="6afc3-119">Bit position: xxxxxxxx</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6afc3-120">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-120">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6afc3-121">Указатель на данные, добавляемые в файл.</span><span class="sxs-lookup"><span data-stu-id="6afc3-121">A pointer to the data to be appended to the file.</span></span>



| <span data-ttu-id="6afc3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-122">Value</span></span>                                                                                                                                                | <span data-ttu-id="6afc3-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-123">Meaning</span></span>                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="Tn"></span><span id="tn"></span><span id="TN"></span><dl> <span data-ttu-id="6afc3-124"><dt>**Код**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-124"><dt>**Tn**</dt></span></span> </dl>     | <span data-ttu-id="6afc3-125">1 байт</span><span class="sxs-lookup"><span data-stu-id="6afc3-125">1 byte</span></span><br/>       |
| <span id="Ln_"></span><span id="ln_"></span><span id="LN_"></span><dl> <span data-ttu-id="6afc3-126"><dt>**LN**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-126"><dt>**Ln** </dt></span></span> </dl> | <span data-ttu-id="6afc3-127">1 или 3 байта</span><span class="sxs-lookup"><span data-stu-id="6afc3-127">1 or 3 bytes</span></span><br/> |
| <span id="data"></span><span id="DATA"></span><dl> <span data-ttu-id="6afc3-128"><dt>**Data**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-128"><dt>**data**</dt></span></span> </dl>                    | <span data-ttu-id="6afc3-129">LN байт</span><span class="sxs-lookup"><span data-stu-id="6afc3-129">Ln bytes</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="6afc3-130">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-130">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6afc3-131">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="6afc3-131">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="6afc3-132">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="6afc3-132">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="6afc3-133">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренне и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="6afc3-133">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6afc3-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-134">Return value</span></span>

<span data-ttu-id="6afc3-135">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="6afc3-135">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="6afc3-136">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6afc3-136">Return code</span></span>                                                                                   | <span data-ttu-id="6afc3-137">Описание</span><span class="sxs-lookup"><span data-stu-id="6afc3-137">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="6afc3-138"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-138"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6afc3-139">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="6afc3-139">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="6afc3-140"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-140"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6afc3-141">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="6afc3-141">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="6afc3-142"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-142"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="6afc3-143">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="6afc3-143">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="6afc3-144"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-144"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6afc3-145">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="6afc3-145">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="6afc3-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6afc3-146">Remarks</span></span>

<span data-ttu-id="6afc3-147">Инкапсулированная команда может быть выполнена только в том случае, если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) удовлетворяет атрибутам безопасности простейшего файла Read.</span><span class="sxs-lookup"><span data-stu-id="6afc3-147">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file read.</span></span>

<span data-ttu-id="6afc3-148">Если во время выполнения этой команды выбран другой простейший файл, он может быть обработан без идентификации текущего выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="6afc3-148">If another elementary file is selected at the time of issuing this command, it may be processed without identification of the currently selected file.</span></span>

<span data-ttu-id="6afc3-149">Невозможно прочитать простейшие файлы без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="6afc3-149">Elementary files without a record structure cannot be read.</span></span> <span data-ttu-id="6afc3-150">Инкапсулированная команда прерывается, если применяется к простейшему файлу без структуры записи.</span><span class="sxs-lookup"><span data-stu-id="6afc3-150">The encapsulated command aborts if applied to an elementary file without a record structure.</span></span>

<span data-ttu-id="6afc3-151">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="6afc3-151">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="6afc3-152">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="6afc3-152">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="6afc3-153">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="6afc3-153">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6afc3-154">Требования</span><span class="sxs-lookup"><span data-stu-id="6afc3-154">Requirements</span></span>



| <span data-ttu-id="6afc3-155">Требование</span><span class="sxs-lookup"><span data-stu-id="6afc3-155">Requirement</span></span> | <span data-ttu-id="6afc3-156">Значение</span><span class="sxs-lookup"><span data-stu-id="6afc3-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6afc3-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6afc3-157">Minimum supported client</span></span><br/> | <span data-ttu-id="6afc3-158">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-158">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6afc3-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6afc3-159">Minimum supported server</span></span><br/> | <span data-ttu-id="6afc3-160">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6afc3-160">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6afc3-161">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6afc3-161">End of client support</span></span><br/>    | <span data-ttu-id="6afc3-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6afc3-162">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="6afc3-163">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6afc3-163">End of server support</span></span><br/>    | <span data-ttu-id="6afc3-164">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6afc3-164">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="6afc3-165">Header</span><span class="sxs-lookup"><span data-stu-id="6afc3-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="6afc3-166"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-166"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6afc3-167">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6afc3-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="6afc3-168"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-168"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6afc3-169">DLL</span><span class="sxs-lookup"><span data-stu-id="6afc3-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6afc3-170"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6afc3-170"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6afc3-171">IID</span><span class="sxs-lookup"><span data-stu-id="6afc3-171">IID</span></span><br/>                      | <span data-ttu-id="6afc3-172">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="6afc3-172">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="6afc3-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6afc3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6afc3-174">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="6afc3-174">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="6afc3-175">**реадрекорд**</span><span class="sxs-lookup"><span data-stu-id="6afc3-175">**ReadRecord**</span></span>](iscardiso7816-readrecord.md)
</dt> <dt>

[<span data-ttu-id="6afc3-176">**упдатерекорд**</span><span class="sxs-lookup"><span data-stu-id="6afc3-176">**UpdateRecord**</span></span>](iscardiso7816-updaterecord.md)
</dt> <dt>

[<span data-ttu-id="6afc3-177">**вритерекорд**</span><span class="sxs-lookup"><span data-stu-id="6afc3-177">**WriteRecord**</span></span>](iscardiso7816-writerecord.md)
</dt> </dl>

 

 
