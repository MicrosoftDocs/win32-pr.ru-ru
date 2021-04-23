---
title: Метод Settings. setMode
description: Метод setMode устанавливает для различных режимов режим "активный" или "Неактивный".
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setMode метод Windows Media Player
- setMode метод Windows Media Player, класс Settings
- Класс параметров проигрыватель Windows Media Player, метод setMode
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651843"
---
# <a name="settingssetmode-method"></a><span data-ttu-id="cf1cf-106">Метод Settings. setMode</span><span class="sxs-lookup"><span data-stu-id="cf1cf-106">Settings.setMode method</span></span>

<span data-ttu-id="cf1cf-107">Метод **setMode** устанавливает для различных режимов режим "активный" или "Неактивный".</span><span class="sxs-lookup"><span data-stu-id="cf1cf-107">The **setMode** method sets various modes to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf1cf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cf1cf-108">Syntax</span></span>


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a><span data-ttu-id="cf1cf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cf1cf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf1cf-110">*моденаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf1cf-110">*modeName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1cf-111">**Строка** , указывающая имя изменяемого режима, содержащее одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-111">**String** specifying the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="cf1cf-112">Строка</span><span class="sxs-lookup"><span data-stu-id="cf1cf-112">String</span></span>     | <span data-ttu-id="cf1cf-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cf1cf-113">Description</span></span>                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1cf-114">ауторевинд</span><span class="sxs-lookup"><span data-stu-id="cf1cf-114">autoRewind</span></span> | <span data-ttu-id="cf1cf-115">Режим, указывающий, следует ли перематывает дорожки в начало после воспроизведения в конец.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-115">Mode indicating whether the tracks are rewound to the beginning after playing to the end.</span></span> <span data-ttu-id="cf1cf-116">Состояние по умолчанию — true.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-116">Default state is true.</span></span>                                                  |
| <span data-ttu-id="cf1cf-117">loop</span><span class="sxs-lookup"><span data-stu-id="cf1cf-117">loop</span></span>       | <span data-ttu-id="cf1cf-118">Режим, указывающий, повторяется ли последовательность дорожек.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-118">Mode indicating whether the sequence of tracks repeats itself.</span></span> <span data-ttu-id="cf1cf-119">Состояние по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-119">Default state is false.</span></span>                                                                            |
| <span data-ttu-id="cf1cf-120">шовфраме</span><span class="sxs-lookup"><span data-stu-id="cf1cf-120">showFrame</span></span>  | <span data-ttu-id="cf1cf-121">Режим, указывающий, отображается ли ближайший кадр видеоключа в текущей позиции, когда не воспроизводится.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-121">Mode indicating whether the nearest video key frame is displayed at the current position when not playing.</span></span> <span data-ttu-id="cf1cf-122">Состояние по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-122">Default state is false.</span></span> <span data-ttu-id="cf1cf-123">Не влияет на звуковые дорожки.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-123">Has no effect on audio tracks.</span></span> |
| <span data-ttu-id="cf1cf-124">shuffle</span><span class="sxs-lookup"><span data-stu-id="cf1cf-124">shuffle</span></span>    | <span data-ttu-id="cf1cf-125">Режим, указывающий, воспроизводятся ли дорожки в случайном порядке.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-125">Mode indicating whether the tracks are played in random order.</span></span> <span data-ttu-id="cf1cf-126">Состояние по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-126">Default state is false.</span></span>                                                                            |



 

</dd> <dt>

<span data-ttu-id="cf1cf-127">*состояние* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cf1cf-127">*state* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf1cf-128">**Логическое значение** , указывающее, активен ли новый заданный режим.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-128">**Boolean** specifying whether the new specified mode is active or not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf1cf-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cf1cf-129">Return value</span></span>

<span data-ttu-id="cf1cf-130">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-130">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf1cf-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cf1cf-131">Remarks</span></span>

<span data-ttu-id="cf1cf-132">Когда активен режим Шовфраме, проигрыватель должен получить доступ к содержимому дорожки, чтобы получить кадр видео.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-132">When the showFrame mode is active, the Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="cf1cf-133">Из-за соображений пропускной способности этот режим следует использовать с осторожностью при воспроизведении нелокального содержимого.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-133">Due to bandwidth considerations, use this mode cautiously when playing non-local content.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf1cf-134">Требования</span><span class="sxs-lookup"><span data-stu-id="cf1cf-134">Requirements</span></span>



| <span data-ttu-id="cf1cf-135">Требование</span><span class="sxs-lookup"><span data-stu-id="cf1cf-135">Requirement</span></span> | <span data-ttu-id="cf1cf-136">Значение</span><span class="sxs-lookup"><span data-stu-id="cf1cf-136">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf1cf-137">Версия</span><span class="sxs-lookup"><span data-stu-id="cf1cf-137">Version</span></span><br/> | <span data-ttu-id="cf1cf-138">Для режимов цикла и случайного воспроизведения проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-138">For loop and shuffle modes, Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="cf1cf-139">Для режимов Ауторевинд и Шовфраме, проигрыватель Windows Media 9 Series или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="cf1cf-139">For autoRewind and showFrame modes, Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="cf1cf-140">DLL</span><span class="sxs-lookup"><span data-stu-id="cf1cf-140">DLL</span></span><br/>     | <dl> <span data-ttu-id="cf1cf-141"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf1cf-141"><dt>Wmp.dll</dt></span></span> </dl>                                                                            |



## <a name="see-also"></a><span data-ttu-id="cf1cf-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cf1cf-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf1cf-143">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="cf1cf-143">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="cf1cf-144">**Settings. Мода**</span><span class="sxs-lookup"><span data-stu-id="cf1cf-144">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> </dl>

 

 





