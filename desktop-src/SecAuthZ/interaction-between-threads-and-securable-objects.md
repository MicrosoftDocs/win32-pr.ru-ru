---
description: При проверке доступа система сравнивает сведения о безопасности в маркере доступа потоков со сведениями о безопасности в дескрипторе безопасности объектов.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Взаимодействие между потоками и защищаемыми объектами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912427"
---
# <a name="interaction-between-threads-and-securable-objects"></a><span data-ttu-id="cd637-103">Взаимодействие между потоками и защищаемыми объектами</span><span class="sxs-lookup"><span data-stu-id="cd637-103">Interaction Between Threads and Securable Objects</span></span>

<span data-ttu-id="cd637-104">Когда поток пытается использовать [защищаемый объект](securable-objects.md), система выполняет проверку доступа, прежде чем разрешить потоку продолжать работу.</span><span class="sxs-lookup"><span data-stu-id="cd637-104">When a thread attempts to use a [securable object](securable-objects.md), the system performs an access check before allowing the thread to proceed.</span></span> <span data-ttu-id="cd637-105">При проверке доступа система сравнивает сведения о безопасности в [*маркере доступа*](/windows/desktop/SecGloss/a-gly) потока со сведениями о безопасности в [*дескрипторе безопасности*](/windows/desktop/SecGloss/s-gly)объекта.</span><span class="sxs-lookup"><span data-stu-id="cd637-105">In an access check, the system compares the security information in the thread's [*access token*](/windows/desktop/SecGloss/a-gly) against the security information in the object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span>

-   <span data-ttu-id="cd637-106">Маркер доступа содержит [*идентификаторы безопасности*](/windows/desktop/SecGloss/s-gly) (SID), которые указывают пользователя, связанного с потоком.</span><span class="sxs-lookup"><span data-stu-id="cd637-106">The access token contains [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) that identify the user associated with the thread.</span></span>
-   <span data-ttu-id="cd637-107">Дескриптор безопасности определяет владельца объекта и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL).</span><span class="sxs-lookup"><span data-stu-id="cd637-107">The security descriptor identifies the object's owner and contains a [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL).</span></span> <span data-ttu-id="cd637-108">Список DACL содержит [*записи контроля доступа*](/windows/desktop/SecGloss/a-gly) (ACE), каждый из которых указывает права доступа, разрешенные или запрещенные конкретному пользователю или группе.</span><span class="sxs-lookup"><span data-stu-id="cd637-108">The DACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs), each of which specify the access rights allowed or denied to a specific user or group.</span></span>

<span data-ttu-id="cd637-109">Система проверяет DACL объекта и ищет ACE, которые применяются к идентификаторам безопасности пользователя и группы из маркера доступа потока.</span><span class="sxs-lookup"><span data-stu-id="cd637-109">The system checks the object's DACL, looking for ACEs that apply to the user and group SIDs from the thread's access token.</span></span> <span data-ttu-id="cd637-110">Система проверяет каждую запись ACE, пока доступ не будет предоставлен или запрещен, или пока нет дополнительных элементов ACE для проверки.</span><span class="sxs-lookup"><span data-stu-id="cd637-110">The system checks each ACE until access is either granted or denied or until there are no more ACEs to check.</span></span> <span data-ttu-id="cd637-111">Как можно представить, [*список управления доступом*](/windows/desktop/SecGloss/a-gly) (ACL) может иметь несколько записей ACE, которые применяются к идентификаторам безопасности маркера.</span><span class="sxs-lookup"><span data-stu-id="cd637-111">Conceivably, an [*access control list*](/windows/desktop/SecGloss/a-gly) (ACL) could have several ACEs that apply to the token's SIDs.</span></span> <span data-ttu-id="cd637-112">И, если это происходит, права доступа, предоставляемые каждым элементом ACE, суммируются.</span><span class="sxs-lookup"><span data-stu-id="cd637-112">And, if this occurs, the access rights granted by each ACE accumulate.</span></span> <span data-ttu-id="cd637-113">Например, если один элемент ACE предоставляет доступ на чтение к группе, а другой ACE предоставляет доступ на запись для пользователя, который является членом группы, пользователь может иметь доступ на чтение и запись к объекту.</span><span class="sxs-lookup"><span data-stu-id="cd637-113">For example, if one ACE grants read access to a group and another ACE grants write access to a user who is a member of the group, the user can have both read and write access to the object.</span></span>

<span data-ttu-id="cd637-114">На следующем рисунке показана связь между этими блоками сведений о безопасности.</span><span class="sxs-lookup"><span data-stu-id="cd637-114">The following illustration shows the relationship between these blocks of security information:</span></span>

![отношения между процессами, записями ACE и списками DACL](images/cssec-02.png)

 

 
