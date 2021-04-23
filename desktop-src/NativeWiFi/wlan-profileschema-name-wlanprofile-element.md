---
description: Содержит имя профиля беспроводной локальной сети.
ms.assetid: b8977183-7b5d-4c79-9065-ade85ed45716
title: Элемент Name (Вланпрофиле)
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
ms.openlocfilehash: 79174d1cb24fff1841b3022fa06e201794415ce5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543743"
---
# <a name="name-wlanprofile-element"></a><span data-ttu-id="dda3c-103">Элемент Name (Вланпрофиле)</span><span class="sxs-lookup"><span data-stu-id="dda3c-103">name (WLANProfile) Element</span></span>

<span data-ttu-id="dda3c-104">Элемент Name (Вланпрофиле) содержит имя профиля беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="dda3c-104">The name (WLANProfile) element contains the name of a wireless LAN profile.</span></span>

``` syntax
<xs:element name="name"
    type="nameType"
 />
```

<span data-ttu-id="dda3c-105">Элемент **Name** определяется элементом [**вланпрофиле**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dda3c-105">The **name** element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="dda3c-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dda3c-106">Remarks</span></span>

<span data-ttu-id="dda3c-107">В именах учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="dda3c-107">Names are case-sensitive.</span></span>

<span data-ttu-id="dda3c-108">Для Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) элемент name игнорируется при сохранении профиля в хранилище профилей.</span><span class="sxs-lookup"><span data-stu-id="dda3c-108">For Windows XP with Service Pack 3 (SP3) and Wireless LAN API for Windows XP with Service Pack 2 (SP2), the name element is ignored when the profile is saved in the profile store.</span></span> <span data-ttu-id="dda3c-109">Имя профиля является производным от SSID сети.</span><span class="sxs-lookup"><span data-stu-id="dda3c-109">The name of the profile is derived from the SSID of the network.</span></span> <span data-ttu-id="dda3c-110">Для сетевых профилей инфраструктуры имя профиля — это идентификатор SSID сети.</span><span class="sxs-lookup"><span data-stu-id="dda3c-110">For infrastructure network profiles, the name of the profile is the SSID of the network.</span></span> <span data-ttu-id="dda3c-111">Для сетевых профилей ad hoc имя профиля — это идентификатор SSID нерегламентированной сети, за которым следует `-adhoc` .</span><span class="sxs-lookup"><span data-stu-id="dda3c-111">For ad hoc network profiles, the name of the profile is the SSID of the ad hoc network followed by `-adhoc`.</span></span> <span data-ttu-id="dda3c-112">Escape-символы XML, такие как &, не отображаются.</span><span class="sxs-lookup"><span data-stu-id="dda3c-112">XML escape characters, such as &, are not displayed.</span></span> <span data-ttu-id="dda3c-113">Избегайте использования escape-символов XML в именах SSID для профилей, развернутых в Windows XP с SP3 или API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="dda3c-113">Avoid using XML escape characters in SSID names for profiles deployed on Windows XP with SP3 or Wireless LAN API for Windows XP with SP2.</span></span>

<span data-ttu-id="dda3c-114">Для любого сетевого профиля, предназначенного для использования только в Windows Vista или Windows Server 2008, имя может быть любой строкой.</span><span class="sxs-lookup"><span data-stu-id="dda3c-114">For any network profile intended for use only on Windows Vista or Windows Server 2008, the name can be any string.</span></span>

## <a name="examples"></a><span data-ttu-id="dda3c-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="dda3c-115">Examples</span></span>

<span data-ttu-id="dda3c-116">Чтобы просмотреть образцы профилей, в которых используется элемент **Name** , см. раздел [образцы профилей беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="dda3c-116">To view sample profiles that use the **name** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dda3c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="dda3c-117">Requirements</span></span>



| <span data-ttu-id="dda3c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="dda3c-118">Requirement</span></span> | <span data-ttu-id="dda3c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dda3c-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="dda3c-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dda3c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dda3c-121">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dda3c-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dda3c-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dda3c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dda3c-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dda3c-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="dda3c-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dda3c-124">Redistributable</span></span><br/>          | <span data-ttu-id="dda3c-125">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="dda3c-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="dda3c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dda3c-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="dda3c-127">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="dda3c-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dda3c-128">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="dda3c-128">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="dda3c-129">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="dda3c-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dda3c-130">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="dda3c-130">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 




