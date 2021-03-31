---
title: Рекомендации по повышению производительности
description: Рекомендации по разработке приложений, которые хорошо работают в среде службы удаленных рабочих столов.
ms.assetid: 50f0c1f6-8046-4ceb-b2c4-6fc1ae86fd73
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea7ada6ee2b51943d47f39446d0b1bb3b7d6718
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411368"
---
# <a name="performance-guidelines"></a><span data-ttu-id="530d1-103">Рекомендации по повышению производительности</span><span class="sxs-lookup"><span data-stu-id="530d1-103">Performance guidelines</span></span>

<span data-ttu-id="530d1-104">В следующих разделах приводятся рекомендации по разработке приложений, которые хорошо работают в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="530d1-104">The following sections provide guidelines for developing applications that perform well in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="530d1-105">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="530d1-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="530d1-106">Графические эффекты</span><span class="sxs-lookup"><span data-stu-id="530d1-106">Graphic effects</span></span>](graphic-effects.md)
</dt> <dd>

<span data-ttu-id="530d1-107">Список функций, которые следует отключить при работе в качестве удаленного сеанса в среде службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="530d1-107">A list of features that should be disabled when running as a remote session in a Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="530d1-108">Рекомендации для фоновых задач в службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="530d1-108">Guidelines for background tasks in Remote Desktop Services</span></span>](background-tasks.md)
</dt> <dd>

<span data-ttu-id="530d1-109">Чтобы обеспечить максимальную доступность ЦП для всех пользователей, отключите фоновые задачи при работе в среде службы удаленных рабочих столов или создайте эффективные фоновые задачи, которые не требуют больших ресурсов.</span><span class="sxs-lookup"><span data-stu-id="530d1-109">To maximize CPU availability for all users, either disable background tasks when running in a Remote Desktop Services environment or create efficient background tasks that are not resource-intensive.</span></span>

</dd> <dt>

[<span data-ttu-id="530d1-110">Использование потока</span><span class="sxs-lookup"><span data-stu-id="530d1-110">Thread usage</span></span>](thread-usage.md)
</dt> <dd>

<span data-ttu-id="530d1-111">Необходимо настроить и сбалансировать использование потоков приложения для многопользовательской многопроцессорной службы удаленных рабочих столов среды.</span><span class="sxs-lookup"><span data-stu-id="530d1-111">You should tune and balance application thread usage for a multiuser, multiprocessor Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="530d1-112">Обнаружение среды службы удаленных рабочих столов</span><span class="sxs-lookup"><span data-stu-id="530d1-112">Detecting the Remote Desktop Services environment</span></span>](detecting-the-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="530d1-113">Для оптимизации производительности в приложениях рекомендуется определить, работают ли они в службы удаленных рабочих столовном сеансе клиента.</span><span class="sxs-lookup"><span data-stu-id="530d1-113">To optimize performance, it is good practice for applications to detect whether they are running in a Remote Desktop Services client session.</span></span>

</dd> </dl>

<span data-ttu-id="530d1-114">Проверьте приложение на наличие утечек памяти и устраните все проблемы.</span><span class="sxs-lookup"><span data-stu-id="530d1-114">Check your application for memory leaks and resolve any problems.</span></span> <span data-ttu-id="530d1-115">Конечно, это хороший совет для любого приложения, но в среде службы удаленных рабочих столов приложение может выполняться несколько раз несколькими пользователями, что позволяет быстро увеличивать воздействие утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="530d1-115">Of course this is good advice for any application, but in a Remote Desktop Services environment, an application can be run multiple times by multiple users, thus rapidly magnifying the effect of a memory leak.</span></span>

<span data-ttu-id="530d1-116">Анимация, крупные изображения, звук и другие службы, интенсивно использующие пропускную способность, должны быть настроены.</span><span class="sxs-lookup"><span data-stu-id="530d1-116">Animations, large images, audio, and other bandwidth-intensive services must be configurable.</span></span> <span data-ttu-id="530d1-117">Если эти службы не являются основной функцией, они могут быть отключены по умолчанию для удаленных сеансов, но включены, когда сеанс выполняется локально или через подключение с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="530d1-117">When these services are not the primary function, they can be off by default for remote sessions, but enabled when a session is running locally or over a high bandwidth connection.</span></span> <span data-ttu-id="530d1-118">Если целью приложения является предоставление служб высокой пропускной способности, таких как потоковая передача видеовещания, служба не должна быть отключена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="530d1-118">If the purpose of an application is to provide high bandwidth services, such as streaming video broadcasts, the service does not have to be off by default.</span></span>

 

 




