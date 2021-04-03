---
description: Набор свойств транспорта внешнего устройства
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Набор свойств транспорта внешнего устройства
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140719"
---
# <a name="external-device-transport-property-set"></a><span data-ttu-id="9bb03-103">Набор свойств транспорта внешнего устройства</span><span class="sxs-lookup"><span data-stu-id="9bb03-103">External Device Transport Property Set</span></span>

<span data-ttu-id="9bb03-104">Этот набор свойств управляет передачей данных на внешнее устройство и с него.</span><span class="sxs-lookup"><span data-stu-id="9bb03-104">This property set controls the transport of data to and from an external device.</span></span> <span data-ttu-id="9bb03-105">В большинстве случаев приложения не должны использовать это свойство напрямую.</span><span class="sxs-lookup"><span data-stu-id="9bb03-105">In most cases, applications should not use this property set directly.</span></span> <span data-ttu-id="9bb03-106">Вместо этого используйте интерфейс [**иамексттранспорт**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .</span><span class="sxs-lookup"><span data-stu-id="9bb03-106">Use the [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) interface instead.</span></span>

<span data-ttu-id="9bb03-107">В следующей таблице перечислены свойства, относящиеся к приложениям пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="9bb03-107">The following table lists the properties that are relevant to user-mode applications.</span></span> <span data-ttu-id="9bb03-108">Полное описание этого набора свойств см. в наборе DDK пакета средств разработки драйверов для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9bb03-108">For a complete description of this property set, refer to the Microsoft Windows Driver Development Kit DDK.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="9bb03-109">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="9bb03-109">Property Set GUID</span></span> | <span data-ttu-id="9bb03-110">ПРОПСЕТИД \_ ext \_ Transport</span><span class="sxs-lookup"><span data-stu-id="9bb03-110">PROPSETID\_EXT\_TRANSPORT</span></span> |



 



| <span data-ttu-id="9bb03-111">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="9bb03-111">Property ID</span></span>                                                                           | <span data-ttu-id="9bb03-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9bb03-112">Description</span></span>                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="9bb03-113">**КСПРОПЕРТИ \_ ексткспорт \_ АТН \_ Search**</span><span class="sxs-lookup"><span data-stu-id="9bb03-113">**KSPROPERTY\_EXTXPORT\_ATN\_SEARCH**</span></span>](ksproperty-extxport-atn-search.md)           | <span data-ttu-id="9bb03-114">Поиск абсолютного номера записи (АТН).</span><span class="sxs-lookup"><span data-stu-id="9bb03-114">Searches for an absolute track number (ATN).</span></span> |
| [<span data-ttu-id="9bb03-115">**Поиск по времени КСПРОПЕРТИ \_ ексткспорт \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9bb03-115">**KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH**</span></span>](ksproperty-extxport-timecode-search.md) | <span data-ttu-id="9bb03-116">Выполняет поиск кода времени.</span><span class="sxs-lookup"><span data-stu-id="9bb03-116">Searches for a time code.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="9bb03-117">См. также</span><span class="sxs-lookup"><span data-stu-id="9bb03-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bb03-118">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="9bb03-118">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



