---
title: IWMPControls3 Жетлангуаженаме, метод
description: Метод Жетлангуаженаме возвращает имя звукового языка с указанным кодом локали (LCID).
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- Жетлангуаженаме метод Windows Media Player
- Жетлангуаженаме метод проигрывателя Windows Media Player, интерфейс IWMPControls3
- Интерфейс IWMPControls3 Windows Media Player, метод Жетлангуаженаме
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649051"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="6d0e4-106">Метод IWMPControls3:: Жетлангуаженаме</span><span class="sxs-lookup"><span data-stu-id="6d0e4-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="6d0e4-107">Метод **жетлангуаженаме** возвращает имя звукового языка с указанным кодом локали (LCID).</span><span class="sxs-lookup"><span data-stu-id="6d0e4-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0e4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d0e4-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="6d0e4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d0e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d0e4-110">*ллангид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d0e4-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d0e4-111">Значение **System. Int32** , которое является LCID.</span><span class="sxs-lookup"><span data-stu-id="6d0e4-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d0e4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d0e4-112">Return value</span></span>

<span data-ttu-id="6d0e4-113">**Строка System. String** , которая является именем звукового языка.</span><span class="sxs-lookup"><span data-stu-id="6d0e4-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0e4-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d0e4-114">Remarks</span></span>

<span data-ttu-id="6d0e4-115">Код языка (LCID) однозначно определяет определенный диалект языка, который называется локальным языком.</span><span class="sxs-lookup"><span data-stu-id="6d0e4-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="6d0e4-116">Для содержимого на основе Windows Media свойства и методы, связанные с выбором языка, поддерживают только один выход.</span><span class="sxs-lookup"><span data-stu-id="6d0e4-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d0e4-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6d0e4-117">Requirements</span></span>



| <span data-ttu-id="6d0e4-118">Требование</span><span class="sxs-lookup"><span data-stu-id="6d0e4-118">Requirement</span></span> | <span data-ttu-id="6d0e4-119">Значение</span><span class="sxs-lookup"><span data-stu-id="6d0e4-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0e4-120">Версия</span><span class="sxs-lookup"><span data-stu-id="6d0e4-120">Version</span></span><br/>   | <span data-ttu-id="6d0e4-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6d0e4-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6d0e4-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d0e4-122">Namespace</span></span><br/> | <span data-ttu-id="6d0e4-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6d0e4-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="6d0e4-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6d0e4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6d0e4-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0e4-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d0e4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0e4-127">**Интерфейс IWMPControls3 (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0e4-128">**IWMPControls3. Аудиолангуажекаунт (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0e4-129">**IWMPControls3. Куррентаудиолангуаже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0e4-130">**IWMPControls3. Куррентаудиолангуажеиндекс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0e4-131">**IWMPControls3. Жетаудиолангуажедескриптион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0e4-132">**IWMPControls3. Жетаудиолангуажеид (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0e4-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





