---
description: Большинство функций Жетксбии переводятся Ws2 \_32.dll в последовательность всалукупсервицебегин, всалукупсервиценекст, всалукупсервицеенд, которая использует один из наборов специальных идентификаторов GUID в качестве класса службы.
ms.assetid: 5028df47-1689-470f-90e0-2859173a7111
title: Базовый подход для Жетксбии в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d635230bb1c1205d0f6e1aee16fe7c7ac9eab5b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897354"
---
# <a name="basic-approach-for-getxbyy-in-the-spi"></a><span data-ttu-id="3bf84-103">Базовый подход для Жетксбии в SPI</span><span class="sxs-lookup"><span data-stu-id="3bf84-103">Basic Approach for GetXbyY in the SPI</span></span>

<span data-ttu-id="3bf84-104">Большинство функций **жетксбии** переводятся Ws2 \_32.dll в последовательность [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) , которая использует один из наборов специальных идентификаторов GUID в качестве класса службы.</span><span class="sxs-lookup"><span data-stu-id="3bf84-104">Most **GetXbyY** functions are translated by Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="3bf84-105">Эти идентификаторы GUID указывают тип **жетксбии** операции, для которой выполняется эмуляция.</span><span class="sxs-lookup"><span data-stu-id="3bf84-105">These GUIDs identify the type of **GetXbyY** operation that is being emulated.</span></span> <span data-ttu-id="3bf84-106">Запрос ограничен теми NSP, которые поддерживают AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="3bf84-106">The query is constrained to those NSPs that support AF\_INET.</span></span> <span data-ttu-id="3bf84-107">Всякий раз, когда функция **жетксбии** возвращает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) или [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) , Ws2 \_32.dll задаст \_ флаг Луп Return \_ BLOB в **всалукупсервицебегин** , чтобы в NSP возвращалась нужная информация.</span><span class="sxs-lookup"><span data-stu-id="3bf84-107">Whenever a **GetXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll will specify the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information will be returned by the NSP.</span></span> <span data-ttu-id="3bf84-108">Эти структуры необходимо немного изменить, чтобы содержащиеся в них указатели в должны быть заменены смещениями относительно начала данных большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="3bf84-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="3bf84-109">Все значения, на которые ссылаются эти члены-указатели, должны быть полностью включены в большой двоичный объект, а все строки — ASCII.</span><span class="sxs-lookup"><span data-stu-id="3bf84-109">All values referenced by these pointer members must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

 

 



