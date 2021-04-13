---
title: Элемент Дисаблеусерпромптфорсервервалидатион (PEAP)
description: Сведения об элементе Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс). Указывает, должен ли пользователь запрашивать проверку сервера. | Элемент Дисаблеусерпромптфорсервервалидатион (PEAP)
ms.assetid: ddb09888-731b-4c67-939e-9f0e6769408b
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
ms.openlocfilehash: 168ce6e371495901f2ed93fb69b605a807bc363c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105647785"
---
# <a name="disableuserpromptforservervalidation-servervalidationparameters-element-peap"></a><span data-ttu-id="3ea12-106">Элемент Дисаблеусерпромптфорсервервалидатион (Сервервалидатионпараметерс) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="3ea12-106">DisableUserPromptForServerValidation (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="3ea12-107">Элемент **дисаблеусерпромптфорсервервалидатион (сервервалидатионпараметерс)** указывает, следует ли пользователю запрашивать проверку сервера.</span><span class="sxs-lookup"><span data-stu-id="3ea12-107">The **DisableUserPromptForServerValidation (ServerValidationParameters)** element indicates whether the user should be asked for server validation.</span></span>

<span data-ttu-id="3ea12-108">Если **дисаблеусерпромптфорсервервалидатион** имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность.</span><span class="sxs-lookup"><span data-stu-id="3ea12-108">If **DisableUserPromptForServerValidation** is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <span data-ttu-id="3ea12-109">Если **дисаблеусерпромптфорсервервалидатион** имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).</span><span class="sxs-lookup"><span data-stu-id="3ea12-109">If **DisableUserPromptForServerValidation** is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span>

<span data-ttu-id="3ea12-110">Элемент **дисаблеусерпромптфорсервервалидатион** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3ea12-110">The **DisableUserPromptForServerValidation** element is optional.</span></span>

``` syntax
<xs:element name="DisableUserPromptForServerValidation"
    type="boolean"
 />
```

<span data-ttu-id="3ea12-111">Элемент **дисаблеусерпромптфорсервервалидатион** определяется сложным типом [**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3ea12-111">The **DisableUserPromptForServerValidation** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ea12-112">Требования</span><span class="sxs-lookup"><span data-stu-id="3ea12-112">Requirements</span></span>



| <span data-ttu-id="3ea12-113">Роль</span><span class="sxs-lookup"><span data-stu-id="3ea12-113">Role</span></span> | <span data-ttu-id="3ea12-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="3ea12-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3ea12-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="3ea12-115">Client</span></span><br/> | <span data-ttu-id="3ea12-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ea12-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ea12-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="3ea12-117">Server</span></span><br/> | <span data-ttu-id="3ea12-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ea12-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3ea12-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ea12-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ea12-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3ea12-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3ea12-121">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="3ea12-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="3ea12-122">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3ea12-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3ea12-123">**Сервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="3ea12-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="3ea12-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3ea12-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3ea12-125">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3ea12-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3ea12-126">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3ea12-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3ea12-127">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3ea12-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





