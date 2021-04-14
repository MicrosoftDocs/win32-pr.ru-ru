---
title: Сеансы изменения
description: Когда служба текстового ввода должна получить, изменить или задать текст в контексте, она должна запросить сеанс изменения.
ms.assetid: e4115227-1036-4892-986d-dc4cef5b178e
keywords:
- Платформа текстовых служб (TSF), изменение сеанса
- TSF (платформа текстовых служб), изменение сеанса
- текстовые службы, сеанс изменения
- сеанс изменения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81897c3c63539626776b693a22be9096f973d02e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532435"
---
# <a name="edit-sessions"></a><span data-ttu-id="c99ec-107">Сеансы изменения</span><span class="sxs-lookup"><span data-stu-id="c99ec-107">Edit Sessions</span></span>

<span data-ttu-id="c99ec-108">Когда служба текстового ввода должна получить, изменить или задать текст в контексте, она должна запросить *сеанс изменения*.</span><span class="sxs-lookup"><span data-stu-id="c99ec-108">When a text service must obtain, modify, or set text in a context, it must request an *edit session*.</span></span> <span data-ttu-id="c99ec-109">Когда запрос на изменение запрашивается, диспетчер TSF выполняет согласование с владельцем целевого контекста для блокировки документа запрошенного типа.</span><span class="sxs-lookup"><span data-stu-id="c99ec-109">When an edit session is requested, the TSF manager negotiates with the owner of the target context for a document lock of the requested type.</span></span> <span data-ttu-id="c99ec-110">При предоставлении блокировки документа Диспетчер TSF позволяет текстовой службе читать и записывать текст в контекст.</span><span class="sxs-lookup"><span data-stu-id="c99ec-110">When the document lock is granted, the TSF manager enables the text service to read and/or write text to or from the context.</span></span>

 

 




