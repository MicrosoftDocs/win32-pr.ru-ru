---
title: Перечисления сборщика событий Windows
description: В следующей таблице перечислены перечисления пакета SDK сборщика событий Windows.
ms.assetid: 3775aa7c-ef35-4534-b709-15624fd7a90d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d2617c6eb0052ec1ac41d5f197d9216c253054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411040"
---
# <a name="windows-event-collector-enumerations"></a><span data-ttu-id="92533-103">Перечисления сборщика событий Windows</span><span class="sxs-lookup"><span data-stu-id="92533-103">Windows Event Collector Enumerations</span></span>

<span data-ttu-id="92533-104">В следующей таблице перечислены перечисления пакета SDK сборщика событий Windows.</span><span class="sxs-lookup"><span data-stu-id="92533-104">The following table lists the enumerations of the Windows Event Collector SDK.</span></span>



| <span data-ttu-id="92533-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="92533-105">Enumeration</span></span>                                                                                               | <span data-ttu-id="92533-106">Описание</span><span class="sxs-lookup"><span data-stu-id="92533-106">Description</span></span>                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="92533-107">**\_ \_ режим конфигурации подписки \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-107">**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode)                       | <span data-ttu-id="92533-108">Задает различные режимы конфигурации, которые изменяют параметры по умолчанию для подписки.</span><span class="sxs-lookup"><span data-stu-id="92533-108">Specifies different configuration modes that change the default settings for a subscription.</span></span>                                            |
| [<span data-ttu-id="92533-109">**\_ \_ Формат содержимого подписки \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-109">**EC\_SUBSCRIPTION\_CONTENT\_FORMAT**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_content_format)                               | <span data-ttu-id="92533-110">Указывает способ подготовки событий к просмотру на компьютере, который отправляет события, прежде чем события будут отправлены на компьютер сборщика событий.</span><span class="sxs-lookup"><span data-stu-id="92533-110">Specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.</span></span> |
| [<span data-ttu-id="92533-111">**\_ \_ тип учетных данных подписки EC \_**</span><span class="sxs-lookup"><span data-stu-id="92533-111">**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type)                           | <span data-ttu-id="92533-112">Указывает тип учетных данных для использования при взаимодействии с источниками событий.</span><span class="sxs-lookup"><span data-stu-id="92533-112">Specifies the type of credentials to use when communicating with event sources.</span></span>                                                         |
| [<span data-ttu-id="92533-113">**\_ \_ режим доставки подписки \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-113">**EC\_SUBSCRIPTION\_DELIVERY\_MODE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_delivery_mode)                                 | <span data-ttu-id="92533-114">Указывает способ доставки событий через подписку на события (с помощью принудительной или опрашивающей модели).</span><span class="sxs-lookup"><span data-stu-id="92533-114">Specifies how events are delivered through an event subscription (using a push or pull model).</span></span>                                          |
| [<span data-ttu-id="92533-115">**\_ \_ идентификатор свойства подписки \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-115">**EC\_SUBSCRIPTION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_property_id)                                     | <span data-ttu-id="92533-116">Определяет значения для определения свойств подписки на события, используемых для конфигурации подписки.</span><span class="sxs-lookup"><span data-stu-id="92533-116">Defines values to identify event subscription properties used for subscription configuration.</span></span>                                           |
| [<span data-ttu-id="92533-117">**\_ \_ \_ \_ активное \_ состояние времени выполнения подписки EC**</span><span class="sxs-lookup"><span data-stu-id="92533-117">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_ACTIVE\_STATUS**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_active_status) | <span data-ttu-id="92533-118">Указывает состояние подписки или источника событий в отношении подписки.</span><span class="sxs-lookup"><span data-stu-id="92533-118">Specifies the status of a subscription or an event source with respect to a subscription.</span></span>                                               |
| [<span data-ttu-id="92533-119">**\_ \_ \_ идентификатор сведений о состоянии среды выполнения \_ подписки EC \_**</span><span class="sxs-lookup"><span data-stu-id="92533-119">**EC\_SUBSCRIPTION\_RUNTIME\_STATUS\_INFO\_ID**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_runtime_status_info_id)             | <span data-ttu-id="92533-120">Задает значение, определяющее свойство состояния среды выполнения для источника события или подписки.</span><span class="sxs-lookup"><span data-stu-id="92533-120">Specifies a value that identifies a property of the runtime status of an event source or a subscription.</span></span>                                |
| [<span data-ttu-id="92533-121">**\_Тип подписки \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-121">**EC\_SUBSCRIPTION\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_type)                                                    | <span data-ttu-id="92533-122">Указывает тип используемой подписки (инициированная источником или подписка, инициированная сборщиком).</span><span class="sxs-lookup"><span data-stu-id="92533-122">Specifies the type of subscription to use (a source initiated or collector initiated subscription).</span></span>                                     |
| [<span data-ttu-id="92533-123">**\_тип варианта \_ EC**</span><span class="sxs-lookup"><span data-stu-id="92533-123">**EC\_VARIANT\_TYPE**</span></span>](/windows/desktop/api/Evcoll/ne-evcoll-ec_variant_type)                                                              | <span data-ttu-id="92533-124">Определяет значения, указывающие типы данных, которые используются в функциях сборщика событий Windows.</span><span class="sxs-lookup"><span data-stu-id="92533-124">Defines the values that specify the data types that are used in the Windows Event Collector functions.</span></span>                                  |



 

 

 




