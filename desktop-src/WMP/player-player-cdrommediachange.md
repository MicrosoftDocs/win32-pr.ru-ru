---
title: Событие Player. Кдроммедиачанже
description: Событие Кдроммедиачанже возникает при вставке или извлечении компакт-диска или DVD-диска из дисковода CD или DVD. | Событие Player. Кдроммедиачанже
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Проигрыватель Windows Media Event Кдроммедиачанже
- Проигрыватель Windows Media Event Кдроммедиачанже, класс Player
- Класс проигрывателя Windows Media Player, событие Кдроммедиачанже
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704344"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="5ce1b-107">Событие Player. Кдроммедиачанже</span><span class="sxs-lookup"><span data-stu-id="5ce1b-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="5ce1b-108">Событие **кдроммедиачанже** возникает при вставке или ИЗВЛЕЧЕНии компакт-диска или DVD-диска из дисковода CD или DVD.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce1b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ce1b-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="5ce1b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ce1b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce1b-111">*кдромнум*</span><span class="sxs-lookup"><span data-stu-id="5ce1b-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="5ce1b-112">**Число** (**длинное**), указывающее индекс компакт-диска или DVD-дисковода.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce1b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ce1b-113">Return value</span></span>

<span data-ttu-id="5ce1b-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce1b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ce1b-115">Remarks</span></span>

<span data-ttu-id="5ce1b-116">Индекс дисковода компакт-дисков соответствует индексу объекта **CDROM** в **кдромколлектион**.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="5ce1b-117">Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="5ce1b-118">Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="5ce1b-119">**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce1b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="5ce1b-120">Requirements</span></span>



| <span data-ttu-id="5ce1b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="5ce1b-121">Requirement</span></span> | <span data-ttu-id="5ce1b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="5ce1b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce1b-123">Версия</span><span class="sxs-lookup"><span data-stu-id="5ce1b-123">Version</span></span><br/> | <span data-ttu-id="5ce1b-124">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="5ce1b-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ce1b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5ce1b-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ce1b-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ce1b-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce1b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ce1b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce1b-128">**Объект CDROM**</span><span class="sxs-lookup"><span data-stu-id="5ce1b-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="5ce1b-129">**Объект Кдромколлектион**</span><span class="sxs-lookup"><span data-stu-id="5ce1b-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="5ce1b-130">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="5ce1b-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





