---
description: 'Запросы данных — это инструкции WQL, которые запрашивают экземпляры классов. Чтобы выдать запрос данных, приложения вызывают метод IWbemServices:: ExecQuery или IWbemServices:: Ексеккуерясинк.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Запрос данных экземпляра класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316291"
---
# <a name="requesting-class-instance-data"></a>Запрос данных экземпляра класса

Запросы данных — это инструкции WQL, которые запрашивают экземпляры классов. Чтобы выдать запрос данных, приложения вызывают метод [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) или [**IWbemServices:: ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .

Для выполнения запросов данных используются следующие инструкции:

-   [SELECT](select-statement-for-data-queries.md)
-   [СОЕДИНИТЕЛи](associators-of-statement.md)
-   [ССЫЛКИ НА](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

инструкция wql SELECT является стандартной инструкцией язык SQL (SQL) для получения сведений с помощью нескольких ограничений и расширений, характерных для WQL. хотя SQL инструкция select обычно используется в среде базы данных для извлечения определенных столбцов из таблиц, в WMI используется инструкция WQL SELECT для получения экземпляров одного класса. WQL не поддерживает запросы в нескольких классах.

СОЕДИНИТЕЛи и ссылки на инструкции относятся только к WQL и не являются частью стандартных SQL. СОЕДИНИТЕЛи оператора получают все экземпляры классов, связанные с определенным экземпляром исходного класса, а ссылки на получение всех экземпляров, ссылающихся на конкретный экземпляр источника. Ассоциации представлены экземплярами [класса Association](declaring-an-association-class.md).

 

 



