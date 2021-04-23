---
title: Атрибуты синхронизации
description: Атрибуты Sync01 через Sync16 представляют собой строковые представления 32-разрядных значений, которые проигрыватель Windows Media использует при синхронизации списков воспроизведения с одним из 16 портативных устройств.
ms.assetid: b9ae3420-aa09-4969-8637-f16d438942f3
keywords:
- Синхронизировать атрибуты проигрыватель Windows Media
topic_type:
- apiref
api_name:
- Sync
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5af26ae563a38efcc40b0bcd319c5fc62b4776dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717832"
---
# <a name="sync-attributes"></a><span data-ttu-id="c3673-104">Атрибуты синхронизации</span><span class="sxs-lookup"><span data-stu-id="c3673-104">Sync Attributes</span></span>

<span data-ttu-id="c3673-105">Атрибуты **Sync01** через **Sync16** представляют собой строковые представления 32-разрядных значений, которые проигрыватель Windows Media использует при синхронизации списков воспроизведения с одним из 16 портативных устройств.</span><span class="sxs-lookup"><span data-stu-id="c3673-105">The **Sync01** through **Sync16** attributes are string representations of 32-bit values that Windows Media Player uses when it synchronizes playlists with one of up to 16 portable devices.</span></span>

## <a name="applies-to"></a><span data-ttu-id="c3673-106">Применение</span><span class="sxs-lookup"><span data-stu-id="c3673-106">Applies To</span></span>

-   [<span data-ttu-id="c3673-107">Списки воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c3673-107">Playlists</span></span>](playlist-attributes-ref.md)

## <a name="remarks"></a><span data-ttu-id="c3673-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c3673-108">Remarks</span></span>

<span data-ttu-id="c3673-109">Они являются атрибутами чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="c3673-109">These are read/write attributes.</span></span> <span data-ttu-id="c3673-110">Нулевое значение указывает, что проигрыватель Windows Media не должен синхронизировать список воспроизведения с соответствующим устройством.</span><span class="sxs-lookup"><span data-stu-id="c3673-110">A value of zero indicates that Windows Media Player should not synchronize the playlist with the associated device.</span></span> <span data-ttu-id="c3673-111">Значение больше нуля указывает приоритет синхронизации для данного списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c3673-111">A value greater than zero indicates a synchronization priority for the given playlist.</span></span>

<span data-ttu-id="c3673-112">В зависимости от вводимых пользователем данных проигрыватель Windows Media устанавливает этот атрибут для каждого списка воспроизведения в библиотеке.</span><span class="sxs-lookup"><span data-stu-id="c3673-112">Based on user input, Windows Media Player sets this attribute for each of the playlists in the library.</span></span> <span data-ttu-id="c3673-113">Когда проигрыватель Windows Media пытается синхронизировать список воспроизведения с портативным устройством, он проверяет каждый список воспроизведения для сравнения значений атрибутов **синхронизации**_XX_ , которые представляют связь устройства.</span><span class="sxs-lookup"><span data-stu-id="c3673-113">When Windows Media Player attempts to synchronize a playlist with a portable device, it examines each playlist to compare the values for the **Sync**_XX_ attributes that represent the device partnership.</span></span> <span data-ttu-id="c3673-114">Списки воспроизведения, имеющие более низкие значения параметров **синхронизации**_XX_ , получают более высокий приоритет синхронизации.</span><span class="sxs-lookup"><span data-stu-id="c3673-114">Playlists that have lower **Sync**_XX_ values receive higher synchronization priority.</span></span>

<span data-ttu-id="c3673-115">Например, Библиотека может содержать следующие четыре списка воспроизведения и соответствующие значения **синхронизации**_XX_ :</span><span class="sxs-lookup"><span data-stu-id="c3673-115">For example, the library might contain the following four playlists and respective **Sync**_XX_ values:</span></span>



| <span data-ttu-id="c3673-116">Имя списка воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c3673-116">Playlist Name</span></span> | <span data-ttu-id="c3673-117">Значение Sync01</span><span class="sxs-lookup"><span data-stu-id="c3673-117">Sync01 Value</span></span> |
|---------------|--------------|
| <span data-ttu-id="c3673-118">Гиммусик. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-118">GymMusic.WPL</span></span>  | <span data-ttu-id="c3673-119">0x0000000D</span><span class="sxs-lookup"><span data-stu-id="c3673-119">0x0000000D</span></span>   |
| <span data-ttu-id="c3673-120">Ослабить. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-120">Relax.WPL</span></span>     | <span data-ttu-id="c3673-121">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c3673-121">0x00000020</span></span>   |
| <span data-ttu-id="c3673-122">Дривехоме. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-122">DriveHome.WPL</span></span> | <span data-ttu-id="c3673-123">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c3673-123">0x00000001</span></span>   |
| <span data-ttu-id="c3673-124">Ного. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-124">NoGo.WPL</span></span>      | <span data-ttu-id="c3673-125">0x00000000</span><span class="sxs-lookup"><span data-stu-id="c3673-125">0x00000000</span></span>   |



 

<span data-ttu-id="c3673-126">Когда проигрыватель Windows Media синхронизирует устройство, связанное с атрибутом, списки воспроизведения будут синхронизироваться в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="c3673-126">When Windows Media Player synchronizes the device associated with the attribute, it will synchronize the playlists in the following order:</span></span>

1.  <span data-ttu-id="c3673-127">Дривехоме. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-127">DriveHome.WPL</span></span>
2.  <span data-ttu-id="c3673-128">Гиммусик. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-128">GymMusic.WPL</span></span>
3.  <span data-ttu-id="c3673-129">Ослабить. WPL</span><span class="sxs-lookup"><span data-stu-id="c3673-129">Relax.WPL</span></span>

<span data-ttu-id="c3673-130">Чтобы определить, можно ли изменить значение этого атрибута, используйте метод [Media. исреадонлитем](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="c3673-130">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3673-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c3673-131">Requirements</span></span>



| <span data-ttu-id="c3673-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c3673-132">Requirement</span></span> | <span data-ttu-id="c3673-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c3673-133">Value</span></span> |
|--------------------|---------------------------------------------|
| <span data-ttu-id="c3673-134">Версия</span><span class="sxs-lookup"><span data-stu-id="c3673-134">Version</span></span><br/> | <span data-ttu-id="c3673-135">Проигрыватель Windows Media 10 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="c3673-135">Windows Media Player 10 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3673-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3673-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3673-137">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="c3673-137">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="c3673-138">**Перечисление списков воспроизведения синхронизации**</span><span class="sxs-lookup"><span data-stu-id="c3673-138">**Enumerating Synchronization Playlists**</span></span>](enumerating-synchronization-playlists.md)
</dt> </dl>

 

 





