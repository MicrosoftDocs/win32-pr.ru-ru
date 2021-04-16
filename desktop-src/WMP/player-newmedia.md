---
title: Метод Player. Невмедиа
description: Метод Невмедиа создает новый объект мультимедиа.
ms.assetid: fccf1559-bac3-4edf-bd88-da2c72cdec21
keywords:
- Невмедиа метод Windows Media Player
- метод Невмедиа проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Невмедиа
topic_type:
- apiref
api_name:
- Player.newMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaafb97f836135aa9dd112372b1931c8561cb40b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708519"
---
# <a name="playernewmedia-method"></a><span data-ttu-id="c41c9-106">Метод Player. Невмедиа</span><span class="sxs-lookup"><span data-stu-id="c41c9-106">Player.newMedia method</span></span>

<span data-ttu-id="c41c9-107">Метод **невмедиа** создает новый объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="c41c9-107">The **newMedia** method creates a new **Media** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c41c9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c41c9-108">Syntax</span></span>


```JScript
retVal = Player.newMedia(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="c41c9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c41c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41c9-110">*URL-адрес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c41c9-110">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41c9-111">**Строка** , содержащая URL-адрес файла цифрового мультимедиа, с которым создается объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="c41c9-111">**String** containing the URL of the digital media file to create the **Media** object with.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c41c9-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c41c9-112">Return value</span></span>

<span data-ttu-id="c41c9-113">Этот метод возвращает объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="c41c9-113">This method returns a **Media** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c41c9-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c41c9-114">Remarks</span></span>

<span data-ttu-id="c41c9-115">Параметр *URL-адреса* не должен быть пустой строкой или иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="c41c9-115">The *URL* parameter must not be an empty string or null.</span></span>

## <a name="requirements"></a><span data-ttu-id="c41c9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="c41c9-116">Requirements</span></span>



| <span data-ttu-id="c41c9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="c41c9-117">Requirement</span></span> | <span data-ttu-id="c41c9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="c41c9-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c41c9-119">Версия</span><span class="sxs-lookup"><span data-stu-id="c41c9-119">Version</span></span><br/> | <span data-ttu-id="c41c9-120">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c41c9-120">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="c41c9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c41c9-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c41c9-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c41c9-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c41c9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c41c9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c41c9-124">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="c41c9-124">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





