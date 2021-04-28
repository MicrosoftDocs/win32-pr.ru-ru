---
description: Событие InkCollector. Невинаирпаккетс — происходит при обнаружении пакета в эфире.
ms.assetid: e8eacdec-0381-435f-b453-24dca1c507c9
title: Событие InkCollector. Невинаирпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5709ae0b468aa6ab49516accf4037695268788
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110132"
---
# <a name="inkcollectornewinairpackets-event"></a><span data-ttu-id="f2233-103">Событие InkCollector. Невинаирпаккетс</span><span class="sxs-lookup"><span data-stu-id="f2233-103">InkCollector.NewInAirPackets event</span></span>

<span data-ttu-id="f2233-104">Происходит при обнаружении пакета в эфире.</span><span class="sxs-lookup"><span data-stu-id="f2233-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2233-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2233-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="f2233-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2233-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2233-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2233-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2233-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **невинаирпаккетс** .</span><span class="sxs-lookup"><span data-stu-id="f2233-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="f2233-109">*Паккеткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f2233-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2233-110">Число полученных пакетов в сети Air.</span><span class="sxs-lookup"><span data-stu-id="f2233-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="f2233-111">*Паккетдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="f2233-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2233-112">При возврате из этого метода содержит массив, который содержит выбранные данные для пакета.</span><span class="sxs-lookup"><span data-stu-id="f2233-112">When this method returns, contains an array that contains the selected data for the packet.</span></span>

<span data-ttu-id="f2233-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="f2233-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2233-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2233-114">Return value</span></span>

<span data-ttu-id="f2233-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f2233-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2233-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="f2233-116">Remarks</span></span>

<span data-ttu-id="f2233-117">Пакет в эфире создается, когда пользователь перемещает перо рядом с планшетом, а курсор находится внутри окна объекта «сборщик рукописных данных» или пользователь перемещает указатель мыши в связанном окне объекта «сборщик рукописных данных».</span><span class="sxs-lookup"><span data-stu-id="f2233-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="f2233-118">События **невинаирпаккетс** создаются быстро, а обработчик событий должен иметь высокую скорость или производительность.</span><span class="sxs-lookup"><span data-stu-id="f2233-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="f2233-119">Этот метод события определен в \_ \_ \_ интерфейсах диспетчеризации (DISP) иинкколлекторевентс, иинковерлайевентс и иинкпиктуривентс с идентификатором DISPID \_ иценевинаирпаккетс.</span><span class="sxs-lookup"><span data-stu-id="f2233-119">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="f2233-120">Событие **невинаирпаккетс** срабатывает даже в режиме выбора или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="f2233-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="f2233-121">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="f2233-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="f2233-122">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="f2233-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="f2233-123">Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) объекта сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="f2233-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="f2233-124">Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="f2233-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="f2233-125">Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.</span><span class="sxs-lookup"><span data-stu-id="f2233-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f2233-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f2233-126">Requirements</span></span>



| <span data-ttu-id="f2233-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f2233-127">Requirement</span></span> | <span data-ttu-id="f2233-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f2233-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2233-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2233-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f2233-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="f2233-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f2233-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2233-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f2233-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f2233-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f2233-133">Header</span><span class="sxs-lookup"><span data-stu-id="f2233-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2233-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="f2233-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f2233-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f2233-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="f2233-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2233-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f2233-137">См. также</span><span class="sxs-lookup"><span data-stu-id="f2233-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2233-138">**Класс InkCollector**</span><span class="sxs-lookup"><span data-stu-id="f2233-138">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="f2233-139">**Десиредпаккетдескриптион, свойство**</span><span class="sxs-lookup"><span data-stu-id="f2233-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="f2233-140">**Событие Невпаккетс**</span><span class="sxs-lookup"><span data-stu-id="f2233-140">**NewPackets Event**</span></span>](inkcollector-newpackets.md)
</dt> <dt>

[<span data-ttu-id="f2233-141">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="f2233-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




