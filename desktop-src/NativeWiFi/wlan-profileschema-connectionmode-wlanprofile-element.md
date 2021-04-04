---
description: Указывает, будет ли подключение к беспроводной локальной сети автоматически или инициировано пользователем.
ms.assetid: 0fad8392-3053-494b-9b30-1db85408a437
title: connectionMode (Вланпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- connectionMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 3dafb9561bf8b5e3c5c66eb23bd5e286cbd38118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811465"
---
# <a name="connectionmode-wlanprofile-element"></a><span data-ttu-id="8d5bb-103">connectionMode (Вланпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="8d5bb-103">connectionMode (WLANProfile) Element</span></span>

<span data-ttu-id="8d5bb-104">Элемент connectionMode (Вланпрофиле) указывает, будет ли подключение к беспроводной локальной сети автоматически или инициировано пользователем.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-104">The connectionMode (WLANProfile) element indicates whether connection to a wireless LAN should be automatic or initiated by user.</span></span>

<span data-ttu-id="8d5bb-105">Если для параметра [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) задано значение ESS, то оно может быть либо автоматически, либо вручную.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-105">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to ESS, this value can be either auto or manual.</span></span> <span data-ttu-id="8d5bb-106">Значение по умолчанию — Auto, если этот элемент отсутствует.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-106">The default value is auto if this element is absent.</span></span>

<span data-ttu-id="8d5bb-107">Если параметр [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) имеет значение ибсс, это значение должно быть задано вручную.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-107">If [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) is set to IBSS, this value must be manual.</span></span>

``` syntax
<xs:element name="connectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="manual"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="8d5bb-108">Элемент **connectionMode** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8d5bb-108">The **connectionMode** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d5bb-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d5bb-109">Remarks</span></span>

<span data-ttu-id="8d5bb-110">В следующей таблице описаны значения перечисления.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-110">The following table describes the enumeration values.</span></span>



| <span data-ttu-id="8d5bb-111">Значение</span><span class="sxs-lookup"><span data-stu-id="8d5bb-111">Value</span></span>  | <span data-ttu-id="8d5bb-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8d5bb-112">Description</span></span>                                                                                                |
|--------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d5bb-113">auto</span><span class="sxs-lookup"><span data-stu-id="8d5bb-113">auto</span></span>   | <span data-ttu-id="8d5bb-114">Подключение к беспроводной сети должно инициироваться автоматически, когда сеть находится в диапазоне.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-114">The connection to the wireless network should be initiated automatically whenever the network is in range.</span></span> |
| <span data-ttu-id="8d5bb-115">manual</span><span class="sxs-lookup"><span data-stu-id="8d5bb-115">manual</span></span> | <span data-ttu-id="8d5bb-116">Подключение к беспроводной сети инитатед только после явного запроса пользователя.</span><span class="sxs-lookup"><span data-stu-id="8d5bb-116">The connection to the wireless network is only initated upon the explicit request of a user.</span></span>               |



 

## <a name="examples"></a><span data-ttu-id="8d5bb-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="8d5bb-117">Examples</span></span>

<span data-ttu-id="8d5bb-118">Чтобы просмотреть образцы профилей, использующих элемент **connectionMode** , см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8d5bb-118">To view sample profiles that use the **connectionMode** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d5bb-119">Требования</span><span class="sxs-lookup"><span data-stu-id="8d5bb-119">Requirements</span></span>



| <span data-ttu-id="8d5bb-120">Требование</span><span class="sxs-lookup"><span data-stu-id="8d5bb-120">Requirement</span></span> | <span data-ttu-id="8d5bb-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8d5bb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="8d5bb-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d5bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8d5bb-123">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8d5bb-123">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8d5bb-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d5bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8d5bb-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8d5bb-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="8d5bb-126">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8d5bb-126">Redistributable</span></span><br/>          | <span data-ttu-id="8d5bb-127">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="8d5bb-127">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="8d5bb-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d5bb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="8d5bb-129">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="8d5bb-129">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8d5bb-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="8d5bb-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="8d5bb-131">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="8d5bb-131">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8d5bb-132">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="8d5bb-132">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




