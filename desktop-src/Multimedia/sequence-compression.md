---
title: Сжатие последовательностей
description: Сжатие последовательностей
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- Диспетчер сжатия видео (ВКМ), сжатие последовательностей
- ВКМ (диспетчер сжатия видео), сжатие последовательностей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986424"
---
# <a name="sequence-compression"></a><span data-ttu-id="cc1fe-105">Сжатие последовательностей</span><span class="sxs-lookup"><span data-stu-id="cc1fe-105">Sequence Compression</span></span>

<span data-ttu-id="cc1fe-106">Приложение может использовать функции [**иксеккомпрессфраме**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**иксеккомпрессфраместарт**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)и [**иксеккомпрессфраминд**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) для сжатия последовательности кадров.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-106">Your application can use the [**ICSeqCompressFrame**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe), [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart), and [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) functions to compress a sequence of frames.</span></span> <span data-ttu-id="cc1fe-107">Эти функции используют данные, хранящиеся в структуре [**компварс**](/windows/desktop/api/Vfw/ns-vfw-compvars) .</span><span class="sxs-lookup"><span data-stu-id="cc1fe-107">These functions use the data stored in the [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) structure.</span></span> <span data-ttu-id="cc1fe-108">Приложения используют функцию [**иккомпрессорчусе**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) , чтобы позволить пользователю выбрать программу сжатия, открыть ее и задать параметры сжатия в структуре **компварс** . Однако приложения могут задавать параметры в структуре вручную.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-108">Applications use the [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) function to allow the user to select a compressor, open it, and set the compression parameters in the **COMPVARS** structure; however, applications can set the parameters in the structure manually.</span></span>

<span data-ttu-id="cc1fe-109">Прежде чем приложение сможет начать сжатие последовательности кадров, оно должно использовать **иксеккомпрессфраместарт** для выделения необходимых ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-109">Before an application can begin compressing a sequence of frames, it must use **ICSeqCompressFrameStart** to allocate the necessary resources.</span></span> <span data-ttu-id="cc1fe-110">После выделения ресурсов приложение может использовать **иксеккомпрессфраме** для сжатия каждого кадра по отдельности.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-110">After the resources are allocated, the application can use **ICSeqCompressFrame** to compress each frame individually.</span></span> <span data-ttu-id="cc1fe-111">Частота кадров и частота ключевых кадров, используемых при сжатии последовательности, задаются в элементах структуры **компварс** .</span><span class="sxs-lookup"><span data-stu-id="cc1fe-111">The frame rate and key-frame frequency used in compressing the sequence are specified in members of the **COMPVARS** structure.</span></span> <span data-ttu-id="cc1fe-112">Возвращаемое значение для **иксеккомпрессфраме** указывает на сжатые данные.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-112">The return value for **ICSeqCompressFrame** points to the compressed data.</span></span>

<span data-ttu-id="cc1fe-113">Когда приложение завершает сжатие последовательности, оно может использовать **иксеккомпрессфраминд** для освобождения системных ресурсов, выделенных для **иксеккомпрессфраместарт**.</span><span class="sxs-lookup"><span data-stu-id="cc1fe-113">When an application finishes compressing a sequence, it can use **ICSeqCompressFrameEnd** to free system resources allocated for **ICSeqCompressFrameStart**.</span></span> <span data-ttu-id="cc1fe-114">Чтобы освободить ресурсы, выделенные для структуры **компварс** , приложение может использовать функцию [**иккомпрессорфри**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) .</span><span class="sxs-lookup"><span data-stu-id="cc1fe-114">To free the resources allocated for the **COMPVARS** structure, the application can use the [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) function.</span></span>

 

 




