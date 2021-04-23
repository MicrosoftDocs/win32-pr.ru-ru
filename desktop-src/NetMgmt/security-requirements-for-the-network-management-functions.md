---
title: Требования безопасности к функции управления сетью
description: Вызов некоторых функций управления сетью не требует специального членства в группе.
ms.assetid: 846a5b81-d5bf-4275-a898-38e6ba308b8f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b0987509294f03b8737aae5e721abf5dbdd90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533422"
---
# <a name="network-management-function-security-requirements"></a><span data-ttu-id="5bc2d-103">Требования безопасности к функции управления сетью</span><span class="sxs-lookup"><span data-stu-id="5bc2d-103">Network management function security requirements</span></span>

<span data-ttu-id="5bc2d-104">Вызов некоторых функций управления сетью не требует специального членства в группе.</span><span class="sxs-lookup"><span data-stu-id="5bc2d-104">Calling some of the network management functions does not require special group membership.</span></span> <span data-ttu-id="5bc2d-105">Для успешного выполнения других функций требуется, чтобы у пользователей был определен уровень привилегий.</span><span class="sxs-lookup"><span data-stu-id="5bc2d-105">Other functions require that users have a specific privilege level to execute successfully.</span></span> <span data-ttu-id="5bc2d-106">Если применимо, в разделе "Примечания" на странице справки по функции указывается уровень привилегий, необходимых пользователю для выполнения определенной функции.</span><span class="sxs-lookup"><span data-stu-id="5bc2d-106">When applicable, the Remarks section on a function's reference page indicates the privilege level a user must have to execute the particular function.</span></span>

<span data-ttu-id="5bc2d-107">Требования к безопасности, применяемые к Active Directory контроллерам домена, могут отличаться от требований к серверам и рабочим станциям.</span><span class="sxs-lookup"><span data-stu-id="5bc2d-107">Security requirements that apply to Active Directory domain controllers can differ from those that apply to servers and workstations.</span></span>

<span data-ttu-id="5bc2d-108">Дополнительные сведения и список затронутых функций см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="5bc2d-108">For more information, and a list of affected functions, see the following topics:</span></span>

-   [<span data-ttu-id="5bc2d-109">Требования к функциям управления сетью на контроллерах домена Active Directory</span><span class="sxs-lookup"><span data-stu-id="5bc2d-109">Requirements for Network Management functions on Active Directory domain controllers</span></span>](requirements-for-network-management-functions-on-active-directory-domain-controllers.md)
-   [<span data-ttu-id="5bc2d-110">Требования к функциям управления сетью на серверах и рабочих станциях</span><span class="sxs-lookup"><span data-stu-id="5bc2d-110">Requirements for Network Management functions on servers and workstations</span></span>](requirements-for-network-management-functions-on-servers-and-workstations.md)

<span data-ttu-id="5bc2d-111">Дополнительные сведения об управлении доступом к защищаемым объектам см. в разделе [Управление доступом](/windows/desktop/SecAuthZ/access-control), [права](/windows/desktop/SecAuthZ/privileges)доступа и [защищаемые объекты](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="5bc2d-111">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span>

<span data-ttu-id="5bc2d-112">Дополнительные сведения о конкретных дескрипторах безопасности, используемых во время проверок доступа, см. на странице справки по отдельным функциям.</span><span class="sxs-lookup"><span data-stu-id="5bc2d-112">For more information about specific security descriptors that are used during access checks, see the individual function reference page.</span></span> <span data-ttu-id="5bc2d-113">Дополнительные сведения о вызове функций, требующих прав администратора, см. [в разделе Запуск с особыми привилегиями](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="5bc2d-113">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 