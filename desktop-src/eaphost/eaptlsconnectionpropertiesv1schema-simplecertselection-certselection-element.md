---
title: Симплецертселектион (Цертселектион), элемент
description: Сведения об элементе Симплецертселектион (Цертселектион). Этот элемент определяет, как пользователь выбирает сертификат.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Элемент Симплецертселектион EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104070633"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="ab208-105">Симплецертселектион (Цертселектион), элемент</span><span class="sxs-lookup"><span data-stu-id="ab208-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="ab208-106">Элемент **симплецертселектион (цертселектион)** определяет, как пользователь выбирает сертификат.</span><span class="sxs-lookup"><span data-stu-id="ab208-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="ab208-107">Элемент **симплецертселектион** определяется сложным типом [**цертселектион**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ab208-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab208-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab208-108">Remarks</span></span>

<span data-ttu-id="ab208-109">По умолчанию **симплецертселектион** имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="ab208-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="ab208-110">Если **симплецертселектион** имеет значение true, EAP-TLS выполняет простой поиск сертификатов без раскрывающихся списков для выбора сертификатов.</span><span class="sxs-lookup"><span data-stu-id="ab208-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="ab208-111">Если **симплецертселектион** имеет значение false, EAP-TLS показывает пользователю подходящий сертификат для выбора.</span><span class="sxs-lookup"><span data-stu-id="ab208-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab208-112">Требования</span><span class="sxs-lookup"><span data-stu-id="ab208-112">Requirements</span></span>



| <span data-ttu-id="ab208-113">Роль</span><span class="sxs-lookup"><span data-stu-id="ab208-113">Role</span></span> | <span data-ttu-id="ab208-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="ab208-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="ab208-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="ab208-115">Client</span></span><br/> | <span data-ttu-id="ab208-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ab208-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab208-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="ab208-117">Server</span></span><br/> | <span data-ttu-id="ab208-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ab208-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab208-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab208-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab208-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ab208-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ab208-121">**цертселектион**</span><span class="sxs-lookup"><span data-stu-id="ab208-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="ab208-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ab208-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ab208-123">**CertificateStore (Кредентиалссаурцепараметерс)**</span><span class="sxs-lookup"><span data-stu-id="ab208-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="ab208-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ab208-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ab208-125">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="ab208-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ab208-126">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ab208-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ab208-127">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ab208-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





