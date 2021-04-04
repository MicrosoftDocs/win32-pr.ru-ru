---
title: Сложный тип Сервервалидатионпараметерс (PEAP)
description: Сведения о сложном типе Сервервалидатионпараметерс. Этот тип содержит сведения о выполнении проверки сервера. | Сложный тип Сервервалидатионпараметерс (PEAP)
ms.assetid: 65b3199c-9462-447b-b560-0713348f9130
keywords:
- Сервервалидатионпараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- ServerValidationParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 42416723c4aaa86665f09ee8aa01d5dc1463c522
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000052"
---
# <a name="servervalidationparameters-complex-type-peap"></a><span data-ttu-id="3cf81-106">Сложный тип Сервервалидатионпараметерс (PEAP)</span><span class="sxs-lookup"><span data-stu-id="3cf81-106">ServerValidationParameters complex type (PEAP)</span></span>

<span data-ttu-id="3cf81-107">Сложный тип **сервервалидатионпараметерс** содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="3cf81-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="complextype"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="PerformServerValidation"
        type="boolean"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3cf81-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3cf81-108">Child elements</span></span>



| <span data-ttu-id="3cf81-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="3cf81-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="3cf81-110">Тип</span><span class="sxs-lookup"><span data-stu-id="3cf81-110">Type</span></span>        | <span data-ttu-id="3cf81-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3cf81-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cf81-112">**дисаблеусерпромптфорсервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="3cf81-112">**DisableUserPromptForServerValidation**</span></span>](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="3cf81-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="3cf81-113">boolean</span></span>     | <span data-ttu-id="3cf81-114">Указывает, должен ли пользователь запрашивать проверку сервера.</span><span class="sxs-lookup"><span data-stu-id="3cf81-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="3cf81-115">Если [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение true, PEAP выполняет проверку сервера без ввода данных пользователем. Если проверка завершается неудачно, PEAP не проверяет подлинность.</span><span class="sxs-lookup"><span data-stu-id="3cf81-115">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then PEAP performs the server validation without user input; if the validation fails, PEAP fails the authentication.</span></span><br/> <span data-ttu-id="3cf81-116">Если [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="3cf81-116">If [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certification authority (CA).</span></span><br/> <span data-ttu-id="3cf81-117">Элемент [**дисаблеусерпромптфорсервервалидатион**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3cf81-117">The [**DisableUserPromptForServerValidation**](mspeapconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="3cf81-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="3cf81-118">**ServerNames**</span></span>](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="3cf81-119">complexType</span><span class="sxs-lookup"><span data-stu-id="3cf81-119">complextype</span></span> | <span data-ttu-id="3cf81-120">Представляет список серверов, которым доверяет клиент.</span><span class="sxs-lookup"><span data-stu-id="3cf81-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="3cf81-121">Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="3cf81-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <br/> <span data-ttu-id="3cf81-122">Элемент [**ServerName**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3cf81-122">The [**ServerNames**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="3cf81-123">**трустедрутка**</span><span class="sxs-lookup"><span data-stu-id="3cf81-123">**TrustedRootCA**</span></span>](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="3cf81-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="3cf81-124">hexBinary</span></span>   | <span data-ttu-id="3cf81-125">Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента.</span><span class="sxs-lookup"><span data-stu-id="3cf81-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="3cf81-126">Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.</span><span class="sxs-lookup"><span data-stu-id="3cf81-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="3cf81-127">Элемент [**трустедрутка**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3cf81-127">The [**TrustedRootCA**](mspeapconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="attributes"></a><span data-ttu-id="3cf81-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="3cf81-128">Attributes</span></span>



| <span data-ttu-id="3cf81-129">Имя</span><span class="sxs-lookup"><span data-stu-id="3cf81-129">Name</span></span>                    | <span data-ttu-id="3cf81-130">Тип</span><span class="sxs-lookup"><span data-stu-id="3cf81-130">Type</span></span>    | <span data-ttu-id="3cf81-131">Описание</span><span class="sxs-lookup"><span data-stu-id="3cf81-131">Description</span></span>                                                                                                                                                                                                                  |
|-------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cf81-132">перформсервервалидатион</span><span class="sxs-lookup"><span data-stu-id="3cf81-132">PerformServerValidation</span></span> | <span data-ttu-id="3cf81-133">Логическое</span><span class="sxs-lookup"><span data-stu-id="3cf81-133">boolean</span></span> | <span data-ttu-id="3cf81-134">Windows 7 или более поздней версии: указывает, выполняется ли проверка сервера.</span><span class="sxs-lookup"><span data-stu-id="3cf81-134">Windows 7 or later: Indicates whether server validation is performed.</span></span> <span data-ttu-id="3cf81-135">Элемент [**перформсервервалидатион**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3cf81-135">The [**PerformServerValidation**](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md) element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3cf81-136">Требования</span><span class="sxs-lookup"><span data-stu-id="3cf81-136">Requirements</span></span>



| <span data-ttu-id="3cf81-137">Роль</span><span class="sxs-lookup"><span data-stu-id="3cf81-137">Role</span></span> | <span data-ttu-id="3cf81-138">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="3cf81-138">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="3cf81-139">Клиент</span><span class="sxs-lookup"><span data-stu-id="3cf81-139">Client</span></span><br/> | <span data-ttu-id="3cf81-140">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3cf81-140">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3cf81-141">Сервер</span><span class="sxs-lookup"><span data-stu-id="3cf81-141">Server</span></span><br/> | <span data-ttu-id="3cf81-142">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3cf81-142">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3cf81-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3cf81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cf81-144">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="3cf81-144">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3cf81-145">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3cf81-145">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3cf81-146">Сложные типы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3cf81-146">mspeapconnectionpropertiesv1 Schema Complex Types</span></span>](mspeapconnectionpropertiesv1schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="3cf81-147">**акцептсервернаме**</span><span class="sxs-lookup"><span data-stu-id="3cf81-147">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv1schema-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





