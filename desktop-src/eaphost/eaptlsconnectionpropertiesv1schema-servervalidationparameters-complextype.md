---
title: Сложный тип Сервервалидатионпараметерс (TLS)
description: Сведения о сложном типе Сервервалидатионпараметерс. Этот тип содержит сведения о выполнении проверки сервера. | Сложный тип Сервервалидатионпараметерс (TLS)
ms.assetid: 7a35c7f5-4cab-43d5-87dc-a4020811d3a9
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
ms.openlocfilehash: edebffd1f2023dd6f460505dc033e4505df338d7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694024"
---
# <a name="servervalidationparameters-complex-type-tls"></a><span data-ttu-id="add60-106">Сложный тип Сервервалидатионпараметерс (TLS)</span><span class="sxs-lookup"><span data-stu-id="add60-106">ServerValidationParameters Complex Type (TLS)</span></span>

<span data-ttu-id="add60-107">Сложный тип **сервервалидатионпараметерс** содержит сведения о выполнении проверки сервера.</span><span class="sxs-lookup"><span data-stu-id="add60-107">The **ServerValidationParameters** complex type contains information about how to perform server validation.</span></span>

``` syntax
<xs:complexType name="ServerValidationParameters">
    <xs:sequence>
        <xs:element name="DisableUserPromptForServerValidation"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="ServerNames"
            type="string"
            minOccurs="0"
         />
        <xs:element name="TrustedRootCA"
            type="hexBinary"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="add60-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="add60-108">Child elements</span></span>



| <span data-ttu-id="add60-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="add60-109">Element</span></span>                                                                                                                                                    | <span data-ttu-id="add60-110">Тип</span><span class="sxs-lookup"><span data-stu-id="add60-110">Type</span></span>      | <span data-ttu-id="add60-111">Описание</span><span class="sxs-lookup"><span data-stu-id="add60-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="add60-112">**дисаблеусерпромптфорсервервалидатион**</span><span class="sxs-lookup"><span data-stu-id="add60-112">**DisableUserPromptForServerValidation**</span></span>](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) | <span data-ttu-id="add60-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="add60-113">boolean</span></span>   | <span data-ttu-id="add60-114">Указывает, должен ли пользователь запрашивать проверку сервера.</span><span class="sxs-lookup"><span data-stu-id="add60-114">Indicates whether the user should be asked for server validation.</span></span> <br/> <span data-ttu-id="add60-115">Если [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение true, то EAP-TLS выполняет проверку сервера без участия пользователя. Если проверка завершается неудачно, EAP-TLS не проверяет подлинность.</span><span class="sxs-lookup"><span data-stu-id="add60-115">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is TRUE, then EAP-TLS performs the server validation without user input; if the validation fails, EAP-TLS fails the authentication.</span></span> <br/> <span data-ttu-id="add60-116">Если [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) имеет значение false, пользователю предлагается ввести проверенный сертификат или имя сервера или корневой центр сертификации (CA).</span><span class="sxs-lookup"><span data-stu-id="add60-116">If [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) is FALSE, the user is prompted for a validated server certificate or name, or root certificate authority (CA).</span></span><br/> <span data-ttu-id="add60-117">Элемент [**дисаблеусерпромптфорсервервалидатион**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="add60-117">The [**DisableUserPromptForServerValidation**](eaptlsconnectionpropertiesv1schema-disableuserpromptforservervalidation-servervalidationparameters-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="add60-118">**ServerNames**</span><span class="sxs-lookup"><span data-stu-id="add60-118">**ServerNames**</span></span>](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)                                                   | <span data-ttu-id="add60-119">строка</span><span class="sxs-lookup"><span data-stu-id="add60-119">string</span></span>    | <span data-ttu-id="add60-120">Представляет список серверов, которым доверяет клиент.</span><span class="sxs-lookup"><span data-stu-id="add60-120">Represents a list of servers the client trusts.</span></span> <span data-ttu-id="add60-121">Каждое имя сервера отделяется точкой с запятой и может быть представлено регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="add60-121">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span><br/> <span data-ttu-id="add60-122">Элемент [**ServerName**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="add60-122">The [**ServerNames**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="add60-123">**трустедрутка**</span><span class="sxs-lookup"><span data-stu-id="add60-123">**TrustedRootCA**</span></span>](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md)                                               | <span data-ttu-id="add60-124">hexBinary</span><span class="sxs-lookup"><span data-stu-id="add60-124">hexBinary</span></span> | <span data-ttu-id="add60-125">Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента.</span><span class="sxs-lookup"><span data-stu-id="add60-125">Captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span> <br/> <span data-ttu-id="add60-126">Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.</span><span class="sxs-lookup"><span data-stu-id="add60-126">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate</span></span><br/> <span data-ttu-id="add60-127">Элемент [**трустедрутка**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="add60-127">The [**TrustedRootCA**](eaptlsconnectionpropertiesv1schema-trustedrootca-servervalidationparameters-element.md) element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="requirements"></a><span data-ttu-id="add60-128">Требования</span><span class="sxs-lookup"><span data-stu-id="add60-128">Requirements</span></span>



| <span data-ttu-id="add60-129">Роль</span><span class="sxs-lookup"><span data-stu-id="add60-129">Role</span></span> | <span data-ttu-id="add60-130">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="add60-130">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="add60-131">Клиент</span><span class="sxs-lookup"><span data-stu-id="add60-131">Client</span></span><br/> | <span data-ttu-id="add60-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="add60-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="add60-133">Сервер</span><span class="sxs-lookup"><span data-stu-id="add60-133">Server</span></span><br/> | <span data-ttu-id="add60-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="add60-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="add60-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="add60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="add60-136">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="add60-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="add60-137">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="add60-137">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="add60-138">Сложные типы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="add60-138">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





