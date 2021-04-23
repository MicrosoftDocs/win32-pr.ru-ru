---
description: Операция парковки позволяет приложению отправить сеанс на специальный адрес, где он будет удерживаться до неприпаркованного.
ms.assetid: 6a82f03e-d8fd-4d0b-8f5d-f7934ba86759
title: Остановк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aded4657a9d337d6d9c663622a5359856e964b90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673845"
---
# <a name="park"></a><span data-ttu-id="a8b24-103">Остановк</span><span class="sxs-lookup"><span data-stu-id="a8b24-103">Park</span></span>

<span data-ttu-id="a8b24-104">Операция парковки позволяет приложению отправить сеанс на специальный адрес, где он будет удерживаться до неприпаркованного.</span><span class="sxs-lookup"><span data-stu-id="a8b24-104">The park operation allows an application to send a session to a special address where it will be held until unparked.</span></span> <span data-ttu-id="a8b24-105">С точки зрения приложения это очень похоже на перемещение.</span><span class="sxs-lookup"><span data-stu-id="a8b24-105">From the point of view of the application, this looks much like a transfer.</span></span> <span data-ttu-id="a8b24-106">Для стороны на другом конце соединения это похоже на удержание.</span><span class="sxs-lookup"><span data-stu-id="a8b24-106">To the party on the other end of the connection, this resembles being put on hold.</span></span>

<span data-ttu-id="a8b24-107">Различие между приостановкой и переносом заключается в том, что припаркованный адрес не является точкой соединения для сеанса, а сеанс не имеет предупреждения или истечения времени ожидания. Разница между приостановкой и удержанием заключается в том, что после завершения операции приостановки сеанс больше не будет связан с адресом приложения.</span><span class="sxs-lookup"><span data-stu-id="a8b24-107">The difference between park and transfer is that the parked address is not a connection point for the session, and the session does not alert or time out. The difference between park and hold is that once park operation completes, the session is no longer associated with the application's address.</span></span>

<span data-ttu-id="a8b24-108">Имеются две формы приостановки сеанса: *направленный приостановленный* и *ненаправленный*.</span><span class="sxs-lookup"><span data-stu-id="a8b24-108">Two forms of parking a session are provided: *directed park* and *nondirected park*.</span></span> <span data-ttu-id="a8b24-109">В окне "приостановить вызов" приложение указывает адрес назначения, на котором будет приостановлен вызов.</span><span class="sxs-lookup"><span data-stu-id="a8b24-109">In directed call park, the application specifies the destination address where the call is to be parked.</span></span> <span data-ttu-id="a8b24-110">При непрямом приостановке поставщик услуг или основное оборудование определяют адрес и возвращают его в приложение.</span><span class="sxs-lookup"><span data-stu-id="a8b24-110">With nondirected park, the service provider or underlying hardware determines the address and returns it to the application.</span></span>

<span data-ttu-id="a8b24-111">Приостановленный сеанс обычно переходит в состояние простоя после его успешного приостановки, после чего приложение должно освободить связанные с ним ресурсы.</span><span class="sxs-lookup"><span data-stu-id="a8b24-111">A parked session typically enters the idle state after it has been successfully parked, and the application should then release the resources associated with it.</span></span> <span data-ttu-id="a8b24-112">Сведения о том, как это сделать, см. в разделе [Завершение сеанса](terminate-a-session-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b24-112">See [Terminate a Session](terminate-a-session-ovr.md) for a summary of how to do this.</span></span>

<span data-ttu-id="a8b24-113">Если приложение отменяет сеанс, то новые ресурсы сеанса выделяются, даже если приложение вернуло предыдущие указатели, поэтому сбой выполнения соответствующих выпусков может привести к различным проблемам.</span><span class="sxs-lookup"><span data-stu-id="a8b24-113">If the application unparks the session, new session resources are allocated even if the application has returned the previous pointers, so failure to do proper releases can result in a variety of problems.</span></span>

<span data-ttu-id="a8b24-114">Некоторые поставщики услуг могут напомнить пользователю о том, что сеанс был приостановлен в течение некоторого длительного периода времени.</span><span class="sxs-lookup"><span data-stu-id="a8b24-114">Some service providers can remind the user after a session has been parked for some long amount of time.</span></span> <span data-ttu-id="a8b24-115">Приложение видит вызов предложения с указанием [причины](reason-ovr.md) вызова напоминание.</span><span class="sxs-lookup"><span data-stu-id="a8b24-115">The application sees an offering call with a call [reason](reason-ovr.md) set to reminder.</span></span>

<span data-ttu-id="a8b24-116">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="a8b24-116">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="a8b24-117">**Интерфейс TAPI 2. x:** См. раздел [**линепарк**](/windows/win32/api/tapi/nf-tapi-linepark), [**линеунпарк**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span><span class="sxs-lookup"><span data-stu-id="a8b24-117">**TAPI 2.x:** See [**linePark**](/windows/win32/api/tapi/nf-tapi-linepark), [**lineUnpark**](/windows/win32/api/tapi/nf-tapi-lineunpark).</span></span>

<span data-ttu-id="a8b24-118">**TAPI 3:** См. раздел [**итбасиккаллконтрол::P аркдирект**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**Итбасиккаллконтрол::P аркиндирект**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**итбасиккаллконтрол:: unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span><span class="sxs-lookup"><span data-stu-id="a8b24-118">**TAPI 3:** See [**ITBasicCallControl::ParkDirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkdirect), [**ITBasicCallControl::ParkIndirect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-parkindirect), [**ITBasicCallControl::Unpark**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-unpark).</span></span>

 

 
