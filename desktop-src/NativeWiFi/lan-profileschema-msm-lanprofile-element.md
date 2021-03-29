---
description: Содержит параметры модуля для конкретных носителей (MSM).
ms.assetid: fe858701-e0eb-4817-b3c2-ae61e96a4cbe
title: Элемент MSM (Ланпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e9e58895ae36a304e713ecdb21b4008a2027e8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265403"
---
# <a name="msm-lanprofile-element"></a><span data-ttu-id="84636-103">Элемент MSM (Ланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="84636-103">MSM (LANProfile) Element</span></span>

<span data-ttu-id="84636-104">Элемент MSM (Ланпрофиле) содержит параметры модуля для конкретного носителя (MSM).</span><span class="sxs-lookup"><span data-stu-id="84636-104">The MSM (LANProfile) element contains media-specific module (MSM) settings.</span></span>

``` syntax
<xs:element name="MSM">
    <xs:complexType>
        <xs:sequence>
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

<span data-ttu-id="84636-105">Элемент **MSM** определяется элементом [**ланпрофиле**](lan-profileschema-lanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="84636-105">The **MSM** element is defined by the [**LANProfile**](lan-profileschema-lanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="84636-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="84636-106">Child elements</span></span>



| <span data-ttu-id="84636-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="84636-107">Element</span></span>                                                                 | <span data-ttu-id="84636-108">Тип</span><span class="sxs-lookup"><span data-stu-id="84636-108">Type</span></span>    | <span data-ttu-id="84636-109">Описание</span><span class="sxs-lookup"><span data-stu-id="84636-109">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84636-110">**онексенаблед**</span><span class="sxs-lookup"><span data-stu-id="84636-110">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="84636-111">Логическое</span><span class="sxs-lookup"><span data-stu-id="84636-111">boolean</span></span> | <span data-ttu-id="84636-112">Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="84636-112">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span><br/>       |
| [<span data-ttu-id="84636-113">**онексенфорцед**</span><span class="sxs-lookup"><span data-stu-id="84636-113">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="84636-114">Логическое</span><span class="sxs-lookup"><span data-stu-id="84636-114">boolean</span></span> | <span data-ttu-id="84636-115">Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="84636-115">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="84636-116">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="84636-116">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="84636-117">Содержит параметры безопасности.</span><span class="sxs-lookup"><span data-stu-id="84636-117">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="requirements"></a><span data-ttu-id="84636-118">Требования</span><span class="sxs-lookup"><span data-stu-id="84636-118">Requirements</span></span>



| <span data-ttu-id="84636-119">Требование</span><span class="sxs-lookup"><span data-stu-id="84636-119">Requirement</span></span> | <span data-ttu-id="84636-120">Значение</span><span class="sxs-lookup"><span data-stu-id="84636-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="84636-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84636-121">Minimum supported client</span></span><br/> | <span data-ttu-id="84636-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="84636-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="84636-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84636-123">Minimum supported server</span></span><br/> | <span data-ttu-id="84636-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="84636-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="84636-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84636-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="84636-126">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="84636-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="84636-127">**ланпрофиле**</span><span class="sxs-lookup"><span data-stu-id="84636-127">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> <dt>

<span data-ttu-id="84636-128">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="84636-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="84636-129">**ланпрофиле**</span><span class="sxs-lookup"><span data-stu-id="84636-129">**LANProfile**</span></span>](lan-profileschema-lanprofile-element.md)
</dt> </dl>

 

 




