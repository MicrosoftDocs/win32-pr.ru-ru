---
description: Происходит при обнаружении пакета в эфире.
ms.assetid: 10dc1909-bfbc-4ea0-b77a-e33149205107
title: Событие InkOverlay. Невинаирпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ac030a2e32ecf662d811a3c91ccdc2dd3c5fd03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104266157"
---
# <a name="inkoverlaynewinairpackets-event"></a><span data-ttu-id="c9fb1-103">Событие InkOverlay. Невинаирпаккетс</span><span class="sxs-lookup"><span data-stu-id="c9fb1-103">InkOverlay.NewInAirPackets event</span></span>

<span data-ttu-id="c9fb1-104">Происходит при обнаружении пакета в эфире.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9fb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9fb1-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="c9fb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9fb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9fb1-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9fb1-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fb1-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие [**невинаирпаккетс**](inkcollector-newinairpackets.md) .</span><span class="sxs-lookup"><span data-stu-id="c9fb1-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the [**NewInAirPackets**](inkcollector-newinairpackets.md) event.</span></span>

</dd> <dt>

<span data-ttu-id="c9fb1-109">*Паккеткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9fb1-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fb1-110">Число полученных пакетов в сети Air.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="c9fb1-111">*Паккетдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="c9fb1-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9fb1-112">Массив, содержащий выбранные данные для пакета.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="c9fb1-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="c9fb1-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9fb1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9fb1-114">Return value</span></span>

<span data-ttu-id="c9fb1-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9fb1-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c9fb1-116">Remarks</span></span>

<span data-ttu-id="c9fb1-117">Пакет в эфире создается, когда пользователь перемещает перо рядом с планшетом, а курсор находится внутри окна объекта «сборщик рукописных данных» или пользователь перемещает указатель мыши в связанном окне объекта «сборщик рукописных данных».</span><span class="sxs-lookup"><span data-stu-id="c9fb1-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="c9fb1-118">События [**невинаирпаккетс**](inkcollector-newinairpackets.md) создаются быстро, а обработчик событий должен иметь высокую скорость или производительность.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-118">[**NewInAirPackets**](inkcollector-newinairpackets.md) events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="c9fb1-119">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ иценевинаирпаккетс.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="c9fb1-120">Событие [**невинаирпаккетс**](inkcollector-newinairpackets.md) срабатывает даже в режиме выбора или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-120">The [**NewInAirPackets**](inkcollector-newinairpackets.md) event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="c9fb1-121">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="c9fb1-122">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="c9fb1-123">Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="c9fb1-124">Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="c9fb1-125">Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.</span><span class="sxs-lookup"><span data-stu-id="c9fb1-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c9fb1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c9fb1-126">Requirements</span></span>



| <span data-ttu-id="c9fb1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c9fb1-127">Requirement</span></span> | <span data-ttu-id="c9fb1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c9fb1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fb1-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9fb1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c9fb1-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c9fb1-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c9fb1-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9fb1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c9fb1-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9fb1-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c9fb1-133">Header</span><span class="sxs-lookup"><span data-stu-id="c9fb1-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9fb1-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c9fb1-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c9fb1-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c9fb1-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9fb1-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9fb1-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c9fb1-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9fb1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9fb1-138">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="c9fb1-138">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="c9fb1-139">**Десиредпаккетдескриптион, свойство**</span><span class="sxs-lookup"><span data-stu-id="c9fb1-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="c9fb1-140">**Событие Невпаккетс**</span><span class="sxs-lookup"><span data-stu-id="c9fb1-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="c9fb1-141">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="c9fb1-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




