---
title: Создание нестандартного формата
description: Создание нестандартного формата
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Диспетчер аудиосжатия (ACM), нестандартные форматы
- ACM (диспетчер аудиосжатия), нестандартные форматы
- Примеры ACM, нестандартные форматы
- Функция Акмформатсугжест
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888284"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="32af6-107">Создание нестандартного формата</span><span class="sxs-lookup"><span data-stu-id="32af6-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="32af6-108">Иногда приложению требуется нестандартный формат.</span><span class="sxs-lookup"><span data-stu-id="32af6-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="32af6-109">Например, приложению может потребоваться файл формата ADPCM размером 16 кГц.</span><span class="sxs-lookup"><span data-stu-id="32af6-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="32af6-110">Поскольку 16 кГц является нестандартным, функции перечисления не будут создавать этот формат.</span><span class="sxs-lookup"><span data-stu-id="32af6-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="32af6-111">На самом деле, при написании пользовательского кода алгоритмов формата в приложении нет надежного способа создания нестандартного формата.</span><span class="sxs-lookup"><span data-stu-id="32af6-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="32af6-112">Однако иногда можно создать аналогичный формат, настроив допустимый формат PCM, указав все необходимые сведения, а затем используя функцию [**акмформатсугжест**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) .</span><span class="sxs-lookup"><span data-stu-id="32af6-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="32af6-113">Так как программа сжатия и декомпрессора пытается предложить формат, ближайший к желаемому формату, число каналов и частота обычно сохраняется.</span><span class="sxs-lookup"><span data-stu-id="32af6-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




