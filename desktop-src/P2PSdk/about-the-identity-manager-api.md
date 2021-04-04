---
description: API однорангового диспетчера удостоверений позволяет создавать и перечислять одноранговые удостоверения в одноранговых приложениях, а также управлять ими.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: О программе Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909792"
---
# <a name="about-identity-manager"></a><span data-ttu-id="dd2f1-103">О программе Identity Manager</span><span class="sxs-lookup"><span data-stu-id="dd2f1-103">About Identity Manager</span></span>

<span data-ttu-id="dd2f1-104">API однорангового диспетчера удостоверений позволяет создавать и перечислять одноранговые удостоверения в одноранговых приложениях, а также управлять ими.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-104">The Peer Identity Manager API allows you to create, enumerate, and manipulate peer identities in a peer application.</span></span> <span data-ttu-id="dd2f1-105">Вы можете использовать удостоверения одноранговых узлов, созданные с помощью этого API, в качестве входных данных для API поставщика пространства имен однорангового группирования и PNRP (Peer Name Resolution Protocol).</span><span class="sxs-lookup"><span data-stu-id="dd2f1-105">You can use the peer identities created using this API as input for the Peer Grouping and Peer Name Resolution Protocol (PNRP) Namespace Provider APIs.</span></span>

## <a name="peer-identity-manager-best-practices"></a><span data-ttu-id="dd2f1-106">Рекомендации для диспетчера одноранговых удостоверений</span><span class="sxs-lookup"><span data-stu-id="dd2f1-106">Peer Identity Manager Best Practices</span></span>

<span data-ttu-id="dd2f1-107">Каждый пользователь должен иметь несколько одноранговых удостоверений, которые могут использоваться для одноранговых действий.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-107">Each user should have a few peer identities that they can use for the peer activities.</span></span> <span data-ttu-id="dd2f1-108">Например, у пользователя может быть два одноранговых удостоверения для работы и свободного использования.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-108">For example, a user might have two peer identities for work and leisure.</span></span>

<span data-ttu-id="dd2f1-109">Хорошо спроектированное одноранговое приложение позволяет пользователю выбрать одноранговый идентификатор для использования.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-109">A well-designed peer application allows a user to select a peer identity to use.</span></span> <span data-ttu-id="dd2f1-110">Пользователь может создать удостоверение однорангового узла, если ни одно из существующих одноранговых идентификаторов не подходит для использования с приложением.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-110">A user can create a new peer identity if none of the existing peer identities are appropriate to use with an application.</span></span>

<span data-ttu-id="dd2f1-111">Хорошо спроектированное однорангическое приложение также управляет количеством создаваемых удостоверений.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-111">A well-designed peer application also controls the number of identities that it creates.</span></span> <span data-ttu-id="dd2f1-112">Если приложение создает временный одноранговый узел, приложение должно удалить удостоверение однорангового узла, если удостоверение не требуется.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-112">If an application creates a temporary peer identity, the application must delete the peer identity when the identity is not needed.</span></span> <span data-ttu-id="dd2f1-113">Если приложение не выполняет это обслуживание, диспетчер одноранговых удостоверений может не иметь возможности создавать одноранговые удостоверения, пока не будут удалены некоторые идентификаторы одноранговых узлов.</span><span class="sxs-lookup"><span data-stu-id="dd2f1-113">If an application does not perform this maintenance, the Peer Identity Manager may not be able to create peer identities until some peer identities are removed.</span></span>

 

 



