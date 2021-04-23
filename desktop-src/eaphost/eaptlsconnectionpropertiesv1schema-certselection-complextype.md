---
title: Сложный тип Цертселектион
description: Сведения о сложном типе Цертселектион. Этот тип определяет, как пользователь выбирает сертификат.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- Цертселектион сложный тип EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339260"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="040a4-105">Сложный тип Цертселектион</span><span class="sxs-lookup"><span data-stu-id="040a4-105">CertSelection Complex Type</span></span>

<span data-ttu-id="040a4-106">Сложный тип **цертселектион** определяет, как пользователь выбирает сертификат.</span><span class="sxs-lookup"><span data-stu-id="040a4-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="040a4-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="040a4-107">Child elements</span></span>



| <span data-ttu-id="040a4-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="040a4-108">Element</span></span>                                                                                                     | <span data-ttu-id="040a4-109">Тип</span><span class="sxs-lookup"><span data-stu-id="040a4-109">Type</span></span>    | <span data-ttu-id="040a4-110">Описание</span><span class="sxs-lookup"><span data-stu-id="040a4-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="040a4-111">**симплецертселектион**</span><span class="sxs-lookup"><span data-stu-id="040a4-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="040a4-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="040a4-112">boolean</span></span> | <span data-ttu-id="040a4-113">По умолчанию имеет значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="040a4-113">Is TRUE by default.</span></span> <span data-ttu-id="040a4-114">Если [**симплецертселектион**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) имеет значение true, EAP-TLS выполняет простой поиск сертификатов без раскрывающихся списков для выбора сертификатов.</span><span class="sxs-lookup"><span data-stu-id="040a4-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="040a4-115">Если **симплецертселектион** имеет значение false, EAP-TLS показывает пользователю подходящий сертификат для выбора.</span><span class="sxs-lookup"><span data-stu-id="040a4-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="040a4-116">Требования</span><span class="sxs-lookup"><span data-stu-id="040a4-116">Requirements</span></span>



| <span data-ttu-id="040a4-117">Роль</span><span class="sxs-lookup"><span data-stu-id="040a4-117">Role</span></span> | <span data-ttu-id="040a4-118">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="040a4-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="040a4-119">Клиент</span><span class="sxs-lookup"><span data-stu-id="040a4-119">Client</span></span><br/> | <span data-ttu-id="040a4-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="040a4-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="040a4-121">Сервер</span><span class="sxs-lookup"><span data-stu-id="040a4-121">Server</span></span><br/> | <span data-ttu-id="040a4-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="040a4-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="040a4-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="040a4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="040a4-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="040a4-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="040a4-125">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="040a4-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="040a4-126">Сложные типы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="040a4-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





