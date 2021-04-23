---
title: Элемент username (TLS)
description: Сведения об элементе username. Этот элемент захватывает имя пользователя, которое будет отправлено в ответе EAP-Identity.
ms.assetid: dda4a7dd-36ba-418d-9b26-2818ef20854d
keywords:
- Элемент username, EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2975b425bc760979b33d83182d94469532944e46
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700933"
---
# <a name="username-element-tls"></a><span data-ttu-id="701a8-105">Элемент username (TLS)</span><span class="sxs-lookup"><span data-stu-id="701a8-105">Username element (TLS)</span></span>

<span data-ttu-id="701a8-106">Элемент **username** захватывает имя пользователя, которое будет отправлено в ответе EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="701a8-106">The **Username** element captures the user name to be sent in the EAP-Identity response.</span></span>

<span data-ttu-id="701a8-107">Если элемент **username** отсутствует, то EAP-TLS использует имя в сертификате, на который ссылается элемент [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="701a8-107">If the **Username** element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span>

``` syntax
<xs:element name="Username"
    substitutionGroup="Identity"
 />
```

## <a name="requirements"></a><span data-ttu-id="701a8-108">Требования</span><span class="sxs-lookup"><span data-stu-id="701a8-108">Requirements</span></span>



| <span data-ttu-id="701a8-109">Роль</span><span class="sxs-lookup"><span data-stu-id="701a8-109">Role</span></span> | <span data-ttu-id="701a8-110">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="701a8-110">Minimum supported OS versions</span></span> |
|------|-------------------------------|
| <span data-ttu-id="701a8-111">Клиент</span><span class="sxs-lookup"><span data-stu-id="701a8-111">Client</span></span><br/> | <span data-ttu-id="701a8-112">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="701a8-112">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="701a8-113">Сервер</span><span class="sxs-lookup"><span data-stu-id="701a8-113">Server</span></span><br/> | <span data-ttu-id="701a8-114">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="701a8-114">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="701a8-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="701a8-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701a8-116">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="701a8-116">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="701a8-117">Схема eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="701a8-117">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





