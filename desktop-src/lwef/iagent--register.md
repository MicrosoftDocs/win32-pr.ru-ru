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
# <a name="iagentregister"></a>Иажент:: Register

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

``` syntax
HRESULT Register(
   IUnknown * punkNotifySink  // IUnknown address for client notification sink
   long * pdwSinkID           // address of the notification sink ID
);
```

Регистрирует приемник уведомлений для клиентского приложения.

-   Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.

<dl> <dt>

<span id="IUnknown"></span><span id="iunknown"></span><span id="IUNKNOWN"></span>*IUnknown*
</dt> <dd>

Адрес [**IUnknown**](https://www.bing.com/search?q=**IUnknown**) для интерфейса приемника уведомлений.

</dd> <dt>

<span id="pdwSinkID"></span><span id="pdwsinkid"></span><span id="PDWSINKID"></span>*пдвсинкид*
</dt> <dd>

Адрес идентификатора приемника уведомлений (используется для отмены регистрации приемника уведомлений).

</dd> </dl>

Чтобы получать события с сервера Microsoft Agent, необходимо зарегистрировать приемник уведомлений (также называемый приемником уведомлений или приемником событий).

## <a name="see-also"></a>См. также:

[**Иажент:: Отмена регистрации**](iagent--unregister.md)


 

 




