---
description: Следующие определения предоставляют набор потоков состояний, которые могут быть полезны для производного класса, хотя их использование не является обязательным. Производные классы могут легко расширять набор доступных состояний, просто определяя дополнительные значения.
ms.assetid: 2c719828-904f-4469-ab3b-a331f009b9c3
title: Определения типов Кмспстреам
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5395227b2c95bddb6b4b7ef7df391b610bf20bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684320"
---
# <a name="cmspstream-type-definitions"></a><span data-ttu-id="acd03-104">Определения типов Кмспстреам</span><span class="sxs-lookup"><span data-stu-id="acd03-104">CMSPStream Type Definitions</span></span>

<span data-ttu-id="acd03-105">Следующие определения предоставляют набор потоков состояний, которые могут быть полезны для производного класса, хотя их использование не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="acd03-105">The following definitions provide a set of stream states that may be useful to the derived class, although their use is not required.</span></span> <span data-ttu-id="acd03-106">Производные классы могут легко расширять набор доступных состояний, просто определяя дополнительные значения.</span><span class="sxs-lookup"><span data-stu-id="acd03-106">Derived classes can conveniently extend the set of available states simply by defining additional values.</span></span>

``` syntax
#define STRM_INITIAL            0x00000000
#define STRM_TERMINALSELECTED   0x00000001
#define STRM_CONFIGURED         0x00000002
#define STRM_RUNNING            0x00000004
#define STRM_PAUSED             0x00000008
#define STRM_STOPPED            0x00000010
```

## <a name="related-topics"></a><span data-ttu-id="acd03-107">См. также</span><span class="sxs-lookup"><span data-stu-id="acd03-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acd03-108">**кмспстреам**</span><span class="sxs-lookup"><span data-stu-id="acd03-108">**CMSPStream**</span></span>](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



