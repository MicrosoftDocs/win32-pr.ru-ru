---
description: Это свойство отправляет на устройство команду для поиска абсолютного номера записи (АТН). Драйвер устройства УВК поддерживает это свойство.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909451"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="b9975-104">КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search</span><span class="sxs-lookup"><span data-stu-id="b9975-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="b9975-105">Это свойство отправляет на устройство команду для поиска абсолютного номера записи (АТН).</span><span class="sxs-lookup"><span data-stu-id="b9975-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="b9975-106">Драйвер устройства УВК поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="b9975-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="b9975-107">Метка</span><span class="sxs-lookup"><span data-stu-id="b9975-107">Label</span></span> | <span data-ttu-id="b9975-108">Значение</span><span class="sxs-lookup"><span data-stu-id="b9975-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="b9975-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="b9975-109">Property Set GUID</span></span> | <span data-ttu-id="b9975-110">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="b9975-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="b9975-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="b9975-111">Property ID</span></span>       | <span data-ttu-id="b9975-112">КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search</span><span class="sxs-lookup"><span data-stu-id="b9975-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="b9975-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b9975-113">Data Type</span></span>         | <span data-ttu-id="b9975-114">**Кспроперти \_ Структура \_ ексткспорт**</span><span class="sxs-lookup"><span data-stu-id="b9975-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b9975-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9975-115">Remarks</span></span>

<span data-ttu-id="b9975-116">Задайте для элемента **двабстраккнумбер** структуры **кспроперти \_ ексткспорт \_** следующее значение:</span><span class="sxs-lookup"><span data-stu-id="b9975-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="b9975-117">Спецификация УВК не определяет, как устройство использует бит непрерывности.</span><span class="sxs-lookup"><span data-stu-id="b9975-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="b9975-118">Структура **кспроперти \_ ексткспорт \_** описана в Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="b9975-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9975-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b9975-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9975-120">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="b9975-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



