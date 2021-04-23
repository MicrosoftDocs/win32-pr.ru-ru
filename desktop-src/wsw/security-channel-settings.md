---
title: Параметры безопасного канала
description: Параметры канала безопасности контролируют способ применения и проверки безопасности в канале.
ms.assetid: ad964874-0bc7-4f03-8ceb-33627ff99f08
keywords:
- Параметры канала безопасности веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6fcd0b42b2d5581a5b7c489e9ada70f32abfefa
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104134807"
---
# <a name="security-channel-settings"></a><span data-ttu-id="cc726-106">Параметры безопасного канала</span><span class="sxs-lookup"><span data-stu-id="cc726-106">Security Channel Settings</span></span>

<span data-ttu-id="cc726-107">Параметры канала безопасности контролируют способ применения и проверки безопасности в канале.</span><span class="sxs-lookup"><span data-stu-id="cc726-107">Security channel settings control the way security is applied and verified on a channel.</span></span> <span data-ttu-id="cc726-108">Каждый параметр канала безопасности представлен коллекцией пар "свойство-значение" с ключами свойств, определяемыми [**\_ \_ \_ идентификатором свойства WS Security**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span><span class="sxs-lookup"><span data-stu-id="cc726-108">Each security channel setting is represented by a collection of property-value pairs, with the property keys defined by the enumeration [**WS\_SECURITY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id).</span></span> <span data-ttu-id="cc726-109">Каждое свойство в коллекции имеет разумное значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cc726-109">Each property in the collection has a reasonable default value.</span></span> <span data-ttu-id="cc726-110">Из-за этих значений по умолчанию можно определить и использовать описание безопасности без указания каких-либо параметров канала безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc726-110">Because of these default values, it is possible to define and use a security description without specifying any of the security channel settings.</span></span>


<span data-ttu-id="cc726-111">[Параметры привязки безопасности](security-binding-settings.md) содержат похожие коллекции пар «свойство-значение», ключи которых определяются структурой [**\_ \_ \_ свойств привязки безопасности WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) .</span><span class="sxs-lookup"><span data-stu-id="cc726-111">[Security binding settings](security-binding-settings.md) contain similar collections of property-value pairs whose keys are defined by the [**WS\_SECURITY\_BINDING\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_security_binding_property) structure.</span></span> <span data-ttu-id="cc726-112">Различие между этими двумя параметрами состоит в том, что параметры каналов безопасности ограничены описанием безопасности (то есть содержат свойства безопасности для всего канала), в то время как параметры привязки безопасности ограничены одной из привязок безопасности, и может существовать множество привязок безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc726-112">The difference between these two sorts of settings is that the security channel settings are scoped to a security description (that is, they contain channel-wide security properties), whereas security binding settings are scoped to one of the security bindings, and there may be many security bindings.</span></span> <span data-ttu-id="cc726-113">Таким образом, например, пользовательское описание безопасности, содержащее три привязки безопасности, будет иметь один набор параметров каналов безопасности для всего канала и три контейнера параметров привязки безопасности, по одному для каждой привязки безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc726-113">Consequently, for example, a custom security description that contains three security bindings will have one security channel settings bag for the entire channel and three security binding settings bags, one for each security binding.</span></span>

<span data-ttu-id="cc726-114">С параметрами канала безопасности используются следующие перечисления.</span><span class="sxs-lookup"><span data-stu-id="cc726-114">The following enumerations are used with security channel settings:</span></span>

-   [<span data-ttu-id="cc726-115">**\_уровень защиты \_ WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-115">**WS\_PROTECTION\_LEVEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_protection_level)
-   [<span data-ttu-id="cc726-116">**\_ \_ \_ идентификатор свойства маркера \_ безопасности \_ запроса WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-116">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_request_security_token_property_id)
-   [<span data-ttu-id="cc726-117">**\_ \_ идентификатор алгоритма безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-117">**WS\_SECURITY\_ALGORITHM\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_algorithm_id)
-   [<span data-ttu-id="cc726-118">**\_ \_ идентификатор свойства алгоритма безопасности WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-118">**WS\_SECURITY\_ALGORITHM\_PROPERTY\_ID**</span></span>](/windows/win32/api/webservices/ne-webservices-ws_move_to)
-   [<span data-ttu-id="cc726-119">**\_ \_ макет заголовка безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-119">**WS\_SECURITY\_HEADER\_LAYOUT**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_layout)
-   [<span data-ttu-id="cc726-120">**\_ \_ версия заголовка безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-120">**WS\_SECURITY\_HEADER\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_header_version)
-   [<span data-ttu-id="cc726-121">**\_ \_ идентификатор свойства безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-121">**WS\_SECURITY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_property_id)
-   [<span data-ttu-id="cc726-122">**\_ \_ Использование метки времени безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-122">**WS\_SECURITY\_TIMESTAMP\_USAGE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_security_timestamp_usage)
-   [<span data-ttu-id="cc726-123">**\_ \_ \_ идентификатор свойства токена \_ безопасности \_ XML WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-123">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_security_token_property_id)

<span data-ttu-id="cc726-124">Для параметров канала безопасности используются следующие структуры:</span><span class="sxs-lookup"><span data-stu-id="cc726-124">The following structures are used with security channel settings:</span></span>

-   [<span data-ttu-id="cc726-125">**\_ \_ \_ свойство токена безопасности WS Request \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-125">**WS\_REQUEST\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_request_security_token_property)
-   [<span data-ttu-id="cc726-126">**\_ \_ свойство алгоритма безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-126">**WS\_SECURITY\_ALGORITHM\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_property)
-   [<span data-ttu-id="cc726-127">**\_ \_ набор алгоритмов безопасности WS \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-127">**WS\_SECURITY\_ALGORITHM\_SUITE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_algorithm_suite)
-   [<span data-ttu-id="cc726-128">**\_свойство безопасности \_ WS**</span><span class="sxs-lookup"><span data-stu-id="cc726-128">**WS\_SECURITY\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_property)
-   [<span data-ttu-id="cc726-129">**\_ \_ \_ свойство токена безопасности XML WS \_**</span><span class="sxs-lookup"><span data-stu-id="cc726-129">**WS\_XML\_SECURITY\_TOKEN\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_security_token_property)

 

 




