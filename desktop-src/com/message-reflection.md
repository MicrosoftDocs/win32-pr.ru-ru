---
title: Отражение сообщений
description: Отражение сообщений
ms.assetid: 26a124d7-6499-4e8f-9001-d2782c1cc290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96cb563597e5aa92440e1b1434420e983268d9b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067295"
---
# <a name="message-reflection"></a><span data-ttu-id="c089b-103">Отражение сообщений</span><span class="sxs-lookup"><span data-stu-id="c089b-103">Message Reflection</span></span>

<span data-ttu-id="c089b-104">Настоятельно рекомендуется, чтобы контейнер элементов управления ActiveX поддерживал отражение сообщений.</span><span class="sxs-lookup"><span data-stu-id="c089b-104">It is strongly recommended that an ActiveX control container supports message reflection.</span></span> <span data-ttu-id="c089b-105">Это приведет к более эффективной работе с подклассами элементов управления.</span><span class="sxs-lookup"><span data-stu-id="c089b-105">This will result in more efficient operation for subclassed controls.</span></span> <span data-ttu-id="c089b-106">Если поддерживается отражение сообщений, свойство окружения Мессажерефлект должно поддерживаться и иметь значение **true**.</span><span class="sxs-lookup"><span data-stu-id="c089b-106">If message reflection is supported, the MessageReflect ambient property must be supported and have a value of **TRUE**.</span></span> <span data-ttu-id="c089b-107">Если контейнер не реализует отражение сообщений, то компонент OLE CDK создает два окна для каждого элемента управления с подклассами, чтобы обеспечить отражение сообщений от имени контейнера элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c089b-107">If a container does not implement message reflection, then the OLE CDK creates two windows for every subclassed control, to provide message reflection on behalf on the control container.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c089b-108">См. также</span><span class="sxs-lookup"><span data-stu-id="c089b-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c089b-109">Контейнеры</span><span class="sxs-lookup"><span data-stu-id="c089b-109">Containers</span></span>](containers.md)
</dt> </dl>

 

 




