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
# <a name="name-resolution-mapping-between-api-and-spi-functions"></a><span data-ttu-id="2caab-103">Сопоставление разрешения имен между API и функциями SPI</span><span class="sxs-lookup"><span data-stu-id="2caab-103">Name Resolution Mapping Between API and SPI Functions</span></span>

<span data-ttu-id="2caab-104">При установке классов служб, регистрации экземпляров службы и основных операций запросов все они сопоставляются непосредственно из API с SPI.</span><span class="sxs-lookup"><span data-stu-id="2caab-104">The installation of service classes, registration of service instances and basic query operations all map fairly directly from the API to the SPI.</span></span> <span data-ttu-id="2caab-105">Функция [**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) не имеет соответствующей функции в SPI, так как эта функция реализована в Ws2 \_32.dll путем совершения вызова [**нспжетсервицеклассинфо**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span><span class="sxs-lookup"><span data-stu-id="2caab-105">The [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) function does not have a corresponding function in the SPI, as this function is implemented in Ws2\_32.dll by making a call to [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo).</span></span>

<span data-ttu-id="2caab-106">Вспомогательные функции [**всааддресстостринг**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) и [**всастрингтоаддресс**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) сопоставляются с соответствующими функциями в транспортном интерфейсе API, так как только поставщик транспорта обязательно должен уметь выполнять перевод в структуре [**SOCKADDR**](sockaddr-2.md) .</span><span class="sxs-lookup"><span data-stu-id="2caab-106">The helper functions [**WSAAddressToString**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa) and [**WSAStringToAddress**](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa) are mapped to the corresponding functions in the transport API, as only a transport provider will necessarily know how to perform the translation on a [**sockaddr**](sockaddr-2.md) structure.</span></span>

 

 



