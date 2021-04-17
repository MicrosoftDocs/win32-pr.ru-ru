---
description: Указывает, зашифрован ли общий ключ.
ms.assetid: 9206ef74-cd3e-4374-bea9-0c10505d10bf
title: protected (sharedKey), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- protected
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0b48ef0e07e5502ea8577904facc52f9f7e69838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673237"
---
# <a name="protected-sharedkey-element"></a><span data-ttu-id="aeca2-103">protected (sharedKey), элемент</span><span class="sxs-lookup"><span data-stu-id="aeca2-103">protected (sharedKey) Element</span></span>

<span data-ttu-id="aeca2-104">Защищенный элемент (sharedKey) указывает, зашифрован ли общий ключ.</span><span class="sxs-lookup"><span data-stu-id="aeca2-104">The protected (sharedKey) element indicates whether a shared key is encrypted.</span></span>

``` syntax
<xs:element name="protected"
    type="boolean"
 />
```

<span data-ttu-id="aeca2-105">Элемент определяется элементом [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="aeca2-105">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeca2-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aeca2-106">Remarks</span></span>

<span data-ttu-id="aeca2-107">Для Windows Vista и Windows Server 2008 параметр **protected** всегда имеет значение true, если профиль был получен из хранилища профилей (например, путем вызова [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span><span class="sxs-lookup"><span data-stu-id="aeca2-107">For Windows Vista and Windows Server 2008, **protected** always has a value of TRUE if the profile was retrieved from the profile store (for example, by calling [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)).</span></span>

<span data-ttu-id="aeca2-108">Для профилей, предназначенных для использования в Windows XP с пакетом обновления 3 (SP3) или API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2), **Защита** должна иметь значение false.</span><span class="sxs-lookup"><span data-stu-id="aeca2-108">For profiles intended for use on Windows XP with Service Pack 3 (SP3) or Wireless LAN API for Windows XP with Service Pack 2 (SP2), **protected** must have a value of FALSE.</span></span>

## <a name="examples"></a><span data-ttu-id="aeca2-109">Примеры</span><span class="sxs-lookup"><span data-stu-id="aeca2-109">Examples</span></span>

<span data-ttu-id="aeca2-110">Для просмотра образцов профилей, использующих **защищенный** элемент, см. раздел [образцы профиля беспроводной связи](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="aeca2-110">To view sample profiles that use the **protected** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aeca2-111">Требования</span><span class="sxs-lookup"><span data-stu-id="aeca2-111">Requirements</span></span>



| <span data-ttu-id="aeca2-112">Требование</span><span class="sxs-lookup"><span data-stu-id="aeca2-112">Requirement</span></span> | <span data-ttu-id="aeca2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="aeca2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="aeca2-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aeca2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aeca2-115">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="aeca2-115">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="aeca2-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aeca2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aeca2-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="aeca2-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="aeca2-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="aeca2-118">Redistributable</span></span><br/>          | <span data-ttu-id="aeca2-119">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="aeca2-119">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="aeca2-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aeca2-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="aeca2-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="aeca2-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="aeca2-122">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="aeca2-122">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="aeca2-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="aeca2-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="aeca2-124">**sharedKey (безопасность)**</span><span class="sxs-lookup"><span data-stu-id="aeca2-124">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




