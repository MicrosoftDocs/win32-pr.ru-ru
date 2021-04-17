---
description: Требования безопасности уровня C2 указывают, что системные администраторы должны иметь возможность аудита событий, связанных с безопасностью, и доступ к этим данным аудита должен быть ограничен полномочными администраторами.
ms.assetid: 411001b1-94cd-465f-8558-c8aa119e4303
title: Создание записей аудита
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d00be8b6d94b29a42436fdabc63be8d2c05789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651134"
---
# <a name="audit-generation"></a><span data-ttu-id="4402d-103">Создание записей аудита</span><span class="sxs-lookup"><span data-stu-id="4402d-103">Audit Generation</span></span>

<span data-ttu-id="4402d-104">Требования безопасности уровня C2 указывают, что системные администраторы должны иметь возможность аудита событий, связанных с безопасностью, и доступ к этим данным аудита должен быть ограничен полномочными администраторами.</span><span class="sxs-lookup"><span data-stu-id="4402d-104">C2-level security requirements specify that system administrators must be able to audit security-related events and that access to this audit data must be limited to authorized administrators.</span></span> <span data-ttu-id="4402d-105">Windows API предоставляет функции, позволяющие администратору отслеживать события, связанные с безопасностью.</span><span class="sxs-lookup"><span data-stu-id="4402d-105">The Windows API provides functions enabling an administrator to monitor security-related events.</span></span>

<span data-ttu-id="4402d-106">Дескриптор безопасности для защищаемого объекта может иметь [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL).</span><span class="sxs-lookup"><span data-stu-id="4402d-106">The security descriptor for a securable object can have a [*system access control list*](/windows/desktop/SecGloss/s-gly) (SACL).</span></span> <span data-ttu-id="4402d-107">Список SACL содержит [*записи управления доступом*](/windows/desktop/SecGloss/a-gly) (ACE), которые указывают типы попыток доступа, создающих отчеты об аудите.</span><span class="sxs-lookup"><span data-stu-id="4402d-107">A SACL contains [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) that specify the types of access attempts that generate audit reports.</span></span> <span data-ttu-id="4402d-108">Каждый элемент ACE определяет доверенное лицо, набор прав доступа и набор флагов, указывающих, создает ли система сообщения аудита для неудачных попыток доступа, успешных попыток доступа или и того, и другого.</span><span class="sxs-lookup"><span data-stu-id="4402d-108">Each ACE identifies a trustee, a set of access rights, and a set of flags that indicate whether the system generates audit messages for failed access attempts, successful access attempts, or both.</span></span>

<span data-ttu-id="4402d-109">Система записывает сообщения аудита в журнал событий безопасности.</span><span class="sxs-lookup"><span data-stu-id="4402d-109">The system writes audit messages to the security event log.</span></span> <span data-ttu-id="4402d-110">Дополнительные сведения о доступе к записям в журнале событий безопасности см. в разделе [ведение журнала регистрации событий](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="4402d-110">For information about accessing the records in a security event log, see [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

<span data-ttu-id="4402d-111">Для чтения или записи списка SACL объекта поток должен сначала включить \_ право доступа к имени безопасности SE \_ .</span><span class="sxs-lookup"><span data-stu-id="4402d-111">To read or write an object's SACL, a thread must first enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="4402d-112">Дополнительные сведения см. в статье [право доступа к SACL](sacl-access-right.md).</span><span class="sxs-lookup"><span data-stu-id="4402d-112">For more information, see [SACL Access Right](sacl-access-right.md).</span></span>

<span data-ttu-id="4402d-113">API Windows также обеспечивает поддержку серверных приложений для создания сообщений аудита, когда клиент пытается получить доступ к закрытому объекту.</span><span class="sxs-lookup"><span data-stu-id="4402d-113">The Windows API also provides support for server applications to generate audit messages when a client tries to access a private object.</span></span> <span data-ttu-id="4402d-114">Дополнительные сведения см. [в разделе Аудит доступа к частным объектам](auditing-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4402d-114">For more information, see [Auditing Access To Private Objects](auditing-access-to-private-objects.md).</span></span>

 

 
