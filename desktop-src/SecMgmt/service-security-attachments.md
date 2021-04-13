---
description: Набор средств настройки безопасности (Майкрософт) — это набор средств консоли управления (MMC), упрощающих настройку и анализ безопасности системы.
ms.assetid: c6558789-84eb-4998-a2c1-725d8a64d255
title: Вложения безопасности службы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47cdd0ca3799615125900a3ae6b0b78c26f4abc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343092"
---
# <a name="service-security-attachments"></a><span data-ttu-id="25124-103">Вложения безопасности службы</span><span class="sxs-lookup"><span data-stu-id="25124-103">Service Security Attachments</span></span>

<span data-ttu-id="25124-104">Набор средств настройки безопасности (Майкрософт) — это набор средств консоли управления (MMC), упрощающих настройку и анализ безопасности системы.</span><span class="sxs-lookup"><span data-stu-id="25124-104">The Microsoft Security Configuration tool set is a set of Microsoft Management Console (MMC) tools that simplify configuration and analysis of system security.</span></span> <span data-ttu-id="25124-105">Однако некоторые службы имеют особые требования к конфигурации, которые выходят за рамки настроек безопасности, предоставляемых стандартным набором средств.</span><span class="sxs-lookup"><span data-stu-id="25124-105">Some services, however, have specialized configuration needs that go beyond the security settings provided by the standard tool set.</span></span> <span data-ttu-id="25124-106">Для решения этих задач можно расширить функциональные возможности набора инструментов, записав вложение, которое обрабатывает задачи безопасности, связанные с конкретной службой.</span><span class="sxs-lookup"><span data-stu-id="25124-106">To handle those needs, you can extend the functionality of the tool set by writing an attachment that handles the service-specific security tasks.</span></span>

<span data-ttu-id="25124-107">Например, диспетчер очереди сообщений — это служба Windows NT, которая определяет закрытые объекты, которые должны быть защищены, например, принтеры.</span><span class="sxs-lookup"><span data-stu-id="25124-107">For example, Spooler is a Windows NT service that defines private objects, which need to be secured, for example, printers.</span></span> <span data-ttu-id="25124-108">Эта функция не обрабатывается стандартным набором инструментов и поэтому требует вложения для обработки конфигурации и анализа объектов принтера.</span><span class="sxs-lookup"><span data-stu-id="25124-108">This functionality is not handled by the standard tool set and thus requires an attachment to handle configuration and analysis of printer objects.</span></span> <span data-ttu-id="25124-109">Настройка общих параметров безопасности, таких как политика вызова службы, по-прежнему обрабатывается набором средств настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="25124-109">Configuration of general security parameters, such as the service invocation policy, is still handled by the Security Configuration tool set.</span></span>

<span data-ttu-id="25124-110">Вложения службы безопасности расширяют функциональные возможности набора средств настройки безопасности для поддержки конфигураций, зависящих от службы.</span><span class="sxs-lookup"><span data-stu-id="25124-110">Security service attachments extend the functionality of the Security Configuration tool set to support service-specific configurations.</span></span>

<span data-ttu-id="25124-111">Вложение имеет два компонента:</span><span class="sxs-lookup"><span data-stu-id="25124-111">An attachment has two components:</span></span>

-   <span data-ttu-id="25124-112">Расширение оснастки MMC, реализующее пользовательский интерфейс вложения.</span><span class="sxs-lookup"><span data-stu-id="25124-112">An MMC snap-in extension that implements the attachment user interface.</span></span>
-   <span data-ttu-id="25124-113">Подсистема вложений, которая обрабатывает задачи по настройке и анализу безопасности для конкретной службы.</span><span class="sxs-lookup"><span data-stu-id="25124-113">An attachment engine that processes service-specific security configuration and analysis tasks.</span></span>

<span data-ttu-id="25124-114">Расширение оснастки вложений размещается в оснастках настройки безопасности. Это оснастки MMC, которые предоставляют пользователю интерфейсы для настройки и анализа общих параметров безопасности службы.</span><span class="sxs-lookup"><span data-stu-id="25124-114">The attachment snap-in extension is hosted by the Security Configuration snap-ins. These are MMC snap-ins that provide the user with interfaces to configure and analyze the general security settings for a service.</span></span> <span data-ttu-id="25124-115">Параметры, зависящие от службы, настраиваются с помощью расширения оснастки вложения.</span><span class="sxs-lookup"><span data-stu-id="25124-115">Service-specific settings are configured using the attachment snap-in extension.</span></span>

<span data-ttu-id="25124-116">Когда пользователь изменяет параметр конфигурации, оснастки "Настройка безопасности" сохраняют новые сведения, а затем передают запрос в подсистему настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="25124-116">When the user changes a configuration setting, the Security Configuration snap-ins store the new information and then pass the request to the Security Configuration Engine.</span></span> <span data-ttu-id="25124-117">Обработчик обрабатывает запрос и задает для службы новую конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="25124-117">The Engine processes the request and sets the service to the new configuration.</span></span> <span data-ttu-id="25124-118">Если запрос влияет на стандартную настройку безопасности, он обрабатывается ядром.</span><span class="sxs-lookup"><span data-stu-id="25124-118">If the request affects a standard security setting, it is handled by the Engine.</span></span> <span data-ttu-id="25124-119">Если запрос зависит от конкретной службы, обработчик вызывает подходящую подсистему вложений для обработки запроса.</span><span class="sxs-lookup"><span data-stu-id="25124-119">If the request is service-specific, the Engine calls the appropriate attachment engine to handle the request.</span></span>

<span data-ttu-id="25124-120">На следующем рисунке показано, как подсистема вложений и расширение оснастки работают в инфраструктуре набора средств настройки безопасности.</span><span class="sxs-lookup"><span data-stu-id="25124-120">The following illustration shows how the attachment engine and snap-in extension work within the framework of the Security Configuration tool set.</span></span>

![Подсистема вложений и оснастки](images/model1a.png)

<span data-ttu-id="25124-122">Дополнительные сведения об использовании набора средств настройки безопасности Майкрософт см. в статье Настройка безопасности с помощью предпочтительной поисковой системы.</span><span class="sxs-lookup"><span data-stu-id="25124-122">For more information about using the Microsoft Security Configuration tool set, search for Security Configuration using your preferred search engine.</span></span>

 

 



