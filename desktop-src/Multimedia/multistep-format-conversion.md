---
title: Многошаговое преобразование формата
description: Многошаговое преобразование формата
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Диспетчер аудиосжатия (ACM), преобразование данных
- ACM (диспетчер аудиосжатия), преобразование данных
- Примеры ACM, преобразование данных
- преобразование данных
- Функция Акмформатсугжест
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986532"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="756da-108">Многошаговое преобразование формата</span><span class="sxs-lookup"><span data-stu-id="756da-108">Multistep Format Conversion</span></span>

<span data-ttu-id="756da-109">Иногда ACM не может преобразовать данные из одного формата в другой за один шаг.</span><span class="sxs-lookup"><span data-stu-id="756da-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="756da-110">Например, приложению может потребоваться преобразовать 16-разрядные стерео-данные 44 кГц в значение, равное 11 кГц моно ADPCM.</span><span class="sxs-lookup"><span data-stu-id="756da-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="756da-111">Если программа сжатия или распаковки не может выполнить это преобразование напрямую, приложение может выполнить это действие в два этапа.</span><span class="sxs-lookup"><span data-stu-id="756da-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="756da-112">Обычно это означает преобразование между двумя форматами PCM, а затем еще одно преобразование в окончательный тип формата.</span><span class="sxs-lookup"><span data-stu-id="756da-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="756da-113">Для преобразования в двух шагах используйте функцию [**акмформатсугжест**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) , чтобы найти формат PCM, соответствующий формату ADPCM.</span><span class="sxs-lookup"><span data-stu-id="756da-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="756da-114">Затем используйте два потока преобразования для выполнения преобразования.</span><span class="sxs-lookup"><span data-stu-id="756da-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="756da-115">Например, выполните одно преобразование из 16-разрядного, 44-кГц стерео PCM в 16-разрядный, 11-кГц моно, а затем преобразуйте с 16-разрядного на час моно на 11-кГц моно ADPCM.</span><span class="sxs-lookup"><span data-stu-id="756da-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="756da-116">Многошаговое преобразование также происходит, если исходный или конечный формат не является PCM.</span><span class="sxs-lookup"><span data-stu-id="756da-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="756da-117">Если исходный формат не является PCM, перед преобразованием его необходимо изменить на формат PCM.</span><span class="sxs-lookup"><span data-stu-id="756da-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="756da-118">Если формат назначения не является PCM, источник должен быть преобразован в промежуточный формат PCM, а затем преобразован в окончательный формат назначения.</span><span class="sxs-lookup"><span data-stu-id="756da-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="756da-119">Наиболее простые преобразования происходят, когда форматы источника и назначения являются форматами PCM.</span><span class="sxs-lookup"><span data-stu-id="756da-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="756da-120">Если исходный или конечный формат не является PCM, для преобразования может потребоваться дополнительный шаг.</span><span class="sxs-lookup"><span data-stu-id="756da-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="756da-121">Если форматы источника и назначения не являются PCM, то преобразование обычно требует более одного шага, и в некоторых случаях преобразование может быть невозможным.</span><span class="sxs-lookup"><span data-stu-id="756da-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




