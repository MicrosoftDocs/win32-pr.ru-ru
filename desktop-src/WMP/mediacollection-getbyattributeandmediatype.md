---
title: Медиаколлектион. Жетбяттрибутеандмедиатипе, метод
description: Метод Жетбяттрибутеандмедиатипе извлекает объект списка воспроизведения, содержащий объекты мультимедиа с указанным атрибутом и типом мультимедиа.
ms.assetid: 75241b38-ae0e-4216-b405-af9a9c71f5ec
keywords:
- Жетбяттрибутеандмедиатипе метод Windows Media Player
- Жетбяттрибутеандмедиатипе метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетбяттрибутеандмедиатипе
topic_type:
- apiref
api_name:
- MediaCollection.getByAttributeAndMediaType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e26abbf2f19d50ec6a10ebbafe12afae8576f34
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648871"
---
# <a name="mediacollectiongetbyattributeandmediatype-method"></a><span data-ttu-id="68a82-106">Медиаколлектион. Жетбяттрибутеандмедиатипе, метод</span><span class="sxs-lookup"><span data-stu-id="68a82-106">MediaCollection.getByAttributeAndMediaType method</span></span>

<span data-ttu-id="68a82-107">Метод **жетбяттрибутеандмедиатипе** извлекает объект **списка воспроизведения** , содержащий объекты **мультимедиа** с указанным атрибутом и типом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="68a82-107">The **getByAttributeAndMediaType** method retrieves a **Playlist** object containing **Media** objects having the specified attribute and media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a82-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68a82-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttributeAndMediaType(
  attribute,
  value,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="68a82-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="68a82-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a82-110">*атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68a82-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a82-111">**Строка** , содержащая атрибут.</span><span class="sxs-lookup"><span data-stu-id="68a82-111">**String** containing the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="68a82-112">*значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68a82-112">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a82-113">**Строка** , содержащая значение.</span><span class="sxs-lookup"><span data-stu-id="68a82-113">**String** containing the value.</span></span>

</dd> <dt>

<span data-ttu-id="68a82-114">*mediaType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="68a82-114">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a82-115">**Строка** , содержащая тип носителя.</span><span class="sxs-lookup"><span data-stu-id="68a82-115">**String** containing the media type.</span></span> <span data-ttu-id="68a82-116">Должно содержать одно из следующих значений: "аудио", "видео", "Фото", "список воспроизведения" или "другое".</span><span class="sxs-lookup"><span data-stu-id="68a82-116">Must contain one of the following values: "audio", "video", "photo", "playlist", or "other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a82-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68a82-117">Return value</span></span>

<span data-ttu-id="68a82-118">Этот метод возвращает объект **списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="68a82-118">This method returns a **Playlist** object</span></span>

## <a name="requirements"></a><span data-ttu-id="68a82-119">Требования</span><span class="sxs-lookup"><span data-stu-id="68a82-119">Requirements</span></span>



| <span data-ttu-id="68a82-120">Требование</span><span class="sxs-lookup"><span data-stu-id="68a82-120">Requirement</span></span> | <span data-ttu-id="68a82-121">Значение</span><span class="sxs-lookup"><span data-stu-id="68a82-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="68a82-122">Версия</span><span class="sxs-lookup"><span data-stu-id="68a82-122">Version</span></span><br/> | <span data-ttu-id="68a82-123">Проигрыватель Windows Media 11.</span><span class="sxs-lookup"><span data-stu-id="68a82-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="68a82-124">DLL</span><span class="sxs-lookup"><span data-stu-id="68a82-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="68a82-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a82-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68a82-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68a82-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a82-127">**Ссылка на атрибут**</span><span class="sxs-lookup"><span data-stu-id="68a82-127">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="68a82-128">**Объект Медиаколлектион**</span><span class="sxs-lookup"><span data-stu-id="68a82-128">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="68a82-129">**Объект списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="68a82-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 





