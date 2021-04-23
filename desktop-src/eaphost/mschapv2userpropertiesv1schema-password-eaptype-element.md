---
title: Password (Еаптипе), элемент
description: Сведения об элементе Password (Еаптипе). Этот элемент определяет пароль пользователя или компьютера, для которого выполняется проверка подлинности.
ms.assetid: d3ad95b8-2d98-420f-a680-a83b49ae2992
keywords:
- Элемент Password EAPHost
topic_type:
- apiref
api_name:
- Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6da29146be7ed2f0c17d7311f79921b44cd0929e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070638"
---
# <a name="password-eaptype-element"></a><span data-ttu-id="70925-105">Password (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="70925-105">Password (EapType) Element</span></span>

<span data-ttu-id="70925-106">Элемент **Password (еаптипе)** определяет пароль пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="70925-106">The **Password (EapType)** element identifies the password of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="Password"
    type="string"
 />
```

<span data-ttu-id="70925-107">Элемент **Password** определяется элементом [**еаптипе**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="70925-107">The **Password** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="70925-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="70925-108">Remarks</span></span>

<span data-ttu-id="70925-109">Если элемент **Password (еаптипе)** отсутствует, то хэш пароля будет получен из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="70925-109">If the **Password (EapType)** element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="70925-110">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="70925-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="70925-111">Требования</span><span class="sxs-lookup"><span data-stu-id="70925-111">Requirements</span></span>



| <span data-ttu-id="70925-112">Роль</span><span class="sxs-lookup"><span data-stu-id="70925-112">Role</span></span> | <span data-ttu-id="70925-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="70925-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="70925-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="70925-114">Client</span></span><br/> | <span data-ttu-id="70925-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="70925-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70925-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="70925-116">Server</span></span><br/> | <span data-ttu-id="70925-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70925-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70925-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70925-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="70925-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="70925-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="70925-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="70925-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="70925-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="70925-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="70925-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="70925-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="70925-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="70925-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="70925-124">Схема mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="70925-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





