---
title: Атрибут Синкстате
description: Атрибут Синкстате представляет собой строковое представление 32-разрядного значения, используемого проигрывателем Windows Media при синхронизации списков воспроизведения с портативными устройствами.
ms.assetid: affc3d1c-7fe6-4811-acfc-57285cb181ca
keywords:
- Синкстате атрибут Windows Media Player
topic_type:
- apiref
api_name:
- SyncState
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a948f6c649d548b375ccb676134177b0273c85c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717830"
---
# <a name="syncstate-attribute"></a><span data-ttu-id="e09f1-104">Атрибут Синкстате</span><span class="sxs-lookup"><span data-stu-id="e09f1-104">SyncState Attribute</span></span>

<span data-ttu-id="e09f1-105">Атрибут **синкстате** представляет собой строковое представление 32-разрядного значения, используемого проигрывателем Windows Media при синхронизации списков воспроизведения с портативными устройствами.</span><span class="sxs-lookup"><span data-stu-id="e09f1-105">The **SyncState** attribute is a string representation of a 32-bit value that Windows Media Player uses when it synchronizes playlists with portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e09f1-106">Применение</span><span class="sxs-lookup"><span data-stu-id="e09f1-106">Applies To</span></span>

-   [<span data-ttu-id="e09f1-107">Звуковые элементы</span><span class="sxs-lookup"><span data-stu-id="e09f1-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="e09f1-108">Другие элементы</span><span class="sxs-lookup"><span data-stu-id="e09f1-108">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="e09f1-109">Элементы фото</span><span class="sxs-lookup"><span data-stu-id="e09f1-109">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="e09f1-110">Элементы видео</span><span class="sxs-lookup"><span data-stu-id="e09f1-110">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="e09f1-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e09f1-111">Remarks</span></span>

<span data-ttu-id="e09f1-112">Этот атрибут состоит из 16 2-разрядных значений, каждый из которых указывает состояние синхронизации для переносимого устройства.</span><span class="sxs-lookup"><span data-stu-id="e09f1-112">This attribute consists of sixteen 2-bit values, each of which specifies the synchronization state of a portable device.</span></span> <span data-ttu-id="e09f1-113">Наиболее значимый бит (старший байт) этого 32-битного значения соответствует устройству 16.</span><span class="sxs-lookup"><span data-stu-id="e09f1-113">The most significant bit (MSB) of this 32-bit value corresponds to device 16.</span></span> <span data-ttu-id="e09f1-114">Наименее важный бит (ЛСБ) соответствует устройству 1.</span><span class="sxs-lookup"><span data-stu-id="e09f1-114">The least significant bit (LSB) corresponds to device 1.</span></span>

<span data-ttu-id="e09f1-115">Значение в 1-й части каждого из двух битов указывает, синхронизировано ли проигрыватель Windows Media с соответствующим устройством.</span><span class="sxs-lookup"><span data-stu-id="e09f1-115">The MSB of each 2-bit value indicates whether Windows Media Player synchronized the content with the corresponding device.</span></span> <span data-ttu-id="e09f1-116">Значение 1 указывает на это.</span><span class="sxs-lookup"><span data-stu-id="e09f1-116">A value of 1 indicates that it did.</span></span> <span data-ttu-id="e09f1-117">Значение 0 указывает, что это не так.</span><span class="sxs-lookup"><span data-stu-id="e09f1-117">A value of 0 indicates that it did not.</span></span>

<span data-ttu-id="e09f1-118">Если значение 0 – 1, ЛСБ указывает причину сбоя синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e09f1-118">If the MSB is 0, the LSB specifies why the synchronization failed.</span></span> <span data-ttu-id="e09f1-119">Значение 1 в ЛСБ указывает на недостаточный объем свободного места для содержимого.</span><span class="sxs-lookup"><span data-stu-id="e09f1-119">A value of 1 in the LSB indicates that there was not enough free space for the content.</span></span> <span data-ttu-id="e09f1-120">Значение 0 в ЛСБ указывает на другую причину, препятствующую синхронизации.</span><span class="sxs-lookup"><span data-stu-id="e09f1-120">A value of 0 in the LSB indicates some other reason prevented synchronization.</span></span>

<span data-ttu-id="e09f1-121">Чтобы получить состояние синхронизации данного устройства, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e09f1-121">To retrieve the synchronization state of a given device, you should do the following:</span></span>

1.  <span data-ttu-id="e09f1-122">Вызов **ивмпсинкдевице:: Get \_ Status** для определения, синхронизировано ли данное устройство.</span><span class="sxs-lookup"><span data-stu-id="e09f1-122">Invoke **IWMPSyncDevice::get\_status** to determine whether a given device is synchronized.</span></span>
2.  <span data-ttu-id="e09f1-123">Если оно синхронизировано, вызовите **ивмпсинкдевице:: Get \_ партнершипиндекс** , чтобы получить индекс битовой пары устройства в атрибуте **синкстате** .</span><span class="sxs-lookup"><span data-stu-id="e09f1-123">If it is synchronized, invoke **IWMPSyncDevice::get\_partnershipIndex** to retrieve the index of the device's bit pair in the **SyncState** attribute.</span></span>
3.  <span data-ttu-id="e09f1-124">Используя этот индекс, маску соответствующей битовой пары атрибута **синкстате** и проверьте результат, чтобы определить состояние синхронизации списка воспроизведения с устройством.</span><span class="sxs-lookup"><span data-stu-id="e09f1-124">Using this index, mask the corresponding bit pair of the **SyncState** attribute and examine the result to determine the synchronization state of the playlist with the device.</span></span>

<span data-ttu-id="e09f1-125">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="e09f1-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e09f1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e09f1-126">Requirements</span></span>



| <span data-ttu-id="e09f1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e09f1-127">Requirement</span></span> | <span data-ttu-id="e09f1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e09f1-128">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="e09f1-129">Версия</span><span class="sxs-lookup"><span data-stu-id="e09f1-129">Version</span></span><br/> | <span data-ttu-id="e09f1-130">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e09f1-130">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e09f1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e09f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e09f1-132">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="e09f1-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="e09f1-133">**Определение состояния синхронизации списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="e09f1-133">**Determining Playlist Synchronization State**</span></span>](determining-playlist-synchronization-state.md)
</dt> <dt>

[<span data-ttu-id="e09f1-134">**Ивмпсинкдевице:: Get \_ партнершипиндекс**</span><span class="sxs-lookup"><span data-stu-id="e09f1-134">**IWMPSyncDevice::get\_partnershipIndex**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)
</dt> <dt>

[<span data-ttu-id="e09f1-135">**Ивмпсинкдевице:: получение \_ состояния**</span><span class="sxs-lookup"><span data-stu-id="e09f1-135">**IWMPSyncDevice::get\_status**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status)
</dt> </dl>

 

 





