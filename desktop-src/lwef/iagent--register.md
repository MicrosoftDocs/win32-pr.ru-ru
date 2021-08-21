---
title: Иажент регистр
description: Иажент регистр
ms.assetid: 3592e8ba-979e-4914-8197-17e645806f97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00f3400e6f29e62b3d8c194186f52591a0f7bb039a858c3d450e8e8332df4313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962674"
---
# <a name="iagentregister"></a>Иажент:: Register

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

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


 

 




