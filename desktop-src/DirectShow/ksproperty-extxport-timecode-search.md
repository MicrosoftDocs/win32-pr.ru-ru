---
description: Это свойство отправляет на устройство команду для поиска указанного кода времени. Драйвер устройства УВК поддерживает это свойство.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072182"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="a665d-104">Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_</span><span class="sxs-lookup"><span data-stu-id="a665d-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="a665d-105">Это свойство отправляет на устройство команду для поиска указанного кода времени.</span><span class="sxs-lookup"><span data-stu-id="a665d-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="a665d-106">Драйвер устройства УВК поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="a665d-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="a665d-107">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="a665d-107">Property Set GUID</span></span> | <span data-ttu-id="a665d-108">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="a665d-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="a665d-109">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="a665d-109">Property ID</span></span>       | <span data-ttu-id="a665d-110">Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_</span><span class="sxs-lookup"><span data-stu-id="a665d-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="a665d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a665d-111">Data Type</span></span>         | <span data-ttu-id="a665d-112">**Кспроперти \_ Структура \_ ексткспорт**</span><span class="sxs-lookup"><span data-stu-id="a665d-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="a665d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a665d-113">Remarks</span></span>

<span data-ttu-id="a665d-114">Заполните **элемент времени в** структуре **кспроперти \_ ексткспорт \_ S** с нужным кадром, вторым, минутным и часовым.</span><span class="sxs-lookup"><span data-stu-id="a665d-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="a665d-115">Структура **кспроперти \_ ексткспорт \_** описана в Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="a665d-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="a665d-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a665d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a665d-117">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="a665d-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



