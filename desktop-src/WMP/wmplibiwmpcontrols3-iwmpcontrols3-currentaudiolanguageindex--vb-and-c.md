---
title: IWMPControls3 Куррентаудиолангуажеиндекс, свойство
description: Свойство Куррентаудиолангуажеиндекс Возвращает или задает отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- Проигрыватель Windows Media для свойства Куррентаудиолангуажеиндекс
- Куррентаудиолангуажеиндекс свойство проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, свойство Куррентаудиолангуажеиндекс
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649058"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="bb33b-106">Свойство IWMPControls3:: Куррентаудиолангуажеиндекс</span><span class="sxs-lookup"><span data-stu-id="bb33b-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="bb33b-107">Свойство **куррентаудиолангуажеиндекс** Возвращает или задает отсчитываемый от единицы индекс, соответствующий звуковому языку для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="bb33b-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb33b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bb33b-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="bb33b-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bb33b-109">Property value</span></span>

<span data-ttu-id="bb33b-110">Объект **System. Int32** , являющийся индексом, основанным на одном из языков.</span><span class="sxs-lookup"><span data-stu-id="bb33b-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb33b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bb33b-111">Remarks</span></span>

<span data-ttu-id="bb33b-112">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="bb33b-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="bb33b-113">Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="bb33b-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb33b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bb33b-114">Requirements</span></span>



| <span data-ttu-id="bb33b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bb33b-115">Requirement</span></span> | <span data-ttu-id="bb33b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bb33b-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb33b-117">Версия</span><span class="sxs-lookup"><span data-stu-id="bb33b-117">Version</span></span><br/>   | <span data-ttu-id="bb33b-118">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bb33b-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bb33b-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bb33b-119">Namespace</span></span><br/> | <span data-ttu-id="bb33b-120">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="bb33b-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bb33b-121">Сборка</span><span class="sxs-lookup"><span data-stu-id="bb33b-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bb33b-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="bb33b-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb33b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bb33b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb33b-124">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb33b-125">**IWMPControls3. Аудиолангуажекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb33b-126">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb33b-127">**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb33b-128">**IWMPControls3. Жетаудиолангуажеид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bb33b-129">**IWMPControls3. Жетлангуаженаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="bb33b-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





