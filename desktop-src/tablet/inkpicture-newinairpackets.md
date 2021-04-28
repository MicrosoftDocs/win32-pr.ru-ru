---
description: Событие InkPicture. Невинаирпаккетс — происходит при обнаружении пакета в эфире.
ms.assetid: 30bc423d-0642-4515-9e51-a8b8b36aecad
title: Событие InkPicture. Невинаирпаккетс (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0de8f2423817bada84f83b63de1517393740db4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108086562"
---
# <a name="inkpicturenewinairpackets-event"></a><span data-ttu-id="35895-103">Событие InkPicture. Невинаирпаккетс</span><span class="sxs-lookup"><span data-stu-id="35895-103">InkPicture.NewInAirPackets event</span></span>

<span data-ttu-id="35895-104">Происходит при обнаружении пакета в эфире.</span><span class="sxs-lookup"><span data-stu-id="35895-104">Occurs when an in-air packet is seen.</span></span>

## <a name="syntax"></a><span data-ttu-id="35895-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35895-105">Syntax</span></span>


```C++
void NewInAirPackets(
  [in]      IInkCursor *Cursor,
  [in]      long       PacketCount,
  [in, out] VARIANT    *PacketData
);
```



## <a name="parameters"></a><span data-ttu-id="35895-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="35895-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35895-107">*Курсор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35895-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35895-108">Объект [**иинккурсор**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) , создавший событие **невинаирпаккетс** .</span><span class="sxs-lookup"><span data-stu-id="35895-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **NewInAirPackets** event.</span></span>

</dd> <dt>

<span data-ttu-id="35895-109">*Паккеткаунт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35895-109">*PacketCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35895-110">Число полученных пакетов в сети Air.</span><span class="sxs-lookup"><span data-stu-id="35895-110">The number of in-air packets received.</span></span>

</dd> <dt>

<span data-ttu-id="35895-111">*Паккетдата* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="35895-111">*PacketData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="35895-112">Массив, содержащий выбранные данные для пакета.</span><span class="sxs-lookup"><span data-stu-id="35895-112">An array that contains the selected data for the packet.</span></span>

<span data-ttu-id="35895-113">Дополнительные сведения о структуре вариантов см. в разделе [Использование библиотеки COM](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="35895-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35895-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35895-114">Return value</span></span>

<span data-ttu-id="35895-115">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="35895-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35895-116">Remarks</span><span class="sxs-lookup"><span data-stu-id="35895-116">Remarks</span></span>

<span data-ttu-id="35895-117">Пакет в эфире создается, когда пользователь перемещает перо рядом с планшетом, а курсор находится внутри окна объекта «сборщик рукописных данных» или пользователь перемещает указатель мыши в связанном окне объекта «сборщик рукописных данных».</span><span class="sxs-lookup"><span data-stu-id="35895-117">An in-air packet is created when a user moves a pen near the tablet and the cursor is within the ink collector object's window or the user moves a mouse within the ink collector object's associated window.</span></span> <span data-ttu-id="35895-118">События **невинаирпаккетс** создаются быстро, а обработчик событий должен иметь высокую скорость или производительность.</span><span class="sxs-lookup"><span data-stu-id="35895-118">**NewInAirPackets** events are generated rapidly, and the event handler must be fast or performance suffers.</span></span>

<span data-ttu-id="35895-119">Этот метод события определен в интерфейсах диспетчеризации (DISP) **\_ иинкколлекторевентс**, **\_ иинковерлайевентс** и **\_ иинкпиктуривентс** с идентификатором DISPID \_ иценевинаирпаккетс.</span><span class="sxs-lookup"><span data-stu-id="35895-119">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICENewInAirPackets.</span></span>

<span data-ttu-id="35895-120">Событие **невинаирпаккетс** срабатывает даже в режиме выбора или стирания, а не только при вставке рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="35895-120">The **NewInAirPackets** event is fired even when in select or erase mode, not just when inserting ink.</span></span> <span data-ttu-id="35895-121">Для этого необходимо наблюдать за режимом редактирования (который вы несете за параметром) и учитывать режим, прежде чем интерпретировать событие.</span><span class="sxs-lookup"><span data-stu-id="35895-121">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="35895-122">Преимуществом этого требования является большая свобода для внедрения инноваций на платформе за счет большей осведомленности о событиях платформы.</span><span class="sxs-lookup"><span data-stu-id="35895-122">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

<span data-ttu-id="35895-123">Чтобы задать, какие свойства содержатся в этом массиве, используйте свойство [**десиредпаккетдескриптион**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) объекта сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="35895-123">To set which properties are contained in this array, use the [**DesiredPacketDescription**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription) property of the ink collector object.</span></span> <span data-ttu-id="35895-124">Массив, возвращаемый параметром *паккетдата* , содержит данные для этих свойств.</span><span class="sxs-lookup"><span data-stu-id="35895-124">The array that the *PacketData* parameter returns contains the data for those properties.</span></span>

> [!Note]  
> <span data-ttu-id="35895-125">Хотя можно изменять данные пакета, эти изменения не сохраняются и не используются.</span><span class="sxs-lookup"><span data-stu-id="35895-125">Although you can modify the packet data, these modifications are not persisted or used.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="35895-126">Требования</span><span class="sxs-lookup"><span data-stu-id="35895-126">Requirements</span></span>



| <span data-ttu-id="35895-127">Требование</span><span class="sxs-lookup"><span data-stu-id="35895-127">Requirement</span></span> | <span data-ttu-id="35895-128">Значение</span><span class="sxs-lookup"><span data-stu-id="35895-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35895-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35895-129">Minimum supported client</span></span><br/> | <span data-ttu-id="35895-130">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="35895-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="35895-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35895-131">Minimum supported server</span></span><br/> | <span data-ttu-id="35895-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35895-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="35895-133">Header</span><span class="sxs-lookup"><span data-stu-id="35895-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="35895-134"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="35895-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="35895-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="35895-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="35895-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35895-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="35895-137">См. также</span><span class="sxs-lookup"><span data-stu-id="35895-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35895-138">InkPicture</span><span class="sxs-lookup"><span data-stu-id="35895-138">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="35895-139">**Десиредпаккетдескриптион, свойство**</span><span class="sxs-lookup"><span data-stu-id="35895-139">**DesiredPacketDescription Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_desiredpacketdescription)
</dt> <dt>

[<span data-ttu-id="35895-140">**Событие Невпаккетс**</span><span class="sxs-lookup"><span data-stu-id="35895-140">**NewPackets Event**</span></span>](inkpicture-newpackets.md)
</dt> <dt>

[<span data-ttu-id="35895-141">**Интерфейс Иинккурсор**</span><span class="sxs-lookup"><span data-stu-id="35895-141">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




