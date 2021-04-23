---
title: Перечисления Windows Connect Now
description: Windows Connect теперь определяет следующие типы перечислений.
ms.assetid: 6ef37f4c-f4f1-4f02-ad73-031d9ce163f2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baeb8481edd189cdf2880ee8cacf42483f8894eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068101"
---
# <a name="windows-connect-now-enumerations"></a><span data-ttu-id="72523-103">Перечисления Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="72523-103">Windows Connect Now Enumerations</span></span>

<span data-ttu-id="72523-104">Windows Connect теперь определяет следующие типы перечислений.</span><span class="sxs-lookup"><span data-stu-id="72523-104">Windows Connect Now defines the following enumeration types.</span></span>



| <span data-ttu-id="72523-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="72523-105">Enumeration</span></span>                                                                                             | <span data-ttu-id="72523-106">Описание</span><span class="sxs-lookup"><span data-stu-id="72523-106">Description</span></span>                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="72523-107">**\_тип атрибута \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-107">**WCN\_ATTRIBUTE\_TYPE**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_attribute_type)                                                      | <span data-ttu-id="72523-108">Определяет различные типы буферов атрибутов, определенные для Wi-Fi защищенной установки.</span><span class="sxs-lookup"><span data-stu-id="72523-108">Defines the various attribute buffer types defined for Wi-Fi Protected Setup.</span></span><br/>                                      |
| [<span data-ttu-id="72523-109">**\_тип пароля \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-109">**WCN\_PASSWORD\_TYPE**</span></span>](/windows/win32/api/wcndevice/ne-wcndevice-wcn_password_type)                                                        | <span data-ttu-id="72523-110">Определяет проверку подлинности, которая будет использоваться в сеансе WPS.</span><span class="sxs-lookup"><span data-stu-id="72523-110">Defines the authentication that will be used in a WPS session.</span></span> <br/>                                                    |
| [<span data-ttu-id="72523-111">**\_состояние сеанса \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-111">**WCN\_SESSION\_STATUS**</span></span>](/windows/win32/api/wcndevice/ne-wcndevice-wcn_session_status)                                                      | <span data-ttu-id="72523-112">Определяет состояние сеанса WPS.</span><span class="sxs-lookup"><span data-stu-id="72523-112">Defines the status of a WPS session.</span></span><br/>                                                                               |
| [<span data-ttu-id="72523-113">**\_ \_ \_ состояние СОПОСТАВЛЕНИЯ типа значения \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-113">**WCN\_VALUE\_TYPE\_ASSOCIATION\_STATE**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_association_state)                        | <span data-ttu-id="72523-114">Определяет возможные состояния взаимосвязей беспроводной станции во время запроса на обнаружение.</span><span class="sxs-lookup"><span data-stu-id="72523-114">Defines the possible association states of a wireless station during a Discovery request.</span></span><br/>                          |
| [<span data-ttu-id="72523-115">**\_тип значения \_ WCN \_ Boolean**</span><span class="sxs-lookup"><span data-stu-id="72523-115">**WCN\_VALUE\_TYPE\_BOOLEAN**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_boolean)                                             | <span data-ttu-id="72523-116">Определяет значения, используемые для представления условий true/false, возникающих во время установки устройства и ассоциации.</span><span class="sxs-lookup"><span data-stu-id="72523-116">Defines values used to represent true/false conditions encountered during device setup and association.</span></span><br/>            |
| [<span data-ttu-id="72523-117">**Тип \_ значения \_ \_ проверки подлинности типа WCN \_**</span><span class="sxs-lookup"><span data-stu-id="72523-117">**WCN\_VALUE\_TYPE\_AUTHENTICATION\_TYPE**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_authentication_type)                    | <span data-ttu-id="72523-118">Определяет методы проверки подлинности, поддерживаемые зарегистрированным объектом (точкой доступа или станцией).</span><span class="sxs-lookup"><span data-stu-id="72523-118">Defines the authentication methods supported by the Enrollee (access point or station).</span></span><br/>                            |
| [<span data-ttu-id="72523-119">**\_ \_ \_ методы конфигурации типа значения \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-119">**WCN\_VALUE\_TYPE\_CONFIG\_METHODS**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_config_methods)                              | <span data-ttu-id="72523-120">Определяет методы конфигурации, поддерживаемые заявителем или регистратором.</span><span class="sxs-lookup"><span data-stu-id="72523-120">Defines the configuration methods supported by the Enrollee or Registrar.</span></span><br/>                                          |
| [<span data-ttu-id="72523-121">**\_ \_ \_ Ошибка конфигурации типа значения \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-121">**WCN\_VALUE\_TYPE\_CONFIGURATION\_ERROR**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_configuration_error)                    | <span data-ttu-id="72523-122">Определяет возможные значения ошибок, возвращаемые на устройство при попытке настроить его и связать с беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="72523-122">Defines possible error values returned to a device while attempting to configure to, and associate with, the WLAN.</span></span><br/> |
| [<span data-ttu-id="72523-123">**\_тип значения \_ WCN \_ \_ идентификатор пароля \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="72523-123">**WCN\_VALUE\_TYPE\_DEVICE\_PASSWORD\_ID**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_device_password_id)                     | <span data-ttu-id="72523-124">Определяет возможные значения пароля.</span><span class="sxs-lookup"><span data-stu-id="72523-124">Defines the possible password values.</span></span><br/>                                                                              |
| [<span data-ttu-id="72523-125">**\_тип значения для типа \_ \_ шифрования \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-125">**WCN\_VALUE\_TYPE\_ENCRYPTION\_TYPE**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_encryption_type)                            | <span data-ttu-id="72523-126">Определяет поддерживаемые типы шифрования WLAN.</span><span class="sxs-lookup"><span data-stu-id="72523-126">Defines the supported WLAN encryption types.</span></span><br/>                                                                       |
| [<span data-ttu-id="72523-127">**\_ \_ радиочастотные типы значений \_ WCN \_**</span><span class="sxs-lookup"><span data-stu-id="72523-127">**WCN\_VALUE\_TYPE\_RF\_BANDS**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_rf_bands)                                          | <span data-ttu-id="72523-128">Определяет частоту радиоволн, на которой подписчик отправляет запросы на обнаружение.</span><span class="sxs-lookup"><span data-stu-id="72523-128">Defines the radio frequency band on which an enrollee sends Discovery requests.</span></span><br/>                                    |
| [<span data-ttu-id="72523-129">**\_ \_ версия типа значения \_ WCN**</span><span class="sxs-lookup"><span data-stu-id="72523-129">**WCN\_VALUE\_TYPE\_VERSION**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_version)                                             | <span data-ttu-id="72523-130">Определяет поддерживаемую версию Wi-Fi Protected Setup (WPS).</span><span class="sxs-lookup"><span data-stu-id="72523-130">Defines the supported version of Wi-Fi Protected Setup (WPS).</span></span><br/>                                                      |
| [<span data-ttu-id="72523-131">**\_тип значения WCN — \_ \_ \_ \_ защищенное \_ \_ состояние установки Wi Fi**</span><span class="sxs-lookup"><span data-stu-id="72523-131">**WCN\_VALUE\_TYPE\_WI\_FI\_PROTECTED\_SETUP\_STATE**</span></span>](/windows/win32/api/wcntypes/ne-wcntypes-wcn_value_type_wi_fi_protected_setup_state) | <span data-ttu-id="72523-132">Определяет значения, которые указывают, настроено ли устройство.</span><span class="sxs-lookup"><span data-stu-id="72523-132">Defines values that indicate if a device is configured.</span></span><br/>                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="72523-133">См. также</span><span class="sxs-lookup"><span data-stu-id="72523-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72523-134">Ссылка на Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="72523-134">Windows Connect Now Reference</span></span>](windows-connect-now-reference.md)
</dt> </dl>

 

 





