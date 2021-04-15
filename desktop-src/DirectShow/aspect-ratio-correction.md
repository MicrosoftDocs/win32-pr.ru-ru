---
description: Исправление пропорций
ms.assetid: 0ed6010b-9168-44b1-be49-0c9d5d77ce3f
title: Исправление пропорций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2460f7ecce1513394d941eafe8bdf8a7a80e9727
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655599"
---
# <a name="aspect-ratio-correction"></a><span data-ttu-id="7fa53-103">Исправление пропорций</span><span class="sxs-lookup"><span data-stu-id="7fa53-103">Aspect Ratio Correction</span></span>

<span data-ttu-id="7fa53-104">Этот раздел относится к пакету обновления 2 (SP2) для Windows XP или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="7fa53-104">This topic applies to Windows XP Service Pack 2 or later.</span></span>

<span data-ttu-id="7fa53-105">В режиме смешивания фильтр VMR изменяет пропорции изображения на правильное.</span><span class="sxs-lookup"><span data-stu-id="7fa53-105">In mixing mode, the VMR sizes the video to the correct aspect ratio.</span></span> <span data-ttu-id="7fa53-106">(Исключение: см. раздел [смешение, не являющийся квадратным](non-square-mixing.md).) Это может потребовать растяжения видео, если предпочтительные пропорции не совпадают с физическими пропорциями изображения.</span><span class="sxs-lookup"><span data-stu-id="7fa53-106">(Exception: See [Non-Square Mixing](non-square-mixing.md).) This may require stretching the video if the preferred aspect ratio is not the same as the image's physical aspect ratio.</span></span> <span data-ttu-id="7fa53-107">Например, формат цифрового видео (DV) — 720 x 480 пикселей (3:2), но он должен отображаться с пропорциями 4:3.</span><span class="sxs-lookup"><span data-stu-id="7fa53-107">For example, digital video (DV) format is 720 x 480 pixels (3:2) but should be displayed at a 4:3 aspect ratio.</span></span>

<span data-ttu-id="7fa53-108">VMR поддерживает два различных поведения для исправления пропорций:</span><span class="sxs-lookup"><span data-stu-id="7fa53-108">The VMR supports two different behaviors for aspect ratio correction:</span></span>

-   <span data-ttu-id="7fa53-109">Измените горизонтальный или вертикальный размер, чтобы изображение всегда растянуто, но не сжато.</span><span class="sxs-lookup"><span data-stu-id="7fa53-109">Adjust either the horizontal or vertical size, so that the image is always stretched, never shrunk.</span></span> <span data-ttu-id="7fa53-110">Теперь это поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7fa53-110">This is now the default behavior.</span></span>
-   <span data-ttu-id="7fa53-111">Настройте горизонтальный размер, растягивание или сжатие видео.</span><span class="sxs-lookup"><span data-stu-id="7fa53-111">Adjust the horizontal size, either stretching or shrinking the video.</span></span>

<span data-ttu-id="7fa53-112">Поскольку второе поведение (только горизонтальная корректировка) может привести к сжатию видео, выходное изображение может иметь меньшее разрешение.</span><span class="sxs-lookup"><span data-stu-id="7fa53-112">Because the second behavior (horizontal adjustment only) may entail shrinking the video, the output image may have less resolution.</span></span> <span data-ttu-id="7fa53-113">По этой причине первое поведение является предпочтительным.</span><span class="sxs-lookup"><span data-stu-id="7fa53-113">For this reason, the first behavior is preferred.</span></span> <span data-ttu-id="7fa53-114">Например, если в 720 x 480 видео соблюдается пропорции 4:3, поведение по умолчанию выдает изображение 720 x 550, а горизонтальная корректировка — изображение с меньшим размером в 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="7fa53-114">For example, in the case of 720 x 480 video at 4:3 aspect ratio, the default behavior produces a 720 x 550 image, while horizontal adjustment produces a smaller 640 x 480 image.</span></span>

<span data-ttu-id="7fa53-115">**VMR-7**: чтобы задать параметры исправления пропорций, вызовите [**Ивмрмиксерконтрол:: сетмиксингпрефс**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span><span class="sxs-lookup"><span data-stu-id="7fa53-115">**VMR-7**: To set the aspect ratio correction preference, call [**IVMRMixerControl::SetMixingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrmixercontrol-setoutputrect).</span></span> <span data-ttu-id="7fa53-116">Установите флаг Миксерпреф \_ араджустксори для поведения по умолчанию или снимите этот флажок только для горизонтальной корректировки.</span><span class="sxs-lookup"><span data-stu-id="7fa53-116">Set the MixerPref\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

<span data-ttu-id="7fa53-117">**VMR-9**. чтобы задать параметры исправления пропорций, вызовите [**IVMRMixerControl9:: сетмиксингпрефс**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span><span class="sxs-lookup"><span data-stu-id="7fa53-117">**VMR-9**: To set the aspect ratio correction preference, call [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs).</span></span> <span data-ttu-id="7fa53-118">Установите флаг MixerPref9 \_ араджустксори для поведения по умолчанию или снимите этот флажок только для горизонтальной корректировки.</span><span class="sxs-lookup"><span data-stu-id="7fa53-118">Set the MixerPref9\_ARAdjustXorY flag for the default behavior, or clear this flag for horizontal adjustment only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fa53-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7fa53-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fa53-120">Использование режима смешения VMR</span><span class="sxs-lookup"><span data-stu-id="7fa53-120">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



