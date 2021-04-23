---
description: Содержит параметры безопасности для проводных сетей.
ms.assetid: 08470cf4-3722-4cb9-9877-13eca2f7d04e
title: Элемент Security (MSM) (LAN_policy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 2bd052679f207cd0778f212a73663d4dfd8ce165
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105674763"
---
# <a name="security-msm-element-lan_policy"></a><span data-ttu-id="4e4c0-103">Элемент Security (MSM) (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="4e4c0-103">Security (MSM) Element (LAN_policy)</span></span>

<span data-ttu-id="4e4c0-104">Элемент Security (MSM) содержит параметры безопасности для проводных сетей.</span><span class="sxs-lookup"><span data-stu-id="4e4c0-104">The security (MSM) element contains security settings for wired networks.</span></span> <span data-ttu-id="4e4c0-105">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4e4c0-105">This element is optional.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OneXEnforced"
                type="boolean"
             />
            <xs:element name="OneXEnabled"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="4e4c0-106">Элемент **Security** определяется элементом [**MSM**](lan-profileschema-msm-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4e4c0-106">The **security** element is defined by the [**MSM**](lan-profileschema-msm-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="4e4c0-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="4e4c0-107">Child elements</span></span>



| <span data-ttu-id="4e4c0-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4e4c0-108">Element</span></span>                                                                 | <span data-ttu-id="4e4c0-109">Тип</span><span class="sxs-lookup"><span data-stu-id="4e4c0-109">Type</span></span>    | <span data-ttu-id="4e4c0-110">Описание</span><span class="sxs-lookup"><span data-stu-id="4e4c0-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4e4c0-111">**онексенаблед**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-111">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="4e4c0-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="4e4c0-112">boolean</span></span> | <span data-ttu-id="4e4c0-113">Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="4e4c0-113">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="4e4c0-114">**онексенфорцед**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-114">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="4e4c0-115">Логическое</span><span class="sxs-lookup"><span data-stu-id="4e4c0-115">boolean</span></span> | <span data-ttu-id="4e4c0-116">Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="4e4c0-116">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="4e4c0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4e4c0-117">Requirements</span></span>



| <span data-ttu-id="4e4c0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4e4c0-118">Requirement</span></span> | <span data-ttu-id="4e4c0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4e4c0-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4e4c0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e4c0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4e4c0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4e4c0-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4e4c0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e4c0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4e4c0-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4e4c0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4e4c0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e4c0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="4e4c0-125">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4e4c0-126">**MSM**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-126">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="4e4c0-127">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4e4c0-128">**MSM (Ланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="4e4c0-128">**MSM (LANProfile)**</span></span>](lan-profileschema-msm-lanprofile-element.md)
</dt> </dl>

 

 




