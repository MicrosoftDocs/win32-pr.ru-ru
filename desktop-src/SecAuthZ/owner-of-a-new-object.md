---
description: Владелец объектов неявным образом записывает \_ доступ DAC к объекту. Это означает, что владелец может изменять список управления доступом на уровне объектов (DACL) и, таким образом, может управлять доступом к объекту.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Владелец нового объекта
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663825"
---
# <a name="owner-of-a-new-object"></a><span data-ttu-id="8f706-104">Владелец нового объекта</span><span class="sxs-lookup"><span data-stu-id="8f706-104">Owner of a New Object</span></span>

<span data-ttu-id="8f706-105">Владелец объекта неявно имеет \_ доступ к объекту уровня данных для записи.</span><span class="sxs-lookup"><span data-stu-id="8f706-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="8f706-106">Это означает, что владелец может изменить [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) объекта и, таким образом, может управлять доступом к объекту.</span><span class="sxs-lookup"><span data-stu-id="8f706-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="8f706-107">Владелец нового объекта является [*идентификатором безопасности*](/windows/desktop/SecGloss/s-gly) (SID) по умолчанию, [*исходя из основного*](/windows/desktop/SecGloss/p-gly) [*маркера или токена олицетворения*](/windows/desktop/SecGloss/i-gly) создаваемого [*процесса*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="8f706-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="8f706-108">Чтобы получить или задать владельца по умолчанию в [*маркере доступа*](/windows/desktop/SecGloss/a-gly), вызовите функцию [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) или [**Сеттокенинформатион**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) с помощью структуры [**\_ владельца маркера**](/windows/desktop/api/Winnt/ns-winnt-token_owner) .</span><span class="sxs-lookup"><span data-stu-id="8f706-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="8f706-109">Система не позволяет задать для владельца маркера по умолчанию недопустимый идентификатор безопасности, например идентификатор безопасности учетной записи другого пользователя.</span><span class="sxs-lookup"><span data-stu-id="8f706-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="8f706-110">Процесс с \_ \_ включенным привилегией на владение SE может быть задан владельцем объекта.</span><span class="sxs-lookup"><span data-stu-id="8f706-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="8f706-111">Процесс, имеющий \_ разрешение SE Restore \_ Name или с \_ доступом владельца записи к объекту, может задать любой допустимый идентификатор безопасности пользователя или группы в качестве владельца объекта.</span><span class="sxs-lookup"><span data-stu-id="8f706-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
