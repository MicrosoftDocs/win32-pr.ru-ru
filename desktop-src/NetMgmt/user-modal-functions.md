---
title: Пользовательские модальные функции
description: Модальные функции пользователя управления сетью получают и устанавливают параметры на уровне системы, связанные с поведением системы безопасности.
ms.assetid: e655b9f6-2808-4bd4-998c-c8a2e980920b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65595f78a412196b9fd54030ec1ac1f1fb8ae59
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987817"
---
# <a name="user-modal-functions"></a><span data-ttu-id="efa07-103">Пользовательские модальные функции</span><span class="sxs-lookup"><span data-stu-id="efa07-103">User Modal Functions</span></span>

<span data-ttu-id="efa07-104">Модальные функции пользователя управления сетью получают и устанавливают параметры на уровне системы, связанные с поведением системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="efa07-104">The network management user modal functions get and set system-wide parameters related to security system behavior.</span></span>

<span data-ttu-id="efa07-105">Модальные пользовательские функции перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="efa07-105">The user modal functions are listed following.</span></span>



| <span data-ttu-id="efa07-106">Функция</span><span class="sxs-lookup"><span data-stu-id="efa07-106">Function</span></span>                                     | <span data-ttu-id="efa07-107">Описание</span><span class="sxs-lookup"><span data-stu-id="efa07-107">Description</span></span>                                                                                                                                                                                             |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="efa07-108">**нетусермодалсжет**</span><span class="sxs-lookup"><span data-stu-id="efa07-108">**NetUserModalsGet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget) | <span data-ttu-id="efa07-109">Возвращает глобальные сведения для всех пользователей и глобальных групп в базе данных безопасности, которая является базой данных диспетчера учетных записей безопасности (SAM) или, в случае контроллеров домена, Active Directory.</span><span class="sxs-lookup"><span data-stu-id="efa07-109">Returns global information for all users and global groups in the security database, which is the security accounts manager (SAM) database or, in the case of domain controllers, the Active Directory.</span></span> |
| [<span data-ttu-id="efa07-110">**нетусермодалссет**</span><span class="sxs-lookup"><span data-stu-id="efa07-110">**NetUserModalsSet**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) | <span data-ttu-id="efa07-111">Задает глобальные сведения для всех пользователей и глобальных групп в базе данных безопасности.</span><span class="sxs-lookup"><span data-stu-id="efa07-111">Sets global information for all users and global groups in the security database.</span></span>                                                                                                                       |



 

<span data-ttu-id="efa07-112">Функции **нетусермодалсжет** и **нетусермодалссет** проверяют и изменяют модальные параметры, которые являются глобальными параметрами, влияющими на каждую учетную запись в базе данных безопасности (например, минимально допустимую длину пароля).</span><span class="sxs-lookup"><span data-stu-id="efa07-112">The **NetUserModalsGet** and **NetUserModalsSet** functions examine and modify the modal settings, which are global parameters that affect every account in the security database (for example, the minimum allowable password length).</span></span> <span data-ttu-id="efa07-113">Все модальные параметры можно изменить путем вызова **нетусермодалссет**.</span><span class="sxs-lookup"><span data-stu-id="efa07-113">All modal settings can be altered by calling **NetUserModalsSet**.</span></span> <span data-ttu-id="efa07-114">Большинство модальных элементов также можно изменить с помощью команды **net accounts** .</span><span class="sxs-lookup"><span data-stu-id="efa07-114">Most of the modals can also be altered by using the **net accounts** command.</span></span> <span data-ttu-id="efa07-115">Для модальных функций пользователя управления сетью не требуется, чтобы сервер имел безопасность на уровне пользователя.</span><span class="sxs-lookup"><span data-stu-id="efa07-115">The network management user modal functions do not require the server to have user-level security.</span></span>

<span data-ttu-id="efa07-116">Модальные данные пользователя доступны на следующих уровнях:</span><span class="sxs-lookup"><span data-stu-id="efa07-116">User modal information is available at the following levels:</span></span>

-   [<span data-ttu-id="efa07-117">**\_Сведения о модальных пользователях \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="efa07-117">**USER\_MODALS\_INFO\_0**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_0)
-   [<span data-ttu-id="efa07-118">**\_Сведения о модальных пользователях \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="efa07-118">**USER\_MODALS\_INFO\_1**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1)
-   [<span data-ttu-id="efa07-119">**\_Сведения о модальных пользователях \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="efa07-119">**USER\_MODALS\_INFO\_2**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_2)
-   [<span data-ttu-id="efa07-120">**\_Сведения о модальных пользователях \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="efa07-120">**USER\_MODALS\_INFO\_3**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_3)

<span data-ttu-id="efa07-121">Следующие уровни информации допустимы только для [**нетусермодалссет**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) и замены старого способа передачи в *пармнум* для задания определенного поля:</span><span class="sxs-lookup"><span data-stu-id="efa07-121">The following information levels are valid only for [**NetUserModalsSet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsset) and replace the older way of passing in a *Parmnum* to set a specific field:</span></span>

-   [<span data-ttu-id="efa07-122">**\_Сведения о модальных пользователях \_ \_ 1001**</span><span class="sxs-lookup"><span data-stu-id="efa07-122">**USER\_MODALS\_INFO\_1001**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1001)
-   [<span data-ttu-id="efa07-123">**\_Сведения о модальных пользователях \_ \_ 1002**</span><span class="sxs-lookup"><span data-stu-id="efa07-123">**USER\_MODALS\_INFO\_1002**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1002)
-   [<span data-ttu-id="efa07-124">**\_Сведения о модальных пользователях \_ \_ 1003**</span><span class="sxs-lookup"><span data-stu-id="efa07-124">**USER\_MODALS\_INFO\_1003**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1003)
-   [<span data-ttu-id="efa07-125">**\_Сведения о модальных пользователях \_ \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="efa07-125">**USER\_MODALS\_INFO\_1004**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1004)
-   [<span data-ttu-id="efa07-126">**\_Сведения о модальных пользователях \_ \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="efa07-126">**USER\_MODALS\_INFO\_1005**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1005)
-   [<span data-ttu-id="efa07-127">**\_Сведения о модальных пользователях \_ \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="efa07-127">**USER\_MODALS\_INFO\_1006**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1006)
-   [<span data-ttu-id="efa07-128">**\_Сведения о модальных пользователях \_ \_ 1007**</span><span class="sxs-lookup"><span data-stu-id="efa07-128">**USER\_MODALS\_INFO\_1007**</span></span>](/windows/desktop/api/Lmaccess/ns-lmaccess-user_modals_info_1007)

<span data-ttu-id="efa07-129">При программировании для Active Directory можно вызвать определенные методы интерфейса Active Directory (ADSI) для достижения тех же функций, которые можно достичь, вызвав модальные функции пользователя управления сетью.</span><span class="sxs-lookup"><span data-stu-id="efa07-129">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management user modal functions.</span></span> <span data-ttu-id="efa07-130">Дополнительные сведения см. в разделе [**иадсдомаин**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span><span class="sxs-lookup"><span data-stu-id="efa07-130">For more information, see [**IADsDomain**](/windows/desktop/api/iads/nn-iads-iadsdomain).</span></span>

 

 