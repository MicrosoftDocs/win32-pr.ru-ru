---
description: Содержит идентификатор SSID беспроводной локальной сети.
ms.assetid: ed23ccd0-9b44-4c97-a5ed-93e86632b819
title: Элемент Name (SSID)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- name
api_type:
- Schema
api_location: ''
ms.openlocfilehash: dbb1301de2a2d70edf8c61de002c28e48b00a5d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911896"
---
# <a name="name-ssid-element"></a><span data-ttu-id="8a300-103">Элемент Name (SSID)</span><span class="sxs-lookup"><span data-stu-id="8a300-103">name (SSID) Element</span></span>

<span data-ttu-id="8a300-104">Элемент Name (SSID) содержит идентификатор SSID беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="8a300-104">The name (SSID) element contains the SSID of a wireless LAN.</span></span>

``` syntax
<xs:element name="name">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="32"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8a300-105">Элемент определяется элементом [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a300-105">The element is defined by the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8a300-106">Remarks</span><span class="sxs-lookup"><span data-stu-id="8a300-106">Remarks</span></span>

<span data-ttu-id="8a300-107">В именах учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="8a300-107">Names are case-sensitive.</span></span>

<span data-ttu-id="8a300-108">Несмотря на то, что [**шестнадцатеричные**](wlan-profileschema-hex-ssid-element.md) элементы и **имена** являются необязательными, по крайней мере один **Шестнадцатеричный** элемент или **имя** должны быть дочерними элементами элемента [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a300-108">Although the [**hex**](wlan-profileschema-hex-ssid-element.md) and **name** elements are optional, at least one **hex** or **name** element must appear as a child of the [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element.</span></span>

<span data-ttu-id="8a300-109">Когда сведения о профиле преобразуются в идентификатор SSID, [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент преобразуется в SSID (если есть), а элемент **Name** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="8a300-109">When profile information is converted to an SSID, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is converted to the SSID (if present) and the **name** element is ignored.</span></span> <span data-ttu-id="8a300-110">Если **Шестнадцатеричный** элемент отсутствует, элемент **Name** преобразуется в идентификатор SSID с помощью преобразования Юникод в ASCII.</span><span class="sxs-lookup"><span data-stu-id="8a300-110">If the **hex** element is not present, the **name** element is converted to an SSID using Unicode to ASCII conversion.</span></span>

<span data-ttu-id="8a300-111">Если идентификатор SSID хранится в профиле, всегда создается [**Шестнадцатеричный**](wlan-profileschema-hex-ssid-element.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="8a300-111">When an SSID is stored in a profile, the [**hex**](wlan-profileschema-hex-ssid-element.md) element is always generated.</span></span> <span data-ttu-id="8a300-112">Элемент **Name** создается только в случае успешного преобразования ASCII в формат SSID и создания профиля XML.</span><span class="sxs-lookup"><span data-stu-id="8a300-112">The **name** element is only generated if the both the ASCII to Unicode conversion of the SSID and the XML profile generation are successful.</span></span> <span data-ttu-id="8a300-113">При преобразовании в **имя** некоторые сведения из исходного идентификатора SSID могут быть потеряны.</span><span class="sxs-lookup"><span data-stu-id="8a300-113">Some information from the original SSID may be lost when it is converted to a **name**.</span></span>

<span data-ttu-id="8a300-114">**Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2):** Escape-символы XML, такие как &, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="8a300-114">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="8a300-115">Избегайте использования escape-символов XML в именах SSID для профилей, развернутых в Windows XP с SP3 и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="8a300-115">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 and Wireless LAN API for Windows XP with SP2.</span></span>

## <a name="examples"></a><span data-ttu-id="8a300-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="8a300-116">Examples</span></span>

<span data-ttu-id="8a300-117">Чтобы просмотреть образцы профилей, в которых используется элемент **Name** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8a300-117">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8a300-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8a300-118">Requirements</span></span>



| <span data-ttu-id="8a300-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8a300-119">Requirement</span></span> | <span data-ttu-id="8a300-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8a300-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8a300-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a300-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8a300-122">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8a300-122">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8a300-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a300-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8a300-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a300-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8a300-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8a300-125">Redistributable</span></span><br/>          | <span data-ttu-id="8a300-126">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="8a300-126">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8a300-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a300-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a300-128">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="8a300-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8a300-129">**SSID**</span><span class="sxs-lookup"><span data-stu-id="8a300-129">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> <dt>

<span data-ttu-id="8a300-130">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="8a300-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8a300-131">**SSID (Ссидконфиг)**</span><span class="sxs-lookup"><span data-stu-id="8a300-131">**SSID (SSIDConfig)**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)
</dt> </dl>

 

 




