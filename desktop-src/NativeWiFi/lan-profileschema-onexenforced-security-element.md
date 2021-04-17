---
description: Указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 X для проверки подлинности портов.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Онексенфорцед (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674039"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="78eda-103">Онексенфорцед (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="78eda-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="78eda-104">Элемент **онексенфорцед** (Security) указывает, требует ли служба автоматической настройки для проводных сетей использование 802.1 x для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="78eda-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="78eda-105">Если **онексенфорцед** имеет значение true, служба автоматической настройки должна использовать 802.1 x для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="78eda-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="78eda-106">Если **онексенфорцед** имеет значение false, служба автоматической настройки будет пытаться использовать 802.1 x для проверки подлинности портов, но служба будет возвращаться к отсутствию проверки подлинности, если по какой-либо причине проверка подлинности по 802.1 x завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="78eda-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="78eda-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="78eda-107">This element is optional.</span></span> <span data-ttu-id="78eda-108">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="78eda-108">The default value is FALSE.</span></span>

<span data-ttu-id="78eda-109">Этот элемент имеет значимое значение, если [**онексенаблед**](lan-profileschema-onexenabled-security-element.md) имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="78eda-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="78eda-110">Если **онексенаблед** имеет значение false, значение этого элемента игнорируется.</span><span class="sxs-lookup"><span data-stu-id="78eda-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="78eda-111">Элемент **онексенфорцед** определяется элементом [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="78eda-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="78eda-112">Требования</span><span class="sxs-lookup"><span data-stu-id="78eda-112">Requirements</span></span>



| <span data-ttu-id="78eda-113">Требование</span><span class="sxs-lookup"><span data-stu-id="78eda-113">Requirement</span></span> | <span data-ttu-id="78eda-114">Значение</span><span class="sxs-lookup"><span data-stu-id="78eda-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="78eda-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78eda-115">Minimum supported client</span></span><br/> | <span data-ttu-id="78eda-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78eda-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="78eda-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78eda-117">Minimum supported server</span></span><br/> | <span data-ttu-id="78eda-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78eda-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78eda-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78eda-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="78eda-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="78eda-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="78eda-121">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="78eda-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="78eda-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="78eda-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="78eda-123">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="78eda-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




