---
title: Обнаружение устройств и служб Bluetooth
description: Чтобы упростить обнаружение устройств и служб Bluetooth, Windows сопоставляет протокол обнаружения службы Bluetooth (SDP) с интерфейсами пространства имен Windows Sockets.
ms.assetid: 4fed0de6-87cc-4093-aa6a-667ca98563e7
keywords:
- Bluetooth, задачи, обнаружение устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e46f2582ceca35668e717c09524e855e585fff0f
ms.sourcegitcommit: 6f905c836d3fd04934fb3e5f1a56b4a421f7596f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "105654267"
---
# <a name="discovering-bluetooth-devices-and-services"></a><span data-ttu-id="aaaf4-104">Обнаружение устройств и служб Bluetooth</span><span class="sxs-lookup"><span data-stu-id="aaaf4-104">Discovering Bluetooth Devices and Services</span></span>

<span data-ttu-id="aaaf4-105">Чтобы упростить обнаружение устройств и служб Bluetooth, Windows сопоставляет протокол обнаружения службы Bluetooth (SDP) с интерфейсами пространства имен Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-105">To facilitate the discovery of Bluetooth devices and services, Windows maps the Bluetooth Service Discovery Protocol (SDP) onto the Windows Sockets namespace interfaces.</span></span> <span data-ttu-id="aaaf4-106">К основным функциям, используемым для этого сопоставления, относятся функции [**всасетсервице**](bluetooth-and-wsasetservice.md), [**всалукупсервицебегин**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md)и [**всалукупсервицеенд**](bluetooth-and-wsalookupserviceend.md) .</span><span class="sxs-lookup"><span data-stu-id="aaaf4-106">The primary functions used for this mapping are the [**WSASetService**](bluetooth-and-wsasetservice.md), [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), [**WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and [**WSALookupServiceEnd**](bluetooth-and-wsalookupserviceend.md) functions.</span></span> <span data-ttu-id="aaaf4-107">Структура [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) также используется вместе с этими функциями.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-107">The [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure is also used in conjunction with these functions.</span></span>

<span data-ttu-id="aaaf4-108">Поскольку некоторые понятия и параметры от SDP по Bluetooth не обязательно сопоставляются непосредственно со структурой [**всакуерисет**](bluetooth-and-wsaqueryset-for-set-service.md) , необходимо уделять внимание способам создания и использования своих членов.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-108">Because certain concepts and parameters from the Bluetooth SDP do not necessarily map directly into the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure, attention must be paid to how its members are created and used.</span></span> <span data-ttu-id="aaaf4-109">Для многих сложных операций Bluetooth, таких как создание записей SDP, используется элемент **лпблоб** в **всакуерисет** .</span><span class="sxs-lookup"><span data-stu-id="aaaf4-109">For many complex Bluetooth operations, such as the creation of SDP records, the **lpBlob** member of the **WSAQUERYSET** is used.</span></span> <span data-ttu-id="aaaf4-110">Если необходимо учитывать такие особенности, они описаны особо, например на страницах ссылок, таких как [**Bluetooth и всалукупсервиценекст**](bluetooth-and-wsalookupservicenext.md), а также в других.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-110">When such special consideration is necessary, it is specifically described, such as in reference pages like [**Bluetooth and WSALookupServiceNext**](bluetooth-and-wsalookupservicenext.md), and others.</span></span>

<span data-ttu-id="aaaf4-111">Важно понимать, что регистрация SDP отделена от управления сокетом.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-111">It is important to understand that SDP registration is separate from socket control.</span></span> <span data-ttu-id="aaaf4-112">Когда серверное приложение подготавливается к приему клиентского подключения, оно должно вызвать функцию [**всасетсервице**](bluetooth-and-wsasetservice.md) , чтобы зарегистрировать запись SDP с поддержкой Bluetooth, соответствующую этой службе.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-112">When a server application is prepared to accept client connection, it should call the [**WSASetService**](bluetooth-and-wsasetservice.md) function to register a Bluetooth SDP record that corresponds to that service.</span></span> <span data-ttu-id="aaaf4-113">Это приложение Bluetooth должно повторно вызвать функцию **всасетсервице** перед закрытием, чтобы отменить регистрацию записи SDP с Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-113">That Bluetooth application must call the **WSASetService** function again before closing, to deregister the Bluetooth SDP record.</span></span>

<span data-ttu-id="aaaf4-114">При использовании функций сопоставления, описанных на этой странице, \_ назначается пространство имен NS БС.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-114">When using the mapping functions described on this page, the NS\_BTH namespace is assigned.</span></span>

<span data-ttu-id="aaaf4-115">Дополнительные сведения об обнаружении устройств и служб см. на следующих справочных страницах:</span><span class="sxs-lookup"><span data-stu-id="aaaf4-115">For further information about discovering devices and services, consult the following reference pages:</span></span>

-   [<span data-ttu-id="aaaf4-116">**Bluetooth и Всасетсервице**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-116">**Bluetooth and WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
-   [<span data-ttu-id="aaaf4-117">**Bluetooth и Всалукупсервицебегин для запроса устройства**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-117">**Bluetooth and WSALookupServiceBegin for Device Inquiry**</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
-   [<span data-ttu-id="aaaf4-118">**Bluetooth и Всалукупсервицебегин для обнаружения служб**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-118">**Bluetooth and WSALookupServiceBegin for Service Discovery**</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
-   [<span data-ttu-id="aaaf4-119">**Bluetooth и Всалукупсервиценекст**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-119">**Bluetooth and WSALookupServiceNext**</span></span>](bluetooth-and-wsalookupservicenext.md)
-   [<span data-ttu-id="aaaf4-120">**Bluetooth и Всалукупсервицеенд**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-120">**Bluetooth and WSALookupServiceEnd**</span></span>](bluetooth-and-wsalookupserviceend.md)
-   [<span data-ttu-id="aaaf4-121">**Bluetooth и большой двоичный объект**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-121">**Bluetooth and BLOB**</span></span>](bluetooth-and-blob.md)
-   [<span data-ttu-id="aaaf4-122">**Bluetooth и ВСАКУЕРИСЕТ**</span><span class="sxs-lookup"><span data-stu-id="aaaf4-122">**Bluetooth and WSAQUERYSET**</span></span>](bluetooth-and-wsaqueryset-for-set-service.md)

<span data-ttu-id="aaaf4-123">Вы также можете скачать [Пример подключения Bluetooth](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) для получения полного примера.</span><span class="sxs-lookup"><span data-stu-id="aaaf4-123">You can also download the [Bluetooth connection sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample) for a complete example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aaaf4-124">См. также</span><span class="sxs-lookup"><span data-stu-id="aaaf4-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaaf4-125">Программирование Bluetooth с помощью сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="aaaf4-125">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md)
</dt> <dt>

[<span data-ttu-id="aaaf4-126">Пример подключения Bluetooth</span><span class="sxs-lookup"><span data-stu-id="aaaf4-126">Bluetooth connection sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Bluetooth%20connection%20sample)
</dt> </dl>

 

 




