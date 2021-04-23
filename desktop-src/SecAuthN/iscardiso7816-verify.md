---
description: Конструирует команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая инициирует сравнение (в карточке) данных проверки, отправляемых с устройства интерфейса, ссылочными данными, хранящимися на карте (например, Password).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'Метод ISCardISO7816:: Verify (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650878"
---
# <a name="iscardiso7816verify-method"></a><span data-ttu-id="8ec4e-103">Метод ISCardISO7816:: Verify</span><span class="sxs-lookup"><span data-stu-id="8ec4e-103">ISCardISO7816::Verify method</span></span>

<span data-ttu-id="8ec4e-104">\[Метод **Verify** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8ec4e-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8ec4e-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8ec4e-107">Метод **Verify** конструирует команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая инициирует сравнение (в карточке) данных проверки, отправляемых с устройства интерфейса, ссылочными данными, хранящимися на карте (например, Password).</span><span class="sxs-lookup"><span data-stu-id="8ec4e-107">The **Verify** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that initiates the comparison (in the card) of the verification data sent from the interface device with the reference data stored in the card (for example, password).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ec4e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ec4e-108">Syntax</span></span>


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="8ec4e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ec4e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ec4e-110">*бирефктрл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-110">*byRefCtrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4e-111">Квантификатор ссылочных данных.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-111">A quantifier of the reference data.</span></span> <span data-ttu-id="8ec4e-112">Кодирование элемента управления ссылки P2 выполняется следующим образом.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-112">Coding of the reference control P2 follows.</span></span>

<span data-ttu-id="8ec4e-113">Если тело пусто, команда может быть использована для получения числа «X» последующих разрешенных повторных попыток (SW1-SW2 = 63CX) или для проверки необязательности проверки (SW1-SW2 = 9000).</span><span class="sxs-lookup"><span data-stu-id="8ec4e-113">When the body is empty, the command may be used either to retrieve the number 'X' of further allowed retries (SW1-SW2=63CX) or to check whether the verification is not required (SW1-SW2=9000).</span></span>



| <span data-ttu-id="8ec4e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec4e-114">Value</span></span>                                                                                                                                                                                    | <span data-ttu-id="8ec4e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec4e-115">Meaning</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <span data-ttu-id="8ec4e-116"><dt>**Нет сведений**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-116"><dt>**No Info**</dt></span></span> </dl>                     | <span data-ttu-id="8ec4e-117">Разрядное расположение: 00000000</span><span class="sxs-lookup"><span data-stu-id="8ec4e-117">Bit position: 00000000</span></span><br/> <span data-ttu-id="8ec4e-118">P2 = 00 зарезервировано, чтобы указать, что в этих картах не используется какой-либо конкретный квалификатор, в котором команда Verify ссылается на секретные данные неоднозначно.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-118">P2=00 is reserved to indicate that no particular qualifier is used in those cards where the verify command references the secret data unambiguously.</span></span><br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <span data-ttu-id="8ec4e-119"><dt>**Глобальная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-119"><dt>**Global Ref**</dt></span></span> </dl>         | <span data-ttu-id="8ec4e-120">Битовое расположение: 0-------</span><span class="sxs-lookup"><span data-stu-id="8ec4e-120">Bit position: 0-------</span></span><br/> <span data-ttu-id="8ec4e-121">Примером глобальной ссылки будет пароль.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-121">An example of Global Ref would be a password.</span></span><br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <span data-ttu-id="8ec4e-122"><dt>**Конкретная ссылка**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-122"><dt>**Specific Ref**</dt></span></span> </dl> | <span data-ttu-id="8ec4e-123">Битовое расположение: 1-------</span><span class="sxs-lookup"><span data-stu-id="8ec4e-123">Bit position: 1-------</span></span><br/> <span data-ttu-id="8ec4e-124">Примером конкретной ссылки является пароль, определяемый DF.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-124">An example of Specific Ref is DF specific password.</span></span><br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <span data-ttu-id="8ec4e-125"><dt>**рфу**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-125"><dt>**RFU**</dt></span></span> </dl>                                                           | <span data-ttu-id="8ec4e-126">Разрядное расположение:-XX-----</span><span class="sxs-lookup"><span data-stu-id="8ec4e-126">Bit position: -xx-----</span></span><br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <span data-ttu-id="8ec4e-127"><dt>**Ссылочные данные \#**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-127"><dt>**Ref Data \#**</dt></span></span> </dl>        | <span data-ttu-id="8ec4e-128">Разрядное расположение:---XXXXX</span><span class="sxs-lookup"><span data-stu-id="8ec4e-128">Bit position: ---xxxxx</span></span><br/> <span data-ttu-id="8ec4e-129">Номер ссылочных данных может быть, например, номером пароля или коротким идентификатором EF.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-129">The reference data number may be, for example, a password number or a short EF identifier.</span></span><br/>                                                           |



 

</dd> <dt>

<span data-ttu-id="8ec4e-130">*pData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-130">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4e-131">Указатель на проверочные данные.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-131">A pointer to the verification data.</span></span> <span data-ttu-id="8ec4e-132">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-132">This parameter can be **NULL**.</span></span> <span data-ttu-id="8ec4e-133">Значение по умолчанию — **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-133">The default value is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8ec4e-134">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-134">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ec4e-135">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-135">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="8ec4e-136">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-136">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="8ec4e-137">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренне и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="8ec4e-137">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned by using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ec4e-138">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ec4e-138">Return value</span></span>

<span data-ttu-id="8ec4e-139">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8ec4e-140">Код возврата</span><span class="sxs-lookup"><span data-stu-id="8ec4e-140">Return code</span></span>                                                                                   | <span data-ttu-id="8ec4e-141">Описание</span><span class="sxs-lookup"><span data-stu-id="8ec4e-141">Description</span></span>                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="8ec4e-142"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8ec4e-143">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-143">The operation completed successfully.</span></span><br/>   |
| <dl> <span data-ttu-id="8ec4e-144"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8ec4e-145">Использован недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-145">A parameter that is not valid was used.</span></span><br/> |
| <dl> <span data-ttu-id="8ec4e-146"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8ec4e-147">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-147">A bad pointer was passed in.</span></span><br/>            |
| <dl> <span data-ttu-id="8ec4e-148"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8ec4e-149">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-149">Out of memory.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="8ec4e-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ec4e-150">Remarks</span></span>

<span data-ttu-id="8ec4e-151">Состояние безопасности может быть изменено в результате сравнения.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-151">The security status may be modified as a result of a comparison.</span></span> <span data-ttu-id="8ec4e-152">Неудачные сравнения могут быть записаны на карту (например, чтобы ограничить число дальнейших попыток использования эталонных данных).</span><span class="sxs-lookup"><span data-stu-id="8ec4e-152">Unsuccessful comparisons may be recorded in the card (for example, to limit the number of further attempts of the use of the reference data).</span></span>

<span data-ttu-id="8ec4e-153">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="8ec4e-153">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="8ec4e-154">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="8ec4e-154">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8ec4e-155">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="8ec4e-155">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8ec4e-156">Требования</span><span class="sxs-lookup"><span data-stu-id="8ec4e-156">Requirements</span></span>



| <span data-ttu-id="8ec4e-157">Требование</span><span class="sxs-lookup"><span data-stu-id="8ec4e-157">Requirement</span></span> | <span data-ttu-id="8ec4e-158">Значение</span><span class="sxs-lookup"><span data-stu-id="8ec4e-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ec4e-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ec4e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="8ec4e-160">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-160">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8ec4e-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ec4e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="8ec4e-162">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8ec4e-162">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8ec4e-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8ec4e-163">End of client support</span></span><br/>    | <span data-ttu-id="8ec4e-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8ec4e-164">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="8ec4e-165">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8ec4e-165">End of server support</span></span><br/>    | <span data-ttu-id="8ec4e-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8ec4e-166">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="8ec4e-167">Header</span><span class="sxs-lookup"><span data-stu-id="8ec4e-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ec4e-168"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-168"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ec4e-169">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="8ec4e-169">Type library</span></span><br/>             | <dl> <span data-ttu-id="8ec4e-170"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-170"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8ec4e-171">DLL</span><span class="sxs-lookup"><span data-stu-id="8ec4e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ec4e-172"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ec4e-172"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8ec4e-173">IID</span><span class="sxs-lookup"><span data-stu-id="8ec4e-173">IID</span></span><br/>                      | <span data-ttu-id="8ec4e-174">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="8ec4e-174">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="8ec4e-175">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ec4e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec4e-176">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="8ec4e-176">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
