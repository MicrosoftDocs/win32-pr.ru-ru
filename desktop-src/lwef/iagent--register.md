---
title: Иажент регистр
description: Иажент регистр
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dd611219fa994f4fe61f7f3e08facf02c9fb73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888476"
---
# <a name="iagentregister"></a><span data-ttu-id="71b7e-103">Иажент:: Register</span><span class="sxs-lookup"><span data-stu-id="71b7e-103">IAgent::Register</span></span>

<span data-ttu-id="71b7e-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="71b7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

<span data-ttu-id="71b7e-105">Регистрирует приемник уведомлений для клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="71b7e-105">Registers a notification sink for the client application.</span></span>

-   <span data-ttu-id="71b7e-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="71b7e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="71b7e-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span><span class="sxs-lookup"><span data-stu-id="71b7e-107"><span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*</span></span>
</dt> <dd>

<span data-ttu-id="71b7e-108">Адрес [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) для интерфейса приемника уведомлений.</span><span class="sxs-lookup"><span data-stu-id="71b7e-108">Address of [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) for your notification sink interface.</span></span>

</dd> <dt>

<span data-ttu-id="71b7e-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*пдвсинкид*</span><span class="sxs-lookup"><span data-stu-id="71b7e-109"><span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*pdwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="71b7e-110">Адрес идентификатора приемника уведомлений (используется для отмены регистрации приемника уведомлений).</span><span class="sxs-lookup"><span data-stu-id="71b7e-110">Address of notification sink ID (used to unregister the notification sink).</span></span>

</dd> </dl>

<span data-ttu-id="71b7e-111">Чтобы получать события с сервера Microsoft Agent, необходимо зарегистрировать приемник уведомлений (также называемый приемником уведомлений или приемником событий).</span><span class="sxs-lookup"><span data-stu-id="71b7e-111">You need to register your notification sink (also known as a notify sink or event sink) to receive events from the Microsoft Agent server.</span></span>

## <a name="see-also"></a><span data-ttu-id="71b7e-112">См. также:</span><span class="sxs-lookup"><span data-stu-id="71b7e-112">See Also</span></span>

[<span data-ttu-id="71b7e-113">**Иажент:: Отмена регистрации**</span><span class="sxs-lookup"><span data-stu-id="71b7e-113">**IAgent::Unregister**</span></span>](iagent--unregister.md)


 

 




