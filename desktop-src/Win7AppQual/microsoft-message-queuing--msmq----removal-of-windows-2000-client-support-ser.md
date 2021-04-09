---
description: .
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Очередь сообщений Майкрософт (MSMQ) — удаление службы поддержки клиентов Windows 2000
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54688ee4ad24eb691c95e4d70ce0acb881e212eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081314"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a><span data-ttu-id="9e563-103">Очередь сообщений Майкрософт (MSMQ) — удаление службы поддержки клиентов Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9e563-103">Microsoft Message Queuing (MSMQ) - Removal of Windows 2000 Client Support Service</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="9e563-104">Затронутые платформы</span><span class="sxs-lookup"><span data-stu-id="9e563-104">Affected Platforms</span></span>

<span data-ttu-id="9e563-105">**Серверы** — Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9e563-105">**Servers** - Windows Server 2008 R2</span></span>  



## <a name="feature-impact"></a><span data-ttu-id="9e563-106">Воздействие на функции</span><span class="sxs-lookup"><span data-stu-id="9e563-106">Feature Impact</span></span>

 <span data-ttu-id="9e563-107">**Серьезность** — высокая</span><span class="sxs-lookup"><span data-stu-id="9e563-107">**Severity** - High</span></span>  
<span data-ttu-id="9e563-108">**Частота** -низкая</span><span class="sxs-lookup"><span data-stu-id="9e563-108">**Frequency** - Low</span></span>  

## <a name="description"></a><span data-ttu-id="9e563-109">Описание</span><span class="sxs-lookup"><span data-stu-id="9e563-109">Description</span></span>

<span data-ttu-id="9e563-110">Служба поддержки клиентов Windows 2000 — это дополнительный компонент сервера очереди сообщений, который можно установить на компьютере с контроллером домена Windows 2003 или Windows 2008.</span><span class="sxs-lookup"><span data-stu-id="9e563-110">The Windows 2000 Client Support Service is an optional component of the Message Queuing Server that you can install on a Windows 2003 or Windows 2008 domain controller machine.</span></span> <span data-ttu-id="9e563-111">Эта служба позволяет клиентам Windows 2000 взаимодействовать в режиме, интегрированном в домен, с любым сервером очереди сообщений, установленным на компьютерах под управлением Windows 2003/2008.</span><span class="sxs-lookup"><span data-stu-id="9e563-111">This service allows Windows 2000 clients to operate in a domain-integrated mode with any Message Queuing server installed on Windows 2003/2008 machines.</span></span> <span data-ttu-id="9e563-112">Клиенты MSMQ, работающие в Windows XP, не нуждаются в этой службе.</span><span class="sxs-lookup"><span data-stu-id="9e563-112">MSMQ Clients operating on Windows XP upwards do not need this service.</span></span>

### <a name="manifestation-of-impact"></a><span data-ttu-id="9e563-113">Влияние на манифесты</span><span class="sxs-lookup"><span data-stu-id="9e563-113">Manifestation of Impact</span></span>

<span data-ttu-id="9e563-114">Это изменение влияет на Windows 2000 при взаимодействии в домене Windows 7, где все контроллеры домена являются Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="9e563-114">This change impacts Windows 2000 when interoperating in a Windows 7 domain where all domain controllers are Windows Server 2008 R2.</span></span> <span data-ttu-id="9e563-115">Если клиент выполняет обновление до домена Windows 7, существующие приложения MSMQ на любых компьютерах Windows 2000 в домене не смогут работать в режиме интеграции с доменами, если эти клиенты не обновляются до более поздней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="9e563-115">If a customer upgrades to the Windows 7 domain, the existing MSMQ applications on any Windows 2000 machines in the domain will not be able to operate in a domain-integrated mode unless these clients upgrade to a higher Windows version.</span></span>

### <a name="mitigation"></a><span data-ttu-id="9e563-116">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="9e563-116">Mitigation</span></span>

<span data-ttu-id="9e563-117">Пользователи, имеющие клиентские компьютеры Windows 2000 в домене Windows 7, могут настроить контроллер домена Windows 2003/2008 в домене и установить службу поддержки клиентов MSMQ Windows 2000 на этом контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="9e563-117">Users who have Windows 2000 Client machines on a Windows 7 domain can configure a Windows 2003/2008 domain controller in the domain and install the MSMQ Windows 2000 Client Support Service on this domain controller.</span></span>

### <a name="leveraging-feature-capabilities"></a><span data-ttu-id="9e563-118">Использование возможностей функций</span><span class="sxs-lookup"><span data-stu-id="9e563-118">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="9e563-119">Пользователи, имеющие клиентские компьютеры Windows 2000 под управлением MSMQ, должны выполнить обновление до более поздней версии Windows, чтобы воспользоваться преимуществами реализации сервера MSMQ на основе Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9e563-119">Users who have Windows 2000 Client machines running MSMQ should upgrade to a higher Windows version in order to take advantage of the Active Directory-based implementation of the MSMQ Server.</span></span>

### <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="9e563-120">Совместимость, производительность, надежность и тестирование на удобство использования</span><span class="sxs-lookup"><span data-stu-id="9e563-120">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="9e563-121">Пользователи, у которых есть клиентские компьютеры Windows 2000, использующие MSMQ в домене Windows 7 с одним или несколькими контроллерами домена нижнего уровня, должны проверить, что их приложения работают в этом смешанном домене.</span><span class="sxs-lookup"><span data-stu-id="9e563-121">Users who have Windows 2000 Client machines running MSMQ on a Windows 7 domain with one or more down-level domain controllers should verify that their applications are functional on this mixed domain.</span></span>

 

 



