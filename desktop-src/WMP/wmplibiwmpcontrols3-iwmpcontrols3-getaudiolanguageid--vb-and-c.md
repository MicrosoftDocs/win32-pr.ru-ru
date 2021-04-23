---
title: IWMPControls3 Жетаудиолангуажеид, метод
description: Метод Жетаудиолангуажеид возвращает код локали (LCID) для указанного индекса языкового звука.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- Жетаудиолангуажеид метод Windows Media Player
- Жетаудиолангуажеид метод проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, метод Жетаудиолангуажеид
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649052"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="58292-106">Метод IWMPControls3:: Жетаудиолангуажеид</span><span class="sxs-lookup"><span data-stu-id="58292-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="58292-107">Метод **жетаудиолангуажеид** возвращает код локали (LCID) для указанного индекса языкового звука.</span><span class="sxs-lookup"><span data-stu-id="58292-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="58292-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58292-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="58292-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="58292-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58292-110">*Линдекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="58292-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58292-111">Объект **System. Int32** , который является индексом аудио языка, основанным на единицах.</span><span class="sxs-lookup"><span data-stu-id="58292-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58292-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58292-112">Return value</span></span>

<span data-ttu-id="58292-113">Значение **System. Int32** , которое является LCID.</span><span class="sxs-lookup"><span data-stu-id="58292-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="58292-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58292-114">Remarks</span></span>

<span data-ttu-id="58292-115">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="58292-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="58292-116">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="58292-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="58292-117">Используйте свойство **аудиолангуажекаунт** , чтобы получить количество поддерживаемых аудио языков, а затем получите доступ к звуковому языку по отдельности с помощью индекса, основанного на единицах.</span><span class="sxs-lookup"><span data-stu-id="58292-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="58292-118">Требования</span><span class="sxs-lookup"><span data-stu-id="58292-118">Requirements</span></span>



| <span data-ttu-id="58292-119">Требование</span><span class="sxs-lookup"><span data-stu-id="58292-119">Requirement</span></span> | <span data-ttu-id="58292-120">Значение</span><span class="sxs-lookup"><span data-stu-id="58292-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="58292-121">Версия</span><span class="sxs-lookup"><span data-stu-id="58292-121">Version</span></span><br/>   | <span data-ttu-id="58292-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="58292-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="58292-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58292-123">Namespace</span></span><br/> | <span data-ttu-id="58292-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="58292-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="58292-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="58292-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="58292-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="58292-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58292-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58292-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58292-128">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58292-129">**IWMPControls3. Аудиолангуажекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58292-130">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58292-131">**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58292-132">**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="58292-133">**IWMPControls3. Жетлангуаженаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="58292-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





