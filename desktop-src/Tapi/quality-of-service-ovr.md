---
description: Сеть в режиме асинхронной пересылки (ATM) является основной частью вычислений, а поддержка ATM была добавлена во многие части операционной системы.
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: Качество обслуживания (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911987"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="82803-103">Качество обслуживания (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="82803-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="82803-104">Сеть в режиме асинхронной пересылки (ATM) является основной частью вычислений, а поддержка ATM была добавлена во многие части операционной системы.</span><span class="sxs-lookup"><span data-stu-id="82803-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="82803-105">TAPI также поддерживает ключевые атрибуты установки вызовов на ATM-телефонах.</span><span class="sxs-lookup"><span data-stu-id="82803-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="82803-106">Наиболее важным из них с точки зрения приложения является возможность запрашивать, согласовывать, повторно согласовывать и принимать указания о параметрах качества обслуживания (QOS) для входящих и исходящих вызовов.</span><span class="sxs-lookup"><span data-stu-id="82803-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="82803-107">Сведения о QOS в TAPI обмениваются данными между приложениями и поставщиками служб в структурах [**фловспек**](/windows/desktop/api/qos/ns-qos-flowspec) , которые определены в Windows sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="82803-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="82803-108">Приложения запрашивают качество обслуживания исходящих вызовов, устанавливая значения сведений о сеансе перед запуском сеанса связи.</span><span class="sxs-lookup"><span data-stu-id="82803-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="82803-109">Поставщик услуг попытается предоставить указанное качество обслуживания и завершить вызов, если это невозможно.</span><span class="sxs-lookup"><span data-stu-id="82803-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="82803-110">Затем приложение может настроить свои параметры и повторить вызов.</span><span class="sxs-lookup"><span data-stu-id="82803-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="82803-111">После установления вызова приложение может запросить изменение в QOS.</span><span class="sxs-lookup"><span data-stu-id="82803-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="82803-112">TAPI предоставляет уведомления о событиях для владельца или мониторинга приложений при наличии изменений в уровнях качества обслуживания.</span><span class="sxs-lookup"><span data-stu-id="82803-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="82803-113">Поддержка QOS не ограничена транспортом ATM. любой поставщик услуг может реализовать функции QOS.</span><span class="sxs-lookup"><span data-stu-id="82803-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="82803-114">Не все поставщики служб поддерживают использование этих сведений.</span><span class="sxs-lookup"><span data-stu-id="82803-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="82803-115">\* \* TAPI 2. x: \* \*[**линесеткаллкуалитйофсервице**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**линежеткаллинфо**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **двсендингфловспексизе**, **двсендингфловспекоффсет**, **dwReceivingFlowspecSize** и **dwReceivingFlowspecOffset** [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="82803-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="82803-116">\* \* TAPI 3. x: \* \*[**итбасиккаллконтрол:: сеткос**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**иткосевент**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="82803-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
