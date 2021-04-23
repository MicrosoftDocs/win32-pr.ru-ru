---
description: Набор свойств транспорта внешнего устройства
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Набор свойств транспорта внешнего устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909222"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="3d155-103">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="3d155-103">External Device Transport Property Set</span></span>

<span data-ttu-id="3d155-104">Этот набор свойств управляет передачей данных на внешнее устройство и с него.</span><span class="sxs-lookup"><span data-stu-id="3d155-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="3d155-105">В большинстве случаев приложения не должны использовать это свойство напрямую.</span><span class="sxs-lookup"><span data-stu-id="3d155-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="3d155-106">Вместо этого используйте интерфейс [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="3d155-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="3d155-107">В следующей таблице перечислены свойства, относящиеся к приложениям пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="3d155-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="3d155-108">Полное описание этого набора свойств см. в наборе DDK пакета средств разработки драйверов для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="3d155-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



| <span data-ttu-id="3d155-109">Метка</span><span class="sxs-lookup"><span data-stu-id="3d155-109">Label</span></span> | <span data-ttu-id="3d155-110">Значение</span><span class="sxs-lookup"><span data-stu-id="3d155-110">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="3d155-111">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="3d155-111">Property Set GUID</span></span> | <span data-ttu-id="3d155-112">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="3d155-112">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="3d155-113">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="3d155-113">Property ID</span></span>                                                                           | <span data-ttu-id="3d155-114">Описание</span><span class="sxs-lookup"><span data-stu-id="3d155-114">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="3d155-115">**КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search**</span><span class="sxs-lookup"><span data-stu-id="3d155-115">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="3d155-116">Поиск абсолютного номера записи (АТН).</span><span class="sxs-lookup"><span data-stu-id="3d155-116">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="3d155-117">**Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3d155-117">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="3d155-118">Выполняет поиск кода времени.</span><span class="sxs-lookup"><span data-stu-id="3d155-118">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="3d155-119">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="3d155-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d155-120">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="3d155-120">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



