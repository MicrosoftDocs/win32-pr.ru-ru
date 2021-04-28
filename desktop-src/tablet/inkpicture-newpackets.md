---
description: Событие InkPicture. Невпаккетс — происходит, когда сборщик рукописных данных получает пакет.
ms.assetid: 7d120198-c016-4452-b8a8-22c4ad87d526
title: Событие InkPicture. Невпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194fb9bffae07cca561fbfc11ff8a185d63bb9e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086482"
---
# <a name="inkpicturenewpackets-event"></a><span data-ttu-id="17d1a-103">Событие InkPicture. Невпаккетс</span><span class="sxs-lookup"><span data-stu-id="17d1a-103">InkPicture.NewPackets event</span></span>

<span data-ttu-id="17d1a-104">Происходит, когда сборщик рукописных данных получает пакет.</span><span class="sxs-lookup"><span data-stu-id="17d1a-104">Occurs when the ink collector receives a packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="17d1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17d1a-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="17d1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="17d1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17d1a-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17d1a-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d1a-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**невинаирпаккетс**](inkpicture-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="17d1a-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkpicture-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="17d1a-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17d1a-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d1a-110">Объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="17d1a-110">The [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="17d1a-111">*Паккеткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="17d1a-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17d1a-112">Число пакетов, полученных для объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="17d1a-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="17d1a-113">*Паккетдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="17d1a-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="17d1a-114">Массив, содержащий выбранные данные для пакета.</span><span class="sxs-lookup"><span data-stu-id="17d1a-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="17d1a-115">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="17d1a-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17d1a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17d1a-116">Return value</span></span>

<span data-ttu-id="17d1a-117">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="17d1a-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17d1a-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="17d1a-118">Remarks</span></span>

<span data-ttu-id="17d1a-119">Пакеты получаются, пока выполняется сбор рукописных фрагментов.</span><span class="sxs-lookup"><span data-stu-id="17d1a-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="17d1a-120">События пакетов происходят быстро, а обработчик событий **невпаккетс** должен быть быстрым или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="17d1a-120">Packet events occur rapidly, and a **NewPackets** event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="17d1a-121">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ иценевпаккетс.</span><span class="sxs-lookup"><span data-stu-id="17d1a-121">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="17d1a-122">Это событие следует использовать осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.</span><span class="sxs-lookup"><span data-stu-id="17d1a-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="17d1a-123">Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="17d1a-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="17d1a-124">Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="17d1a-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="17d1a-125">Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.</span><span class="sxs-lookup"><span data-stu-id="17d1a-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="17d1a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="17d1a-126">Requirements</span></span>



| <span data-ttu-id="17d1a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="17d1a-127">Requirement</span></span> | <span data-ttu-id="17d1a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="17d1a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d1a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17d1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="17d1a-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="17d1a-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="17d1a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17d1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="17d1a-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="17d1a-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="17d1a-133">Header</span><span class="sxs-lookup"><span data-stu-id="17d1a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="17d1a-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="17d1a-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="17d1a-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="17d1a-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="17d1a-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17d1a-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="17d1a-137">См. также</span><span class="sxs-lookup"><span data-stu-id="17d1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17d1a-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="17d1a-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="17d1a-139">**Событие Невинаирпаккетс**</span><span class="sxs-lookup"><span data-stu-id="17d1a-139">**NewInAirPackets Event**</span></span>](inkpicture-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="17d1a-140">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="17d1a-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="17d1a-141">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="17d1a-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




