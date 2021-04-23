---
description: Функция экспорта Рекогнизефраме указывает, распознается ли фрагмент данных как протокол, обнаруженный анализатором. Функция экспорта Рекогнизефраме должна быть реализована для каждого средства синтаксического анализа, поддерживаемого библиотекой DLL средства синтаксического анализа.
ms.assetid: 3f835f58-b011-4329-b9b2-ff865a1f0ae5
title: Функция обратного вызова Рекогнизефраме (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognizeFrame
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: e2660629cecfa279377794749714102077fb6979
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674421"
---
# <a name="recognizeframe-callback-function"></a><span data-ttu-id="22f3d-104">Функция обратного вызова Рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="22f3d-104">RecognizeFrame callback function</span></span>

<span data-ttu-id="22f3d-105">Функция экспорта **рекогнизефраме** указывает, распознается ли фрагмент данных как протокол, обнаруженный анализатором.</span><span class="sxs-lookup"><span data-stu-id="22f3d-105">The **RecognizeFrame** export function indicates whether a piece of data is recognized as the protocol that the parser detects.</span></span> <span data-ttu-id="22f3d-106">Функция экспорта **рекогнизефраме** должна быть реализована для каждого средства синтаксического анализа, ПОДДЕРЖИВАЕМого библиотекой DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="22f3d-106">The **RecognizeFrame** export function must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="22f3d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22f3d-107">Syntax</span></span>


```C++
LPBYTE RecognizeFrame(
  _In_    HFRAME      hFrame,
  _In_    LPBYTE      lpFrame,
  _In_    LPBYTE      lpProtocol,
  _In_    DWORD       MacType,
  _In_    DWORD       BytesLeft,
  _In_    HPROTOCOL   hPreviousProtocol,
  _In_    DWORD       nPreviousProtocolOffset,
  _Out_   LPDWORD     ProtocolStatusCode,
  _Out_   LPHPROTOCOL phNextProtocol,
  _Inout_ PDWORD_PTR  lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="22f3d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="22f3d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22f3d-109">*хфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-110">Обработчик для фрейма, содержащего данные.</span><span class="sxs-lookup"><span data-stu-id="22f3d-110">Handle to the frame that contains the data.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-111">*лпфраме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-112">Указатель на первый байт кадра.</span><span class="sxs-lookup"><span data-stu-id="22f3d-112">Pointer to the first byte of a frame.</span></span> <span data-ttu-id="22f3d-113">Указатель предоставляет способ просмотра данных, распознаваемых другими анализаторами.</span><span class="sxs-lookup"><span data-stu-id="22f3d-113">The pointer provides a way to view data that other parsers recognize.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-114">*лппротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-114">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-115">Указатель на начало неутвержденных данных.</span><span class="sxs-lookup"><span data-stu-id="22f3d-115">Pointer to the start of the unclaimed data.</span></span> <span data-ttu-id="22f3d-116">Как правило, необработанные данные расположены в середине кадра, так как перед этим анализатором были запрошены данные предыдущим синтаксическим анализатором.</span><span class="sxs-lookup"><span data-stu-id="22f3d-116">Typically, the unclaimed data is located in the middle of a frame because a previous parser has claimed data before this parser.</span></span> <span data-ttu-id="22f3d-117">Синтаксический анализатор должен сначала протестировать необработанные данные.</span><span class="sxs-lookup"><span data-stu-id="22f3d-117">The parser must test the unclaimed data first.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-118">*MacType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-118">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-119">Значение MAC первого протокола в кадре.</span><span class="sxs-lookup"><span data-stu-id="22f3d-119">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="22f3d-120">Как правило, значение *MacType* используется, когда анализатор должен распознать первый протокол в кадре.</span><span class="sxs-lookup"><span data-stu-id="22f3d-120">Typically, the *MacType* value is used when the parser must identify the first protocol in a frame.</span></span> <span data-ttu-id="22f3d-121">Значение *MacType* может быть одним из следующих:</span><span class="sxs-lookup"><span data-stu-id="22f3d-121">The *MacType* value can be one of the following:</span></span>



| <span data-ttu-id="22f3d-122">Значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-122">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="22f3d-123">Значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-123">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="22f3d-124"><dt>**\_тип Mac \_ Ethernet**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-124"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="22f3d-125">802.3</span><span class="sxs-lookup"><span data-stu-id="22f3d-125">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="22f3d-126"><dt>**\_тип Mac \_ токенринг**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-126"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="22f3d-127">802.5</span><span class="sxs-lookup"><span data-stu-id="22f3d-127">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="22f3d-128"><dt>**\_тип Mac \_ FDDI**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-128"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="22f3d-129">ANSI X3T 9,5</span><span class="sxs-lookup"><span data-stu-id="22f3d-129">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="22f3d-130">*Битеслефт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-130">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-131">Оставшееся число байтов от расположения в кадре до конца кадра.</span><span class="sxs-lookup"><span data-stu-id="22f3d-131">The remaining number of bytes from a location in a frame to the end of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-132">*хпревиауспротокол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-132">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-133">Обработчик предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-133">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-134">*нпревиауспротоколоффсет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-134">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-135">Смещение предыдущего протокола в начале кадра.</span><span class="sxs-lookup"><span data-stu-id="22f3d-135">Offset of the previous protocol   beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-136">*Протоколстатускоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-136">*ProtocolStatusCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-137">Индикатор состояния протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-137">Protocol status indicator.</span></span> <span data-ttu-id="22f3d-138">Библиотека DLL средства синтаксического анализа должна иметь один из следующих кодов состояния.</span><span class="sxs-lookup"><span data-stu-id="22f3d-138">The parser DLL must set one of the following status codes.</span></span>



| <span data-ttu-id="22f3d-139">Значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-139">Value</span></span>                                                                                                                                                                                                              | <span data-ttu-id="22f3d-140">Значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-140">Meaning</span></span>                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PROTOCOL_STATUS_RECOGNIZED"></span><span id="protocol_status_recognized"></span><dl> <span data-ttu-id="22f3d-141"><dt>**\_ \_ распознанное состояние протокола**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-141"><dt>**PROTOCOL\_STATUS\_RECOGNIZED**</dt></span></span> </dl>              | <span data-ttu-id="22f3d-142">Средство синтаксического анализа распознает данные, но не знает, какой протокол следует за ним.</span><span class="sxs-lookup"><span data-stu-id="22f3d-142">The parser recognizes the data but does not know which protocol follows.</span></span> <span data-ttu-id="22f3d-143">После задания кода возвратите указатель на оставшиеся неутвержденные данные, которые следуют за распознаваемым протоколом.</span><span class="sxs-lookup"><span data-stu-id="22f3d-143">After setting the code, return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="22f3d-144">Для продолжения синтаксического анализа сетевой монитор использует [*следующий набор*](f.md) протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-144">Network Monitor uses the [*follow set*](f.md) of the protocol to continue parsing.</span></span> <br/> |
| <span id="PROTOCOL_STATUS_NOT_RECOGNIZED"></span><span id="protocol_status_not_recognized"></span><dl> <span data-ttu-id="22f3d-145"><dt>**\_состояние протокола \_ не \_ распознано**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-145"><dt>**PROTOCOL\_STATUS\_NOT\_RECOGNIZED**</dt></span></span> </dl> | <span data-ttu-id="22f3d-146">Синтаксический анализатор не распознает данные.</span><span class="sxs-lookup"><span data-stu-id="22f3d-146">The parser does not recognize the data.</span></span> <span data-ttu-id="22f3d-147">После задания этого кода верните указатель на начало данных с помощью указателя, который параметр *лппротокол* передает в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="22f3d-147">After setting this code, return the pointer to the beginning of the data   using the pointer that the *lpProtocol* parameter passes to the parser DLL.</span></span> <span data-ttu-id="22f3d-148">Сетевой монитор использует *следующий набор* предыдущих протоколов для продолжения синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="22f3d-148">Network Monitor uses the *follow set* of the previous protocol to continue parsing.</span></span> <br/>                |
| <span id="PROTOCOL_STATUS_CLAIMED"></span><span id="protocol_status_claimed"></span><dl> <span data-ttu-id="22f3d-149"><dt>**\_состояние протокола \_ затребовано**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-149"><dt>**PROTOCOL\_STATUS\_CLAIMED**</dt></span></span> </dl>                       | <span data-ttu-id="22f3d-150">Средство синтаксического анализа распознает данные и заявляет оставшиеся данные.</span><span class="sxs-lookup"><span data-stu-id="22f3d-150">The parser recognizes the data and claims the remaining data.</span></span> <span data-ttu-id="22f3d-151">После задания кода возвратите **значение NULL** для сетевой монитор, чтобы завершить синтаксический анализ кадра.</span><span class="sxs-lookup"><span data-stu-id="22f3d-151">After setting the code, return **NULL** for Network Monitor to terminate parsing a frame.</span></span> <br/>                                                                                                                                           |
| <span id="PROTOCOL_STATUS_NEXT_PROTOCOL"></span><span id="protocol_status_next_protocol"></span><dl> <span data-ttu-id="22f3d-152"><dt>**протокол \_ состояния \_ следующий \_ протокол**</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-152"><dt>**PROTOCOL\_STATUS\_NEXT\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="22f3d-153">Средство синтаксического анализа распознает данные и знает, какой протокол следует за ним.</span><span class="sxs-lookup"><span data-stu-id="22f3d-153">The parser recognizes the data and knows which protocol follows.</span></span> <span data-ttu-id="22f3d-154">После задания кода задайте параметр *фнекстпротокол* и возвратите указатель на оставшиеся неутвержденные данные, которые следуют за распознаваемым протоколом.</span><span class="sxs-lookup"><span data-stu-id="22f3d-154">After setting the code, set the *phNextProtocol* parameter, and return a pointer to the remaining unclaimed data that follow the recognized protocol.</span></span> <span data-ttu-id="22f3d-155">Сетевой монитор продолжит анализ кадра.</span><span class="sxs-lookup"><span data-stu-id="22f3d-155">Network Monitor continues parsing the frame.</span></span> <br/>                               |



 

</dd> <dt>

<span data-ttu-id="22f3d-156">*фнекстпротокол* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-156">*phNextProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-157">Указатель на маркер следующего протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-157">Pointer to the handle of the next protocol.</span></span> <span data-ttu-id="22f3d-158">Этот параметр задается, когда протокол определяет протокол, который следует за протоколом.</span><span class="sxs-lookup"><span data-stu-id="22f3d-158">This parameter is set when a protocol identifies the protocol that follows a protocol.</span></span> <span data-ttu-id="22f3d-159">Чтобы получить маркер следующего протокола, вызовите функцию [жетпротоколфромтабле](getprotocolfromtable.md) .</span><span class="sxs-lookup"><span data-stu-id="22f3d-159">To obtain the handle of the next protocol, call the [GetProtocolFromTable](getprotocolfromtable.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="22f3d-160">*лпинстдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-160">*lpInstData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="22f3d-161">На входе — указатель на данные экземпляра из предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-161">On input, a pointer to the instance data from the previous protocol.</span></span>

<span data-ttu-id="22f3d-162">На выходе — указатель на данные экземпляра для текущего протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-162">On output, a pointer to the instance data for the current protocol.</span></span> <span data-ttu-id="22f3d-163">Длина данных экземпляра не может превышать значение типа DWORD \_ .</span><span class="sxs-lookup"><span data-stu-id="22f3d-163">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22f3d-164">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-164">Return value</span></span>

<span data-ttu-id="22f3d-165">Если функция выполнена успешно, возвращаемое значение является указателем на первый байт после распознанных данных средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="22f3d-165">If the function is successful, the return value is a pointer to the first byte after the recognized parser data.</span></span> <span data-ttu-id="22f3d-166">Если средство синтаксического анализа заявляет все оставшиеся данные, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="22f3d-166">If the parser claims all the remaining data, the return value is **NULL**.</span></span>

<span data-ttu-id="22f3d-167">Если функция завершается неудачно, возвращаемое значение является начальным указателем, который передается параметром *лппротокол* .</span><span class="sxs-lookup"><span data-stu-id="22f3d-167">If the function is unsuccessful, the return value is an initial pointer that the *lpProtocol* parameter passes-in.</span></span>

## <a name="remarks"></a><span data-ttu-id="22f3d-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="22f3d-168">Remarks</span></span>

<span data-ttu-id="22f3d-169">Функция **рекогнизефраме** определяет, распознает ли синтаксический анализатор необработанные данные, начиная с указателя *лппротокол* .</span><span class="sxs-lookup"><span data-stu-id="22f3d-169">The **RecognizeFrame** function determines whether the parser recognizes the raw data   starting at the *lpProtocol* pointer.</span></span>

-   <span data-ttu-id="22f3d-170">Если протокол распознает данные, функция **рекогнизефраме** возвращает указатель на оставшиеся данные или возвращает **значение NULL** , если текущий протокол является последним в кадре.</span><span class="sxs-lookup"><span data-stu-id="22f3d-170">If the protocol recognizes the data, the **RecognizeFrame** function returns a pointer to the remaining data, or returns **NULL** if the current protocol is the last protocol in a frame.</span></span>
-   <span data-ttu-id="22f3d-171">Если протокол не распознает данные, функция **рекогнизефраме** возвращает указатель, передаваемый в библиотеку DLL средства синтаксического анализа в параметре *лппротокол* .</span><span class="sxs-lookup"><span data-stu-id="22f3d-171">If the protocol does not recognize the data, the **RecognizeFrame** function returns the pointer passed to the parser DLL in the *lpProtocol* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="22f3d-172">*Рекогнизефраме* можно вызвать до вызова функции [*Register*](register-parser.md) для регистрации свойств протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-172">*RecognizeFrame* can be called before the [*Register*](register-parser.md) function is called to register the protocol properties.</span></span> <span data-ttu-id="22f3d-173">По этой причине реализация функции *рекогнизефраме* не зависит от каких бы то ни было свойств или структур, созданных или инициализированных во время реализации функции **Register** протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-173">For that reason, the implementation of the *RecognizeFrame* function does not rely on any properties or structures that are created or initialized during the implementation of the protocol **Register** function.</span></span>

 

<span data-ttu-id="22f3d-174">**Установленный набор и следовать за ним**</span><span class="sxs-lookup"><span data-stu-id="22f3d-174">**Handoff Set and Follow Set**</span></span>

<span data-ttu-id="22f3d-175">Средство синтаксического анализа может использовать переданный набор или следовать за набором, чтобы определить сетевой монитор протокола, который следует за распознанными данными.</span><span class="sxs-lookup"><span data-stu-id="22f3d-175">A parser can use a handoff set or follow set to identify for Network Monitor the protocol that follows recognized data.</span></span>

-   <span data-ttu-id="22f3d-176">Если информация доступна в распознанных данных, средство синтаксического анализа использует его для получения маркера к следующему протоколу, а затем передает этот обработчик в сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="22f3d-176">If information is available in recognized data, the parser uses its handoff set to obtain a handle to the next protocol, and then passes that handle to Network Monitor.</span></span>
-   <span data-ttu-id="22f3d-177">Если информация недоступна, средство синтаксического анализа не передает маркер, а сетевой монитор использует синтаксический анализатор, чтобы определить, какой протокол следует использовать.</span><span class="sxs-lookup"><span data-stu-id="22f3d-177">If information is not available, the parser does not pass a handle, and Network Monitor uses the parser follow set to determine which protocol follows.</span></span>

<span data-ttu-id="22f3d-178">**Передача сведений между протоколами**</span><span class="sxs-lookup"><span data-stu-id="22f3d-178">**Passing information between protocols**</span></span>

<span data-ttu-id="22f3d-179">Используйте параметр *лпинстдата* для передачи сведений между протоколами.</span><span class="sxs-lookup"><span data-stu-id="22f3d-179">Use the *lpInstData* parameter to pass information between protocols.</span></span> <span data-ttu-id="22f3d-180">На входе можно получить сведения из предыдущего протокола.</span><span class="sxs-lookup"><span data-stu-id="22f3d-180">On input, you can retrieve the information from the previous protocol.</span></span> <span data-ttu-id="22f3d-181">На выходе можно передать сведения в следующий протокол.</span><span class="sxs-lookup"><span data-stu-id="22f3d-181">On output, you can pass information to the next protocol.</span></span>

<span data-ttu-id="22f3d-182">Данные экземпляра могут быть любыми данными, размер которых меньше или равен DWORD или \_ указателем на данные, например необработанные данные кадра, которые не должны выделяться или освобождаться анализатором.</span><span class="sxs-lookup"><span data-stu-id="22f3d-182">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span>



| <span data-ttu-id="22f3d-183">Дополнительные сведения о</span><span class="sxs-lookup"><span data-stu-id="22f3d-183">For Information on</span></span>                                        | <span data-ttu-id="22f3d-184">См.</span><span class="sxs-lookup"><span data-stu-id="22f3d-184">See</span></span>                                                                                                                       |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22f3d-185">Какие анализаторы и как они работают с сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="22f3d-185">What parsers are, and how they work with Network Monitor.</span></span> | [<span data-ttu-id="22f3d-186">Анализаторы</span><span class="sxs-lookup"><span data-stu-id="22f3d-186">Parsers</span></span>](parsers.md)                                                                                                    |
| <span data-ttu-id="22f3d-187">Какие точки входа включены в библиотеку DLL средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="22f3d-187">Which entry points are included in the parser DLL.</span></span>        | [<span data-ttu-id="22f3d-188">Архитектура библиотеки DLL средства синтаксического анализа</span><span class="sxs-lookup"><span data-stu-id="22f3d-188">Parser DLL Architecture</span></span>](parser-dll-architecture.md)                                                                    |
| <span data-ttu-id="22f3d-189">Реализация **рекогнизефраме**  включает пример.</span><span class="sxs-lookup"><span data-stu-id="22f3d-189">How to implement **RecognizeFrame**  includes an example.</span></span> | [<span data-ttu-id="22f3d-190">Реализация Рекогнизефраме</span><span class="sxs-lookup"><span data-stu-id="22f3d-190">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)                                                            |
| <span data-ttu-id="22f3d-191">Как указать переданный набор и следовать за набором.</span><span class="sxs-lookup"><span data-stu-id="22f3d-191">How to specify a handoff set and follow set.</span></span>              | <span data-ttu-id="22f3d-192">[Указание](specifying-a-handoff-set.md)переданного набора,[указывающего следующий набор](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="22f3d-192">[Specifying a Handoff Set](specifying-a-handoff-set.md)[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="22f3d-193">Требования</span><span class="sxs-lookup"><span data-stu-id="22f3d-193">Requirements</span></span>



| <span data-ttu-id="22f3d-194">Требование</span><span class="sxs-lookup"><span data-stu-id="22f3d-194">Requirement</span></span> | <span data-ttu-id="22f3d-195">Значение</span><span class="sxs-lookup"><span data-stu-id="22f3d-195">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="22f3d-196">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22f3d-196">Minimum supported client</span></span><br/> | <span data-ttu-id="22f3d-197">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="22f3d-198">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22f3d-198">Minimum supported server</span></span><br/> | <span data-ttu-id="22f3d-199">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="22f3d-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="22f3d-200">Заголовок</span><span class="sxs-lookup"><span data-stu-id="22f3d-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="22f3d-201"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="22f3d-201"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22f3d-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22f3d-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22f3d-203">жетпротоколфромтабле</span><span class="sxs-lookup"><span data-stu-id="22f3d-203">GetProtocolFromTable</span></span>](getprotocolfromtable.md)
</dt> </dl>

 

 




