---
description: При установке классов служб, регистрации экземпляров службы и основных операций запросов все они сопоставляются непосредственно из API с SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Сопоставление разрешения имен между API и функциями SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad02896ea15fb1b7c7e2aa2e01d9ec0727492da43d0446819dd1f2e04ad591d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733628"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Сопоставление разрешения имен между API и функциями SPI

При установке классов служб, регистрации экземпляров службы и основных операций запросов все они сопоставляются непосредственно из API с SPI. Функция [**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) не имеет соответствующей функции в SPI, так как эта функция реализована в Ws2 \_32.dll путем совершения вызова [**нспжетсервицеклассинфо**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Вспомогательные функции [**всааддресстостринг**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) и [**всастрингтоаддресс**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) сопоставляются с соответствующими функциями в транспортном интерфейсе API, так как только поставщик транспорта обязательно должен уметь выполнять перевод в структуре [**SOCKADDR**](sockaddr-2.md) .

 

 



