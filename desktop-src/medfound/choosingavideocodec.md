---
description: Выбор видеокодека
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: Выбор видеокодека (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262818"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="39578-103">Выбор видеокодека (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="39578-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="39578-104">Кодировщик Windows Media Video 9 поддерживает три категории закодированных выходных данных: основной профиль, расширенный профиль и образ.</span><span class="sxs-lookup"><span data-stu-id="39578-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="39578-105">Основная категория профиля обеспечивает Видеосжатие для сложного видеоматериала, например фильмов или музыкальных видео.</span><span class="sxs-lookup"><span data-stu-id="39578-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="39578-106">Функции основного профиля предоставляют широкий спектр параметров кодирования.</span><span class="sxs-lookup"><span data-stu-id="39578-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="39578-107">Основной профиль можно использовать для создания видео с очень низкими скоростями для доставки на карманные устройства или, на другом конце спектра, можно использовать для создания видео с высоким уровнем четкости для цифрового кинотеатра.</span><span class="sxs-lookup"><span data-stu-id="39578-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="39578-108">Выделение алгоритмов кодирования в основном профиле осуществляется на динамическом видеоматериале, но они подходят и для других видеоматериалов.</span><span class="sxs-lookup"><span data-stu-id="39578-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="39578-109">Основной профиль должен быть категорией по умолчанию для содержимого видео.</span><span class="sxs-lookup"><span data-stu-id="39578-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="39578-110">Для удовлетворения конкретных потребностей можно использовать категорию расширенного профиля, категорию образа или отдельный кодировщик, называемый кодировщиком экрана Windows Media Video 9.</span><span class="sxs-lookup"><span data-stu-id="39578-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="39578-111">В следующей таблице перечислены четыре варианта.</span><span class="sxs-lookup"><span data-stu-id="39578-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="39578-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="39578-112">Purpose</span></span></th>
<th><span data-ttu-id="39578-113">Кодек</span><span class="sxs-lookup"><span data-stu-id="39578-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39578-114">Кодировка видео общего назначения</span><span class="sxs-lookup"><span data-stu-id="39578-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="39578-115"><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="39578-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="39578-116">Профиль Main</span><span class="sxs-lookup"><span data-stu-id="39578-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39578-117">Кодирование видео или видео с высоким определением, которое соответствует расширенному профилю VC-1 SMPTE Standard</span><span class="sxs-lookup"><span data-stu-id="39578-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="39578-118"><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="39578-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="39578-119">Расширенный профиль</span><span class="sxs-lookup"><span data-stu-id="39578-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39578-120">Преобразование растровых изображений в динамическое видео</span><span class="sxs-lookup"><span data-stu-id="39578-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="39578-121"><a href="windowsmediavideo9encoder.md">Кодировщик Windows Media Video 9</a></span><span class="sxs-lookup"><span data-stu-id="39578-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="39578-122">Образ</span><span class="sxs-lookup"><span data-stu-id="39578-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39578-123">Кодирование компьютера — видео приложения (снимок экрана) или другое очень статическое видео</span><span class="sxs-lookup"><span data-stu-id="39578-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="39578-124"><a href="windowsmediavideo9screenencoder.md"><strong>Кодировщик экрана Windows Media видео 9</strong></a></span><span class="sxs-lookup"><span data-stu-id="39578-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="39578-125">См. также</span><span class="sxs-lookup"><span data-stu-id="39578-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39578-126">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="39578-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



