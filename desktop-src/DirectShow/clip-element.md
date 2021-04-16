---
description: Клип епеЦифиес источник мультимедиа.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Элемент Clip
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104494499"
---
# <a name="clip-element"></a><span data-ttu-id="02086-103">Элемент Clip</span><span class="sxs-lookup"><span data-stu-id="02086-103">clip Element</span></span>

> [!Note]  
> <span data-ttu-id="02086-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="02086-104">\[Deprecated.</span></span> <span data-ttu-id="02086-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="02086-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="02086-106">`clip`ЕпеЦифиес источник мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="02086-106">The `clip` epecifies a media source.</span></span>

## <a name="attributes"></a><span data-ttu-id="02086-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="02086-107">Attributes</span></span>

<span data-ttu-id="02086-108">[**CLSID**](clsid-attribute.md), [**Частота кадров**](framerate-attribute.md), [**Блокировка**](lock-attribute.md), [**мленгс**](mlength-attribute.md), [**мстарт**](mstart-attribute.md), [**МСТОП**](mstop-attribute.md), [**выкл**](mute-attribute.md)., [**src**](src-attribute.md), [**Запуск**](start-attribute.md), [**Завершение**](stop-attribute.md), [**поток**](stream-attribute.md), [**стретчмоде**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="02086-108">[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)</span></span>

## <a name="parentchild-information"></a><span data-ttu-id="02086-109">Сведения о родителе и дочернем элементе</span><span class="sxs-lookup"><span data-stu-id="02086-109">Parent/Child Information</span></span>



|          |                                  |
|----------|----------------------------------|
| <span data-ttu-id="02086-110">Parent</span><span class="sxs-lookup"><span data-stu-id="02086-110">Parent</span></span>   | [<span data-ttu-id="02086-111">**дорожк**</span><span class="sxs-lookup"><span data-stu-id="02086-111">**track**</span></span>](track-element.md)   |
| <span data-ttu-id="02086-112">Дети</span><span class="sxs-lookup"><span data-stu-id="02086-112">Children</span></span> | [<span data-ttu-id="02086-113">**тень**</span><span class="sxs-lookup"><span data-stu-id="02086-113">**effect**</span></span>](effect-element.md) |



 

## <a name="remarks"></a><span data-ttu-id="02086-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02086-114">Remarks</span></span>

<span data-ttu-id="02086-115">Атрибут **CLSID** задает идентификатор CLSID исходного фильтра, используемого в качестве источника.</span><span class="sxs-lookup"><span data-stu-id="02086-115">The **clsid** attribute specifies the CLSID of a source filter to use as the source.</span></span> <span data-ttu-id="02086-116">Не указывайте атрибуты **src** и **CLSID** в пределах одного `clip` элемента.</span><span class="sxs-lookup"><span data-stu-id="02086-116">Do not specify the **src** and **clsid** attributes within the same `clip` element.</span></span>

<span data-ttu-id="02086-117">Укажите по меньшей мере один атрибут времени запуска (**Start** или **мстарт**) и один атрибут времени окончания ("**останавливаться** " или " **МСТОП**").</span><span class="sxs-lookup"><span data-stu-id="02086-117">Specify at least one start-time attribute (**start** or **mstart**) and one stop-time attribute (**stop** or **mstop**).</span></span> <span data-ttu-id="02086-118">Если один из атрибутов времени начала не задан, по умолчанию используется значение 0 (начало временной шкалы для **начала** или начало клипа для **мстарт**).</span><span class="sxs-lookup"><span data-stu-id="02086-118">If one of the start-time attributes is unspecified, it defaults to 0 (the beginning of the timeline for **start**, or the beginning of the clip for **mstart**).</span></span> <span data-ttu-id="02086-119">Если один из атрибутов времени окончания не указан, DES предполагает нормальную скорость воспроизведения и соответственно вычисляет неопределенное время окончания.</span><span class="sxs-lookup"><span data-stu-id="02086-119">If one of the stop-time attributes is unspecified, DES assumes a normal playback rate and calculates the unspecified stop time accordingly.</span></span> <span data-ttu-id="02086-120">Если заданы оба значения времени окончания, при необходимости воспроизведение выполняется быстрее или медленнее обычного.</span><span class="sxs-lookup"><span data-stu-id="02086-120">If both stop times are specified, playback is faster or slower than normal, if necessary.</span></span>

<span data-ttu-id="02086-121">В следующем примере Длительность временной шкалы составляет семь секунд (время **окончания** — " **Начало**").</span><span class="sxs-lookup"><span data-stu-id="02086-121">In the following example, the timeline duration is seven seconds (**stop** minus **start**).</span></span> <span data-ttu-id="02086-122">Предполагается нормальная скорость воспроизведения, поэтому время окончания по умолчанию — 10 секунд (длительность плюс **мстарт**).</span><span class="sxs-lookup"><span data-stu-id="02086-122">Normal playback rate is assumed, so the media stop time defaults to 10 seconds (the duration plus **mstart**).</span></span>


```
<clip start="2" stop="9" mstart="3" />
```



<span data-ttu-id="02086-123">В следующем примере время запуска носителя по умолчанию равно 0, что приводит к превышению длительности носителя в 10 секунд.</span><span class="sxs-lookup"><span data-stu-id="02086-123">In the next example, the media start time defaults to 0, forcing the media duration to be 10 seconds.</span></span> <span data-ttu-id="02086-124">Длительность временной шкалы составляет пять секунд, поэтому клип воспроизводится в два раза больше обычного.</span><span class="sxs-lookup"><span data-stu-id="02086-124">The timeline duration is five seconds, so the clip plays back at twice the normal rate.</span></span>


```
<clip start="5" stop="10" mstop="10" />  
```



<span data-ttu-id="02086-125">Если атрибут **src** задает изображение по-прежнему, то des пытается загрузить ряд еще изображений для создания анимации.</span><span class="sxs-lookup"><span data-stu-id="02086-125">If the **src** attribute specifies a still image, DES attempts to load a series of still images to create an animation.</span></span> <span data-ttu-id="02086-126">Например, если атрибут **src** имеет значение IMAGE001.BMP, то DES ищет IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP и т. д.</span><span class="sxs-lookup"><span data-stu-id="02086-126">For example, if the **src** attribute is IMAGE001.BMP, DES looks for IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP, and so on.</span></span> <span data-ttu-id="02086-127">Если они существуют, они отображаются последовательно в числовом порядке с частотой, заданной атрибутом **частоты кадров** .</span><span class="sxs-lookup"><span data-stu-id="02086-127">Assuming they exist, they are displayed in sequential numerical order, at the rate specified by the **framerate** attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="02086-128">Примеры</span><span class="sxs-lookup"><span data-stu-id="02086-128">Examples</span></span>


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a><span data-ttu-id="02086-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02086-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02086-130">Элементы КСТЛ</span><span class="sxs-lookup"><span data-stu-id="02086-130">XTL Elements</span></span>](xtl-elements.md)
</dt> </dl>

 

 



