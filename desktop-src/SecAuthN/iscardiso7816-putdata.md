---
description: Метод Путдата конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), в которой хранится один примитивный объект данных или набор объектов данных, содержащихся в сконструированном объекте данных, в зависимости от выбранного файла.
ms.assetid: 6bad45fb-b202-4eb0-b2f4-fe0a6af64330
title: 'ISCardISO7816: метод:P Утдата (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.PutData
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3c15239943a92067011011b6cedca191fa78c3a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911615"
---
# <a name="iscardiso7816putdata-method"></a><span data-ttu-id="25200-103">ISCardISO7816: метод:P Утдата</span><span class="sxs-lookup"><span data-stu-id="25200-103">ISCardISO7816::PutData method</span></span>

<span data-ttu-id="25200-104">\[Метод **путдата** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="25200-104">\[The **PutData** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="25200-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="25200-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="25200-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="25200-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="25200-107">Метод **путдата** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), в которой хранится один примитивный объект данных или набор объектов данных, содержащихся в сконструированном объекте данных, в зависимости от выбранного файла.</span><span class="sxs-lookup"><span data-stu-id="25200-107">The **PutData** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that stores a single primitive data object or the set of data objects contained in a constructed data object, depending on the file selected.</span></span>

<span data-ttu-id="25200-108">Метод хранения объектов (написание одного раза и (или) обновления или добавления) зависит от определения или природы объектов данных.</span><span class="sxs-lookup"><span data-stu-id="25200-108">How the objects are stored (writing once and/or updating and/or appending) depends on the definition or the nature of the data objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="25200-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25200-109">Syntax</span></span>


```C++
HRESULT PutData(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="25200-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="25200-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25200-111">*byP1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25200-111">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25200-112">Программирование P1-P2.</span><span class="sxs-lookup"><span data-stu-id="25200-112">Coding of P1-P2.</span></span>



| <span data-ttu-id="25200-113">Значение</span><span class="sxs-lookup"><span data-stu-id="25200-113">Value</span></span>                                                                                  | <span data-ttu-id="25200-114">Значение</span><span class="sxs-lookup"><span data-stu-id="25200-114">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="25200-115"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="25200-115"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="25200-116">рфу</span><span class="sxs-lookup"><span data-stu-id="25200-116">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="25200-117"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-117"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="25200-118">ЛИЧЕСТВО — тег TLV (1 байт) в P2</span><span class="sxs-lookup"><span data-stu-id="25200-118">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="25200-119"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-119"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="25200-120">Данные приложения (собственная кодировка)</span><span class="sxs-lookup"><span data-stu-id="25200-120">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="25200-121"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-121"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="25200-122">Тег SIMPLE-TLV в P2</span><span class="sxs-lookup"><span data-stu-id="25200-122">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="25200-123"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-123"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="25200-124">рфу</span><span class="sxs-lookup"><span data-stu-id="25200-124">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="25200-125"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-125"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="25200-126">ЛИЧЕСТВО-TLV тега (2 байта) в P1-P2</span><span class="sxs-lookup"><span data-stu-id="25200-126">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="25200-127">*byP2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25200-127">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25200-128">Программирование P1-P2.</span><span class="sxs-lookup"><span data-stu-id="25200-128">Coding of P1-P2.</span></span>



| <span data-ttu-id="25200-129">Значение</span><span class="sxs-lookup"><span data-stu-id="25200-129">Value</span></span>                                                                                  | <span data-ttu-id="25200-130">Значение</span><span class="sxs-lookup"><span data-stu-id="25200-130">Meaning</span></span>                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="25200-131"><dt>0000-003F</dt></span><span class="sxs-lookup"><span data-stu-id="25200-131"><dt>0000 - 003F</dt></span></span> </dl> | <span data-ttu-id="25200-132">рфу</span><span class="sxs-lookup"><span data-stu-id="25200-132">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="25200-133"><dt>0040-00FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-133"><dt>0040 - 00FF</dt></span></span> </dl> | <span data-ttu-id="25200-134">ЛИЧЕСТВО — тег TLV (1 байт) в P2</span><span class="sxs-lookup"><span data-stu-id="25200-134">BER-TLV tag (1 byte) in P2</span></span><br/>            |
| <dl> <span data-ttu-id="25200-135"><dt>0100-01FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-135"><dt>0100 - 01FF</dt></span></span> </dl> | <span data-ttu-id="25200-136">Данные приложения (собственная кодировка)</span><span class="sxs-lookup"><span data-stu-id="25200-136">Application data (proprietary coding)</span></span><br/> |
| <dl> <span data-ttu-id="25200-137"><dt>0200-02FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-137"><dt>0200 - 02FF</dt></span></span> </dl> | <span data-ttu-id="25200-138">Тег SIMPLE-TLV в P2</span><span class="sxs-lookup"><span data-stu-id="25200-138">SIMPLE-TLV tag in P2</span></span><br/>                  |
| <dl> <span data-ttu-id="25200-139"><dt>0300-03FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-139"><dt>0300 - 03FF</dt></span></span> </dl> | <span data-ttu-id="25200-140">рфу</span><span class="sxs-lookup"><span data-stu-id="25200-140">RFU</span></span><br/>                                   |
| <dl> <span data-ttu-id="25200-141"><dt>0400 - 04FF</dt></span><span class="sxs-lookup"><span data-stu-id="25200-141"><dt>0400 - 04FF</dt></span></span> </dl> | <span data-ttu-id="25200-142">ЛИЧЕСТВО-TLV тега (2 байта) в P1-P2</span><span class="sxs-lookup"><span data-stu-id="25200-142">BER-TLV tag (2 bytes) in P1-P2</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="25200-143">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25200-143">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25200-144">Указатель на буфер байтов, содержащий параметры и данные, которые необходимо записать.</span><span class="sxs-lookup"><span data-stu-id="25200-144">Pointer to a byte buffer that contains the parameters and data to be written.</span></span>

</dd> <dt>

<span data-ttu-id="25200-145">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="25200-145">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25200-146">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="25200-146">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="25200-147">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="25200-147">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="25200-148">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="25200-148">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25200-149">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25200-149">Return value</span></span>

<span data-ttu-id="25200-150">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="25200-150">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="25200-151">Код возврата</span><span class="sxs-lookup"><span data-stu-id="25200-151">Return code</span></span>                                                                                   | <span data-ttu-id="25200-152">Описание</span><span class="sxs-lookup"><span data-stu-id="25200-152">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="25200-153"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="25200-153"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="25200-154">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="25200-154">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="25200-155"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="25200-155"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="25200-156">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="25200-156">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="25200-157"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="25200-157"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="25200-158">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="25200-158">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="25200-159"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25200-159"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="25200-160">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="25200-160">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="25200-161">Комментарии</span><span class="sxs-lookup"><span data-stu-id="25200-161">Remarks</span></span>

<span data-ttu-id="25200-162">Команду можно выполнить, только если состояние безопасности удовлетворяет условиям безопасности, определенным приложением в [*контексте*](../secgloss/c-gly.md) функции.</span><span class="sxs-lookup"><span data-stu-id="25200-162">The command can be performed only if the security status satisfies the security conditions defined by the application within the [*context*](../secgloss/c-gly.md) for the function.</span></span>

<dl> <dt>

<span data-ttu-id="25200-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Хранение данных приложения</span><span class="sxs-lookup"><span data-stu-id="25200-163"><span id="Store_Application_Data"></span><span id="store_application_data"></span><span id="STORE_APPLICATION_DATA"></span>Store Application Data</span></span>
</dt> <dd>

<span data-ttu-id="25200-164">Если значение P1-P2 находится в диапазоне от 0100 до 01FF, значение P1-P2 должно быть идентификатором, зарезервированным для внутренних тестов карты и для частных служб, осмысленных в данном контексте приложения.</span><span class="sxs-lookup"><span data-stu-id="25200-164">When the value of P1-P2 lies in the range from 0100 to 01FF, the value of P1-P2 shall be an identifier reserved for card internal tests and for proprietary services meaningful within a given application context.</span></span>

</dd> <dt>

<span data-ttu-id="25200-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Хранение объектов данных</span><span class="sxs-lookup"><span data-stu-id="25200-165"><span id="Store_Data_Objects"></span><span id="store_data_objects"></span><span id="STORE_DATA_OBJECTS"></span>Store Data Objects</span></span>
</dt> <dd>

<span data-ttu-id="25200-166">Если значение P1-P2 находится в диапазоне от 0040 до 00FF, значение P2 должно быть тегом ЛИЧЕСТВО-TLV в одном байте.</span><span class="sxs-lookup"><span data-stu-id="25200-166">When the value P1-P2 lies in the range from 0040 to 00FF, the value of P2 shall be a BER-TLV tag on a single byte.</span></span> <span data-ttu-id="25200-167">Значение 00FF зарезервировано для указания того, что поле данных содержит объекты данных ЛИЧЕСТВО-TLV.</span><span class="sxs-lookup"><span data-stu-id="25200-167">The value of 00FF is reserved for indicating that the data field carries BER-TLV data objects.</span></span>

<span data-ttu-id="25200-168">Если значение P1-P2 находится в диапазоне от 0200 до 02FF, значение P2 должно быть простым TLV-тегом.</span><span class="sxs-lookup"><span data-stu-id="25200-168">When the value of P1-P2 lies in the range 0200 to 02FF, the value of P2 shall be a SIMPLE-TLV tag.</span></span> <span data-ttu-id="25200-169">Значение 0200 — РФУ.</span><span class="sxs-lookup"><span data-stu-id="25200-169">The value 0200 is RFU.</span></span> <span data-ttu-id="25200-170">Значение 02FF зарезервировано для указания того, что поле данных содержит объекты данных с ПРОСТЫМи TLVми.</span><span class="sxs-lookup"><span data-stu-id="25200-170">The value 02FF is reserved for indicating that the data field carries SIMPLE-TLV data objects.</span></span>

<span data-ttu-id="25200-171">Если значение P1-P2 находится в диапазоне от 4000 до FFFF, значение P1-P2 должно быть ЛИЧЕСТВО тегом на два байта.</span><span class="sxs-lookup"><span data-stu-id="25200-171">When the value of P1-P2 lies in the range from 4000 to FFFF, the value of P1-P2 shall be a BER-TLV tag on two bytes.</span></span> <span data-ttu-id="25200-172">Значения 4000 — FFFF — РФУ.</span><span class="sxs-lookup"><span data-stu-id="25200-172">The values 4000 to FFFF are RFU.</span></span>

<span data-ttu-id="25200-173">Если предоставлен примитивный объект данных, поле данных командного сообщения должно содержать значение соответствующего объекта-примитива данных.</span><span class="sxs-lookup"><span data-stu-id="25200-173">When a primitive data object is provided, the data field of the command message shall contain the value of the corresponding primitive data object.</span></span>

<span data-ttu-id="25200-174">Если предоставлен сконструированный объект данных, поле данных командного сообщения должно содержать значение сконструированного объекта данных (то есть объекты данных, включая теги, длину и значение).</span><span class="sxs-lookup"><span data-stu-id="25200-174">When a constructed data object is provided, the data field of the command message shall contain the value of the constructed data object (that is, data objects including their tag, length, and value).</span></span>

</dd> </dl>

<span data-ttu-id="25200-175">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="25200-175">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="25200-176">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="25200-176">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="25200-177">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="25200-177">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25200-178">Требования</span><span class="sxs-lookup"><span data-stu-id="25200-178">Requirements</span></span>



| <span data-ttu-id="25200-179">Требование</span><span class="sxs-lookup"><span data-stu-id="25200-179">Requirement</span></span> | <span data-ttu-id="25200-180">Значение</span><span class="sxs-lookup"><span data-stu-id="25200-180">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25200-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25200-181">Minimum supported client</span></span><br/> | <span data-ttu-id="25200-182">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="25200-182">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="25200-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25200-183">Minimum supported server</span></span><br/> | <span data-ttu-id="25200-184">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25200-184">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="25200-185">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="25200-185">End of client support</span></span><br/>    | <span data-ttu-id="25200-186">Windows XP</span><span class="sxs-lookup"><span data-stu-id="25200-186">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="25200-187">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="25200-187">End of server support</span></span><br/>    | <span data-ttu-id="25200-188">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="25200-188">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="25200-189">Header</span><span class="sxs-lookup"><span data-stu-id="25200-189">Header</span></span><br/>                   | <dl> <span data-ttu-id="25200-190"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="25200-190"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="25200-191">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="25200-191">Type library</span></span><br/>             | <dl> <span data-ttu-id="25200-192"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="25200-192"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="25200-193">DLL</span><span class="sxs-lookup"><span data-stu-id="25200-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25200-194"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25200-194"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="25200-195">IID</span><span class="sxs-lookup"><span data-stu-id="25200-195">IID</span></span><br/>                      | <span data-ttu-id="25200-196">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="25200-196">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="25200-197">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25200-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25200-198">**GetData**</span><span class="sxs-lookup"><span data-stu-id="25200-198">**GetData**</span></span>](iscardiso7816-getdata.md)
</dt> <dt>

[<span data-ttu-id="25200-199">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="25200-199">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
