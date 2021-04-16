---
description: Задает конфигурацию EAPHost.
ms.assetid: 71ec3ed6-3670-46fc-a24b-580d15297437
title: Элемент Еапконфиг (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 955b3647aca787097495b6051407b718dfa91f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663048"
---
# <a name="eapconfig-onex-element"></a><span data-ttu-id="020ac-103">Элемент Еапконфиг (OneX)</span><span class="sxs-lookup"><span data-stu-id="020ac-103">EAPConfig (OneX) Element</span></span>

<span data-ttu-id="020ac-104">Элемент **еапконфиг** (OneX) указывает конфигурацию EAPHost.</span><span class="sxs-lookup"><span data-stu-id="020ac-104">The **EAPConfig** (OneX) element specifies the EAPHost configuration.</span></span>

<span data-ttu-id="020ac-105">В отличие от большинства элементов в схеме профиля 802.1 X, этот элемент находится в `https://www.microsoft.com/provisioning/EapHostConfig` пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="020ac-105">Unlike most elements in the 802.1X profile schema, this element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span> <span data-ttu-id="020ac-106">Его дочерние элементы определяются в [схеме еафостконфиг](../eaphost/eaphostconfigschema-schema.md).</span><span class="sxs-lookup"><span data-stu-id="020ac-106">Its child elements are defined in the [eaphostconfig schema](../eaphost/eaphostconfigschema-schema.md).</span></span> <span data-ttu-id="020ac-107">Элемент [**еафостконфиг**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) является дочерним по отношению к элементу **еапконфиг** .</span><span class="sxs-lookup"><span data-stu-id="020ac-107">The [**EapHostConfig**](../eaphost/eaphostconfigschema-eaphostconfig-element.md) element is a child of the **EAPConfig** element.</span></span>

``` syntax
<xs:element name="EAPConfig">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                minOccurs="1"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="020ac-108">Элемент **еапконфиг** определяется элементом [**OneX**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="020ac-108">The **EAPConfig** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="020ac-109">Требования</span><span class="sxs-lookup"><span data-stu-id="020ac-109">Requirements</span></span>



| <span data-ttu-id="020ac-110">Требование</span><span class="sxs-lookup"><span data-stu-id="020ac-110">Requirement</span></span> | <span data-ttu-id="020ac-111">Значение</span><span class="sxs-lookup"><span data-stu-id="020ac-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="020ac-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="020ac-112">Minimum supported client</span></span><br/> | <span data-ttu-id="020ac-113">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="020ac-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="020ac-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="020ac-114">Minimum supported server</span></span><br/> | <span data-ttu-id="020ac-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="020ac-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="020ac-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="020ac-116">Redistributable</span></span><br/>          | <span data-ttu-id="020ac-117">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="020ac-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="020ac-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="020ac-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="020ac-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="020ac-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="020ac-120">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="020ac-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="020ac-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="020ac-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="020ac-122">**Таймаут**</span><span class="sxs-lookup"><span data-stu-id="020ac-122">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 
