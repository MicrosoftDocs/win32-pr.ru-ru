---
description: .
ms.assetid: 51df3fb9-416d-46b8-b3a7-0281401fb390
title: Рекомендации по минимизации неотвечающих служб
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e1fbad7fe60c4165ebb97847c303482314f68e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913212"
---
# <a name="best-practices-for-minimizing-unresponsive-services"></a><span data-ttu-id="60ac6-103">Рекомендации по минимизации неотвечающих служб</span><span class="sxs-lookup"><span data-stu-id="60ac6-103">Best Practices for Minimizing Unresponsive Services</span></span>

## <a name="affected-platform"></a><span data-ttu-id="60ac6-104">Затронутая платформа</span><span class="sxs-lookup"><span data-stu-id="60ac6-104">Affected Platform</span></span>

 <span data-ttu-id="60ac6-105">**Клиенты** — Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="60ac6-105">**Clients** – Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="60ac6-106">Описание</span><span class="sxs-lookup"><span data-stu-id="60ac6-106">Description</span></span>

<span data-ttu-id="60ac6-107">Неотвечающие службы могут привести к превышению времени ожидания, прекращению сеансов и даже потере данных.</span><span class="sxs-lookup"><span data-stu-id="60ac6-107">Unresponsive services can result in timeouts, terminated sessions, and even lost data.</span></span> <span data-ttu-id="60ac6-108">Применение рекомендаций может значительно сократить количество нереагирующих служб.</span><span class="sxs-lookup"><span data-stu-id="60ac6-108">Employing best practices can greatly reduce the occurrence of unresponsive services.</span></span>

## <a name="best-practices"></a><span data-ttu-id="60ac6-109">Рекомендации</span><span class="sxs-lookup"><span data-stu-id="60ac6-109">Best Practices</span></span>

<span data-ttu-id="60ac6-110">Убедитесь, что приложения и все зависимые от них службы и драйверы отвечают на уведомления о питании и завершении работы системы.</span><span class="sxs-lookup"><span data-stu-id="60ac6-110">Make sure your applications and all of their dependent services and drivers respond to system power and shutdown notifications.</span></span>

-   <span data-ttu-id="60ac6-111">Все приложения должны отвечать быстро и соответствующим образом, чтобы завершить работу таких сообщений \_ , как WM куерендсессион и WM \_ ENDSESSION, которые указывают на выполнение завершения работы.</span><span class="sxs-lookup"><span data-stu-id="60ac6-111">All applications should respond promptly and appropriately to shutdown messages such as WM\_QUERYENDSESSION and WM\_ENDSESSION that indicate a shutdown is in progress.</span></span>
-   <span data-ttu-id="60ac6-112">Все службы должны быстро реагировать на уведомления о завершении работы диспетчера служб.</span><span class="sxs-lookup"><span data-stu-id="60ac6-112">All services should promptly respond to SCM shutdown notifications.</span></span> <span data-ttu-id="60ac6-113">Если это не так, компьютер рассматривает их как не отвечающий и инициирует 20-секундный тайм-аут и останавливает их, открывая возможность потери данных.</span><span class="sxs-lookup"><span data-stu-id="60ac6-113">If they fail to do so, the machine treats them as unresponsive and initiates a 20-second time-out and stops them, opening up the possibility of lost data.</span></span> <span data-ttu-id="60ac6-114">Это также добавляет 20 секунд к времени завершения работы компьютера.</span><span class="sxs-lookup"><span data-stu-id="60ac6-114">This also adds 20 seconds to the shutdown time of a machine shutdown.</span></span>
-   <span data-ttu-id="60ac6-115">Все службы, имеющие зависимости драйверов устройств ядра, должны быстро реагировать на \_ \_ уведомления о завершении работы (IRP MJ) в подпрограмме диспатчшутдовн.</span><span class="sxs-lookup"><span data-stu-id="60ac6-115">All services that have kernel device driver dependencies should respond promptly and appropriately to IRP\_MJ\_SHUTDOWN notification in their DispatchShutdown routines.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="60ac6-116">Ссылки на другие ресурсы</span><span class="sxs-lookup"><span data-stu-id="60ac6-116">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="60ac6-117">Набор средств для оценки производительности Windows</span><span class="sxs-lookup"><span data-stu-id="60ac6-117">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)  
</dl>

 

 



