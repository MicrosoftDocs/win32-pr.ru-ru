---
title: Controls. Куррентаудиолангуажеиндекс
description: Свойство Куррентаудиолангуажеиндекс указывает или получает Отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения.
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- Проигрыватель Windows Media Controls. Куррентаудиолангуажеиндекс
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698795"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="ca44e-104">Controls. Куррентаудиолангуажеиндекс</span><span class="sxs-lookup"><span data-stu-id="ca44e-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="ca44e-105">Свойство **куррентаудиолангуажеиндекс** указывает или получает Отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ca44e-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="ca44e-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ca44e-106">Possible Values</span></span>

<span data-ttu-id="ca44e-107">Это свойство имеет **номер** для чтения и записи (**Long**).</span><span class="sxs-lookup"><span data-stu-id="ca44e-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="ca44e-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca44e-108">Remarks</span></span>

<span data-ttu-id="ca44e-109">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="ca44e-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="ca44e-110">Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="ca44e-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="ca44e-111">**Проигрыватель Windows Media 10 Mobile:** Это свойство принимает или возвращает значение 0.</span><span class="sxs-lookup"><span data-stu-id="ca44e-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca44e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ca44e-112">Requirements</span></span>



| <span data-ttu-id="ca44e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="ca44e-113">Requirement</span></span> | <span data-ttu-id="ca44e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="ca44e-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca44e-115">Версия</span><span class="sxs-lookup"><span data-stu-id="ca44e-115">Version</span></span><br/> | <span data-ttu-id="ca44e-116">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ca44e-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="ca44e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ca44e-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="ca44e-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca44e-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca44e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca44e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca44e-120">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="ca44e-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="ca44e-121">**Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="ca44e-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="ca44e-122">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="ca44e-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="ca44e-123">**Controls. Жетаудиолангуажедескриптион**</span><span class="sxs-lookup"><span data-stu-id="ca44e-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="ca44e-124">**Controls. Жетаудиолангуажеид**</span><span class="sxs-lookup"><span data-stu-id="ca44e-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="ca44e-125">**Controls. Жетлангуаженаме**</span><span class="sxs-lookup"><span data-stu-id="ca44e-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





