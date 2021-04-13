---
title: Несколько служб каталогов
description: Одной из проблем работы в распределенных вычислительных средах является определение и поиск ресурсов, таких как пользователи, группы, очереди печати и документы.
ms.assetid: 66929290-b830-4768-a2ae-604d1a9de5c4
ms.tgt_platform: multiple
keywords:
- ADSI для нескольких служб каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccc2e174fc1b07564f1cca6c12093a289a0c865a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328411"
---
# <a name="multiple-directory-services"></a><span data-ttu-id="a578e-104">Несколько служб каталогов</span><span class="sxs-lookup"><span data-stu-id="a578e-104">Multiple Directory Services</span></span>

<span data-ttu-id="a578e-105">Одной из проблем работы в распределенных вычислительных средах является определение и поиск ресурсов, таких как пользователи, группы, очереди печати и документы.</span><span class="sxs-lookup"><span data-stu-id="a578e-105">One challenge of working within a distributed computing environment is identifying and locating resources such as users, groups, print queues, and documents.</span></span> <span data-ttu-id="a578e-106">Служба каталогов является частью распределенной вычислительной среды, которая предоставляет способ поиска и выявления пользователей и ресурсов, доступных в системе.</span><span class="sxs-lookup"><span data-stu-id="a578e-106">A directory service is the part of a distributed computing environment that provides a way to locate and identify the users and resources available in the system.</span></span> <span data-ttu-id="a578e-107">Служба каталогов похожа на телефонный каталог.</span><span class="sxs-lookup"><span data-stu-id="a578e-107">A directory service is like a phone directory.</span></span> <span data-ttu-id="a578e-108">Учитывая имя пользователя или ресурса, он предоставляет данные, необходимые для доступа к этому пользователю или ресурсу.</span><span class="sxs-lookup"><span data-stu-id="a578e-108">Given a name for a person or a resource, it provides the data necessary to access that person or resource.</span></span> <span data-ttu-id="a578e-109">Для доступа к ресурсам в сети не нужно начинать с привязки данных.</span><span class="sxs-lookup"><span data-stu-id="a578e-109">You do not have to start with binding data to access a resource on the network.</span></span>

<span data-ttu-id="a578e-110">Для большинства предприятий уже существует множество разных каталогов.</span><span class="sxs-lookup"><span data-stu-id="a578e-110">Most enterprises already have many different directories in place.</span></span> <span data-ttu-id="a578e-111">Например, сетевые операционные системы, системы электронной почты и "коллективные" продукты имеют собственные каталоги.</span><span class="sxs-lookup"><span data-stu-id="a578e-111">For example, network operating systems, electronic mail systems, and "groupware" products all have their own directories.</span></span> <span data-ttu-id="a578e-112">Многие проблемы возникают, когда один предприятие развертывает несколько каталогов.</span><span class="sxs-lookup"><span data-stu-id="a578e-112">Many issues arise when a single enterprise deploys multiple directories.</span></span> <span data-ttu-id="a578e-113">Эти проблемы включают в себя удобство использования, согласованность данных, затраты на разработку и стоимость поддержки.</span><span class="sxs-lookup"><span data-stu-id="a578e-113">These issues include usability, data consistency, development cost, and support cost, among others.</span></span>

<span data-ttu-id="a578e-114">Эти проблемы решаются в интерфейсе ADSI, в котором предусмотрен единый, согласованный, Открытый набор интерфейсов, который можно использовать для управления и использования любой службы каталогов, имеющей поставщик ADSI.</span><span class="sxs-lookup"><span data-stu-id="a578e-114">These issues are addressed in ADSI, in that there is provided a single, consistent, open set of interfaces that can be used for managing and using any directory service that has an ADSI provider.</span></span>

 

 




