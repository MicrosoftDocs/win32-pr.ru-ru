---
description: Альфа-смешение
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Альфа-смешение (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4293448849926cfc6723495619137262e004636e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140458"
---
# <a name="alpha-blending-directshow"></a><span data-ttu-id="9d264-103">Альфа-смешение (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="9d264-103">Alpha Blending (DirectShow)</span></span>

<span data-ttu-id="9d264-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="9d264-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="9d264-105">В этой статье описывается альфа-смешение в [службах редактирования DirectShow](directshow-editing-services.md) (DES).</span><span class="sxs-lookup"><span data-stu-id="9d264-105">This article describes alpha blending in [DirectShow Editing Services](directshow-editing-services.md) (DES).</span></span>

<span data-ttu-id="9d264-106">Альфа измеряет прозрачность пикселя или изображения.</span><span class="sxs-lookup"><span data-stu-id="9d264-106">Alpha measures the transparency of a pixel or image.</span></span> <span data-ttu-id="9d264-107">В 32-битном несжатом видео RGB четыре компонента определяют каждый пиксел: альфа-канал (A) и три цветовых компонента (RGB).</span><span class="sxs-lookup"><span data-stu-id="9d264-107">In 32-bit uncompressed RGB video, four components define each pixel: an alpha channel (A) and three color components (RGB).</span></span> <span data-ttu-id="9d264-108">Пиксел со значением альфа, равным нулю, полностью прозрачен.</span><span class="sxs-lookup"><span data-stu-id="9d264-108">A pixel with an alpha value of zero is completely transparent.</span></span> <span data-ttu-id="9d264-109">Пиксель с альфа-значением 255 является непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="9d264-109">A pixel with an alpha value of 255 is opaque.</span></span> <span data-ttu-id="9d264-110">Между этими значениями пиксел имеет различные степени прозрачности.</span><span class="sxs-lookup"><span data-stu-id="9d264-110">Between these values, the pixel has various degrees of transparency.</span></span>

<span data-ttu-id="9d264-111">DirectShow определяет два типа мультимедиа для 32-разрядного видео RGB:</span><span class="sxs-lookup"><span data-stu-id="9d264-111">DirectShow defines two media types for 32-bit RGB video:</span></span>

-   <span data-ttu-id="9d264-112">**Медиасубтипе \_ ARGB32**: видео — 32-разрядный RGB с допустимым альфа-каналом.</span><span class="sxs-lookup"><span data-stu-id="9d264-112">**MEDIASUBTYPE\_ARGB32**: The video is 32-bit RGB with a valid alpha channel.</span></span>
-   <span data-ttu-id="9d264-113">**Медиасубтипе \_ RGB32**: пикселей — 32 бит, но альфа-канал необязательно должен быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="9d264-113">**MEDIASUBTYPE\_RGB32**: Pixels are 32 bits, but the alpha channel is not necessarily valid.</span></span>

<span data-ttu-id="9d264-114">Чтобы выполнить альфа-смешение в DES, задайте для несжатого носителя видеогруппы тип МЕДИАСУБТИПЕ \_ ARGB32.</span><span class="sxs-lookup"><span data-stu-id="9d264-114">To perform alpha blending in DES, set the video group's uncompressed media type to MEDIASUBTYPE\_ARGB32.</span></span> <span data-ttu-id="9d264-115">В C++ вызовите метод [**иамтимелинеграуп:: сетмедиатипе**](iamtimelinegroup-setmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="9d264-115">In C++, call the [**IAMTimelineGroup::SetMediaType**](iamtimelinegroup-setmediatype.md) method.</span></span> <span data-ttu-id="9d264-116">В формате КСТЛ установка для атрибута [**битдепс**](bitdepth-attribute.md) элемента [**group**](group-element.md) равна 32.</span><span class="sxs-lookup"><span data-stu-id="9d264-116">In the XTL format, setting the [**bitdepth**](bitdepth-attribute.md) attribute of the [**group**](group-element.md) element to 32 accomplishes this as well.</span></span>

<span data-ttu-id="9d264-117">Далее необходимы данные видео, содержащие альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="9d264-117">Next, you need video data that contains an alpha channel.</span></span> <span data-ttu-id="9d264-118">Существует несколько вариантов:</span><span class="sxs-lookup"><span data-stu-id="9d264-118">There are several options:</span></span>

-   <span data-ttu-id="9d264-119">Вы можете использовать AVI-файл, в котором уже есть 32 разряд видео RGB с данными Alpha.</span><span class="sxs-lookup"><span data-stu-id="9d264-119">You can use an AVI file that already has 32-bit RGB video with alpha data.</span></span> <span data-ttu-id="9d264-120">В настоящее время альфа не поддерживается для исходных файлов MPEG или Microsoft Windows Media Format (WMF).</span><span class="sxs-lookup"><span data-stu-id="9d264-120">Currently, alpha is not supported for MPEG or Microsoft Windows Media Format (WMF) source files.</span></span>
-   <span data-ttu-id="9d264-121">DES поддерживает 32-битовые точечные (BMP) и Targa (TGA) файлы с альфа-данными.</span><span class="sxs-lookup"><span data-stu-id="9d264-121">DES supports 32-bit bitmap (.bmp) and Targa (.tga) files with alpha data.</span></span>
-   <span data-ttu-id="9d264-122">Можно написать настраиваемый фильтр источника, создающий 32-битные данные RGB с альфа.</span><span class="sxs-lookup"><span data-stu-id="9d264-122">You can write a custom source filter that creates 32-bit RGB data with alpha.</span></span> <span data-ttu-id="9d264-123">Тип выходного носителя должен быть **медиасубтипе \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="9d264-123">The output media type must be **MEDIASUBTYPE\_ARGB32**.</span></span> <span data-ttu-id="9d264-124">Используйте фильтр в качестве подобъекта в исходном объекте временной шкалы.</span><span class="sxs-lookup"><span data-stu-id="9d264-124">Use the filter as the subobject in a timeline source object.</span></span>

<span data-ttu-id="9d264-125">Если источник видео не имеет альфа-канала, можно использовать эффекты, создающие альфа-данные.</span><span class="sxs-lookup"><span data-stu-id="9d264-125">If your video source does not have alpha, you can use an effect that creates alpha data.</span></span> <span data-ttu-id="9d264-126">В [результате установки альфа](alpha-setter-effect.md) -канала для всего изображения устанавливается постоянное значение.</span><span class="sxs-lookup"><span data-stu-id="9d264-126">The [Alpha Setter Effect](alpha-setter-effect.md) sets the alpha channel for the entire image to a constant value.</span></span> <span data-ttu-id="9d264-127">Для изменения альфа-канала с течением времени используйте интерфейс [**ипропертисеттер**](ipropertysetter.md) с параметром альфа-установки.</span><span class="sxs-lookup"><span data-stu-id="9d264-127">To vary the alpha over time, use the [**IPropertySetter**](ipropertysetter.md) interface with the Alpha Setter Effect.</span></span> <span data-ttu-id="9d264-128">Размер исходного источника не должен составлять 32 бит, если тип носителя группы **медиасубтипе \_ ARGB32**.</span><span class="sxs-lookup"><span data-stu-id="9d264-128">The original source does not have to be 32 bits, as long as the group's uncompressed media type is **MEDIASUBTYPE\_ARGB32**.</span></span>

<span data-ttu-id="9d264-129">Наконец, передайте видео в действие или переход, которое выполняет альфа-смешение.</span><span class="sxs-lookup"><span data-stu-id="9d264-129">Finally, pass the video to an effect or transition that performs alpha blending.</span></span> <span data-ttu-id="9d264-130">[Переход компоновщика](compositor-transition.md) выполняет альфа-смешение, а [ключевой переход](key-transition.md) может иметь ключевое значение по альфа-значению.</span><span class="sxs-lookup"><span data-stu-id="9d264-130">The [Compositor Transition](compositor-transition.md) performs alpha blending, and the [Key Transition](key-transition.md) can key by alpha value.</span></span>

<span data-ttu-id="9d264-131">В следующем примере проекта КСТЛ выполняется альфа-смешение:</span><span class="sxs-lookup"><span data-stu-id="9d264-131">The following sample XTL project performs alpha blending:</span></span>


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a><span data-ttu-id="9d264-132">См. также</span><span class="sxs-lookup"><span data-stu-id="9d264-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d264-133">Использование служб редактирования DirectShow</span><span class="sxs-lookup"><span data-stu-id="9d264-133">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



