---
title: Интерфейсы запросов
description: Для выполнения поиска по каталогу можно использовать три типа интерфейсов ADSI. Среда приложения и другие требования могут указывать, какой интерфейс используется.
ms.assetid: 42843e02-b685-492e-9046-aea460e84584
ms.tgt_platform: multiple
keywords:
- Интерфейсы интерфейсов запросов ADSI
- Запросы ADSI, интерфейсы запросов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 967f111107549fd0e6352f0e93d3a747b287c040ea7d5e6cee48415aa7f7925f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637724"
---
# <a name="query-interfaces"></a>Интерфейсы запросов

Для выполнения поиска по каталогу можно использовать три типа интерфейсов ADSI. Среда приложения и другие требования могут указывать, какой интерфейс используется.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** — это базовый COM-интерфейс, доступный только программистам C/C++. Дополнительные сведения см. [в разделе Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md).
-   Нудить. интерфейсы объектов данных ActiveX (ADO) — это интерфейсы автоматизации, использующие OLE DB. Используйте ADO для запросов в приложениях, которые используют автоматизацию. к ним относятся Visual Basic приложения, Active Server страницы и т. д. дополнительные сведения см. [в разделе поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB — это набор интерфейсов C/C++, используемых для запроса баз данных. Благодаря поддержке этих интерфейсов поставщики ADSI могут реализовывать дополнительные OLE DB функции, такие как распределенные запросы с другими поставщиками OLE DB. Дополнительные сведения см. [в разделе Поиск с помощью OLE DB](searching-with-ole-db.md).

 

 




