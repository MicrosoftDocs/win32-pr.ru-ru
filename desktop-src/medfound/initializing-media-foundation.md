---
description: Инициализация Media Foundation
ms.assetid: e4db81d3-7a9e-47d7-8611-6dac8026259c
title: Инициализация Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb876ec3493d6c4fac1c2f6d6757ef647c511a98
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105674553"
---
# <a name="initializing-media-foundation"></a><span data-ttu-id="b1501-103">Инициализация Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1501-103">Initializing Media Foundation</span></span>

<span data-ttu-id="b1501-104">Перед использованием любых Microsoft Media Foundation объектов или интерфейсов необходимо вызвать функцию [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) .</span><span class="sxs-lookup"><span data-stu-id="b1501-104">Before using any Microsoft Media Foundation objects or interfaces, you must call the [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function.</span></span> <span data-ttu-id="b1501-105">Передайте постоянную **\_ версию MF**.</span><span class="sxs-lookup"><span data-stu-id="b1501-105">Pass in the constant **MF\_VERSION**.</span></span>


```C++
    hr = MFStartup(MF_VERSION);
```



<span data-ttu-id="b1501-106">Функция [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) инициализирует Media Foundationную платформу.</span><span class="sxs-lookup"><span data-stu-id="b1501-106">The [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) function initializes the Media Foundation platform.</span></span> <span data-ttu-id="b1501-107">Если **мфстартуп** возвращает MF \_ \_ неверную \_ начальную \_ версию, это означает, что приложение было скомпилировано с использованием версии Media Foundation заголовков, которые не соответствуют Media Foundationным DLL-библиотекам в системе.</span><span class="sxs-lookup"><span data-stu-id="b1501-107">If **MFStartup** returns MF\_E\_BAD\_STARTUP\_VERSION, it means your application was compiled using a version of the Media Foundation headers that does not match the Media Foundation DLLs on your system.</span></span>

<span data-ttu-id="b1501-108">Для каждого вызова [**мфстартуп**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)приложение должно вызывать [**мфшутдовн**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="b1501-108">For every call to [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup), your application must call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span>


```C++
MFShutdown();
```



## <a name="related-topics"></a><span data-ttu-id="b1501-109">См. также</span><span class="sxs-lookup"><span data-stu-id="b1501-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1501-110">Архитектура Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b1501-110">Media Foundation Architecture</span></span>](media-foundation-architecture.md)
</dt> <dt>

[<span data-ttu-id="b1501-111">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="b1501-111">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



