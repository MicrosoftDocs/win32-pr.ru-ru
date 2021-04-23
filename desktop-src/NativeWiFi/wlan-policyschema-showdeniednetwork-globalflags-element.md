---
description: Указывает, отображаются ли запрещенные сети в мастере подключения к сети.
ms.assetid: d0a13a80-2532-4383-8946-2536cc1f5e12
title: Шовдениеднетворк (Глобалфлагс), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- showDeniedNetwork
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 33049dad00e5fda22e3f739d3dc200a282481a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543759"
---
# <a name="showdeniednetwork-globalflags-element"></a><span data-ttu-id="a8dc6-103">Шовдениеднетворк (Глобалфлагс), элемент</span><span class="sxs-lookup"><span data-stu-id="a8dc6-103">showDeniedNetwork (globalFlags) Element</span></span>

<span data-ttu-id="a8dc6-104">Элемент **шовдениеднетворк** (глобалфлагс) указывает, отображаются ли запрещенные сети в мастере **подключения к сети** .</span><span class="sxs-lookup"><span data-stu-id="a8dc6-104">The **showDeniedNetwork** (globalFlags) element specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <span data-ttu-id="a8dc6-105">Сети могут быть отклонены групповой политикой или параметрами пользователя.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-105">Networks may be denied by group policy or by user settings.</span></span> <span data-ttu-id="a8dc6-106">Если **шовдениеднетворк** имеет значение true, в мастере **подключения к сети** отображаются запрещенные сети. в противном случае запрещенные сети не будут отображаться в мастере.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-106">When **showDeniedNetwork** has a value of TRUE, denied networks appear in the **Connect to a Network** wizard; otherwise, denied networks do not appear in the wizard.</span></span>

<span data-ttu-id="a8dc6-107">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-107">This element is mandatory.</span></span> <span data-ttu-id="a8dc6-108">При создании профиля службой автонастройки этот элемент будет принимать значение по умолчанию FALSE.</span><span class="sxs-lookup"><span data-stu-id="a8dc6-108">When a profile is created by the AutoConfig service, this element will take the default value of FALSE.</span></span>

``` syntax
<xs:element name="showDeniedNetwork"
    type="boolean"
 />
```

<span data-ttu-id="a8dc6-109">Элемент **шовдениеднетворк** определяется элементом [**глобалфлагс**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a8dc6-109">The **showDeniedNetwork** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8dc6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="a8dc6-110">Requirements</span></span>



| <span data-ttu-id="a8dc6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="a8dc6-111">Requirement</span></span> | <span data-ttu-id="a8dc6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="a8dc6-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8dc6-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8dc6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="a8dc6-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8dc6-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8dc6-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8dc6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="a8dc6-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8dc6-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8dc6-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8dc6-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8dc6-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a8dc6-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8dc6-119">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="a8dc6-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="a8dc6-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a8dc6-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8dc6-121">**Глобалфлагс (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="a8dc6-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




