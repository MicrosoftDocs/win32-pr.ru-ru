---
description: '\_Константы побитового флага линемедиаконтрол описывают набор универсальных операций с потоками мультимедиа.'
ms.assetid: 1e8aeda8-2810-462a-bfba-0296d854d9aa
title: Константы LINEMEDIACONTROL_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3241a3b5f4f8a0363f30ce7aefaded0c63fc4189
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689120"
---
# <a name="linemediacontrol_-constants"></a><span data-ttu-id="b099d-103">\_Константы линемедиаконтрол</span><span class="sxs-lookup"><span data-stu-id="b099d-103">LINEMEDIACONTROL\_ Constants</span></span>

<span data-ttu-id="b099d-104">Константы побитового флага **линемедиаконтрол \_** описывают набор универсальных операций с потоками мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-104">The **LINEMEDIACONTROL\_** bit-flag constants describe a set of generic operations on media streams.</span></span> <span data-ttu-id="b099d-105">Интерпретация определяется потоком мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-105">The interpretations are determined by the media stream.</span></span> <span data-ttu-id="b099d-106">Для того чтобы любая операция управления мультимедиа действовала, устройство должно иметь возможность управления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-106">The line device must have the media-control capability for any media-control operation to be effective.</span></span>

<dl> <dt>

<span data-ttu-id="b099d-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ None**</span><span class="sxs-lookup"><span data-stu-id="b099d-107"><span id="LINEMEDIACONTROL_NONE"></span><span id="linemediacontrol_none"></span>**LINEMEDIACONTROL\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-108">В поток мультимедиа не вносятся изменения.</span><span class="sxs-lookup"><span data-stu-id="b099d-108">No change is to be made to the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**Приостановка ЛИНЕМЕДИАКОНТРОЛ \_**</span><span class="sxs-lookup"><span data-stu-id="b099d-109"><span id="LINEMEDIACONTROL_PAUSE"></span><span id="linemediacontrol_pause"></span>**LINEMEDIACONTROL\_PAUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-110">Временная приостановка потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-110">Temporarily pause the media stream.</span></span>

<span data-ttu-id="b099d-111">Скорость потока мультимедиа возвращается в нормальный режим.</span><span class="sxs-lookup"><span data-stu-id="b099d-111">The speed of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратедовн**</span><span class="sxs-lookup"><span data-stu-id="b099d-112"><span id="LINEMEDIACONTROL_RATEDOWN"></span><span id="linemediacontrol_ratedown"></span>**LINEMEDIACONTROL\_RATEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-113">Скорость потока мультимедиа уменьшается по количеству, определяемому потоком.</span><span class="sxs-lookup"><span data-stu-id="b099d-113">The speed of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратенормал**</span><span class="sxs-lookup"><span data-stu-id="b099d-114"><span id="LINEMEDIACONTROL_RATENORMAL"></span><span id="linemediacontrol_ratenormal"></span>**LINEMEDIACONTROL\_RATENORMAL**</span></span>
</dt> <dd> <dl> <dt>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ ратеуп**</span><span class="sxs-lookup"><span data-stu-id="b099d-115"><span id="LINEMEDIACONTROL_RATEUP"></span><span id="linemediacontrol_rateup"></span>**LINEMEDIACONTROL\_RATEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-116">Скорость потока мультимедиа увеличивается на определенное потоком количество.</span><span class="sxs-lookup"><span data-stu-id="b099d-116">The speed of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**\_Сброс линемедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="b099d-117"><span id="LINEMEDIACONTROL_RESET"></span><span id="linemediacontrol_reset"></span>**LINEMEDIACONTROL\_RESET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-118">Сбросьте поток мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-118">Reset the media stream.</span></span> <span data-ttu-id="b099d-119">Эквивалент конца входных данных.</span><span class="sxs-lookup"><span data-stu-id="b099d-119">Equivalent to an end-of-input.</span></span> <span data-ttu-id="b099d-120">Освобождаются все буферы.</span><span class="sxs-lookup"><span data-stu-id="b099d-120">All buffers are released.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**возобновление ЛИНЕМЕДИАКОНТРОЛ \_**</span><span class="sxs-lookup"><span data-stu-id="b099d-121"><span id="LINEMEDIACONTROL_RESUME"></span><span id="linemediacontrol_resume"></span>**LINEMEDIACONTROL\_RESUME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-122">Возобновление приостановленного потока мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-122">Resume a paused media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**\_Запуск линемедиаконтрол**</span><span class="sxs-lookup"><span data-stu-id="b099d-123"><span id="LINEMEDIACONTROL_START"></span><span id="linemediacontrol_start"></span>**LINEMEDIACONTROL\_START**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-124">Запустите поток мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-124">Start the media stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волумедовн**</span><span class="sxs-lookup"><span data-stu-id="b099d-125"><span id="LINEMEDIACONTROL_VOLUMEDOWN"></span><span id="linemediacontrol_volumedown"></span>**LINEMEDIACONTROL\_VOLUMEDOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-126">Амплитуда потока мультимедиа уменьшается на определенное потоком количество.</span><span class="sxs-lookup"><span data-stu-id="b099d-126">The amplitude of the media stream is decreased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волуменормал**</span><span class="sxs-lookup"><span data-stu-id="b099d-127"><span id="LINEMEDIACONTROL_VOLUMENORMAL"></span><span id="linemediacontrol_volumenormal"></span>**LINEMEDIACONTROL\_VOLUMENORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-128">Амплитуда потока мультимедиа возвращается в нормальный режим.</span><span class="sxs-lookup"><span data-stu-id="b099d-128">The amplitude of the media stream is returned to normal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b099d-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**ЛИНЕМЕДИАКОНТРОЛ \_ волумеуп**</span><span class="sxs-lookup"><span data-stu-id="b099d-129"><span id="LINEMEDIACONTROL_VOLUMEUP"></span><span id="linemediacontrol_volumeup"></span>**LINEMEDIACONTROL\_VOLUMEUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b099d-130">Амплитуда потока мультимедиа увеличивается на определенное потоком количество.</span><span class="sxs-lookup"><span data-stu-id="b099d-130">The amplitude of the media stream is increased by some stream-defined quantity.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b099d-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b099d-131">Remarks</span></span>

<span data-ttu-id="b099d-132">Старшие 16 бит можно назначить для расширений для конкретных устройств.</span><span class="sxs-lookup"><span data-stu-id="b099d-132">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="b099d-133">16 младших разрядов зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b099d-133">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="b099d-134">Управление носителями обеспечивает повышение производительности действий в потоках мультимедиа в ответ на связанные с телефонами события.</span><span class="sxs-lookup"><span data-stu-id="b099d-134">Media control is provided to improve performance of actions on media streams in response to telephony-related events.</span></span> <span data-ttu-id="b099d-135">Приложение обычно управляет потоком мультимедиа с помощью API-интерфейса для конкретного носителя.</span><span class="sxs-lookup"><span data-stu-id="b099d-135">The application should normally manage a media stream through the media-specific API.</span></span> <span data-ttu-id="b099d-136">Функции управления мультимедиа, предоставляемые здесь, не предназначены для замены собственных API-интерфейсов мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="b099d-136">The media-control functionality provided here is not intended to replace the native media APIs.</span></span>

<span data-ttu-id="b099d-137">Действия управления мультимедиа могут быть связаны с обнаружением цифр, обнаружением тонов, переходом в состояние вызова и обнаружением типа носителя.</span><span class="sxs-lookup"><span data-stu-id="b099d-137">Media-control actions can be associated with the detection of digits, the detection of tones, the transition into a call state, and the detection of a media type.</span></span> <span data-ttu-id="b099d-138">Ознакомьтесь с возможностями устройства линии, чтобы определить, доступен ли элемент управления мультимедиа в строке.</span><span class="sxs-lookup"><span data-stu-id="b099d-138">Consult a line's device capabilities to determine whether media control is available on the line.</span></span>

## <a name="requirements"></a><span data-ttu-id="b099d-139">Требования</span><span class="sxs-lookup"><span data-stu-id="b099d-139">Requirements</span></span>



| <span data-ttu-id="b099d-140">Требование</span><span class="sxs-lookup"><span data-stu-id="b099d-140">Requirement</span></span> | <span data-ttu-id="b099d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="b099d-141">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b099d-142">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b099d-142">TAPI version</span></span><br/> | <span data-ttu-id="b099d-143">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b099d-143">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b099d-144">Header</span><span class="sxs-lookup"><span data-stu-id="b099d-144">Header</span></span><br/>       | <dl> <span data-ttu-id="b099d-145"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b099d-145"><dt>Tapi.h</dt></span></span> </dl> |



 

 




