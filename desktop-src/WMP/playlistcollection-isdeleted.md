---
title: Плайлистколлектион. isDeleted, метод
description: Метод IsDeleted извлекает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, класс Плайлистколлектион
- Класс Плайлистколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717965"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="02296-106">Плайлистколлектион. isDeleted, метод</span><span class="sxs-lookup"><span data-stu-id="02296-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="02296-107">Метод **IsDeleted** извлекает значение, указывающее, находится ли указанный список воспроизведения в папке удаленных элементов.</span><span class="sxs-lookup"><span data-stu-id="02296-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="02296-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02296-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="02296-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="02296-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02296-110">*список воспроизведения* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="02296-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="02296-111">Искомый объект **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="02296-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02296-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="02296-112">Return value</span></span>

<span data-ttu-id="02296-113">Этот метод возвращает **логическое значение**.</span><span class="sxs-lookup"><span data-stu-id="02296-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="02296-114">**Проигрыватель Windows Media 10 Mobile**: Этот метод всегда возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="02296-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="02296-115">Требования</span><span class="sxs-lookup"><span data-stu-id="02296-115">Requirements</span></span>



| <span data-ttu-id="02296-116">Требование</span><span class="sxs-lookup"><span data-stu-id="02296-116">Requirement</span></span> | <span data-ttu-id="02296-117">Значение</span><span class="sxs-lookup"><span data-stu-id="02296-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02296-118">Версия</span><span class="sxs-lookup"><span data-stu-id="02296-118">Version</span></span><br/> | <span data-ttu-id="02296-119">Проигрыватель Windows Media версии 7,0, Windows Media Player версии 7,1 или Windows Media Player для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="02296-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="02296-120">Этот метод не поддерживается для серии проигрывателя Windows Media 9 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="02296-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="02296-121">DLL</span><span class="sxs-lookup"><span data-stu-id="02296-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="02296-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02296-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="02296-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02296-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02296-124">**Объект Плайлистколлектион**</span><span class="sxs-lookup"><span data-stu-id="02296-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





