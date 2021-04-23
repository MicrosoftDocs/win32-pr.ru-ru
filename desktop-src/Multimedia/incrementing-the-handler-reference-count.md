---
title: Увеличение счетчика ссылок на обработчик
description: Увеличение счетчика ссылок на обработчик
ms.assetid: 9e71ce1f-5805-4240-9dcc-7e71fbabfe7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a990f2570fca0057156a39a955930cca2d71858
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068462"
---
# <a name="incrementing-the-handler-reference-count"></a><span data-ttu-id="706dc-103">Увеличение счетчика ссылок на обработчик</span><span class="sxs-lookup"><span data-stu-id="706dc-103">Incrementing the Handler Reference Count</span></span>

<span data-ttu-id="706dc-104">Метод **AddRef** увеличивает число ссылок обработчика потока или дескриптора файла.</span><span class="sxs-lookup"><span data-stu-id="706dc-104">The **AddRef** method increments the stream-hander or file-handler reference count.</span></span>


```C++
STDMETHODIMP_(ULONG) CAVIFileCF::AddRef() 
{ 
    return ++m_refs; 
} 

```



 

 




