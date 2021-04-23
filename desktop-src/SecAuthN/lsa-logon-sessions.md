---
description: Сеанс входа в систему — это вычислительный сеанс, который начинается после успешного выполнения проверки подлинности пользователя и заканчивается при выходе пользователя из системы.
ms.assetid: 14f0f9e7-90ba-47d7-a8d5-06f9d2f1a7a1
title: Сеансы входа LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32a4912218b68c25c5c23334f7b34ef875fa318
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265808"
---
# <a name="lsa-logon-sessions"></a><span data-ttu-id="083d1-103">Сеансы входа LSA</span><span class="sxs-lookup"><span data-stu-id="083d1-103">LSA Logon Sessions</span></span>

<span data-ttu-id="083d1-104">[*Сеанс входа*](../secgloss/l-gly.md) в систему — это вычислительный сеанс, который начинается после успешного выполнения проверки подлинности пользователя и заканчивается при выходе пользователя из системы.</span><span class="sxs-lookup"><span data-stu-id="083d1-104">A [*logon session*](../secgloss/l-gly.md) is a computing session that begins when a user authentication is successful and ends when the user logs off of the system.</span></span>

<span data-ttu-id="083d1-105">При успешной проверке подлинности пользователя пакет проверки подлинности создает сеанс входа в систему и возвращает сведения в [*локальный центр безопасности*](../secgloss/l-gly.md) (LSA), который используется для создания [*маркера*](../secgloss/t-gly.md) для нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="083d1-105">When a user is successfully authenticated, the authentication package creates a logon session and returns information to the [*Local Security Authority*](../secgloss/l-gly.md) (LSA) that is used to create a [*token*](../secgloss/t-gly.md) for the new user.</span></span> <span data-ttu-id="083d1-106">Этот маркер включает, помимо прочего, [*локально уникальный идентификатор*](../secgloss/l-gly.md) (LUID) для сеанса входа в систему, который называется [*идентификатором входа*](../secgloss/l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="083d1-106">This token includes, among other things, a [*locally unique identifier*](../secgloss/l-gly.md) (LUID) for the logon session, called the [*logon Id*](../secgloss/l-gly.md).</span></span>

<span data-ttu-id="083d1-107">При создании маркера [*счетчик ссылок*](../secgloss/r-gly.md) для сеанса входа увеличивается.</span><span class="sxs-lookup"><span data-stu-id="083d1-107">When a token is created, the [*reference count*](../secgloss/r-gly.md) for the logon session is incremented.</span></span> <span data-ttu-id="083d1-108">Счетчик ссылок также увеличивается каждый раз, когда создаются копии маркера для создания, олицетворения или других применений процесса.</span><span class="sxs-lookup"><span data-stu-id="083d1-108">The reference count is also incremented whenever copies of the token are created for process creation, impersonation, or other uses.</span></span> <span data-ttu-id="083d1-109">По мере того, как используются токены, и копии маркера удаляются, счетчик ссылок для сеанса входа уменьшается.</span><span class="sxs-lookup"><span data-stu-id="083d1-109">As token uses are completed and copies of the token are deleted, the reference count for the logon session is decremented.</span></span> <span data-ttu-id="083d1-110">Когда счетчик ссылок достигнет нуля, сеанс входа будет удален.</span><span class="sxs-lookup"><span data-stu-id="083d1-110">When the reference count reaches zero, the logon session is deleted.</span></span>

> [!Note]  
> <span data-ttu-id="083d1-111">Если проверка подлинности не прошла успешно, [*пакету проверки подлинности*](../secgloss/a-gly.md) не следует создавать сеанс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="083d1-111">If authentication is not successful, the [*authentication package*](../secgloss/a-gly.md) should not create a logon session.</span></span> <span data-ttu-id="083d1-112">Если пакет проверки подлинности должен создать сеанс входа в систему до окончательного определения действительности пользователя, а в случае сбоя проверки подлинности, пакет проверки подлинности должен удалить сеанс.</span><span class="sxs-lookup"><span data-stu-id="083d1-112">If the authentication package must create a logon session before making a final determination about the validity of the user, and if authentication fails, the authentication package must delete the session.</span></span>

 

 

 
