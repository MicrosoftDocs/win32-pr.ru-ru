---
description: Метод GetData конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая извлекает один примитивный объект данных или набор объектов данных (содержащихся в сконструированном объекте данных) в зависимости от типа выбранного файла.
ms.assetid: d764a765-f451-4bf7-9d06-f5901062dcac
title: 'Метод ISCardISO7816:: GetData (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.GetData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 93dca04daa50e068a68dc62cf11a580eb8e3b1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815817"
---
# <a name="iscardiso7816getdata-method"></a><span data-ttu-id="4c227-103">Метод ISCardISO7816:: GetData</span><span class="sxs-lookup"><span data-stu-id="4c227-103">ISCardISO7816::GetData method</span></span>

<span data-ttu-id="4c227-104">\[Метод **GetData** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4c227-104">\[The **GetData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c227-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="4c227-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4c227-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="4c227-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="4c227-107">Метод **GetData** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая извлекает один примитивный объект данных или набор объектов данных (содержащихся в сконструированном объекте данных) в зависимости от типа выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="4c227-107">The **GetData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that retrieves either a single primitive data object or a set of data objects (contained in a constructed data object), depending on the type of file selected.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c227-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c227-108">Syntax</span></span>


```C++
HRESULT GetData(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToGet,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="4c227-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4c227-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c227-110">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c227-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c227-111">Параметры.</span><span class="sxs-lookup"><span data-stu-id="4c227-111">Parameters.</span></span>



| <span data-ttu-id="4c227-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c227-112">Value</span></span>                                                                                  | <span data-ttu-id="4c227-113">Значение</span><span class="sxs-lookup"><span data-stu-id="4c227-113">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4c227-114"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-114"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="4c227-115">рфу</span><span class="sxs-lookup"><span data-stu-id="4c227-115">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c227-116"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-116"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="4c227-117">ЛИЧЕСТВО — тег TLV (1 байт) в P2</span><span class="sxs-lookup"><span data-stu-id="4c227-117">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="4c227-118"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-118"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="4c227-119">Данные приложения (собственная кодировка)</span><span class="sxs-lookup"><span data-stu-id="4c227-119">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="4c227-120"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-120"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="4c227-121">Тег SIMPLE-TLV в P2</span><span class="sxs-lookup"><span data-stu-id="4c227-121">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="4c227-122"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-122"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="4c227-123">рфу</span><span class="sxs-lookup"><span data-stu-id="4c227-123">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c227-124"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-124"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="4c227-125">ЛИЧЕСТВО-TLV тега (2 байта) в P1-P2</span><span class="sxs-lookup"><span data-stu-id="4c227-125">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="4c227-126">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c227-126">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c227-127">Параметры.</span><span class="sxs-lookup"><span data-stu-id="4c227-127">Parameters.</span></span>



| <span data-ttu-id="4c227-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4c227-128">Value</span></span>                                                                                  | <span data-ttu-id="4c227-129">Значение</span><span class="sxs-lookup"><span data-stu-id="4c227-129">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="4c227-130"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-130"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="4c227-131">рфу</span><span class="sxs-lookup"><span data-stu-id="4c227-131">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c227-132"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-132"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="4c227-133">ЛИЧЕСТВО — тег TLV (1 байт) в P2</span><span class="sxs-lookup"><span data-stu-id="4c227-133">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="4c227-134"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-134"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="4c227-135">Данные приложения (собственная кодировка)</span><span class="sxs-lookup"><span data-stu-id="4c227-135">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="4c227-136"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-136"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="4c227-137">Тег SIMPLE-TLV в P2</span><span class="sxs-lookup"><span data-stu-id="4c227-137">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="4c227-138"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-138"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="4c227-139">рфу</span><span class="sxs-lookup"><span data-stu-id="4c227-139">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="4c227-140"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-140"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="4c227-141">ЛИЧЕСТВО-TLV тега (2 байта) в P1-P2</span><span class="sxs-lookup"><span data-stu-id="4c227-141">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="4c227-142">*лбитестожет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4c227-142">*lBytesToGet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c227-143">Число байтов, ожидаемых в ответе.</span><span class="sxs-lookup"><span data-stu-id="4c227-143">Number of bytes expected in the response.</span></span>

</dd> <dt>

<span data-ttu-id="4c227-144">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="4c227-144">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c227-145">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4c227-145">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="4c227-146">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="4c227-146">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="4c227-147">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="4c227-147">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c227-148">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4c227-148">Return value</span></span>

<span data-ttu-id="4c227-149">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="4c227-149">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="4c227-150">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4c227-150">Return code</span></span>                                                                                   | <span data-ttu-id="4c227-151">Описание</span><span class="sxs-lookup"><span data-stu-id="4c227-151">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="4c227-152"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-152"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="4c227-153">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="4c227-153">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="4c227-154"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-154"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="4c227-155">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="4c227-155">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="4c227-156"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-156"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="4c227-157">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="4c227-157">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="4c227-158"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-158"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="4c227-159">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="4c227-159">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="4c227-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c227-160">Remarks</span></span>

<span data-ttu-id="4c227-161">Инкапсулированная команда может быть выполнена, только если состояние безопасности [*смарт-карты*](../secgloss/s-gly.md) удовлетворяет атрибутам безопасности простейшего считываемого файла.</span><span class="sxs-lookup"><span data-stu-id="4c227-161">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being read.</span></span> <span data-ttu-id="4c227-162">Условия безопасности зависят от политики карты и могут работать с помощью [**екстерналаусентикате**](iscardiso7816-externalauthenticate.md), [**интерналаусентикате**](iscardiso7816-internalauthenticate.md), [**искардаус**](iscardauth.md)и т. д.</span><span class="sxs-lookup"><span data-stu-id="4c227-162">Security conditions are dependent on the policy of the card, and may be manipulated through [**ExternalAuthenticate**](iscardiso7816-externalauthenticate.md), [**InternalAuthenticate**](iscardiso7816-internalauthenticate.md), [**ISCardAuth**](iscardauth.md), and so on.</span></span>

<span data-ttu-id="4c227-163">Чтобы выбрать файл, вызовите [**селектфиле**](iscardiso7816-selectfile.md).</span><span class="sxs-lookup"><span data-stu-id="4c227-163">To select a file, call [**SelectFile**](iscardiso7816-selectfile.md).</span></span>

<span data-ttu-id="4c227-164">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="4c227-164">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="4c227-165">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="4c227-165">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="4c227-166">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="4c227-166">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c227-167">Требования</span><span class="sxs-lookup"><span data-stu-id="4c227-167">Requirements</span></span>



| <span data-ttu-id="4c227-168">Требование</span><span class="sxs-lookup"><span data-stu-id="4c227-168">Requirement</span></span> | <span data-ttu-id="4c227-169">Значение</span><span class="sxs-lookup"><span data-stu-id="4c227-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c227-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c227-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4c227-171">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4c227-171">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4c227-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c227-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4c227-173">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4c227-173">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4c227-174">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4c227-174">End of client support</span></span><br/>    | <span data-ttu-id="4c227-175">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c227-175">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="4c227-176">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4c227-176">End of server support</span></span><br/>    | <span data-ttu-id="4c227-177">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="4c227-177">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="4c227-178">Header</span><span class="sxs-lookup"><span data-stu-id="4c227-178">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c227-179"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-179"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c227-180">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4c227-180">Type library</span></span><br/>             | <dl> <span data-ttu-id="4c227-181"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-181"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4c227-182">DLL</span><span class="sxs-lookup"><span data-stu-id="4c227-182">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c227-183"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c227-183"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4c227-184">IID</span><span class="sxs-lookup"><span data-stu-id="4c227-184">IID</span></span><br/>                      | <span data-ttu-id="4c227-185">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="4c227-185">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="4c227-186">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c227-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c227-187">**екстерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="4c227-187">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="4c227-188">**интерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="4c227-188">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="4c227-189">**искардаус**</span><span class="sxs-lookup"><span data-stu-id="4c227-189">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="4c227-190">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="4c227-190">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="4c227-191">**путдата**</span><span class="sxs-lookup"><span data-stu-id="4c227-191">**PutData**</span></span>](iscardiso7816-putdata.md)
</dt> <dt>

[<span data-ttu-id="4c227-192">**селектфиле**</span><span class="sxs-lookup"><span data-stu-id="4c227-192">**SelectFile**</span></span>](iscardiso7816-selectfile.md)
</dt> </dl>

 

 
