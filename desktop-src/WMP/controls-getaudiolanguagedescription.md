---
title: Controls. Жетаудиолангуажедескриптион, метод
description: Метод Жетаудиолангуажедескриптион Извлекает описание для языкового аудио, соответствующего указанному индексу, основанному на единице.
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- Жетаудиолангуажедескриптион метод Windows Media Player
- метод Жетаудиолангуажедескриптион Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Жетаудиолангуажедескриптион
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694849"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="b12bd-106">Controls. Жетаудиолангуажедескриптион, метод</span><span class="sxs-lookup"><span data-stu-id="b12bd-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="b12bd-107">Метод **жетаудиолангуажедескриптион** Извлекает описание для языкового аудио, соответствующего указанному индексу, основанному на единице.</span><span class="sxs-lookup"><span data-stu-id="b12bd-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b12bd-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b12bd-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b12bd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b12bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12bd-110">*индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b12bd-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b12bd-111">**Число** (**длинное целое**), указывающее индекс языкового аудио на основе единицы.</span><span class="sxs-lookup"><span data-stu-id="b12bd-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b12bd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b12bd-112">Return value</span></span>

<span data-ttu-id="b12bd-113">Этот метод возвращает **строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="b12bd-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b12bd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b12bd-114">Remarks</span></span>

<span data-ttu-id="b12bd-115">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="b12bd-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="b12bd-116">Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков, а затем получите доступ к звуковому языку по отдельности с помощью индекса, основанного на единицах.</span><span class="sxs-lookup"><span data-stu-id="b12bd-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="b12bd-117">**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b12bd-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b12bd-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b12bd-118">Requirements</span></span>



| <span data-ttu-id="b12bd-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b12bd-119">Requirement</span></span> | <span data-ttu-id="b12bd-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b12bd-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b12bd-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b12bd-121">Version</span></span><br/> | <span data-ttu-id="b12bd-122">Проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="b12bd-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="b12bd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b12bd-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="b12bd-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b12bd-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b12bd-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b12bd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12bd-126">**Объект Controls**</span><span class="sxs-lookup"><span data-stu-id="b12bd-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="b12bd-127">**Controls. Аудиолангуажекаунт**</span><span class="sxs-lookup"><span data-stu-id="b12bd-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="b12bd-128">**Controls. Куррентаудиолангуаже**</span><span class="sxs-lookup"><span data-stu-id="b12bd-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="b12bd-129">**Controls. Куррентаудиолангуажеиндекс**</span><span class="sxs-lookup"><span data-stu-id="b12bd-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="b12bd-130">**Controls. Жетаудиолангуажеид**</span><span class="sxs-lookup"><span data-stu-id="b12bd-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="b12bd-131">**Controls. Жетлангуаженаме**</span><span class="sxs-lookup"><span data-stu-id="b12bd-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





