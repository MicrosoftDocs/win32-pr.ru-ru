---
title: Шаблоны соответствия устройств
description: Шаблоны соответствия устройств
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK, шаблоны соответствия устройств
- кодеки, шаблоны соответствия устройств
- шаблоны соответствия устройств, сведения
- шаблоны, шаблоны соответствия устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332328"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="ebeb3-107">Шаблоны соответствия устройств</span><span class="sxs-lookup"><span data-stu-id="ebeb3-107">Device Conformance Templates</span></span>

<span data-ttu-id="ebeb3-108">Кодеки Windows Media 9 Series поддерживают шаблоны согласованности устройств, которые задают диапазоны параметров конфигурации потока и алгоритмов кодеков.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="ebeb3-109">Каждый шаблон определяет диапазоны значений, соответствующих определенным устройствам.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="ebeb3-110">Раньше производители оборудования, которые предоставили устройствам, способным воспроизводить файлы ASF, работали со своими стандартами.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="ebeb3-111">Это привело к широкому разнородному спектру возможностей на схожих устройствах, которые в настоящее время существуют.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="ebeb3-112">С помощью шаблонов соответствия устройств кодеки Windows Media устанавливают общий Земля для аналогичных устройств.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="ebeb3-113">Производители оборудования могут указать, к каким шаблонам соответствуют устройства, а создателям содержимого — более уверенно нацелить их файлы на чтение устройств.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="ebeb3-114">Кроме того, приложения-проигрыватели легче определить, не подходит ли файл для устройства, прежде чем пытаться его воспроизвести.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="ebeb3-115">Шаблон соответствия устройств определяется строкой, которая хранится в виде атрибута метаданных, связанного с потоком, к которому применяется шаблон.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="ebeb3-116">Список шаблонов и их строк и параметров см. в разделе [Параметры шаблона соответствия устройств](device-conformance-template-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ebeb3-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="ebeb3-117">Шаблоны соответствия устройств поддерживаются для всех кодеков Windows Media 9 и более поздних версий, за исключением экранного кодека Windows Media Video 9 и кодека Windows Media Audio 9 без потерь.</span><span class="sxs-lookup"><span data-stu-id="ebeb3-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebeb3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ebeb3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebeb3-119">**Функции кодеков**</span><span class="sxs-lookup"><span data-stu-id="ebeb3-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="ebeb3-120">**Работа с шаблонами соответствия устройств**</span><span class="sxs-lookup"><span data-stu-id="ebeb3-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




