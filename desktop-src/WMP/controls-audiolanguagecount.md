---
title: Controls. Аудиолангуажекаунт
description: Свойство Аудиолангуажекаунт извлекает количество поддерживаемых аудио языков.
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- Проигрыватель Windows Media Controls. Аудиолангуажекаунт
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698798"
---
# <a name="controlsaudiolanguagecount"></a><span data-ttu-id="08dec-104">Controls. Аудиолангуажекаунт</span><span class="sxs-lookup"><span data-stu-id="08dec-104">Controls.audioLanguageCount</span></span>

<span data-ttu-id="08dec-105">Свойство **аудиолангуажекаунт** извлекает количество поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="08dec-105">The **audioLanguageCount** property retrieves the count of supported audio languages.</span></span>

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a><span data-ttu-id="08dec-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="08dec-106">Possible Values</span></span>

<span data-ttu-id="08dec-107">Это свойство является **числом** только для чтения (**длинное целое**).</span><span class="sxs-lookup"><span data-stu-id="08dec-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="08dec-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08dec-108">Remarks</span></span>

<span data-ttu-id="08dec-109">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="08dec-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="08dec-110">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает значение 1.</span><span class="sxs-lookup"><span data-stu-id="08dec-110">**Windows Media Player 10 Mobile:** This property always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="08dec-111">Требования</span><span class="sxs-lookup"><span data-stu-id="08dec-111">Requirements</span></span>



| <span data-ttu-id="08dec-112">Требование</span><span class="sxs-lookup"><span data-stu-id="08dec-112">Requirement</span></span> | <span data-ttu-id="08dec-113">Значение</span><span class="sxs-lookup"><span data-stu-id="08dec-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08dec-114">Версия</span><span class="sxs-lookup"><span data-stu-id="08dec-114">Version</span></span><br/> | <span data-ttu-id="08dec-115">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="08dec-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="08dec-116">DLL</span><span class="sxs-lookup"><span data-stu-id="08dec-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="08dec-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08dec-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08dec-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="08dec-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08dec-119">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="08dec-119">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="08dec-120">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="08dec-120">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="08dec-121">**Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="08dec-121">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="08dec-122">**Controls. Жетаудиолангуажедескриптион**</span><span class="sxs-lookup"><span data-stu-id="08dec-122">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="08dec-123">**Controls. Жетаудиолангуажеид**</span><span class="sxs-lookup"><span data-stu-id="08dec-123">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="08dec-124">**Controls. Жетлангуаженаме**</span><span class="sxs-lookup"><span data-stu-id="08dec-124">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





