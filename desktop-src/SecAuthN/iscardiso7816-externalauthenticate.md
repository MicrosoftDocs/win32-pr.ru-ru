---
description: Конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая условно обновляет состояние безопасности, проверяя удостоверение компьютера, когда смарт-карта не доверяет ей.
ms.assetid: 6db063d5-48a7-4c8b-ae84-cbcf34edc79d
title: 'Метод ISCardISO7816:: Екстерналаусентикате (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ExternalAuthenticate
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 1c8d56b6f2210974bd86dbecea06f16b68548659
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423818"
---
# <a name="iscardiso7816externalauthenticate-method"></a><span data-ttu-id="7fe9c-103">Метод ISCardISO7816:: Екстерналаусентикате</span><span class="sxs-lookup"><span data-stu-id="7fe9c-103">ISCardISO7816::ExternalAuthenticate method</span></span>

<span data-ttu-id="7fe9c-104">\[Метод **екстерналаусентикате** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-104">\[The **ExternalAuthenticate** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7fe9c-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7fe9c-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="7fe9c-107">Метод **екстерналаусентикате** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая условно обновляет состояние безопасности, проверяя удостоверение компьютера, когда [*смарт-карта*](../secgloss/s-gly.md) не доверяет ей.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-107">The **ExternalAuthenticate** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that conditionally updates security status, verifying the identity of the computer when the [*smart card*](../secgloss/s-gly.md) does not trust it.</span></span>

<span data-ttu-id="7fe9c-108">В команде используется результат (да или нет) вычисления картой (в зависимости от запроса, ранее выданного картой, например \_ команды "получить \_ запрос"), ключа (возможно, секрета), сохраненного на карте, и данных проверки подлинности, передаваемых устройством интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-108">The command uses the result (yes or no) of the computation by the card (based on a challenge previously issued by the card, for example, by the INS\_GET\_CHALLENGE command), a key (possibly secret) stored in the card, and authentication data transmitted by the interface device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fe9c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fe9c-109">Syntax</span></span>


```C++
HRESULT ExternalAuthenticate(
  [in]      BYTE         byAlgorithmRef,
  [in]      BYTE         bySecretRef,
  [in]      LPBYTEBUFFER pChallenge,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="7fe9c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7fe9c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fe9c-111">*бялгорисмреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-111">*byAlgorithmRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe9c-112">Ссылка на алгоритм в карточке.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-112">The reference of the algorithm in the card.</span></span>

<span data-ttu-id="7fe9c-113">Если это значение равно нулю, это означает, что сведения не указаны.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-113">If this value is zero, this indicates that no information is given.</span></span> <span data-ttu-id="7fe9c-114">Ссылка на алгоритм известна либо перед выдачей команды, либо в поле данных.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-114">The reference of the algorithm is known either before issuing the command or is provided in the data field.</span></span>

</dd> <dt>

<span data-ttu-id="7fe9c-115">*бисекретреф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-115">*bySecretRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe9c-116">Ссылка на секрет.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-116">The reference of the secret.</span></span>



| <span data-ttu-id="7fe9c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe9c-117">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="7fe9c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe9c-118">Meaning</span></span>                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="7fe9c-119"><dt>**Нет сведений**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-119"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="7fe9c-120">Разрядное расположение: 00000000</span><span class="sxs-lookup"><span data-stu-id="7fe9c-120">Bit position: 00000000</span></span><br/> <span data-ttu-id="7fe9c-121">Сведения не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-121">No information is given.</span></span> <span data-ttu-id="7fe9c-122">Ссылка на секрет известен либо перед выдачей команды, либо в поле данных.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-122">The reference of the secret is known either before issuing the command or is provided in the data field.</span></span><br/> |
| <span id="Global_ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="7fe9c-123"><dt>**Глобальная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-123"><dt>**Global ref**</dt></span></span> </dl>         | <span data-ttu-id="7fe9c-124">Битовое расположение: 0-------</span><span class="sxs-lookup"><span data-stu-id="7fe9c-124">Bit position: 0-------</span></span><br/> <span data-ttu-id="7fe9c-125">Глобальные эталонные данные (ключ, определяемый протоколом MF).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-125">Global reference data (an MF specific key).</span></span><br/>                                                                                       |
| <span id="Specific_ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="7fe9c-126"><dt>**Конкретная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-126"><dt>**Specific ref**</dt></span></span> </dl> | <span data-ttu-id="7fe9c-127">Битовое расположение: 1-------</span><span class="sxs-lookup"><span data-stu-id="7fe9c-127">Bit position: 1-------</span></span><br/> <span data-ttu-id="7fe9c-128">Конкретные ссылочные данные (ключ, определяемый DF).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-128">Specific reference data (a DF specific key).</span></span><br/>                                                                                      |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="7fe9c-129"><dt>**рфу**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-129"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="7fe9c-130">Разрядное расположение:-XX-----</span><span class="sxs-lookup"><span data-stu-id="7fe9c-130">Bit position: -xx-----</span></span><br/> <span data-ttu-id="7fe9c-131">00 (другие значения — РФУ).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-131">00 (other values are RFU).</span></span><br/>                                                                                                        |
| <span id="Secret"></span><span id="secret"></span><span id="SECRET"></span><dl> <span data-ttu-id="7fe9c-132"><dt>**Владел**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-132"><dt>**Secret**</dt></span></span> </dl>                         | <span data-ttu-id="7fe9c-133">Разрядное расположение:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="7fe9c-133">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="7fe9c-134">Номер секрета.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-134">Number of the secret.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="7fe9c-135">*пчалленже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-135">*pChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe9c-136">Указатель на данные, связанные с проверкой подлинности.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-136">A pointer to the authentication-related data.</span></span> <span data-ttu-id="7fe9c-137">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-137">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7fe9c-138">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-138">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7fe9c-139">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-139">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="7fe9c-140">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-140">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="7fe9c-141">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренне и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="7fe9c-141">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fe9c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7fe9c-142">Return value</span></span>

<span data-ttu-id="7fe9c-143">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-143">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="7fe9c-144">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7fe9c-144">Return code</span></span>                                                                                   | <span data-ttu-id="7fe9c-145">Описание</span><span class="sxs-lookup"><span data-stu-id="7fe9c-145">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="7fe9c-146"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-146"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7fe9c-147">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-147">The operation completed successfully.</span></span><br/>     |
| <dl> <span data-ttu-id="7fe9c-148"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-148"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7fe9c-149">Передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-149">A parameter that is not valid was passed.</span></span><br/> |
| <dl> <span data-ttu-id="7fe9c-150"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-150"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7fe9c-151">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-151">A bad pointer was passed in.</span></span><br/>              |
| <dl> <span data-ttu-id="7fe9c-152"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-152"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7fe9c-153">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-153">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="7fe9c-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fe9c-154">Remarks</span></span>

<span data-ttu-id="7fe9c-155">Для успешного выполнения инкапсулированной команды последний запрос, полученный из карточки, должен быть допустимым.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-155">For the encapsulated command to be successful, the last challenge obtained from the card must be valid.</span></span>

<span data-ttu-id="7fe9c-156">Неудачные сравнения могут быть записаны на карту (например, чтобы ограничить число дальнейших попыток использования эталонных данных).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-156">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="7fe9c-157">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-157">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="7fe9c-158">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="7fe9c-158">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="7fe9c-159">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7fe9c-159">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7fe9c-160">Требования</span><span class="sxs-lookup"><span data-stu-id="7fe9c-160">Requirements</span></span>



| <span data-ttu-id="7fe9c-161">Требование</span><span class="sxs-lookup"><span data-stu-id="7fe9c-161">Requirement</span></span> | <span data-ttu-id="7fe9c-162">Значение</span><span class="sxs-lookup"><span data-stu-id="7fe9c-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fe9c-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fe9c-163">Minimum supported client</span></span><br/> | <span data-ttu-id="7fe9c-164">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-164">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7fe9c-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fe9c-165">Minimum supported server</span></span><br/> | <span data-ttu-id="7fe9c-166">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7fe9c-166">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7fe9c-167">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="7fe9c-167">End of client support</span></span><br/>    | <span data-ttu-id="7fe9c-168">Windows XP</span><span class="sxs-lookup"><span data-stu-id="7fe9c-168">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="7fe9c-169">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="7fe9c-169">End of server support</span></span><br/>    | <span data-ttu-id="7fe9c-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7fe9c-170">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="7fe9c-171">Header</span><span class="sxs-lookup"><span data-stu-id="7fe9c-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="7fe9c-172"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-172"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fe9c-173">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7fe9c-173">Type library</span></span><br/>             | <dl> <span data-ttu-id="7fe9c-174"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-174"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7fe9c-175">DLL</span><span class="sxs-lookup"><span data-stu-id="7fe9c-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fe9c-176"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fe9c-176"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7fe9c-177">IID</span><span class="sxs-lookup"><span data-stu-id="7fe9c-177">IID</span></span><br/>                      | <span data-ttu-id="7fe9c-178">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="7fe9c-178">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="7fe9c-179">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fe9c-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fe9c-180">**интерналаусентикате**</span><span class="sxs-lookup"><span data-stu-id="7fe9c-180">**InternalAuthenticate**</span></span>](iscardiso7816-internalauthenticate.md)
</dt> <dt>

[<span data-ttu-id="7fe9c-181">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="7fe9c-181">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
