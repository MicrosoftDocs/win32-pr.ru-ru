---
description: Это свойство отправляет на устройство команду для поиска абсолютного номера записи (АТН). Драйвер устройства УВК поддерживает это свойство.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682182"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="6a11b-104">КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search</span><span class="sxs-lookup"><span data-stu-id="6a11b-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="6a11b-105">Это свойство отправляет на устройство команду для поиска абсолютного номера записи (АТН).</span><span class="sxs-lookup"><span data-stu-id="6a11b-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="6a11b-106">Драйвер устройства УВК поддерживает это свойство.</span><span class="sxs-lookup"><span data-stu-id="6a11b-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="6a11b-107">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="6a11b-107">Property Set GUID</span></span> | <span data-ttu-id="6a11b-108">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="6a11b-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="6a11b-109">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="6a11b-109">Property ID</span></span>       | <span data-ttu-id="6a11b-110">КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search</span><span class="sxs-lookup"><span data-stu-id="6a11b-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="6a11b-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="6a11b-111">Data Type</span></span>         | <span data-ttu-id="6a11b-112">**Кспроперти \_ Структура \_ ексткспорт**</span><span class="sxs-lookup"><span data-stu-id="6a11b-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6a11b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6a11b-113">Remarks</span></span>

<span data-ttu-id="6a11b-114">Задайте для элемента **двабстраккнумбер** структуры **кспроперти \_ ексткспорт \_** следующее значение:</span><span class="sxs-lookup"><span data-stu-id="6a11b-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="6a11b-115">Спецификация УВК не определяет, как устройство использует бит непрерывности.</span><span class="sxs-lookup"><span data-stu-id="6a11b-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="6a11b-116">Структура **кспроперти \_ ексткспорт \_** описана в Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="6a11b-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="6a11b-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a11b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a11b-118">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="6a11b-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



