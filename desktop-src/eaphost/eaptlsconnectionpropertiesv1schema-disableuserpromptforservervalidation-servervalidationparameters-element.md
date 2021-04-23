---
title: Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс)
description: Сведения об элементе Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс). Указывает, должен ли пользователь запрашивать проверку сервера. | Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс)
ms.assetid: d1c2f334-286b-4aac-b723-806b90fc7b1f
keywords:
- Элемент Дисаблеусерпромптфорсервервалидатион EAPHost
topic_type:
- apiref
api_name:
- DisableUserPromptForServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 368b2593b3c55ef571e3f1892634318e54447643
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273472"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-tls"></a><span data-ttu-id="ba3e1-106">Элемент Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс) (TLS)</span><span class="sxs-lookup"><span data-stu-id="ba3e1-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="ba3e1-107">Элемент **дисаблеусерпромптфорсервервалидатион (сервервалидатионпараметерс)** указывает, следует ли пользователю запрашивать проверку сервера.</span><span class="sxs-lookup"><span data-stu-id="ba3e1-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="ba3e1-108">Если **дисаблеусерпромптфорсервервалидатион** имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность.</span><span class="sxs-lookup"><span data-stu-id="ba3e1-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="ba3e1-109">Если **дисаблеусерпромптфорсервервалидатион** имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).</span><span class="sxs-lookup"><span data-stu-id="ba3e1-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="ba3e1-110">Элемент **дисаблеусерпромптфорсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ba3e1-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="ba3e1-111">Элемент **дисаблеусерпромптфорсервервалидатион** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ba3e1-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3e1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ba3e1-112">Requirements</span></span>



| <span data-ttu-id="ba3e1-113">Роль</span><span class="sxs-lookup"><span data-stu-id="ba3e1-113">Role</span></span> | <span data-ttu-id="ba3e1-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="ba3e1-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="ba3e1-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="ba3e1-115">Client</span></span><br/> | <span data-ttu-id="ba3e1-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba3e1-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ba3e1-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="ba3e1-117">Server</span></span><br/> | <span data-ttu-id="ba3e1-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba3e1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ba3e1-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba3e1-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="ba3e1-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ba3e1-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ba3e1-121">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="ba3e1-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="ba3e1-122">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ba3e1-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ba3e1-123">**Сервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="ba3e1-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="ba3e1-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ba3e1-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ba3e1-125">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="ba3e1-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ba3e1-126">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ba3e1-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ba3e1-127">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ba3e1-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





