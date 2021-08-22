---
description: начиная с поставщиков услуг телефонии Windows 2000, которые согласовывают версию 3,0 или более поздней версии, должны иметь соответствующий поставщик службы мультимедиа.
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: Взаимодействие с поставщиком службы мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3797d02c67fc86ebfb44ff9e0e7b2c85cd1604206a58f1d8f5c3ca293599e92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404824"
---
# <a name="media-service-provider-communication"></a>Взаимодействие с поставщиком службы мультимедиа

начиная с поставщиков услуг телефонии Windows 2000, которые согласовывают версию 3,0 или более поздней версии, должны иметь соответствующий поставщик службы мультимедиа. Точное деление эксплуатационных обязанностей зависит от реализации. Например, TSP может использовать соответствующий MSP для определения типа носителя во входящем сеансе. Однако TSP должен соответствовать ТСПИ, что означает получение этого определения из MSP и составление отчетов на TAPI.

ТСПИ предоставляет следующие функции и сообщения для разрешения виртуального подключения между TSP и MSP:

-   [**ТСПИ \_ линеклосемспинстанце**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**ТСПИ \_ линекреатемспинстанце**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**ТСПИ \_ линемспидентифи**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**ТСПИ \_ линерецеивемспдата**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**Строка \_ косинфо**](line-qosinfo.md)
-   [**Строка \_ сендмспдата**](line-sendmspdata.md)

 

 
