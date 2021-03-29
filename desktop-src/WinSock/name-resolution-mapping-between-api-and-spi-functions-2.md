---
description: При установке классов служб, регистрации экземпляров службы и основных операций запросов все они сопоставляются непосредственно из API с SPI.
ms.assetid: 2ae937f6-e0a6-4a02-9838-0a42575bae66
title: Сопоставление разрешения имен между API и функциями SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a031ea8af72bb2733fc647c817a850ab7f311b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897325"
---
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a>Сопоставление разрешения имен между API и функциями SPI

При установке классов служб, регистрации экземпляров службы и основных операций запросов все они сопоставляются непосредственно из API с SPI. Функция [**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) не имеет соответствующей функции в SPI, так как эта функция реализована в Ws2 \_32.dll путем совершения вызова [**нспжетсервицеклассинфо**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).

Вспомогательные функции [**всааддресстостринг**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) и [**всастрингтоаддресс**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) сопоставляются с соответствующими функциями в транспортном интерфейсе API, так как только поставщик транспорта обязательно должен уметь выполнять перевод в структуре [**SOCKADDR**](sockaddr-2.md) .

 

 



