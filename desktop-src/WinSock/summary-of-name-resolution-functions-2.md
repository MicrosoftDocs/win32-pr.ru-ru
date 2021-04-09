---
description: 'Функции разрешения имен можно сгруппировать в три категории: Установка службы, клиентские запросы и вспомогательное приложение (с макросами).'
ms.assetid: c16a7163-11f5-4ad6-9df1-9bad2a964e48
title: Общие сведения о функциях разрешения имен
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5969cb2cf145124446374dcb86eb1e0a8a837c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809700"
---
# <a name="summary-of-name-resolution-functions"></a><span data-ttu-id="d32da-103">Общие сведения о функциях разрешения имен</span><span class="sxs-lookup"><span data-stu-id="d32da-103">Summary of Name Resolution Functions</span></span>

<span data-ttu-id="d32da-104">Функции разрешения имен можно сгруппировать в три категории: Установка службы, клиентские запросы и вспомогательное приложение (с макросами).</span><span class="sxs-lookup"><span data-stu-id="d32da-104">The name resolution functions can be grouped into three categories: Service installation, client queries, and helper (with macros).</span></span> <span data-ttu-id="d32da-105">В следующих разделах определяются функции в каждой категории и кратко описывается их предполагаемое использование.</span><span class="sxs-lookup"><span data-stu-id="d32da-105">The sections that follow identify the functions in each category and briefly describe their intended use.</span></span> <span data-ttu-id="d32da-106">Также описаны основные структуры данных.</span><span class="sxs-lookup"><span data-stu-id="d32da-106">Key data structures are also described.</span></span>

## <a name="service-installation"></a><span data-ttu-id="d32da-107">Установка службы</span><span class="sxs-lookup"><span data-stu-id="d32da-107">Service Installation</span></span>

-   [<span data-ttu-id="d32da-108">**всаинсталлсервицекласс**</span><span class="sxs-lookup"><span data-stu-id="d32da-108">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
-   [<span data-ttu-id="d32da-109">**всаремовесервицекласс**</span><span class="sxs-lookup"><span data-stu-id="d32da-109">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
-   [<span data-ttu-id="d32da-110">**всасетсервице**</span><span class="sxs-lookup"><span data-stu-id="d32da-110">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)

<span data-ttu-id="d32da-111">Если требуемый класс службы еще не существует, приложение использует [**всаинсталлсервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) для установки нового класса службы, указав имя класса службы, идентификатор GUID для идентификатора класса службы и ряд структур [**всансклассинфо**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) .</span><span class="sxs-lookup"><span data-stu-id="d32da-111">When the required service class does not already exist, an application uses [**WSAInstallServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa) to install a new service class by supplying a service class name, a GUID for the service class identifier, and a series of [**WSANSCLASSINFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow) structures.</span></span> <span data-ttu-id="d32da-112">Эти структуры зависят от конкретного пространства имен и предоставляют общие значения, такие как Рекомендуемые номера TCP-портов или идентификаторы NetWare SAP.</span><span class="sxs-lookup"><span data-stu-id="d32da-112">These structures are each specific to a particular namespace, and supply common values such as recommended TCP port numbers or NetWare SAP Identifiers.</span></span> <span data-ttu-id="d32da-113">Класс службы можно удалить путем вызова [**всаремовесервицекласс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) и указания идентификатора GUID, соответствующего идентификатору класса.</span><span class="sxs-lookup"><span data-stu-id="d32da-113">A service class can be removed by calling [**WSARemoveServiceClass**](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass) and supplying the GUID corresponding to the class identifier.</span></span>

<span data-ttu-id="d32da-114">После существования класса службы определенные экземпляры службы можно установить или удалить с помощью [**всасетсервице**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span><span class="sxs-lookup"><span data-stu-id="d32da-114">Once a service class exists, specific instances of a service can be installed or removed through [**WSASetService**](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea).</span></span> <span data-ttu-id="d32da-115">Эта функция принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входного параметра вместе с кодом операции и флагами операций.</span><span class="sxs-lookup"><span data-stu-id="d32da-115">This function takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as an input parameter along with an operation code and operation flags.</span></span> <span data-ttu-id="d32da-116">Код операции указывает, выполняется ли установка или удаление службы.</span><span class="sxs-lookup"><span data-stu-id="d32da-116">The operation code indicates whether the service is being installed or removed.</span></span> <span data-ttu-id="d32da-117">Структура **всакуерисет** предоставляет все необходимые сведения о службе, включая идентификатор класса службы, имя службы (для этого экземпляра), применимый идентификатор пространства имен и сведения о протоколе, а также набор транспортных адресов, на которых служба прослушивает службу.</span><span class="sxs-lookup"><span data-stu-id="d32da-117">The **WSAQUERYSET** structure provides all of the relevant information about the service including service class identifier, service name (for this instance), applicable namespace identifier and protocol information, and a set of transport addresses at which the service listens.</span></span> <span data-ttu-id="d32da-118">Службы должны вызывать **всасетсервице** при инициализации для объявления их присутствия в динамических пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="d32da-118">Services should invoke **WSASetService** when they initialize to advertise their presence in dynamic namespaces.</span></span>

## <a name="client-query"></a><span data-ttu-id="d32da-119">Клиентский запрос</span><span class="sxs-lookup"><span data-stu-id="d32da-119">Client Query</span></span>

-   [<span data-ttu-id="d32da-120">**всаенумнамеспацепровидерс**</span><span class="sxs-lookup"><span data-stu-id="d32da-120">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
-   [<span data-ttu-id="d32da-121">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="d32da-121">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
-   [<span data-ttu-id="d32da-122">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="d32da-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
-   [<span data-ttu-id="d32da-123">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="d32da-123">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)

<span data-ttu-id="d32da-124">Функция [**всаенумнамеспацепровидерс**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) позволяет приложению определить, какие пространства имен доступны через средства разрешения имен Winsock.</span><span class="sxs-lookup"><span data-stu-id="d32da-124">The [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) function allows an application to discover which namespaces are accessible through Winsock name resolution facilities.</span></span> <span data-ttu-id="d32da-125">Он также позволяет приложению определить, поддерживается ли данное пространство имен несколькими поставщиками пространства имен, и определить идентификатор поставщика для любого конкретного поставщика пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d32da-125">It also allows an application to determine whether a given namespace is supported by more than one namespace provider, and to discover the provider identifier for any particular namespace provider.</span></span> <span data-ttu-id="d32da-126">С помощью идентификатора поставщика приложение может ограничить операцию запроса указанным поставщиком пространства имен.</span><span class="sxs-lookup"><span data-stu-id="d32da-126">Using a provider identifier, the application can restrict a query operation to a specified namespace provider.</span></span>

<span data-ttu-id="d32da-127">Пространство имен Winsock — операции запроса содержат ряд вызовов: [**всалукупсервицебегин**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), за которыми следует один или несколько вызовов [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) и заканчиваются вызовом [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="d32da-127">Winsock namespace–query operations involve a series of calls: [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), followed by one or more calls to [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) and ending with a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="d32da-128">**Всалукупсервицебегин** принимает структуру [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) в качестве входных данных для определения параметров запроса вместе с набором флагов для предоставления дополнительного контроля над поисковой операцией.</span><span class="sxs-lookup"><span data-stu-id="d32da-128">**WSALookupServiceBegin** takes a [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) structure as input to define the query parameters along with a set of flags to provide additional control over the search operation.</span></span> <span data-ttu-id="d32da-129">Он возвращает маркер запроса, который используется в последующих вызовах **всалукупсервиценекст** и **всалукупсервицеенд**.</span><span class="sxs-lookup"><span data-stu-id="d32da-129">It returns a query handle which is used in the subsequent calls to **WSALookupServiceNext** and **WSALookupServiceEnd**.</span></span>

<span data-ttu-id="d32da-130">Приложение вызывает [**всалукупсервиценекст**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) для получения результатов запроса, в котором результаты передаются в буфер [**всакуерисет**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) , предоставленный приложением.</span><span class="sxs-lookup"><span data-stu-id="d32da-130">The application invokes [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) to obtain query results, with results supplied in an application-supplied [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) buffer.</span></span> <span data-ttu-id="d32da-131">Приложение будет вызывать **всалукупсервиценекст** до тех пор, пока не будет возвращен код ошибки WSA \_ E, \_ \_ указывающий, что все результаты получены.</span><span class="sxs-lookup"><span data-stu-id="d32da-131">The application continues to call **WSALookupServiceNext** until the error code WSA\_E\_NO\_MORE is returned indicating that all results have been retrieved.</span></span> <span data-ttu-id="d32da-132">После этого поиск завершается вызовом [**всалукупсервицеенд**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span><span class="sxs-lookup"><span data-stu-id="d32da-132">The search is then terminated by a call to [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend).</span></span> <span data-ttu-id="d32da-133">Функция **всалукупсервицеенд** может также использоваться для отмены ожидающего в данный момент **всалукупсервиценекст** при вызове из другого потока.</span><span class="sxs-lookup"><span data-stu-id="d32da-133">The **WSALookupServiceEnd** function can also be used to cancel a currently pending **WSALookupServiceNext** when called from another thread.</span></span>

<span data-ttu-id="d32da-134">В Windows Sockets 2 для ВСАЕНОМОРЕ (10102) и WSA \_ E ( \_ 10110) определены конфликтующие коды ошибок \_ .</span><span class="sxs-lookup"><span data-stu-id="d32da-134">In Windows Sockets 2, conflicting error codes are defined for WSAENOMORE (10102) and WSA\_E\_NO\_MORE (10110).</span></span> <span data-ttu-id="d32da-135">Код ошибки ВСАЕНОМОРЕ будет удален в следующей версии, и только WSA E больше \_ \_ не \_ останется.</span><span class="sxs-lookup"><span data-stu-id="d32da-135">The error code WSAENOMORE will be removed in a future version and only WSA\_E\_NO\_MORE will remain.</span></span> <span data-ttu-id="d32da-136">Однако для сокетов Windows 2 приложения должны проверять как ВСАЕНОМОРЕ, так и WSA \_ E, \_ но не \_ больше для самой широкой совместимости с поставщиками пространства имен, которые используют один из них.</span><span class="sxs-lookup"><span data-stu-id="d32da-136">For Windows Sockets 2, however, applications should check for both WSAENOMORE and WSA\_E\_NO\_MORE for the widest possible compatibility with namespace providers that use either one.</span></span>

## <a name="helper-functions"></a><span data-ttu-id="d32da-137">Вспомогательные функции</span><span class="sxs-lookup"><span data-stu-id="d32da-137">Helper Functions</span></span>

-   [<span data-ttu-id="d32da-138">**всажетсервицекласснамебиклассид**</span><span class="sxs-lookup"><span data-stu-id="d32da-138">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
-   [<span data-ttu-id="d32da-139">**всааддресстостринг**</span><span class="sxs-lookup"><span data-stu-id="d32da-139">**WSAAddressToString**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaddresstostringa)
-   [<span data-ttu-id="d32da-140">**всастрингтоаддресс**</span><span class="sxs-lookup"><span data-stu-id="d32da-140">**WSAStringToAddress**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsastringtoaddressa)
-   [<span data-ttu-id="d32da-141">**всажетсервицеклассинфо**</span><span class="sxs-lookup"><span data-stu-id="d32da-141">**WSAGetServiceClassInfo**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa)

<span data-ttu-id="d32da-142">Вспомогательные функции разрешения имен включают функцию для получения имени класса службы по заданному идентификатору класса службы, пару функций, используемых для преобразования транспортного адреса между структурой [**SOCKADDR**](sockaddr-2.md) и строковым представлением ASCII, функцию для получения сведений о схеме класса службы для данного класса службы и набор макросов для сопоставления хорошо известных служб с предварительно ВЫДЕЛЕНными идентификаторами GUID.</span><span class="sxs-lookup"><span data-stu-id="d32da-142">The name resolution helper functions include a function to retrieve a service class name given a service class identifier, a pair of functions used to translate a transport address between a [**SOCKADDR**](sockaddr-2.md) structure and an ASCII string representation, a function to retrieve the service class schema information for a given service class, and a set of macros for mapping well known services to preallocated GUIDs.</span></span>

<span data-ttu-id="d32da-143">Следующие макросы из Winsock2. h помогают в сопоставлении между известными классами служб и этими пространствами имен:</span><span class="sxs-lookup"><span data-stu-id="d32da-143">The following macros from Winsock2.h aid in mapping between well known service classes and these namespaces:</span></span>

| <span data-ttu-id="d32da-144">Макрос</span><span class="sxs-lookup"><span data-stu-id="d32da-144">Macro</span></span>                                                                                                            | <span data-ttu-id="d32da-145">Описание</span><span class="sxs-lookup"><span data-stu-id="d32da-145">Description</span></span>                                                                                                                |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32da-146">СВЦИД \_ TCP (порт) свЦид \_ UDP (порт)</span><span class="sxs-lookup"><span data-stu-id="d32da-146">SVCID\_TCP(Port) SVCID\_UDP(Port)</span></span><br/> <span data-ttu-id="d32da-147">СВЦИД \_ NetWare (тип объекта)</span><span class="sxs-lookup"><span data-stu-id="d32da-147">SVCID\_NETWARE(Object Type)</span></span><br/>                              | <span data-ttu-id="d32da-148">При наличии порта для TCP/IP или UDP/IP или типа объекта в случае с NetWare возвращает идентификатор GUID (номер порта в порядке размещения).</span><span class="sxs-lookup"><span data-stu-id="d32da-148">Given a port for TCP/IP or UDP/IP or the object type in the case of NetWare, returns the GUID (port number in host order).</span></span> |
| <span data-ttu-id="d32da-149">\_свЦид \_ TCP (GUID) — это \_ СВЦИД \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="d32da-149">IS\_SVCID\_TCP(GUID)IS\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="d32da-150">ЯВЛЯЕТСЯ \_ свЦид \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="d32da-150">IS\_SVCID\_NETWARE(GUID)</span></span><br/>                          | <span data-ttu-id="d32da-151">Возвращает **значение true** , если идентификатор GUID находится в допустимом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="d32da-151">Returns **TRUE** if the GUID is within the allowable range.</span></span>                                                                |
| <span data-ttu-id="d32da-152">SET \_ TCP \_ СВЦИД (GUID, порт) Set \_ UDP \_ свЦид (GUID, порт)</span><span class="sxs-lookup"><span data-stu-id="d32da-152">SET\_TCP\_SVCID(GUID, port)SET\_UDP\_SVCID(GUID, port)</span></span><br/>                                                | <span data-ttu-id="d32da-153">Инициализирует структуру GUID с эквивалентом GUID для номера порта TCP или UDP (номер порта должен быть в порядке размещения).</span><span class="sxs-lookup"><span data-stu-id="d32da-153">Initializes a GUID structure with the GUID equivalent for a TCP or UDP port number (port number must be in host order).</span></span>    |
| <span data-ttu-id="d32da-154">Порт \_ из \_ \_ порта СВЦИД TCP (GUID) \_ из \_ свЦид \_ UDP (GUID)</span><span class="sxs-lookup"><span data-stu-id="d32da-154">PORT\_FROM\_SVCID\_TCP(GUID)PORT\_FROM\_SVCID\_UDP(GUID)</span></span><br/> <span data-ttu-id="d32da-155">SAPI \_ из \_ свЦид \_ NetWare (GUID)</span><span class="sxs-lookup"><span data-stu-id="d32da-155">SAPID\_FROM\_SVCID\_NETWARE(GUID)</span></span><br/> | <span data-ttu-id="d32da-156">Возвращает порт или тип объекта, связанный с идентификатором GUID (номер порта в порядке размещения).</span><span class="sxs-lookup"><span data-stu-id="d32da-156">Returns the port or object type associated with the GUID (port number in host order).</span></span>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="d32da-157">См. также</span><span class="sxs-lookup"><span data-stu-id="d32da-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d32da-158">**функцию getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="d32da-158">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="d32da-159">**жетаддринфоекс**</span><span class="sxs-lookup"><span data-stu-id="d32da-159">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
</dt> <dt>

[<span data-ttu-id="d32da-160">**жетаддринфов**</span><span class="sxs-lookup"><span data-stu-id="d32da-160">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
</dt> <dt>

[<span data-ttu-id="d32da-161">**жетнамеинфо**</span><span class="sxs-lookup"><span data-stu-id="d32da-161">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
</dt> <dt>

[<span data-ttu-id="d32da-162">**жетнамеинфов**</span><span class="sxs-lookup"><span data-stu-id="d32da-162">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)
</dt> <dt>

[<span data-ttu-id="d32da-163">Структуры данных разрешения имен</span><span class="sxs-lookup"><span data-stu-id="d32da-163">Name Resolution Data Structures</span></span>](name-resolution-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="d32da-164">Модель разрешения имен</span><span class="sxs-lookup"><span data-stu-id="d32da-164">Name Resolution Model</span></span>](name-resolution-model-2.md)
</dt> <dt>

[<span data-ttu-id="d32da-165">Разрешение имен, не зависящее от протокола</span><span class="sxs-lookup"><span data-stu-id="d32da-165">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="d32da-166">Регистрация и разрешение имен</span><span class="sxs-lookup"><span data-stu-id="d32da-166">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="d32da-167">**SOCKADDR**</span><span class="sxs-lookup"><span data-stu-id="d32da-167">**SOCKADDR**</span></span>](sockaddr-2.md)
</dt> <dt>

[<span data-ttu-id="d32da-168">**всаенумнамеспацепровидерс**</span><span class="sxs-lookup"><span data-stu-id="d32da-168">**WSAEnumNameSpaceProviders**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa)
</dt> <dt>

[<span data-ttu-id="d32da-169">**всажетсервицекласснамебиклассид**</span><span class="sxs-lookup"><span data-stu-id="d32da-169">**WSAGetServiceClassNameByClassId**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida)
</dt> <dt>

[<span data-ttu-id="d32da-170">**всаинсталлсервицекласс**</span><span class="sxs-lookup"><span data-stu-id="d32da-170">**WSAInstallServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsainstallserviceclassa)
</dt> <dt>

[<span data-ttu-id="d32da-171">**всалукупсервицебегин**</span><span class="sxs-lookup"><span data-stu-id="d32da-171">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="d32da-172">**всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="d32da-172">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="d32da-173">**всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="d32da-173">**WSALookupServiceNext**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="d32da-174">**всаремовесервицекласс**</span><span class="sxs-lookup"><span data-stu-id="d32da-174">**WSARemoveServiceClass**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaremoveserviceclass)
</dt> <dt>

[<span data-ttu-id="d32da-175">**всасетсервице**</span><span class="sxs-lookup"><span data-stu-id="d32da-175">**WSASetService**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsasetservicea)
</dt> <dt>

[<span data-ttu-id="d32da-176">**всакуерисет**</span><span class="sxs-lookup"><span data-stu-id="d32da-176">**WSAQUERYSET**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="d32da-177">**всансклассинфо**</span><span class="sxs-lookup"><span data-stu-id="d32da-177">**WSANSCLASSINFO**</span></span>](/windows/desktop/api/Winsock2/ns-winsock2-wsansclassinfow)
</dt> </dl>

 

 




