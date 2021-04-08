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
ms.openlocfilehash: 805303a972b4a8140a9e632857287aeebca9b32f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887496"
---
# <a name="query-interfaces"></a>Интерфейсы запросов

Для выполнения поиска по каталогу можно использовать три типа интерфейсов ADSI. Среда приложения и другие требования могут указывать, какой интерфейс используется.

-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch). **IDirectorySearch** — это базовый COM-интерфейс, доступный только программистам C/C++. Дополнительные сведения см. [в разделе Поиск с помощью интерфейса IDirectorySearch](searching-with-idirectorysearch.md).
-   Нудить. Интерфейсы объектов данных ActiveX (ADO) — это интерфейсы автоматизации, использующие OLE DB. Используйте ADO для запросов в приложениях, которые используют автоматизацию. К ним относятся Visual Basic приложения, Active Server страницы и т. д. Дополнительные сведения см. [в разделе Поиск с помощью объекты данных ActiveX](searching-with-activex-data-objects-ado.md).
-   OLE DB. OLE DB — это набор интерфейсов C/C++, используемых для запроса баз данных. Благодаря поддержке этих интерфейсов поставщики ADSI могут реализовывать дополнительные OLE DB функции, такие как распределенные запросы с другими поставщиками OLE DB. Дополнительные сведения см. [в разделе Поиск с помощью OLE DB](searching-with-ole-db.md).

 

 




