---
description: Пересылка является отклонения входящего сеанса от другого адреса назначения.
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: Вперед
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897386"
---
# <a name="forward"></a><span data-ttu-id="7a2a7-103">Вперед</span><span class="sxs-lookup"><span data-stu-id="7a2a7-103">Forward</span></span>

<span data-ttu-id="7a2a7-104">Пересылка является отклонения входящего сеанса от другого адреса назначения.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="7a2a7-105">TAPI позволяет приложению указать список условий переадресации для адреса.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="7a2a7-106">Условия переадресации могут быть достаточно детализированы как разные режимы назначения и [**перенаправления**](./lineforwardmode--constants.md) для каждого адреса вызывающего.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="7a2a7-107">Операцию пересылки можно также использовать для реализации функции выборочной неактивности, перенаправляя некоторые вызывающие объекты в голосовое сообщение и разрешив попытку выполнения других.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="7a2a7-108">Операция пересылки также может отменить все действующие в данный момент перенаправления.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="7a2a7-109">Некоторым поставщикам услуг требуется, чтобы приложение вызывало вызов консультации до выполнения операции пересылки.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="7a2a7-110">Затем операция пересылки передает указатель на вызов консультации.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="7a2a7-111">Не все поставщики служб поддерживают использование этой операции.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="7a2a7-112">**Интерфейс TAPI 2. x:** Чтобы задать для [**линефорвард**](/windows/win32/api/tapi/nf-tapi-lineforward) значение Get [**линежетаддрессстатус**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), измените сообщение с уведомлением [**\_ аддрессстате в строке**](./line-addressstate.md) линеаддрессстате \_ вперед.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="7a2a7-113">**Интерфейс TAPI 3. x:** См. раздел [**итаддресс:: Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**итаддресс:: Get \_ куррентфорвардинфо**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), уведомление об изменении: [**итаддрессевент:: Get \_ событие**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) с \_ пересылкой AE.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="7a2a7-114">Поставщику услуг может быть невозможно узнать, какое время переадресации действует для адреса.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="7a2a7-115">Пересылка может быть отменена или изменена способами, которые не приводят к уведомлению поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="7a2a7-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
