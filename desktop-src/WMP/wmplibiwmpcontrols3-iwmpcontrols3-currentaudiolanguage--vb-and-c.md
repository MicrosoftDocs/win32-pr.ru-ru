---
title: IWMPControls3 Куррентаудиолангуаже, свойство
description: Свойство Куррентаудиолангуаже Возвращает или задает код локали (LCID) звукового языка для воспроизведения.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- Проигрыватель Windows Media для свойства Куррентаудиолангуаже
- Куррентаудиолангуаже свойство проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, свойство Куррентаудиолангуаже
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708546"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="dbee6-106">Свойство IWMPControls3:: Куррентаудиолангуаже</span><span class="sxs-lookup"><span data-stu-id="dbee6-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="dbee6-107">Свойство **куррентаудиолангуаже** Возвращает или задает код локали (LCID) звукового языка для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="dbee6-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbee6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbee6-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="dbee6-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dbee6-109">Property value</span></span>

<span data-ttu-id="dbee6-110">Объект **System. Int32** , который является идентификатором языка аудио.</span><span class="sxs-lookup"><span data-stu-id="dbee6-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbee6-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dbee6-111">Remarks</span></span>

<span data-ttu-id="dbee6-112">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="dbee6-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="dbee6-113">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="dbee6-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="dbee6-114">При работе с содержимым DVD при указании LCID будет выбрана первая доступная звуковая дорожка с указанным ИДЕНТИФИКАТОРом языка.</span><span class="sxs-lookup"><span data-stu-id="dbee6-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbee6-115">Требования</span><span class="sxs-lookup"><span data-stu-id="dbee6-115">Requirements</span></span>



| <span data-ttu-id="dbee6-116">Требование</span><span class="sxs-lookup"><span data-stu-id="dbee6-116">Requirement</span></span> | <span data-ttu-id="dbee6-117">Значение</span><span class="sxs-lookup"><span data-stu-id="dbee6-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dbee6-118">Версия</span><span class="sxs-lookup"><span data-stu-id="dbee6-118">Version</span></span><br/>   | <span data-ttu-id="dbee6-119">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="dbee6-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dbee6-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dbee6-120">Namespace</span></span><br/> | <span data-ttu-id="dbee6-121">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="dbee6-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dbee6-122">Сборка</span><span class="sxs-lookup"><span data-stu-id="dbee6-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dbee6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="dbee6-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbee6-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbee6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbee6-125">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbee6-126">**IWMPControls3. Аудиолангуажекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbee6-127">**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbee6-128">**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbee6-129">**IWMPControls3. Жетаудиолангуажеид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dbee6-130">**IWMPControls3. Жетлангуаженаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="dbee6-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





