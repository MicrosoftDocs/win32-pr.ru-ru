---
title: Куча
description: Куча отслеживает группу выделений, освобожденных как единое целое.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Веб-службы кучи для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a581d4173ed16423ac55e82d3dde356bad1e310047dd44d8f92fded0c6f458e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005934"
---
# <a name="heap"></a>Куча

Куча отслеживает группу выделений, освобожденных как единое целое.

Это позволяет избежать сложных шаблонов выделения и освобождения памяти при использовании ВВСАПИ.


Существует куча, связанная с каждым сообщением. При отправке сообщения или при получении сообщения используется куча сообщения для всех выделений, связанных с конкретным сообщением. После отправки или получения сообщения куча сбрасывается (что очищает все выделения, связанные с конкретным сообщением).

Кучи также можно использовать для хранения данных сообщений отдельно от времени существования сообщения. Многие из спецификаций API, позволяющие использовать кучу для считывания данных, предоставляют явный контроль над временем существования любых считываемых данных.

При выделении из кучи гарантированно выводятся по крайней мере 8-байтная граница.

Выделение нулевого байта вернет непустой указатель.

в Windows 7, если включен параметр пажехеап, для управления памятью используется куча, возвращенная из хеапкреате. В этом случае [**всаллок**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) сопоставляется напрямую с хеапаллок, а [**Всресесеап**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) — с хеапдестрой.

В куче используется следующее перечисление:

-   [**\_ \_ идентификатор свойства WS \_ heap**](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

В куче используются следующие функции:

-   [**всаллок**](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [**вскреатехеап**](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [**всфрихеап**](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [**всжесеаппроперти**](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [**всресесеап**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

В куче используется следующий маркер:

-   [\_куча WS](ws-heap.md)

В куче используются следующие структуры:

-   [**\_Свойства КУЧИ \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [**\_свойство WS heap \_**](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




