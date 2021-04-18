---
description: Содержит различные параметры подключения.
ms.assetid: 2938f607-47a1-49eb-bf3f-247cab8637ec
title: Элемент подключения (MSM)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectivity
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 938e5b19ffab490066fbbe299bd250191d9226a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674423"
---
# <a name="connectivity-msm-element"></a><span data-ttu-id="047fe-103">Элемент подключения (MSM)</span><span class="sxs-lookup"><span data-stu-id="047fe-103">connectivity (MSM) Element</span></span>

<span data-ttu-id="047fe-104">Элемент подключения (MSM) содержит различные параметры подключения.</span><span class="sxs-lookup"><span data-stu-id="047fe-104">The connectivity (MSM) element contains various connectivity settings.</span></span>

``` syntax
<xs:element name="connectivity"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="phyType"
                minOccurs="0"
                maxOccurs="4"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="a"
                         />
                        <xs:enumeration
                            value="b"
                         />
                        <xs:enumeration
                            value="g"
                         />
                        <xs:enumeration
                            value="n"
                         />
                    </xs:restriction>
                </xs:simpleType>
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

<span data-ttu-id="047fe-105">Элемент определяется элементом [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="047fe-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="047fe-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="047fe-106">Child elements</span></span>



| <span data-ttu-id="047fe-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="047fe-107">Element</span></span>                                                            | <span data-ttu-id="047fe-108">Тип</span><span class="sxs-lookup"><span data-stu-id="047fe-108">Type</span></span> |
|--------------------------------------------------------------------|------|
| [<span data-ttu-id="047fe-109">**фитипе**</span><span class="sxs-lookup"><span data-stu-id="047fe-109">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md) |      |



## <a name="examples"></a><span data-ttu-id="047fe-110">Примеры</span><span class="sxs-lookup"><span data-stu-id="047fe-110">Examples</span></span>

<span data-ttu-id="047fe-111">Чтобы просмотреть образцы профилей, в которых используется элемент **подключения** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="047fe-111">To view sample profiles that use the **connectivity** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="047fe-112">Требования</span><span class="sxs-lookup"><span data-stu-id="047fe-112">Requirements</span></span>



| <span data-ttu-id="047fe-113">Требование</span><span class="sxs-lookup"><span data-stu-id="047fe-113">Requirement</span></span> | <span data-ttu-id="047fe-114">Значение</span><span class="sxs-lookup"><span data-stu-id="047fe-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="047fe-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="047fe-115">Minimum supported client</span></span><br/> | <span data-ttu-id="047fe-116">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="047fe-116">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="047fe-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="047fe-117">Minimum supported server</span></span><br/> | <span data-ttu-id="047fe-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="047fe-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="047fe-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="047fe-119">Redistributable</span></span><br/>          | <span data-ttu-id="047fe-120">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="047fe-120">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="047fe-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="047fe-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="047fe-122">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="047fe-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="047fe-123">**MSM**</span><span class="sxs-lookup"><span data-stu-id="047fe-123">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="047fe-124">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="047fe-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="047fe-125">**MSM (Вланпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="047fe-125">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 




