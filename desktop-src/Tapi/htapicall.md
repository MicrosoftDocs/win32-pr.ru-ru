---
description: Тип данных ХТАПИКАЛЛ представляет непрозрачный маркер TAPI для структуры данных вызова.
ms.assetid: a2a17b03-5779-411e-8959-6e2de5e53c5a
title: хтапикалл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abd90dc8453be5f5bec18e92b384b7ace830d14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344282"
---
# <a name="htapicall"></a><span data-ttu-id="2f997-103">хтапикалл</span><span class="sxs-lookup"><span data-stu-id="2f997-103">HTAPICALL</span></span>

<span data-ttu-id="2f997-104">Тип данных **хтапикалл** представляет непрозрачный маркер TAPI для структуры данных вызова.</span><span class="sxs-lookup"><span data-stu-id="2f997-104">The **HTAPICALL** datatype represents the TAPI opaque handle for a call data structure.</span></span> <span data-ttu-id="2f997-105">TAPI должен разрешить значение этого типа в ссылку на соответствующий экземпляр структуры данных.</span><span class="sxs-lookup"><span data-stu-id="2f997-105">TAPI must resolve a value of this type into a reference to the appropriate data structure instance.</span></span> <span data-ttu-id="2f997-106">Поставщик услуг не должен пытаться ссылаться на него так, как если бы он был указателем, делать предположения о его значениях или интерпретировать его представление любым способом, отличным от передачи его значения в TAPI в нужное время.</span><span class="sxs-lookup"><span data-stu-id="2f997-106">The service provider must not attempt to reference through this as if it were a pointer, make assumptions about its values, or interpret its representation in any way other than passing its value to TAPI at appropriate times.</span></span>

 

 



