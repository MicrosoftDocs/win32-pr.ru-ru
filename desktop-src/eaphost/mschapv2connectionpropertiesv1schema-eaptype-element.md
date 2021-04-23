---
title: Элемент Еаптипе (mschapv2connectionpropertiesv1schema)
description: Является производным типом элемента Еаптипе из схемы baseeapconnectionpropertiesv1. Это верхний элемент, который отображается внутри элемента config схемы Еафостконфиг.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187761"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="22b83-105">Элемент Еаптипе (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="22b83-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="22b83-106">Элемент **еаптипе** является производным типом элемента [еаптипе](baseeapconnectionpropertiesv1schema-eaptype-element.md) из схемы [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="22b83-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="22b83-107">Это верхний элемент, который отображается внутри элемента config схемы [еафостконфиг](eaphostconfigschema-elements.md)</span><span class="sxs-lookup"><span data-stu-id="22b83-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="22b83-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="22b83-108">Child elements</span></span>



| <span data-ttu-id="22b83-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="22b83-109">Element</span></span>                                                                                                       | <span data-ttu-id="22b83-110">Тип</span><span class="sxs-lookup"><span data-stu-id="22b83-110">Type</span></span>    | <span data-ttu-id="22b83-111">Описание</span><span class="sxs-lookup"><span data-stu-id="22b83-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22b83-112">**усевинлогонкредентиалс**</span><span class="sxs-lookup"><span data-stu-id="22b83-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="22b83-113">Логическое</span><span class="sxs-lookup"><span data-stu-id="22b83-113">boolean</span></span> | <span data-ttu-id="22b83-114">Управляет использованием учетных данных винлогин.</span><span class="sxs-lookup"><span data-stu-id="22b83-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="22b83-115">Если значение — TRUE, EAP MS-CHAPv2 получает учетные данные из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="22b83-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="22b83-116">Если значение равно FALSE, то EAP MS-CHAPv2 получает учетные данные от пользователя.</span><span class="sxs-lookup"><span data-stu-id="22b83-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="22b83-117">Элемент [**усевинлогонкредентиалс (еаптипе)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="22b83-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="22b83-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="22b83-118">Remarks</span></span>

<span data-ttu-id="22b83-119">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="22b83-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="22b83-120">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="22b83-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="22b83-121">Требования</span><span class="sxs-lookup"><span data-stu-id="22b83-121">Requirements</span></span>



| <span data-ttu-id="22b83-122">Требование</span><span class="sxs-lookup"><span data-stu-id="22b83-122">Requirement</span></span> | <span data-ttu-id="22b83-123">Значение</span><span class="sxs-lookup"><span data-stu-id="22b83-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22b83-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22b83-124">Minimum supported client</span></span><br/> | <span data-ttu-id="22b83-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="22b83-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="22b83-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22b83-126">Minimum supported server</span></span><br/> | <span data-ttu-id="22b83-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="22b83-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="22b83-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="22b83-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22b83-129">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="22b83-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="22b83-130">Схема mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="22b83-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





