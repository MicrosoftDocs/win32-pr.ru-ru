---
title: Controls. Куррентаудиолангуаже
description: Свойство Куррентаудиолангуаже указывает или получает код локали (LCID) звукового языка для воспроизведения.
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- Проигрыватель Windows Media Controls. Куррентаудиолангуаже
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698796"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="39ccc-104">Controls. Куррентаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="39ccc-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="39ccc-105">Свойство **куррентаудиолангуаже** указывает или получает код локали (LCID) звукового языка для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="39ccc-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="39ccc-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="39ccc-106">Possible Values</span></span>

<span data-ttu-id="39ccc-107">Это свойство имеет **номер** для чтения и записи (**Long**).</span><span class="sxs-lookup"><span data-stu-id="39ccc-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="39ccc-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39ccc-108">Remarks</span></span>

<span data-ttu-id="39ccc-109">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="39ccc-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="39ccc-110">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="39ccc-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="39ccc-111">При работе с содержимым DVD при указании LCID будет выбрана первая доступная звуковая дорожка с указанным ИДЕНТИФИКАТОРом языка.</span><span class="sxs-lookup"><span data-stu-id="39ccc-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="39ccc-112">**Проигрыватель Windows Media 10 Mobile:** Это свойство принимает или возвращает только код, не зависящий от языка (0).</span><span class="sxs-lookup"><span data-stu-id="39ccc-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="39ccc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="39ccc-113">Requirements</span></span>



| <span data-ttu-id="39ccc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="39ccc-114">Requirement</span></span> | <span data-ttu-id="39ccc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="39ccc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="39ccc-116">Версия</span><span class="sxs-lookup"><span data-stu-id="39ccc-116">Version</span></span><br/> | <span data-ttu-id="39ccc-117">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="39ccc-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="39ccc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="39ccc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="39ccc-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ccc-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39ccc-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39ccc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39ccc-121">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="39ccc-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="39ccc-122">**Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="39ccc-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="39ccc-123">**Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="39ccc-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="39ccc-124">**Controls. Жетаудиолангуажедескриптион**</span><span class="sxs-lookup"><span data-stu-id="39ccc-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="39ccc-125">**Controls. Жетаудиолангуажеид**</span><span class="sxs-lookup"><span data-stu-id="39ccc-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="39ccc-126">**Controls. Жетлангуаженаме**</span><span class="sxs-lookup"><span data-stu-id="39ccc-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





