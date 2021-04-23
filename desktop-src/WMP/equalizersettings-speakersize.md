---
title: ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе
description: Атрибут Спеакерсизе указывает или получает номер индекса текущего размера динамика.
ms.assetid: 454d07bf-49cd-48a5-9724-6415a925367a
keywords:
- Проигрыватель Windows Media ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.speakerSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26dc49af55e96d3ef8de4e8a4567b3a4296ca214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694930"
---
# <a name="equalizersettingsspeakersize"></a><span data-ttu-id="8cd1a-104">ЕКУАЛИЗЕРСЕТТИНГС. Спеакерсизе</span><span class="sxs-lookup"><span data-stu-id="8cd1a-104">EQUALIZERSETTINGS.speakerSize</span></span>

<span data-ttu-id="8cd1a-105">Атрибут **спеакерсизе** указывает или получает номер индекса текущего размера динамика.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-105">The **speakerSize** attribute specifies or retrieves the index number of the current speaker size.</span></span>

``` syntax
        elementID.speakerSize
```

## <a name="possible-values"></a><span data-ttu-id="8cd1a-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="8cd1a-106">Possible Values</span></span>

<span data-ttu-id="8cd1a-107">Этот атрибут является **числом** для чтения и записи (длинное), содержащим одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-107">This attribute is a read/write **Number** (long) containing one of the following values.</span></span>



| <span data-ttu-id="8cd1a-108">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd1a-108">Value</span></span> | <span data-ttu-id="8cd1a-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8cd1a-109">Description</span></span>                              |
|-------|------------------------------------------|
| <span data-ttu-id="8cd1a-110">0</span><span class="sxs-lookup"><span data-stu-id="8cd1a-110">0</span></span>     | <span data-ttu-id="8cd1a-111">Текущие динамики — наушники.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-111">The current speakers are headphones.</span></span>     |
| <span data-ttu-id="8cd1a-112">1</span><span class="sxs-lookup"><span data-stu-id="8cd1a-112">1</span></span>     | <span data-ttu-id="8cd1a-113">Текущие динамики имеют нормальный размер.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-113">The current speakers are of normal size.</span></span> |
| <span data-ttu-id="8cd1a-114">2</span><span class="sxs-lookup"><span data-stu-id="8cd1a-114">2</span></span>     | <span data-ttu-id="8cd1a-115">Текущие динамики имеют большой размер.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-115">The current speakers are large.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="8cd1a-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8cd1a-116">Remarks</span></span>

<span data-ttu-id="8cd1a-117">Понятное имя размера динамика можно получить с помощью атрибута **куррентспеакернаме** .</span><span class="sxs-lookup"><span data-stu-id="8cd1a-117">The friendly name of the speaker size can be retrieved using the **currentSpeakerName** attribute.</span></span>

<span data-ttu-id="8cd1a-118">Этот атрибут пропускается, если **енханцедаудио** имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="8cd1a-118">This attribute is ignored if **enhancedAudio** is set to false.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cd1a-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8cd1a-119">Requirements</span></span>



| <span data-ttu-id="8cd1a-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8cd1a-120">Requirement</span></span> | <span data-ttu-id="8cd1a-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8cd1a-121">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="8cd1a-122">Версия</span><span class="sxs-lookup"><span data-stu-id="8cd1a-122">Version</span></span><br/> | <span data-ttu-id="8cd1a-123">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="8cd1a-123">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8cd1a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8cd1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cd1a-125">**ЕКУАЛИЗЕРСЕТТИНГС, элемент**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-125">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="8cd1a-126">**ЕКУАЛИЗЕРСЕТТИНГС. Куррентспеакернаме**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-126">**EQUALIZERSETTINGS.currentSpeakerName**</span></span>](equalizersettings-currentspeakername.md)
</dt> <dt>

[<span data-ttu-id="8cd1a-127">**ЕКУАЛИЗЕРСЕТТИНГС. Енханцедаудио**</span><span class="sxs-lookup"><span data-stu-id="8cd1a-127">**EQUALIZERSETTINGS.enhancedAudio**</span></span>](equalizersettings-enhancedaudio.md)
</dt> </dl>

 

 





