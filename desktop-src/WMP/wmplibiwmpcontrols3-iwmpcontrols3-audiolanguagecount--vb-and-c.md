---
title: IWMPControls3 Аудиолангуажекаунт, свойство
description: Свойство Аудиолангуажекаунт возвращает число поддерживаемых аудио языков.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- Проигрыватель Windows Media для свойства Аудиолангуажекаунт
- Аудиолангуажекаунт свойство проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, свойство Аудиолангуажекаунт
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689292"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="72b05-106">Свойство IWMPControls3:: Аудиолангуажекаунт</span><span class="sxs-lookup"><span data-stu-id="72b05-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="72b05-107">Свойство **аудиолангуажекаунт** возвращает число поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="72b05-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b05-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72b05-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="72b05-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="72b05-109">Property value</span></span>

<span data-ttu-id="72b05-110">Значение **System. Int32** , которое является числом поддерживаемых аудио языков.</span><span class="sxs-lookup"><span data-stu-id="72b05-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="72b05-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72b05-111">Remarks</span></span>

<span data-ttu-id="72b05-112">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="72b05-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b05-113">Требования</span><span class="sxs-lookup"><span data-stu-id="72b05-113">Requirements</span></span>



| <span data-ttu-id="72b05-114">Требование</span><span class="sxs-lookup"><span data-stu-id="72b05-114">Requirement</span></span> | <span data-ttu-id="72b05-115">Значение</span><span class="sxs-lookup"><span data-stu-id="72b05-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72b05-116">Версия</span><span class="sxs-lookup"><span data-stu-id="72b05-116">Version</span></span><br/>   | <span data-ttu-id="72b05-117">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="72b05-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="72b05-118">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72b05-118">Namespace</span></span><br/> | <span data-ttu-id="72b05-119">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="72b05-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="72b05-120">Сборка</span><span class="sxs-lookup"><span data-stu-id="72b05-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="72b05-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="72b05-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b05-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72b05-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b05-123">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b05-124">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b05-125">**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b05-126">**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b05-127">**IWMPControls3. Жетаудиолангуажеид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="72b05-128">**IWMPControls3. Жетлангуаженаме (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="72b05-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





