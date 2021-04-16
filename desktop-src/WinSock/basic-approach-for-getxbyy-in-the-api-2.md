---
description: Большинство функций Жетксбии преобразуются32.dll Ws2 \_ в последовательность всалукупсервицебегин, всалукупсервиценекст и всалукупсервицеенд, которая использует один из наборов специальных идентификаторов GUID в качестве класса службы.
ms.assetid: c64db095-bd7c-489a-871a-fb887624967c
title: Базовый подход для Жетксбии в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4c038c87d6eb6e7ab2a4476271662d5b9567ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541634"
---
# <a name="basic-approach-for-getxbyy-in-the-api"></a><span data-ttu-id="cd6f8-103">Базовый подход для Жетксбии в API</span><span class="sxs-lookup"><span data-stu-id="cd6f8-103">Basic Approach for GetXbyY in the API</span></span>

<span data-ttu-id="cd6f8-104">Большинство функций **жетксбии** преобразуются32.dll Ws2 \_ в последовательность [**Всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)и [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) , которая использует один из наборов специальных идентификаторов GUID в качестве класса службы.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-104">Most **getXbyY** functions are translated by the Ws2\_32.dll to a [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), and [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) sequence that uses one of a set of special GUIDs as the service class.</span></span> <span data-ttu-id="cd6f8-105">Эти идентификаторы GUID указывают тип **жетксбии** операции, для которой выполняется эмуляция.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-105">These GUIDs identify the type of **getXbyY** operation that is being emulated.</span></span> <span data-ttu-id="cd6f8-106">Запрос ограничен теми поставщиками службы имен, которые поддерживают AF \_ inet.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-106">The query is constrained to those name service providers that support AF\_INET.</span></span> <span data-ttu-id="cd6f8-107">Всякий раз, когда функция **жетксбии** возвращает структуру [**хостент**](/windows/desktop/api/winsock/ns-winsock-hostent) или [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) , Ws2 \_32.dll указывает \_ флаг Луп Return \_ BLOB в **всалукупсервицебегин** , чтобы требуемые сведения возвращал поставщик службы имен.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-107">Whenever a **getXbyY** function returns a [**HOSTENT**](/windows/desktop/api/winsock/ns-winsock-hostent) or [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure, the Ws2\_32.dll specifies the LUP\_RETURN\_BLOB flag in **WSALookupServiceBegin** so that the desired information is returned by the name service provider.</span></span> <span data-ttu-id="cd6f8-108">Эти структуры необходимо немного изменить, чтобы содержащиеся в них указатели в должны быть заменены смещениями относительно начала данных большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-108">These structures must be modified slightly in that the pointers contained within must be replaced with offsets that are relative to the start of the blob's data.</span></span> <span data-ttu-id="cd6f8-109">Все значения, на которые ссылаются эти параметры-указатели, должны быть полностью включены в большой двоичный объект, а все строки — ASCII.</span><span class="sxs-lookup"><span data-stu-id="cd6f8-109">All values referenced by these pointer parameters must, of course, be completely contained within the blob, and all strings are ASCII.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd6f8-110">См. также</span><span class="sxs-lookup"><span data-stu-id="cd6f8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd6f8-111">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="cd6f8-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="cd6f8-112">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="cd6f8-112">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="cd6f8-113">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="cd6f8-113">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



