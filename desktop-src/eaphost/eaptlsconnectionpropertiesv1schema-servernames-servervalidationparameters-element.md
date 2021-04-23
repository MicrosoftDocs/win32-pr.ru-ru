---
title: Элемент ServerName (Сервервалидатионпараметерс) (TLS)
description: Сведения об элементе ServerName (Сервервалидатионпараметерс). Этот элемент представляет список имен серверов, разделенных точкой с запятой. | Элемент ServerName (Сервервалидатионпараметерс) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- ServerName, элемент EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694062"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="26b77-106">Элемент ServerName (Сервервалидатионпараметерс) (TLS)</span><span class="sxs-lookup"><span data-stu-id="26b77-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="26b77-107">Элемент **ServerName (сервервалидатионпараметерс)** представляет список имен серверов, разделенных точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="26b77-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="26b77-108">Элемент **ServerName** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="26b77-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="26b77-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="26b77-109">Remarks</span></span>

<span data-ttu-id="26b77-110">Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="26b77-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="26b77-111">Элемент **ServerName** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="26b77-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="26b77-112">Требования</span><span class="sxs-lookup"><span data-stu-id="26b77-112">Requirements</span></span>



| <span data-ttu-id="26b77-113">Роль</span><span class="sxs-lookup"><span data-stu-id="26b77-113">Role</span></span> | <span data-ttu-id="26b77-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="26b77-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="26b77-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="26b77-115">Client</span></span><br/> | <span data-ttu-id="26b77-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="26b77-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="26b77-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="26b77-117">Server</span></span><br/> | <span data-ttu-id="26b77-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="26b77-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="26b77-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="26b77-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="26b77-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="26b77-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="26b77-121">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="26b77-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="26b77-122">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="26b77-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="26b77-123">**Сервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="26b77-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="26b77-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="26b77-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="26b77-125">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="26b77-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="26b77-126">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="26b77-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="26b77-127">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="26b77-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





