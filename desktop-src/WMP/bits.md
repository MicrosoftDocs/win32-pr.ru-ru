---
title: BITS
description: BITS
ms.assetid: 67159ad9-e11b-4fea-bff2-468d5a7447be
keywords:
- Интернет-магазины проигрывателя Windows Media, фоновая интеллектуальная служба передачи (BITS)
- Интернет-магазины, фоновая интеллектуальная служба передачи (BITS)
- Тип 2 Интернет-магазинов, фоновая интеллектуальная служба передачи (BITS)
- Фоновая интеллектуальная служба передачи (BITS)
- БИТ (фоновая интеллектуальная служба передачи)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527edf56e7505c64657d167e0210190e00d697d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337924"
---
# <a name="bits"></a><span data-ttu-id="6be18-108">BITS</span><span class="sxs-lookup"><span data-stu-id="6be18-108">BITS</span></span>

<span data-ttu-id="6be18-109">[Фоновая интеллектуальная служба передачи](/windows/desktop/Bits/background-intelligent-transfer-service-portal) является компонентом операционной системы Windows.</span><span class="sxs-lookup"><span data-stu-id="6be18-109">The [Background Intelligent Transfer Service](/windows/desktop/Bits/background-intelligent-transfer-service-portal) is a feature of the Windows operating system.</span></span> <span data-ttu-id="6be18-110">Служба BITS передает файлы (загрузки или передачи) между клиентом и сервером и предоставляет сведения о ходе выполнения, связанные с передачей.</span><span class="sxs-lookup"><span data-stu-id="6be18-110">BITS transfers files (downloads or uploads) between a client and server, and provides progress information related to the transfers.</span></span> <span data-ttu-id="6be18-111">Если вы хотите передавать файлы с помощью кода C++, нужно использовать BITS.</span><span class="sxs-lookup"><span data-stu-id="6be18-111">If you want to transfer files using C++ code, BITS is the correct technology to use.</span></span> <span data-ttu-id="6be18-112">Если вы хотите передавать файлы с помощью кода JScript на веб-страницу Интернет-магазина, используйте вместо этого диспетчер загрузки.</span><span class="sxs-lookup"><span data-stu-id="6be18-112">If you want to transfer files using JScript code in your online store webpage, use the Download Manager instead.</span></span>

<span data-ttu-id="6be18-113">Так как диспетчер загрузки проигрывателя Windows Media использует службу BITS, можно настроить задания копирования BITS таким образом, чтобы проигрыватель Windows Media управлял заданиями.</span><span class="sxs-lookup"><span data-stu-id="6be18-113">Because the Windows Media Player Download Manager uses BITS, you can take steps to configure your BITS copy jobs in such a way that Windows Media Player manages the jobs for you.</span></span> <span data-ttu-id="6be18-114">Для этого необходимо следовать правилам, описанным в разделе [соглашения о задании Windows Media Player BITS](windows-media-player-bits-job-convention.md) при добавлении заданий в очередь передачи BITS.</span><span class="sxs-lookup"><span data-stu-id="6be18-114">To do this, you must follow the convention described in the [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md) section when adding your jobs to the BITS transfer queue.</span></span> <span data-ttu-id="6be18-115">В этом разделе также описывается механизм извлечения сведений о заданиях BITS с веб-страницы Интернет-магазинов.</span><span class="sxs-lookup"><span data-stu-id="6be18-115">This section also describes a mechanism for retrieving information about your BITS jobs from your online stores webpage.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6be18-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6be18-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6be18-117">**Использование диспетчера загрузки**</span><span class="sxs-lookup"><span data-stu-id="6be18-117">**Using the Download Manager**</span></span>](using-the-download-manager.md)
</dt> <dt>

[<span data-ttu-id="6be18-118">**Сведения о типе 2 Интернет-магазинов**</span><span class="sxs-lookup"><span data-stu-id="6be18-118">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> </dl>

 

 