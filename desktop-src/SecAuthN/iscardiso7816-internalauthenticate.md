---
description: Конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая инициирует вычисление данных проверки подлинности с помощью карточки, используя данные запроса, отправленные с устройства интерфейса, и соответствующий секрет (например, ключ), хранящийся в карточке.
ms.assetid: cb0b2535-6e5b-4fb2-b540-cd037259baab
title: 'Метод ISCardISO7816:: Интерналаусентикате (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.InternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1e30dbb06373907c5cea07e45d4f7a390b773349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080595"
---
# <a name="iscardiso7816internalauthenticate-method"></a><span data-ttu-id="bccc6-103">Метод ISCardISO7816:: Интерналаусентикате</span><span class="sxs-lookup"><span data-stu-id="bccc6-103">ISCardISO7816::InternalAuthenticate method</span></span>

<span data-ttu-id="bccc6-104">\[Метод **интерналаусентикате** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="bccc6-104">\[The **InternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bccc6-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="bccc6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bccc6-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="bccc6-107">Метод **интерналаусентикате** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая инициирует вычисление данных проверки подлинности с помощью карточки, используя данные запроса, отправленные с устройства интерфейса, и соответствующий секрет (например, ключ), хранящийся в карточке.</span><span class="sxs-lookup"><span data-stu-id="bccc6-107">The **InternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the computation of the authentication data by the card using the challenge data sent from the interface device and a relevant secret (for example, a key) stored in the card.</span></span>

<span data-ttu-id="bccc6-108">Если соответствующий секрет прикреплен к MF, команда может использоваться для проверки подлинности карты в целом.</span><span class="sxs-lookup"><span data-stu-id="bccc6-108">When the relevant secret is attached to the MF, the command may be used to authenticate the card as a whole.</span></span>

<span data-ttu-id="bccc6-109">Если соответствующий секрет присоединен к другой DF, для проверки подлинности этой DF можно использовать команду.</span><span class="sxs-lookup"><span data-stu-id="bccc6-109">When the relevant secret is attached to another DF, the command may be used to authenticate that DF.</span></span>

## <a name="syntax"></a><span data-ttu-id="bccc6-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bccc6-110">Syntax</span></span>


```C++
HRESULT InternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in]      LONG         lReplyBytes,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="bccc6-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="bccc6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bccc6-112">*бялгорисмреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-112">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccc6-113">Ссылка на алгоритм в карточке.</span><span class="sxs-lookup"><span data-stu-id="bccc6-113">Reference of the algorithm in the card.</span></span>

<span data-ttu-id="bccc6-114">Если это значение равно нулю, это означает, что сведения не указаны.</span><span class="sxs-lookup"><span data-stu-id="bccc6-114">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="bccc6-115">Ссылка на алгоритм известна либо перед выдачей команды, либо в поле данных.</span><span class="sxs-lookup"><span data-stu-id="bccc6-115">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="bccc6-116">*бисекретреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-116">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccc6-117">Ссылка на секрет.</span><span class="sxs-lookup"><span data-stu-id="bccc6-117">Reference of the secret.</span></span>



| <span data-ttu-id="bccc6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bccc6-118">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="bccc6-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bccc6-119">Meaning</span></span>                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="bccc6-120"><dt>**Нет сведений**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-120"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="bccc6-121">Разрядное расположение: 00000000</span><span class="sxs-lookup"><span data-stu-id="bccc6-121">Bit position: 00000000</span></span> <br/> <span data-ttu-id="bccc6-122">Сведения не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="bccc6-122">No information is given.</span></span> <span data-ttu-id="bccc6-123">Ссылка на секрет известен либо перед выдачей команды, либо в поле данных.</span><span class="sxs-lookup"><span data-stu-id="bccc6-123">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="bccc6-124"><dt>**Глобальная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-124"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="bccc6-125">Битовое расположение: 0-------</span><span class="sxs-lookup"><span data-stu-id="bccc6-125">Bit position: 0-------</span></span> <br/> <span data-ttu-id="bccc6-126">Глобальные эталонные данные (ключ, определяемый протоколом MF).</span><span class="sxs-lookup"><span data-stu-id="bccc6-126">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="bccc6-127"><dt>**Конкретная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-127"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="bccc6-128">Битовое расположение: 1-------</span><span class="sxs-lookup"><span data-stu-id="bccc6-128">Bit position: 1-------</span></span><br/> <span data-ttu-id="bccc6-129">Конкретные ссылочные данные (ключ, определяемый DF).</span><span class="sxs-lookup"><span data-stu-id="bccc6-129">Specific reference data (a DF specific key).</span></span><br/>                                                                                       |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="bccc6-130"><dt>**рфу**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-130"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="bccc6-131">Разрядное расположение:-XX-----</span><span class="sxs-lookup"><span data-stu-id="bccc6-131">Bit position: -xx-----</span></span><br/> <span data-ttu-id="bccc6-132">00 (другие значения — РФУ).</span><span class="sxs-lookup"><span data-stu-id="bccc6-132">00 (other values are RFU).</span></span><br/>                                                                                                         |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="bccc6-133"><dt>**Владел**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-133"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="bccc6-134">Разрядное расположение:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="bccc6-134">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="bccc6-135">Номер секрета.</span><span class="sxs-lookup"><span data-stu-id="bccc6-135">Number of the secret.</span></span><br/>                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="bccc6-136">*пчалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-136">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccc6-137">Указатель на данные, связанные с проверкой подлинности (например, сложность).</span><span class="sxs-lookup"><span data-stu-id="bccc6-137">Pointer to the authentication-related data (for example, challenge).</span></span>

</dd> <dt>

<span data-ttu-id="bccc6-138">*лреплибитес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-138">*lReplyBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccc6-139">Максимальное число байтов, ожидаемое в ответе.</span><span class="sxs-lookup"><span data-stu-id="bccc6-139">Maximum number of bytes expected in response.</span></span>

</dd> <dt>

<span data-ttu-id="bccc6-140">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-140">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bccc6-141">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bccc6-141">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="bccc6-142">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="bccc6-142">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="bccc6-143">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="bccc6-143">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bccc6-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bccc6-144">Return value</span></span>

<span data-ttu-id="bccc6-145">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="bccc6-145">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="bccc6-146">Код возврата</span><span class="sxs-lookup"><span data-stu-id="bccc6-146">Return code</span></span>                                                                                   | <span data-ttu-id="bccc6-147">Описание</span><span class="sxs-lookup"><span data-stu-id="bccc6-147">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bccc6-148"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-148"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="bccc6-149">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="bccc6-149">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="bccc6-150"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-150"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="bccc6-151">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="bccc6-151">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="bccc6-152"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-152"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="bccc6-153">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="bccc6-153">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="bccc6-154"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-154"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="bccc6-155">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="bccc6-155">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="bccc6-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bccc6-156">Remarks</span></span>

<span data-ttu-id="bccc6-157">Успешное выполнение команды может быть успешным при завершении выполнения предыдущих команд (например, проверка или выбор файла) или выбора (например, соответствующего секрета).</span><span class="sxs-lookup"><span data-stu-id="bccc6-157">The successful execution of the command may be subject to successful completion of prior commands (for example, VERIFY or SELECT FILE) or selections (for example, the relevant secret).</span></span>

<span data-ttu-id="bccc6-158">Если при выполнении команды в данный момент выбран ключ и алгоритм, то команда может неявно использовать ключ и алгоритм.</span><span class="sxs-lookup"><span data-stu-id="bccc6-158">If a key and an algorithm are currently selected when issuing the command, then the command may implicitly use the key and the algorithm.</span></span>

<span data-ttu-id="bccc6-159">Количество попыток выполнения команды может быть записано в карточке, чтобы ограничить количество дальнейших повторов использования соответствующего секрета или алгоритма.</span><span class="sxs-lookup"><span data-stu-id="bccc6-159">The number of times the command is issued may be recorded in the card to limit the number of further attempts of using the relevant secret or the algorithm.</span></span>

<span data-ttu-id="bccc6-160">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="bccc6-160">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="bccc6-161">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="bccc6-161">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="bccc6-162">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="bccc6-162">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bccc6-163">Требования</span><span class="sxs-lookup"><span data-stu-id="bccc6-163">Requirements</span></span>



| <span data-ttu-id="bccc6-164">Требование</span><span class="sxs-lookup"><span data-stu-id="bccc6-164">Requirement</span></span> | <span data-ttu-id="bccc6-165">Значение</span><span class="sxs-lookup"><span data-stu-id="bccc6-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bccc6-166">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bccc6-166">Minimum supported client</span></span><br/> | <span data-ttu-id="bccc6-167">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-167">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="bccc6-168">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bccc6-168">Minimum supported server</span></span><br/> | <span data-ttu-id="bccc6-169">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bccc6-169">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bccc6-170">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="bccc6-170">End of client support</span></span><br/>    | <span data-ttu-id="bccc6-171">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bccc6-171">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="bccc6-172">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="bccc6-172">End of server support</span></span><br/>    | <span data-ttu-id="bccc6-173">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bccc6-173">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="bccc6-174">Header</span><span class="sxs-lookup"><span data-stu-id="bccc6-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="bccc6-175"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-175"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bccc6-176">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="bccc6-176">Type library</span></span><br/>             | <dl> <span data-ttu-id="bccc6-177"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-177"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bccc6-178">DLL</span><span class="sxs-lookup"><span data-stu-id="bccc6-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bccc6-179"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bccc6-179"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bccc6-180">IID</span><span class="sxs-lookup"><span data-stu-id="bccc6-180">IID</span></span><br/>                      | <span data-ttu-id="bccc6-181">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="bccc6-181">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="bccc6-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bccc6-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bccc6-183">**екстерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="bccc6-183">**ExternalAuthenticate**</span></span>](iscardiso7816-externalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="bccc6-184">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="bccc6-184">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
