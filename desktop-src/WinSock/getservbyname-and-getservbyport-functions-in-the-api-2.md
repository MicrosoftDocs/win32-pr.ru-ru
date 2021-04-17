---
description: Функции жетсервбинаме и жетсервбипорт используют функцию Всалукупсервицебегин для запроса СВЦИД \_ inet \_ сервицебинаме в качестве GUID класса службы.
ms.assetid: 6d4eb1d4-1498-4367-886b-6b08e87bc4a0
title: Функции жетсервбинаме и жетсервбипорт в API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0028b9ed090463234d01e2b13191ff2328baf2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711031"
---
# <a name="getservbyname-and-getservbyport-functions-in-the-api"></a><span data-ttu-id="95625-103">Функции жетсервбинаме и жетсервбипорт в API</span><span class="sxs-lookup"><span data-stu-id="95625-103">getservbyname and getservbyport Functions in the API</span></span>

<span data-ttu-id="95625-104">Функции [**жетсервбинаме**](/windows/desktop/api/winsock/nf-winsock-getservbyname) и [**Жетсервбипорт**](/windows/desktop/api/winsock/nf-winsock-getservbyport) используют функцию [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) для запроса свЦид \_ inet \_ сервицебинаме в качестве GUID класса службы.</span><span class="sxs-lookup"><span data-stu-id="95625-104">The [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions use the [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) function to query SVCID\_INET\_SERVICEBYNAME as the service class GUID.</span></span> <span data-ttu-id="95625-105">Элемент *лпсзсервицеинстанценаме* в структуре [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , переданный функции **всалукупсервицебегин** , ссылается на строку, указывающую имя службы или порт службы, а также (необязательно) протокол службы.</span><span class="sxs-lookup"><span data-stu-id="95625-105">The *lpszServiceInstanceName* member in the [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure passed to the **WSALookupServiceBegin** function references a string to indicate the service name or service port, and (optionally) the service protocol.</span></span> <span data-ttu-id="95625-106">Форматирование строки проиллюстрировано как FTP или TCP или 21/TCP или просто FTP.</span><span class="sxs-lookup"><span data-stu-id="95625-106">The formatting of the string is illustrated as FTP or TCP or 21/TCP or just FTP.</span></span> <span data-ttu-id="95625-107">Строка не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="95625-107">The string is not case sensitive.</span></span> <span data-ttu-id="95625-108">Знак косой черты, если он есть, отделяет идентификатор протокола от предыдущей части строки.</span><span class="sxs-lookup"><span data-stu-id="95625-108">The slash mark, if present, separates the protocol identifier from the preceding part of the string.</span></span> <span data-ttu-id="95625-109">В \_32.dll Ws2 будет указан \_ BLOB-объект Луп Return \_ , а поставщик пространства имен поместит структуру [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) в большой двоичный объект (с использованием смещений вместо указателей, как описано выше).</span><span class="sxs-lookup"><span data-stu-id="95625-109">The Ws2\_32.dll will specify LUP\_RETURN\_BLOB and the namespace provider will place a [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in the blob (using offsets instead of pointers as described above).</span></span> <span data-ttu-id="95625-110">Поставщики пространств имен также должны учитывать эти другие ЛУПные \_ \_ \* флаги.</span><span class="sxs-lookup"><span data-stu-id="95625-110">Namespace providers should honor these other LUP\_RETURN\_\* flags as well.</span></span>

| <span data-ttu-id="95625-111">Flag</span><span class="sxs-lookup"><span data-stu-id="95625-111">Flag</span></span>              | <span data-ttu-id="95625-112">Описание</span><span class="sxs-lookup"><span data-stu-id="95625-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95625-113">\_имя возврата \_ Луп</span><span class="sxs-lookup"><span data-stu-id="95625-113">LUP\_RETURN\_NAME</span></span> | <span data-ttu-id="95625-114">Возвращает элемент **\_ имени s** из структуры [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) в *лпсзсервицеинстанценаме*.</span><span class="sxs-lookup"><span data-stu-id="95625-114">Returns the **s\_name** member from [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure in *lpszServiceInstanceName*.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="95625-115">\_тип возвращаемого значения Луп \_</span><span class="sxs-lookup"><span data-stu-id="95625-115">LUP\_RETURN\_TYPE</span></span> | <span data-ttu-id="95625-116">Возвращает канонический идентификатор GUID в *лпсервицеклассид* . он понимает, что служба, идентифицированная как FTP или 21, может находиться на другом порте в соответствии с локально установленными соглашениями.</span><span class="sxs-lookup"><span data-stu-id="95625-116">Returns canonical GUID in *lpServiceClassId* It is understood that a service identified as FTP or 21 may be on another port according to locally established conventions.</span></span> <span data-ttu-id="95625-117">Параметр **\_ порта s** структуры [**Сервент**](/windows/desktop/api/winsock/ns-winsock-servent) должен указывать, где можно связаться со службой в локальной среде.</span><span class="sxs-lookup"><span data-stu-id="95625-117">The **s\_port** parameter of the [**SERVENT**](/windows/desktop/api/winsock/ns-winsock-servent) structure should indicate where the service can be contacted in the local environment.</span></span> <span data-ttu-id="95625-118">Канонический идентификатор GUID, возвращаемый, если \_ задан тип возвращаемого значения Луп, \_ должен быть одним из стандартных идентификаторов GUID из SVC. h, который соответствует номеру порта, указанному в структуре **Сервент** .</span><span class="sxs-lookup"><span data-stu-id="95625-118">The canonical GUID returned when LUP\_RETURN\_TYPE is set should be one of the predefined GUIDs from Svcs.h that corresponds to the port number indicated in the **SERVENT** structure.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="95625-119">См. также</span><span class="sxs-lookup"><span data-stu-id="95625-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95625-120">Совместимое разрешение имен для TCP/IP в API-интерфейсе сокетов Windows 1,1</span><span class="sxs-lookup"><span data-stu-id="95625-120">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)
</dt> <dt>

[<span data-ttu-id="95625-121">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="95625-121">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="95625-122">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="95625-122">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 



