---
description: Происходит, когда рукописный коллекто ррецеивес пакет.
ms.assetid: 26d5a3eb-430a-4e21-8a3f-fdec5005cd6e
title: Событие InkOverlay. Невпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43743b47d007b44d4f2460266e7198266c36afd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272313"
---
# <a name="inkoverlaynewpackets-event"></a><span data-ttu-id="842c4-103">Событие InkOverlay. Невпаккетс</span><span class="sxs-lookup"><span data-stu-id="842c4-103">InkOverlay.NewPackets event</span></span>

<span data-ttu-id="842c4-104">Происходит, когда рукописный коллекто ррецеивес пакет</span><span class="sxs-lookup"><span data-stu-id="842c4-104">Occurs when the ink collecto rreceives a packet</span></span>

## <a name="syntax"></a><span data-ttu-id="842c4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="842c4-105">Syntax</span></span>


```C++
void NewPackets(
  [in]      IInkCursor     *Cursor,
  [in]      IInkStrokeDisp *Stroke,
  [in]      long           PacketCount,
  [in, out] VARIANT        *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="842c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="842c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="842c4-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="842c4-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842c4-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**невинаирпаккетс**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="842c4-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="842c4-109">*Штриховая линия* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="842c4-109">*Stroke* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842c4-110">Указывает объект [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="842c4-110">Specifies the [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="842c4-111">*Паккеткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="842c4-111">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842c4-112">Число пакетов, полученных для объекта [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) .</span><span class="sxs-lookup"><span data-stu-id="842c4-112">The number of packets received for a [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object.</span></span>

</dd> <dt>

<span data-ttu-id="842c4-113">*Паккетдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="842c4-113">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="842c4-114">Массив, содержащий выбранные данные для пакета.</span><span class="sxs-lookup"><span data-stu-id="842c4-114">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="842c4-115">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="842c4-115">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="842c4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="842c4-116">Return value</span></span>

<span data-ttu-id="842c4-117">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="842c4-117">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="842c4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="842c4-118">Remarks</span></span>

<span data-ttu-id="842c4-119">Пакеты получаются, пока выполняется сбор рукописных фрагментов.</span><span class="sxs-lookup"><span data-stu-id="842c4-119">Packets are received while a stroke is being collected.</span></span> <span data-ttu-id="842c4-120">События пакетов происходят быстро, а обработчик событий [**невпаккетс**](inkcollector-newpackets.md) должен быть быстрым или отрицательным.</span><span class="sxs-lookup"><span data-stu-id="842c4-120">Packet events occur rapidly, and a [**NewPackets**](inkcollector-newpackets.md) event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="842c4-121">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ иценевпаккетс.</span><span class="sxs-lookup"><span data-stu-id="842c4-121">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewPackets.</span></span>

<span data-ttu-id="842c4-122">Это событие следует использовать осторожно, так как оно может оказать негативное воздействие на производительность рукописного ввода, если в обработчиках событий выполняется слишком много кода.</span><span class="sxs-lookup"><span data-stu-id="842c4-122">This event should be used carefully as it could have an adverse effect on ink performance if too much code is executed in the event handlers.</span></span>

<span data-ttu-id="842c4-123">Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="842c4-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="842c4-124">Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="842c4-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="842c4-125">Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.</span><span class="sxs-lookup"><span data-stu-id="842c4-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="842c4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="842c4-126">Requirements</span></span>



| <span data-ttu-id="842c4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="842c4-127">Requirement</span></span> | <span data-ttu-id="842c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="842c4-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="842c4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="842c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="842c4-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="842c4-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="842c4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="842c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="842c4-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="842c4-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="842c4-133">Header</span><span class="sxs-lookup"><span data-stu-id="842c4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="842c4-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="842c4-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="842c4-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="842c4-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="842c4-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="842c4-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="842c4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="842c4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842c4-138">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="842c4-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="842c4-139">**Событие Невинаирпаккетс**</span><span class="sxs-lookup"><span data-stu-id="842c4-139">**NewInAirPackets Event**</span></span>](inkcollector-newinairpackets.md)
</dt> <dt>

[<span data-ttu-id="842c4-140">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="842c4-140">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> <dt>

[<span data-ttu-id="842c4-141">**Интерфейс Иинкстрокедисп**</span><span class="sxs-lookup"><span data-stu-id="842c4-141">**IInkStrokeDisp Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)
</dt> </dl>

 

 




