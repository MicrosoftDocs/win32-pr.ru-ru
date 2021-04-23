---
description: нспжетсервицеклассинфо
ms.assetid: 6fbe9c0c-ac1f-4f2b-a542-eae2195b1335
title: Вспомогательные функции в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e687529bf1ede1598225708cf288e49bb7e9b5c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701519"
---
# <a name="helper-functions-in-the-spi"></a><span data-ttu-id="7dcaf-103">Вспомогательные функции в SPI</span><span class="sxs-lookup"><span data-stu-id="7dcaf-103">Helper Functions in the SPI</span></span>

-   [<span data-ttu-id="7dcaf-104">**нспжетсервицеклассинфо**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-104">**NSPGetServiceClassInfo**</span></span>](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo)

<span data-ttu-id="7dcaf-105">Функция [**нспжетсервицеклассинфо**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) извлекает сведения о схеме класса службы, которые были сохранены поставщиком пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-105">The [**NSPGetServiceClassInfo**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpnspgetserviceclassinfo) function retrieves service class schema information that has been retained by a namespace provider.</span></span> <span data-ttu-id="7dcaf-106">Он также используется библиотекой DLL Windows Sockets 2 в своей реализации [**всажетсервицекласснамебиклассид**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span><span class="sxs-lookup"><span data-stu-id="7dcaf-106">It is also used by the Windows Sockets 2 DLL in its implementation of [**WSAGetServiceClassNameByClassId**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida).</span></span>

<span data-ttu-id="7dcaf-107">Следующие макросы определены в файле заголовка *свкгуид. h* и могут помочь в сопоставлении между известными классами служб и этими пространствами имен.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-107">The following macros defined in the *Svcguid.h* header file and can aid in mapping between well known service classes and these namespaces.</span></span>

| <span data-ttu-id="7dcaf-108">Имени макроса</span><span class="sxs-lookup"><span data-stu-id="7dcaf-108">Macro name</span></span>                                                                              | <span data-ttu-id="7dcaf-109">Описание</span><span class="sxs-lookup"><span data-stu-id="7dcaf-109">Description</span></span>                                                                                                                                        |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcaf-110">**СВЦИД \_ TCP (порт)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-110">**SVCID\_TCP(Port)**</span></span><br/> <span data-ttu-id="7dcaf-111">**СВЦИД \_ UDP (порт)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-111">**SVCID\_UDP(Port)**</span></span><br/>                         | <span data-ttu-id="7dcaf-112">При наличии порта TCP или UDP для протокола Интернета возвращает идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-112">Given a TCP or UDP port for the Internet protocol, returns the GUID.</span></span>                                                                               |
| <span data-ttu-id="7dcaf-113">**\_свЦид \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-113">**IS\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="7dcaf-114">**ЯВЛЯЕТСЯ \_ свЦид \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-114">**IS\_SVCID\_UDP(GUID)**</span></span><br/>                 | <span data-ttu-id="7dcaf-115">Возвращает **значение true** , если идентификатор GUID для TCP или UDP находится в пределах допустимого диапазона.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-115">Returns **TRUE** if the GUID for TCP or UDP is within the allowable range.</span></span>                                                                         |
| <span data-ttu-id="7dcaf-116">**Порт \_ из \_ свЦид \_ TCP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-116">**PORT\_FROM\_SVCID\_TCP(GUID)**</span></span><br/> <span data-ttu-id="7dcaf-117">**Порт \_ из \_ свЦид \_ UDP (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-117">**PORT\_FROM\_SVCID\_UDP(GUID)**</span></span><br/> | <span data-ttu-id="7dcaf-118">Возвращает порт TCP или UDP, связанный с идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-118">Returns the TCP or UDP port associated with the GUID.</span></span>                                                                                              |
| <span data-ttu-id="7dcaf-119">**СВЦИД \_ NetWare (SAPI)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-119">**SVCID\_NETWARE(SAPID)**</span></span><br/>                                                    | <span data-ttu-id="7dcaf-120">Если указан идентификатор протокола SAP, возвращает идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-120">Given the Service Advertising Protocol (SAP) identifier, returns the GUID.</span></span> <span data-ttu-id="7dcaf-121">Этот макрос используется с пространством имен SAP в среде NetWare.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-121">This macro is used with the SAP namespace within a NetWare environment.</span></span> |
| <span data-ttu-id="7dcaf-122">**SAPI \_ из \_ свЦид \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-122">**SAPID\_FROM\_SVCID\_NETWARE(GUID)**</span></span><br/>                                        | <span data-ttu-id="7dcaf-123">Возвращает идентификатор NetWare SAP, связанный с идентификатором GUID.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-123">Returns the NetWare SAP identifier associated with the GUID.</span></span> <span data-ttu-id="7dcaf-124">Этот макрос используется с пространством имен SAP в среде NetWare.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-124">This macro is used with the SAP namespace within a NetWare environment.</span></span>               |
| <span data-ttu-id="7dcaf-125">**ЯВЛЯЕТСЯ \_ свЦид \_ NetWare (GUID)**</span><span class="sxs-lookup"><span data-stu-id="7dcaf-125">**IS\_SVCID\_NETWARE(GUID)**</span></span><br/>                                                 | <span data-ttu-id="7dcaf-126">Возвращает **значение true** , если идентификатор GUID для NetWare находится в допустимом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-126">Returns **TRUE** if the GUID for NetWare is within the allowable range.</span></span> <span data-ttu-id="7dcaf-127">Этот макрос используется с пространством имен SAP в среде NetWare.</span><span class="sxs-lookup"><span data-stu-id="7dcaf-127">This macro is used with the SAP namespace within a NetWare environment.</span></span>    |



 

> [!Note]  
> <span data-ttu-id="7dcaf-128">Заголовочный файл *свкгуид. h* не включается автоматически в заголовочный файл *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="7dcaf-128">The *Svcguid.h* header file is not automatically included by the *Winsock2.h* header file.</span></span>

 

 

 




