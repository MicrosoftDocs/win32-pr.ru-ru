---
description: Метод Манажечаннел создает команду блока данных протокола приложения (КАТЕГОРИЯХ APDU), которая открывает и закрывает логические каналы.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'Метод ISCardISO7816:: Манажечаннел (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080594"
---
# <a name="iscardiso7816managechannel-method"></a><span data-ttu-id="9853d-103">Метод ISCardISO7816:: Манажечаннел</span><span class="sxs-lookup"><span data-stu-id="9853d-103">ISCardISO7816::ManageChannel method</span></span>

<span data-ttu-id="9853d-104">\[Метод **манажечаннел** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9853d-104">\[The **ManageChannel** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9853d-105">Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы.</span><span class="sxs-lookup"><span data-stu-id="9853d-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9853d-106">[Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]</span><span class="sxs-lookup"><span data-stu-id="9853d-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9853d-107">Метод **манажечаннел** создает команду [*блока данных протокола приложения*](../secgloss/a-gly.md) (категориях APDU), которая открывает и закрывает логические каналы.</span><span class="sxs-lookup"><span data-stu-id="9853d-107">The **ManageChannel** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that opens and closes logical channels.</span></span>

<span data-ttu-id="9853d-108">Функция Open открывает новый логический канал, отличный от основного.</span><span class="sxs-lookup"><span data-stu-id="9853d-108">The open function opens a new logical channel other than the basic one.</span></span> <span data-ttu-id="9853d-109">Для карты можно назначить номер логического канала или указать номер логического канала, который будет предоставлен карте.</span><span class="sxs-lookup"><span data-stu-id="9853d-109">Options are provided for the card to assign a logical channel number, or for the logical channel number to be supplied to the card.</span></span>

<span data-ttu-id="9853d-110">Функция Close явным образом закрывает логический канал, отличный от базового.</span><span class="sxs-lookup"><span data-stu-id="9853d-110">The close function explicitly closes a logical channel other than the basic one.</span></span> <span data-ttu-id="9853d-111">После успешного закрытия логический канал должен быть доступен для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="9853d-111">After the successful closing, the logical channel shall be available for re-use.</span></span>

## <a name="syntax"></a><span data-ttu-id="9853d-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9853d-112">Syntax</span></span>


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="9853d-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="9853d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9853d-114">*бичаннелстате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9853d-114">*byChannelState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9853d-115">Bit B8 P1 используется для указания функции Open или функции Close; Если B8 имеет значение 0, то Управление КАНАЛом должно открыть логический канал, а если B8 — 1, то Управление КАНАЛом должно закрывать логический канал:</span><span class="sxs-lookup"><span data-stu-id="9853d-115">Bit b8 of P1 is used to indicate the open function or the close function; if b8 is 0, then MANAGE CHANNEL shall open a logical channel and if b8 is 1, then MANAGE CHANNEL shall close a logical channel:</span></span>

<span data-ttu-id="9853d-116">P1 = "00" для открытия</span><span class="sxs-lookup"><span data-stu-id="9853d-116">P1 = '00' to open</span></span>

<span data-ttu-id="9853d-117">P1 = ' 80 ' для закрытия</span><span class="sxs-lookup"><span data-stu-id="9853d-117">P1 = '80' to close</span></span>

<span data-ttu-id="9853d-118">Другие значения — РФУ</span><span class="sxs-lookup"><span data-stu-id="9853d-118">Other values are RFU</span></span>

</dd> <dt>

<span data-ttu-id="9853d-119">*бичаннел* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9853d-119">*byChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9853d-120">Для функции Open (P1 = ' 00 ') биты B1 и B2 в P2 используются для кодирования номера логического канала таким же образом, как в байте класса, остальные биты P2 — это РФУ.</span><span class="sxs-lookup"><span data-stu-id="9853d-120">For the open function (P1 = '00'), the bits b1 and b2 of P2 are used to code the logical channel number in the same manner as in the class byte, the other bits of P2 are RFU.</span></span>

<span data-ttu-id="9853d-121">Если значения B1 и B2 для p2 равны **null**, то карта присвоит номер логического канала, который будет возвращен в битах B1 и B2 поля данных.</span><span class="sxs-lookup"><span data-stu-id="9853d-121">When b1 and b2 of P2 are **NULL**, then the card will assign a logical channel number that will be returned in bits b1 and b2 of the data field.</span></span>

<span data-ttu-id="9853d-122">Если B1 и/или B2 в P2 не равны **null**, они направляют логический номер канала, отличный от базового. затем карточка будет открывать внешний назначенный номер логического канала.</span><span class="sxs-lookup"><span data-stu-id="9853d-122">When b1 and/or b2 of P2 are not **NULL**, they code a logical channel number other than the basic one; then the card will open the externally assigned logical channel number.</span></span>

</dd> <dt>

<span data-ttu-id="9853d-123">*ппкмд* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9853d-123">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9853d-124">На входе — указатель на объект интерфейса [**искардкмд**](iscardcmd.md) или **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="9853d-124">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="9853d-125">При возвращении он заполняется командой КАТЕГОРИЯХ APDU, созданной этой операцией.</span><span class="sxs-lookup"><span data-stu-id="9853d-125">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="9853d-126">Если для *ппкмд* было задано **значение NULL**, то объект [*смарт-карты*](../secgloss/s-gly.md) [**искардкмд**](iscardcmd.md) создается внутренним образом и возвращается с помощью указателя *ппкмд* .</span><span class="sxs-lookup"><span data-stu-id="9853d-126">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9853d-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9853d-127">Return value</span></span>

<span data-ttu-id="9853d-128">Метод возвращает одно из следующих возможных значений.</span><span class="sxs-lookup"><span data-stu-id="9853d-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9853d-129">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9853d-129">Return code</span></span>                                                                                   | <span data-ttu-id="9853d-130">Описание</span><span class="sxs-lookup"><span data-stu-id="9853d-130">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9853d-131"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9853d-132">Operation completed successfully (Операция выполнена успешно).</span><span class="sxs-lookup"><span data-stu-id="9853d-132">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9853d-133"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9853d-134">Недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="9853d-134">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9853d-135"><dt>**\_указатель E**</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9853d-136">Передан неверный указатель.</span><span class="sxs-lookup"><span data-stu-id="9853d-136">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9853d-137"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9853d-138">Недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="9853d-138">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9853d-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9853d-139">Remarks</span></span>

<span data-ttu-id="9853d-140">Когда функция Open успешно выполняется из базового логического канала, необходимо неявно выбрать MF в качестве текущей DF, а состояние безопасности нового логического канала должно совпадать с базовым логическим каналом после ATR.</span><span class="sxs-lookup"><span data-stu-id="9853d-140">When the open function is successfully performed from the basic logical channel, the MF shall be implicitly selected as the current DF and the security status of the new logical channel should be the same as the basic logical channel after ATR.</span></span> <span data-ttu-id="9853d-141">Состояние безопасности нового логического канала должно быть отдельно от другого логического канала.</span><span class="sxs-lookup"><span data-stu-id="9853d-141">The security status of the new logical channel should be separate from that of any other logical channel.</span></span>

<span data-ttu-id="9853d-142">Когда функция Open успешно выполняется из логического канала, который не является базовым, текущий DF логического канала, выдавшего команду, будет выбрана в качестве текущей DF.</span><span class="sxs-lookup"><span data-stu-id="9853d-142">When the open function is successfully performed from a logical channel, which is not the basic one, the current DF of the logical channel that issued the command will be selected as the current DF.</span></span> <span data-ttu-id="9853d-143">Кроме того, состояние безопасности для нового логического канала должно совпадать с состоянием безопасности логического канала, из которого была выполнена функция Open.</span><span class="sxs-lookup"><span data-stu-id="9853d-143">In addition, the security status for the new logical channel should be the same as the security status of the logical channel from which the open function was performed.</span></span>

<span data-ttu-id="9853d-144">После успешного завершения функции закрытия состояние безопасности, связанное с этим логическим каналом, будет потеряно.</span><span class="sxs-lookup"><span data-stu-id="9853d-144">After a successful close function, the security status related to this logical channel is lost.</span></span>

<span data-ttu-id="9853d-145">Список всех методов, предоставляемых этим интерфейсом, см. в разделе [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="9853d-145">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="9853d-146">Кроме приведенных выше кодов ошибок COM, этот интерфейс может возвращать код ошибки смарт-карты, если для завершения запроса была вызвана функция смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="9853d-146">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9853d-147">Дополнительные сведения см. в статье [возвращаемые значения смарт-карты](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9853d-147">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9853d-148">Требования</span><span class="sxs-lookup"><span data-stu-id="9853d-148">Requirements</span></span>



| <span data-ttu-id="9853d-149">Требование</span><span class="sxs-lookup"><span data-stu-id="9853d-149">Requirement</span></span> | <span data-ttu-id="9853d-150">Значение</span><span class="sxs-lookup"><span data-stu-id="9853d-150">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9853d-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9853d-151">Minimum supported client</span></span><br/> | <span data-ttu-id="9853d-152">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="9853d-152">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9853d-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9853d-153">Minimum supported server</span></span><br/> | <span data-ttu-id="9853d-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9853d-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9853d-155">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9853d-155">End of client support</span></span><br/>    | <span data-ttu-id="9853d-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9853d-156">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9853d-157">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9853d-157">End of server support</span></span><br/>    | <span data-ttu-id="9853d-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9853d-158">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9853d-159">Header</span><span class="sxs-lookup"><span data-stu-id="9853d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="9853d-160"><dt>Скардссп. h</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-160"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9853d-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="9853d-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="9853d-162"><dt>Скардсрв. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-162"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9853d-163">DLL</span><span class="sxs-lookup"><span data-stu-id="9853d-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9853d-164"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9853d-164"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9853d-165">IID</span><span class="sxs-lookup"><span data-stu-id="9853d-165">IID</span></span><br/>                      | <span data-ttu-id="9853d-166">IID \_ ISCardISO7816 определен как 53B6AA68-3F56-11D0-916B-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="9853d-166">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9853d-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9853d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9853d-168">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="9853d-168">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> </dl>

 

 
