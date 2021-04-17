---
title: Controls. Жетаудиолангуажеид, метод
description: Метод Жетаудиолангуажеид извлекает код локали (LCID) для указанного индекса языкового звука.
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- Жетаудиолангуажеид метод Windows Media Player
- метод Жетаудиолангуажеид Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Жетаудиолангуажеид
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694848"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="abfd3-106">Controls. Жетаудиолангуажеид, метод</span><span class="sxs-lookup"><span data-stu-id="abfd3-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="abfd3-107">Метод **жетаудиолангуажеид** извлекает код локали (LCID) для указанного индекса языкового звука.</span><span class="sxs-lookup"><span data-stu-id="abfd3-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="abfd3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="abfd3-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="abfd3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="abfd3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abfd3-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="abfd3-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abfd3-111">**Число** (**длинное**), указывающее индекс языкового звука.</span><span class="sxs-lookup"><span data-stu-id="abfd3-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abfd3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="abfd3-112">Return value</span></span>

<span data-ttu-id="abfd3-113">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="abfd3-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="abfd3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="abfd3-114">Remarks</span></span>

<span data-ttu-id="abfd3-115">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="abfd3-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="abfd3-116">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="abfd3-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="abfd3-117">**Проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает код языка (0), не зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="abfd3-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="abfd3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="abfd3-118">Requirements</span></span>



| <span data-ttu-id="abfd3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="abfd3-119">Requirement</span></span> | <span data-ttu-id="abfd3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="abfd3-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abfd3-121">Версия</span><span class="sxs-lookup"><span data-stu-id="abfd3-121">Version</span></span><br/> | <span data-ttu-id="abfd3-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="abfd3-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="abfd3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="abfd3-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="abfd3-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abfd3-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abfd3-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="abfd3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abfd3-126">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="abfd3-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="abfd3-127">**Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="abfd3-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="abfd3-128">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="abfd3-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="abfd3-129">**Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="abfd3-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="abfd3-130">**Controls. Жетаудиолангуажедескриптион**</span><span class="sxs-lookup"><span data-stu-id="abfd3-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="abfd3-131">**Controls. Жетлангуаженаме**</span><span class="sxs-lookup"><span data-stu-id="abfd3-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





