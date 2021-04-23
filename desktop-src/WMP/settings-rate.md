---
title: Параметры. rate
description: Свойство Rate указывает или получает текущую скорость воспроизведения видео мультимедиа.
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- Параметры. частота Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105651845"
---
# <a name="settingsrate"></a><span data-ttu-id="3d8d9-104">Параметры. rate</span><span class="sxs-lookup"><span data-stu-id="3d8d9-104">Settings.rate</span></span>

<span data-ttu-id="3d8d9-105">Свойство **Rate** указывает или получает текущую скорость воспроизведения видео мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8d9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d8d9-106">Syntax</span></span>

<span data-ttu-id="3d8d9-107">Player. Settings. rate</span><span class="sxs-lookup"><span data-stu-id="3d8d9-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="3d8d9-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="3d8d9-108">Possible Values</span></span>

<span data-ttu-id="3d8d9-109">Это свойство имеет **номер** для чтения и записи (**Double**) со значением по умолчанию 1,0.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d8d9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d8d9-110">Remarks</span></span>

<span data-ttu-id="3d8d9-111">Это свойство выступает в качестве значения множителя, которое позволяет воспроизводить клип с более высокой или низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="3d8d9-112">Значение по умолчанию 1,0 указывает на созданную скорость.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="3d8d9-113">Обратите внимание, что звуковая дорожка будет трудной для понимания на скорости ниже 0,5 или выше 1,5.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="3d8d9-114">Скорость воспроизведения 2 равна удвоенной обычной скорости воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="3d8d9-115">Проигрыватель Windows Media попытается использовать наиболее эффективный из четырех различных режимов воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="3d8d9-116">Эти режимы поддерживают плавное воспроизведение видео с выходом звука, плавное воспроизведение видео с неподдерживаемыми звуковыми сигналами, плавное воспроизведение видео без звука и воспроизведение видео по опорным кадрам без звука.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="3d8d9-117">Режим, выбранный проигрывателем, зависит от множества факторов, включая тип файла и расположение, операционную систему, сеть и сервер.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="3d8d9-118">Кроме того, в зависимости от типа носителя также применяются и другие соображения.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="3d8d9-119">Формат Windows Media Format (WMV) и ASF-файлы. оптимальные значения для этого свойства: от 1 до 10 или от 1 до 10 для обратного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="3d8d9-120">Значения от 0,5 до 1,0 или от-0,5 до-1,0 могут также работать в случаях, когда звук может поддерживаться, например при воспроизведении файлов, расположенных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="3d8d9-121">Значения с абсолютной величиной больше 10 допускаются, но не очень важны.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="3d8d9-122">Другие типы мультимедиа: это свойство может принимать значения от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="3d8d9-123">Отрицательные значения не допускаются.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-123">Negative values are not allowed.</span></span> <span data-ttu-id="3d8d9-124">Значения меньше 1 представляют медленное движение.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="3d8d9-125">Значения, указанные выше 9, разрешены, но не очень важны.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="3d8d9-126">*Элементы управления*. метод **фастфорвард** изменяет значение **Rate** на 5,0, а *элементы управления*. **Частота** изменения метода **фастреверсе** равна 5,0.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="3d8d9-127">Скорость воспроизведения некоторых типов носителей не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="3d8d9-128">Используйте *Параметры*. **доступный** метод, позволяющий определить, можно ли указать это свойство для конкретного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="3d8d9-129">**Проигрыватель Windows Media 10 Mobile**: это свойство принимает или возвращает значения-5,0, 1,0 или 5,0.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="3d8d9-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="3d8d9-130">Examples</span></span>

<span data-ttu-id="3d8d9-131">В следующем примере создается HTML-элемент SELECT, который позволяет пользователю изменить скорость воспроизведения текущего носителя.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="3d8d9-132">Параметры SELECT обеспечивают нормальную скорость воспроизведения с половинной скоростью и двойной скоростью.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="3d8d9-133">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="3d8d9-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="3d8d9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="3d8d9-134">Requirements</span></span>



| <span data-ttu-id="3d8d9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="3d8d9-135">Requirement</span></span> | <span data-ttu-id="3d8d9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="3d8d9-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8d9-137">Версия</span><span class="sxs-lookup"><span data-stu-id="3d8d9-137">Version</span></span><br/> | <span data-ttu-id="3d8d9-138">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="3d8d9-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3d8d9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="3d8d9-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="3d8d9-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d8d9-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d8d9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d8d9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d8d9-142">**Controls. Фастфорвард**</span><span class="sxs-lookup"><span data-stu-id="3d8d9-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="3d8d9-143">**Controls. Фастреверсе**</span><span class="sxs-lookup"><span data-stu-id="3d8d9-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="3d8d9-144">**Объект параметров**</span><span class="sxs-lookup"><span data-stu-id="3d8d9-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="3d8d9-145">**Settings. Available**</span><span class="sxs-lookup"><span data-stu-id="3d8d9-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





