---
description: Фильтры паролей
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: Фильтры паролей
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272442"
---
# <a name="password-filters"></a><span data-ttu-id="7fb6f-103">Фильтры паролей</span><span class="sxs-lookup"><span data-stu-id="7fb6f-103">Password Filters</span></span>

<span data-ttu-id="7fb6f-104">Фильтры паролей позволяют реализовать политику паролей и уведомления об изменениях.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-104">Password filters provide a way for you to implement password policy and change notification.</span></span>

<span data-ttu-id="7fb6f-105">Когда выполняется запрос на изменение пароля, [*локальный администратор безопасности*](/windows/desktop/SecGloss/l-gly) вызывает фильтры паролей, зарегистрированные в системе.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-105">When a password change request is made, the [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) calls the password filters registered on the system.</span></span> <span data-ttu-id="7fb6f-106">Каждый фильтр паролей вызывается дважды: сначала проверяется новый пароль, а затем, после того, как все фильтры проверяют новый пароль, чтобы уведомить о внесенных изменениях.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-106">Each password filter is called twice: first to validate the new password and then, after all filters have validated the new password, to notify the filters that the change has been made.</span></span> <span data-ttu-id="7fb6f-107">Данный процесс показан на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-107">The following illustration shows this process.</span></span>

![запрос на смену пароля](images/pswdfilte.png)

<span data-ttu-id="7fb6f-109">Уведомление о смене пароля используется для синхронизации изменений паролей с базами данных внешней учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-109">Password change notification is used to synchronize password changes to foreign account databases.</span></span>

<span data-ttu-id="7fb6f-110">Фильтры паролей используются для принудительного применения политики паролей.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-110">Password filters are used to enforce password policy.</span></span> <span data-ttu-id="7fb6f-111">Фильтры проверяют новые пароли и указывают, соответствует ли новый пароль реализованной политике паролей.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-111">Filters validate new passwords and indicate whether the new password conforms to the implemented password policy.</span></span>

<span data-ttu-id="7fb6f-112">Общие сведения об использовании фильтров паролей см. в разделе [Использование фильтров паролей](using-password-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7fb6f-112">For an overview of using password filters, see [Using Password Filters](using-password-filters.md).</span></span>

<span data-ttu-id="7fb6f-113">Список функций фильтрации паролей см. в разделе [функции фильтрации паролей](management-functions.md).</span><span class="sxs-lookup"><span data-stu-id="7fb6f-113">For a list of password filter functions, see [Password Filter Functions](management-functions.md).</span></span>

<span data-ttu-id="7fb6f-114">Следующие разделы содержат дополнительные сведения о фильтрах паролей.</span><span class="sxs-lookup"><span data-stu-id="7fb6f-114">The following topics provide more information about password filters:</span></span>

-   [<span data-ttu-id="7fb6f-115">Рекомендации по программированию фильтрации паролей</span><span class="sxs-lookup"><span data-stu-id="7fb6f-115">Password Filter Programming Considerations</span></span>](password-filter-programming-considerations.md)
-   [<span data-ttu-id="7fb6f-116">Принудительное применение надежных паролей и Passfilt.dll</span><span class="sxs-lookup"><span data-stu-id="7fb6f-116">Strong Password Enforcement and Passfilt.dll</span></span>](strong-password-enforcement-and-passfilt-dll.md)

 

 
