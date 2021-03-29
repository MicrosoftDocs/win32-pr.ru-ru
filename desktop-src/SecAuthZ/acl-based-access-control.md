---
description: Точно так же, как система использует дескрипторы безопасности для управления доступом к защищаемым объектам, сервер может использовать дескрипторы безопасности для управления доступом к своим частным объектам. Дополнительные сведения о модели безопасности Windows см. в разделе модель контроля доступа.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Управление доступом на основе ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813288"
---
# <a name="acl-based-access-control"></a><span data-ttu-id="1e3b3-104">Управление доступом на основе ACL</span><span class="sxs-lookup"><span data-stu-id="1e3b3-104">ACL-based Access Control</span></span>

<span data-ttu-id="1e3b3-105">Точно так же, как система использует [дескрипторы безопасности](security-descriptors.md) для управления доступом к защищаемым объектам, сервер может использовать дескрипторы безопасности для управления доступом к своим частным объектам.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-105">Just as the system uses [security descriptors](security-descriptors.md) to control access to securable objects, a server can use security descriptors to control access to its private objects.</span></span> <span data-ttu-id="1e3b3-106">Дополнительные сведения о модели безопасности Windows см. в разделе [модель контроля доступа](access-control-model.md).</span><span class="sxs-lookup"><span data-stu-id="1e3b3-106">For more information about the Windows security model, see [Access Control Model](access-control-model.md).</span></span>

<span data-ttu-id="1e3b3-107">Защищенный сервер может [создать дескриптор безопасности](security-descriptors-for-private-objects.md) с DACL, который указывает типы доступа, разрешенные для различных [доверенных лиц](trustees.md).</span><span class="sxs-lookup"><span data-stu-id="1e3b3-107">A protected server can [create a security descriptor](security-descriptors-for-private-objects.md) with a DACL that specifies the types of access allowed for various [trustees](trustees.md).</span></span> <span data-ttu-id="1e3b3-108">В простом случае сервер может создать один дескриптор безопасности для [управления доступом ко всем данным и функциональным возможностям сервера](checking-access-to-private-objects.md).</span><span class="sxs-lookup"><span data-stu-id="1e3b3-108">In a simple case, the server could create a single security descriptor to [control access to all of the server's data and functionality](checking-access-to-private-objects.md).</span></span> <span data-ttu-id="1e3b3-109">Для более точной гранулярности защиты сервер может создать дескрипторы безопасности для каждого из его частных объектов или для различных типов функциональности.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-109">For a finer granularity of protection, the server could create security descriptors for each of its private objects, or for different types of functionality.</span></span>

<span data-ttu-id="1e3b3-110">Например, когда клиент запрашивает у сервера создание нового объекта в базе данных, сервер может создать дескриптор безопасности для нового закрытого объекта.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-110">For example, when a client asks the server to create a new object in a database, the server could create a security descriptor for the new private object.</span></span> <span data-ttu-id="1e3b3-111">Затем сервер может сохранить дескриптор безопасности с закрытым объектом в базе данных.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-111">The server could then store the security descriptor with the private object in the database.</span></span> <span data-ttu-id="1e3b3-112">Когда клиент пытается получить доступ к объекту, сервер получает дескриптор безопасности для проверки прав доступа клиента.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-112">When a client tries to access the object, the server retrieves the security descriptor to check the client's access rights.</span></span> <span data-ttu-id="1e3b3-113">Важно отметить, что в дескрипторе безопасности нет ничего, который связывает его с объектом или функциональной функциональностью, которую он защищает.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-113">It is important to note that there is nothing in a security descriptor that associates it with the object or functionality it is protecting.</span></span> <span data-ttu-id="1e3b3-114">Вместо этого он должен поддерживать связь с защищенным сервером.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-114">Instead, it is up to the protected server to maintain the association.</span></span>

<span data-ttu-id="1e3b3-115">Доступ к закрытому объекту также можно проследить.</span><span class="sxs-lookup"><span data-stu-id="1e3b3-115">Access to the private object can also be audited.</span></span> <span data-ttu-id="1e3b3-116">Описание этого см. в разделе [Аудит доступа к частным объектам](auditing-access-to-private-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="1e3b3-116">Refer to [Auditing Access to Private Objects](auditing-access-to-private-objects.md) for a description of this.</span></span>

 

 



