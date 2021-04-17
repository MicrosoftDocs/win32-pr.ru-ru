---
description: Указывает, заблокирован ли доступ ко всем компьютерным сетям.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Деняллибсс (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673247"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="42afa-103">Деняллибсс (Нетворкфилтер), элемент</span><span class="sxs-lookup"><span data-stu-id="42afa-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="42afa-104">Элемент Деняллибсс (Нетворкфилтер) указывает, заблокирован ли доступ ко всем компьютерам ad-hoc.</span><span class="sxs-lookup"><span data-stu-id="42afa-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="42afa-105">Если **деняллибсс** имеет значение true, компьютеры не могут подключаться к сети ad-hoc; в противном случае компьютеры могут подключаться к компьютерным сетям.</span><span class="sxs-lookup"><span data-stu-id="42afa-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="42afa-106">Значение по умолчанию для этого элемента — FALSE.</span><span class="sxs-lookup"><span data-stu-id="42afa-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="42afa-107">Если **деняллибсс** не указан в профиле, компьютеры по умолчанию могут подключаться к сетям с прямым подключением.</span><span class="sxs-lookup"><span data-stu-id="42afa-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="42afa-108">Элемент **деняллибсс** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="42afa-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="42afa-109">Требования</span><span class="sxs-lookup"><span data-stu-id="42afa-109">Requirements</span></span>



| <span data-ttu-id="42afa-110">Требование</span><span class="sxs-lookup"><span data-stu-id="42afa-110">Requirement</span></span> | <span data-ttu-id="42afa-111">Значение</span><span class="sxs-lookup"><span data-stu-id="42afa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42afa-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="42afa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="42afa-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="42afa-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42afa-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="42afa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="42afa-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="42afa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42afa-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="42afa-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="42afa-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="42afa-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="42afa-118">**нетворкфилтер**</span><span class="sxs-lookup"><span data-stu-id="42afa-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="42afa-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="42afa-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="42afa-120">**Нетворкфилтер (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="42afa-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




