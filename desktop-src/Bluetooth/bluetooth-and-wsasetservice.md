---
title: Bluetooth и Всасетсервице
description: Bluetooth использует функцию Всасетсервице для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ БС) из реестра.
ms.assetid: 71c5ed9c-fade-4d15-848e-eb810ad4cbb2
keywords:
- Bluetooth Bluetooth
- Всасетсервице Bluetooth
- Bluetooth и Всасетсервице Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70399b73bf24477ee1a0ec0c7585a9f46b7657ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487785"
---
# <a name="bluetooth-and-wsasetservice"></a><span data-ttu-id="5af6d-106">Bluetooth и Всасетсервице</span><span class="sxs-lookup"><span data-stu-id="5af6d-106">Bluetooth and WSASetService</span></span>

<span data-ttu-id="5af6d-107">Bluetooth использует функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) для регистрации или удаления экземпляра службы в пространстве имен Bluetooth (NS \_ БС) из реестра.</span><span class="sxs-lookup"><span data-stu-id="5af6d-107">Bluetooth uses the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to register or remove a service instance within the Bluetooth namespace (NS\_BTH) from the registry.</span></span> <span data-ttu-id="5af6d-108">Маркер, возвращаемый этой операцией, может использоваться только для удаления службы.</span><span class="sxs-lookup"><span data-stu-id="5af6d-108">The handle returned by this operation may only be used to delete the service.</span></span>

<span data-ttu-id="5af6d-109">Bluetooth имеет два средства рекламы служб, использующих функцию [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) :</span><span class="sxs-lookup"><span data-stu-id="5af6d-109">Bluetooth has two means of advertising services using the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function:</span></span>

-   <span data-ttu-id="5af6d-110">В приложении может быть объявлена простая запись службы SDP для Bluetooth, созданная на основе стандартных членов в структуре [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="5af6d-110">The application can have the system advertise a simple Bluetooth SDP service record, constructed from standard members in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span>
-   <span data-ttu-id="5af6d-111">В приложении может быть объявлена собственная запись SDP для Bluetooth путем передачи структуры [**службы БС \_ Set \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) в элемент **лпблоб** структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) .</span><span class="sxs-lookup"><span data-stu-id="5af6d-111">The application can have the system advertise their own Bluetooth SDP record by passing a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure in the **lpBlob** member of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure.</span></span> <span data-ttu-id="5af6d-112">Это более сложный подход.</span><span class="sxs-lookup"><span data-stu-id="5af6d-112">This is a more complex approach.</span></span>

> [!Note]  
> <span data-ttu-id="5af6d-113">Записи SDP, объявленные [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) , не сохраняются после завершения процесса, который их опубликовал.</span><span class="sxs-lookup"><span data-stu-id="5af6d-113">SDP records advertised by [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) do not persist after the process that published them has quit.</span></span>

 

<span data-ttu-id="5af6d-114">Использование [**всасетсервице**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) с Bluetooth имеет следующие требования.</span><span class="sxs-lookup"><span data-stu-id="5af6d-114">Use of [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) with Bluetooth has the following requirements:</span></span>

-   <span data-ttu-id="5af6d-115">Параметр *лпксрегинфо* — это адрес структуры [**всакуерисет**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) , подрегистрируемой.</span><span class="sxs-lookup"><span data-stu-id="5af6d-115">The *lpqsRegInfo* parameter is the address of the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure to be registered.</span></span>
-   <span data-ttu-id="5af6d-116">Параметр *ессоператион* является перечислением, которое содержит одну из операций, показанных в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="5af6d-116">The *essOperation* parameter is an enumeration that contains one of the operations shown in the following table.</span></span>



| <span data-ttu-id="5af6d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5af6d-117">Value</span></span>                  | <span data-ttu-id="5af6d-118">Описание</span><span class="sxs-lookup"><span data-stu-id="5af6d-118">Description</span></span>                                                                                |
|------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af6d-119">РНРСЕРВИЦЕ \_ регистр</span><span class="sxs-lookup"><span data-stu-id="5af6d-119">RNRSERVICE\_REGISTER</span></span>   | <span data-ttu-id="5af6d-120">Начинает объявлять службу для запросов удаленных радиостанций с помощью протокола Bluetooth SDP.</span><span class="sxs-lookup"><span data-stu-id="5af6d-120">Starts advertising the service to remote radios querying using the Bluetooth SDP protocol.</span></span> |
| <span data-ttu-id="5af6d-121">РНРСЕРВИЦЕ \_ Отмена регистрации</span><span class="sxs-lookup"><span data-stu-id="5af6d-121">RNRSERVICE\_DEREGISTER</span></span> | <span data-ttu-id="5af6d-122">Недопустимый.</span><span class="sxs-lookup"><span data-stu-id="5af6d-122">Not valid.</span></span> <span data-ttu-id="5af6d-123">Возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="5af6d-123">Returns an error.</span></span>                                                               |
| <span data-ttu-id="5af6d-124">РНРСЕРВИЦЕ \_ Удаление</span><span class="sxs-lookup"><span data-stu-id="5af6d-124">RNRSERVICE\_DELETE</span></span>     | <span data-ttu-id="5af6d-125">Останавливает объявление службы.</span><span class="sxs-lookup"><span data-stu-id="5af6d-125">Stops advertising the service.</span></span>                                                             |



 

> [!Note]  
> <span data-ttu-id="5af6d-126">Дескрипторы служб, обнаруженные во время вызова [**всалукупсервицебегин**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) или [**всалукупсервиценекст**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) , несовместимы с \_ операцией удаления рнрсервице.</span><span class="sxs-lookup"><span data-stu-id="5af6d-126">Service handles discovered during a [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) or [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) call are incompatible with the RNRSERVICE\_DELETE operation.</span></span>

 

-   <span data-ttu-id="5af6d-127">Параметр *двконтролфлагс* зарезервирован и должен быть равен нулю.</span><span class="sxs-lookup"><span data-stu-id="5af6d-127">The *dwControlFlags* parameter is reserved, and must be zero.</span></span>

<span data-ttu-id="5af6d-128">Дополнительные сведения и список параметров сокетов Bluetooth см. в разделе [Параметры Bluetooth и сокета](bluetooth-and-socket-options.md).</span><span class="sxs-lookup"><span data-stu-id="5af6d-128">For more information and a list of Bluetooth socket options, see [Bluetooth and Socket Options](bluetooth-and-socket-options.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5af6d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="5af6d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5af6d-130">Сокеты Windows</span><span class="sxs-lookup"><span data-stu-id="5af6d-130">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 