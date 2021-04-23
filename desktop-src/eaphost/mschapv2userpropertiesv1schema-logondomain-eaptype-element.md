---
title: LogonDomain (Еаптипе), элемент
description: Сведения об элементе LogonDomain (Еаптипе). Этот элемент определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Элемент LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070608"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="09a36-105">LogonDomain (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="09a36-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="09a36-106">Элемент **LogonDomain (еаптипе)** определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="09a36-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="09a36-107">Элемент **LogonDomain** определяется элементом [**еаптипе**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="09a36-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="09a36-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="09a36-108">Remarks</span></span>

<span data-ttu-id="09a36-109">Если элемент **LogonDomain (еаптипе)** отсутствует, используется домен из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="09a36-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="09a36-110">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="09a36-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a36-111">Требования</span><span class="sxs-lookup"><span data-stu-id="09a36-111">Requirements</span></span>



| <span data-ttu-id="09a36-112">Роль</span><span class="sxs-lookup"><span data-stu-id="09a36-112">Role</span></span> | <span data-ttu-id="09a36-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="09a36-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="09a36-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="09a36-114">Client</span></span><br/> | <span data-ttu-id="09a36-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09a36-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09a36-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="09a36-116">Server</span></span><br/> | <span data-ttu-id="09a36-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09a36-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09a36-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09a36-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="09a36-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="09a36-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="09a36-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="09a36-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="09a36-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="09a36-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="09a36-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="09a36-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="09a36-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="09a36-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="09a36-124">Схема mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="09a36-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





