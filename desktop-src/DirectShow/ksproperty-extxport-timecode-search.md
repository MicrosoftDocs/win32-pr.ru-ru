---
description: Это свойство отправляет на устройство команду для поиска указанного кода времени. Драйвер устройства УВК поддерживает это свойство.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909442"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="1caeb-104">Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_</span><span class="sxs-lookup"><span data-stu-id="1caeb-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="1caeb-105">Это свойство отправляет на устройство команду для поиска указанного кода времени.</span><span class="sxs-lookup"><span data-stu-id="1caeb-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="1caeb-106">Драйвер устройства УВК поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="1caeb-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="1caeb-107">Метка</span><span class="sxs-lookup"><span data-stu-id="1caeb-107">Label</span></span> | <span data-ttu-id="1caeb-108">Значение</span><span class="sxs-lookup"><span data-stu-id="1caeb-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="1caeb-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="1caeb-109">Property Set GUID</span></span> | <span data-ttu-id="1caeb-110">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="1caeb-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="1caeb-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="1caeb-111">Property ID</span></span>       | <span data-ttu-id="1caeb-112">Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_</span><span class="sxs-lookup"><span data-stu-id="1caeb-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="1caeb-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1caeb-113">Data Type</span></span>         | <span data-ttu-id="1caeb-114">**Кспроперти \_ Структура \_ ексткспорт**</span><span class="sxs-lookup"><span data-stu-id="1caeb-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="1caeb-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1caeb-115">Remarks</span></span>

<span data-ttu-id="1caeb-116">Заполните **элемент времени в** структуре **кспроперти \_ ексткспорт \_ S** с нужным кадром, вторым, минутным и часовым.</span><span class="sxs-lookup"><span data-stu-id="1caeb-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="1caeb-117">Структура **кспроперти \_ ексткспорт \_** описана в Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="1caeb-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="1caeb-118">См. также</span><span class="sxs-lookup"><span data-stu-id="1caeb-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1caeb-119">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="1caeb-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



