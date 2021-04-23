---
title: IWMPControls3 Жетаудиолангуажедескриптион, метод
description: Метод Жетаудиолангуажедескриптион Возвращает описание для аудио-языка, соответствующего указанному индексу, основанному на единице.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- Жетаудиолангуажедескриптион метод Windows Media Player
- Жетаудиолангуажедескриптион метод проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, метод Жетаудиолангуажедескриптион
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649053"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="a6793-106">Метод IWMPControls3:: Жетаудиолангуажедескриптион</span><span class="sxs-lookup"><span data-stu-id="a6793-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="a6793-107">Метод **жетаудиолангуажедескриптион** Возвращает описание для аудио-языка, соответствующего указанному индексу, основанному на единице.</span><span class="sxs-lookup"><span data-stu-id="a6793-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6793-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6793-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="a6793-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6793-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a6793-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6793-111">Объект **System. Int32** , который является индексом звукового языка на основе одного.</span><span class="sxs-lookup"><span data-stu-id="a6793-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6793-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a6793-112">Return value</span></span>

<span data-ttu-id="a6793-113">**Строка System. String** , которая является описанием звукового языка.</span><span class="sxs-lookup"><span data-stu-id="a6793-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6793-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6793-114">Remarks</span></span>

<span data-ttu-id="a6793-115">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="a6793-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="a6793-116">Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков, а затем получите доступ к звуковому языку по отдельности с помощью индекса, основанного на единицах.</span><span class="sxs-lookup"><span data-stu-id="a6793-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6793-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a6793-117">Requirements</span></span>



| <span data-ttu-id="a6793-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a6793-118">Requirement</span></span> | <span data-ttu-id="a6793-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a6793-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6793-120">Версия</span><span class="sxs-lookup"><span data-stu-id="a6793-120">Version</span></span><br/>   | <span data-ttu-id="a6793-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="a6793-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a6793-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a6793-122">Namespace</span></span><br/> | <span data-ttu-id="a6793-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="a6793-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a6793-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="a6793-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a6793-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a6793-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6793-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a6793-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6793-127">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6793-128">**IWMPControls3. Аудиолангуажекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6793-129">**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6793-130">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6793-131">**IWMPControls3. Жетаудиолангуажеид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a6793-132">**IWMPControls3. Жетлангуаженаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="a6793-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





