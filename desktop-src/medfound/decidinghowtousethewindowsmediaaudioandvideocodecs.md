---
description: Использование кодеков и объектов DSP
ms.assetid: ec571d31-6542-421a-8027-d4c61ce00035
title: Использование кодеков и объектов DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a88670298bfc16ca1dc5053cabeb4f4e631c5c47
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713275"
---
# <a name="using-the-codec-and-dsp-objects"></a><span data-ttu-id="e54f4-103">Использование кодеков и объектов DSP</span><span class="sxs-lookup"><span data-stu-id="e54f4-103">Using the Codec and DSP Objects</span></span>

<span data-ttu-id="e54f4-104">Существует несколько способов использования кодеков аудио и видео Windows Media и DSP для кодирования, декодирования или преобразования мультимедийного содержимого.</span><span class="sxs-lookup"><span data-stu-id="e54f4-104">There are several ways to use the Windows Media Audio and Video codecs and DSPs to encode, decode, or transform your digital media content.</span></span> <span data-ttu-id="e54f4-105">Аудиокодек Windows Media аудио и видео и API DSP предназначены для тех пользователей, которым требуется ручная настройка кодеков и объектов DSP, или их использование вне контекста одного из пакетов SDK для Windows Media, таких как Windows Media Format SDK или Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="e54f4-105">The Windows Media Audio and Video Codec and DSP API is intended for those users who need to configure codec and DSP objects manually or use them outside of the context one of the Windows Media SDKs, such as the Windows Media Format SDK or Media Foundation SDK.</span></span>

<span data-ttu-id="e54f4-106">Создатели содержимого и конечные пользователи могут использовать разнообразные средства и приложения для кодирования содержимого в потоках Windows Media Audio или Windows Media Video Streams.</span><span class="sxs-lookup"><span data-stu-id="e54f4-106">Content creators and end users can use a variety of tools and applications to encode content in Windows Media Audio or Windows Media Video streams.</span></span> <span data-ttu-id="e54f4-107">Например, кодировщик Windows Media специально разработан для упрощения процесса кодирования.</span><span class="sxs-lookup"><span data-stu-id="e54f4-107">Windows Media Encoder, for example, is specifically designed to make the encoding process easy.</span></span> <span data-ttu-id="e54f4-108">Аналогичным образом проигрыватель Windows Media специально разработан для работы с цифровыми данными мультимедиа, закодированными в форматах Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e54f4-108">Likewise, Windows Media Player is specially designed to work well with digital media data that is encoded in Windows Media formats.</span></span> <span data-ttu-id="e54f4-109">Для многих приложений требуется только использование пакета SDK для кодировщика Windows Media или пакета SDK проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e54f4-109">For many applications, using the Windows Media Encoder SDK or the Windows Media Player SDK is all that is needed.</span></span> <span data-ttu-id="e54f4-110">В частности, эти две технологии хорошо подходят для сценариев, которые похожи на функциональные возможности средств, которые они автоматизируют.</span><span class="sxs-lookup"><span data-stu-id="e54f4-110">In particular, these two technologies are good for scenarios that resemble the functionality of the tools they automate.</span></span>

<span data-ttu-id="e54f4-111">Если вам требуется больший контроль над процессом кодирования или декодирования, но вы по-прежнему планируете использовать расширенный системный формат (ASF) в качестве контейнера для мультимедийных данных, может быть хорошим выбором пакет SDK для формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e54f4-111">If you need greater control over the encoding or decoding process, but you still intend to use the Advanced Systems Format (ASF) as a container for your media data, the Windows Media Format SDK might be a good choice.</span></span> <span data-ttu-id="e54f4-112">Объекты пакета SDK Windows Media Format предоставляют гибкую платформу для создания файлов ASF и предоставляют встроенную поддержку кодеков аудио и видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e54f4-112">The objects of the Windows Media Format SDK provide a flexible framework for creating ASF files, and provide built-in support for the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="e54f4-113">Пакет SDK для Media Foundation, который впервые используется для Windows Vista, значительно упрощает кодирование и декодирование, предоставляя настраиваемый конвейер мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e54f4-113">The Media Foundation SDK, which is new for Windows Vista, greatly simplifies encoding and decoding by providing a customizable media pipeline.</span></span> <span data-ttu-id="e54f4-114">Вы можете задать свойства входного и выходного медиа, а Media Foundation загрузчик топологии будет настраивать необходимые кодеки и поставщики для вас.</span><span class="sxs-lookup"><span data-stu-id="e54f4-114">You can set input and output media properties and the Media Foundation topology loader will configure the necessary codecs and DSPs for you.</span></span>

<span data-ttu-id="e54f4-115">Основная причина для непосредственного использования объектов кодека заключается в использовании кодеков аудио и видео Windows Media за пределами контейнера ASF.</span><span class="sxs-lookup"><span data-stu-id="e54f4-115">The primary reason for using the codec objects directly is to use the Windows Media Audio and Video codecs outside of the ASF container.</span></span> <span data-ttu-id="e54f4-116">Использование кодеков и объектов DSP также обеспечивает уровень контроля, недоступный при использовании любой из более абстрактных технологий.</span><span class="sxs-lookup"><span data-stu-id="e54f4-116">Using the codec and DSP objects also provides a level of control that is unavailable using any of the more abstracted technologies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e54f4-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e54f4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e54f4-118">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="e54f4-118">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



