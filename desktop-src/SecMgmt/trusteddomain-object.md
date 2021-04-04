---
description: Объект Трустеддомаин хранит сведения о доверительных отношениях с доменом.
ms.assetid: fab69367-2143-49ef-a1b9-9c1d846fd4e1
title: Объект Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 837d8a9e56273a87b22b9697ef4e5917d73bcc81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897065"
---
# <a name="trusteddomain-object"></a><span data-ttu-id="4a4fc-103">Объект Трустеддомаин</span><span class="sxs-lookup"><span data-stu-id="4a4fc-103">TrustedDomain Object</span></span>

<span data-ttu-id="4a4fc-104">Объект **трустеддомаин** хранит сведения о доверительных отношениях с доменом.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-104">The **TrustedDomain** object stores information about a trust relationship with a domain.</span></span> <span data-ttu-id="4a4fc-105">Объект **трустеддомаин** создается в доверяющей системе для идентификации учетной записи в доверенном домене, которая может использоваться для отправки запросов проверки подлинности, а также для выполнения других операций, таких как переводы имен и [*идентификаторов безопасности*](/windows/desktop/SecGloss/s-gly) (SID).</span><span class="sxs-lookup"><span data-stu-id="4a4fc-105">A **TrustedDomain** object is created on the trusting system to identify an account within the trusted domain that can be used to submit authentication requests and to perform other operations, such as name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) translations.</span></span>

<span data-ttu-id="4a4fc-106">Данные, хранящиеся в объекте **трустеддомаин** , включают:</span><span class="sxs-lookup"><span data-stu-id="4a4fc-106">The information stored in a **TrustedDomain** object includes:</span></span>

-   <span data-ttu-id="4a4fc-107">Идентификатор безопасности доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-107">The SID of the trusted domain.</span></span> <span data-ttu-id="4a4fc-108">Эти сведения не доявляются изменяемыми и должны быть уникальными для всех объектов **трустеддомаин** .</span><span class="sxs-lookup"><span data-stu-id="4a4fc-108">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="4a4fc-109">Имя доверенного домена.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-109">The name of the trusted domain.</span></span> <span data-ttu-id="4a4fc-110">Эти сведения не доявляются изменяемыми и должны быть уникальными для всех объектов **трустеддомаин** .</span><span class="sxs-lookup"><span data-stu-id="4a4fc-110">This information is not modifiable and must be unique among all **TrustedDomain** objects.</span></span>
-   <span data-ttu-id="4a4fc-111">Имя учетной записи в доверенном домене, используемой для отправки запросов проверки подлинности, а также для выполнения переводов имен и идентификаторов безопасности.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-111">The name of the account in the trusted domain used to submit authentication requests and to perform name and SID translations.</span></span> <span data-ttu-id="4a4fc-112">Это имя нельзя изменять.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-112">This name is not modifiable.</span></span>
-   <span data-ttu-id="4a4fc-113">Пароль, используемый для отправки запросов проверки подлинности и выполнения переводов имени и SID.</span><span class="sxs-lookup"><span data-stu-id="4a4fc-113">The password used to submit authentication requests and perform name and SID translations.</span></span>

<span data-ttu-id="4a4fc-114">Дополнительные сведения см. в описании [типа объекта трустеддомаин](the-trusteddomain-object-type.md).</span><span class="sxs-lookup"><span data-stu-id="4a4fc-114">For more information, see [The TrustedDomain Object Type](the-trusteddomain-object-type.md).</span></span>

 

 
