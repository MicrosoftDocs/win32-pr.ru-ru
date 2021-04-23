---
description: Указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Онексенаблед (Security), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265402"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="eff4f-103">Онексенаблед (Security), элемент</span><span class="sxs-lookup"><span data-stu-id="eff4f-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="eff4f-104">Элемент **онексенаблед** (Security) указывает, будет ли служба автоматической настройки для проводных сетей попытаться выполнить проверку подлинности через порт 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="eff4f-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="eff4f-105">Если **онексенаблед** имеет значение false, служба автоматической настройки никогда не использует 802.1 x для проверки подлинности портов.</span><span class="sxs-lookup"><span data-stu-id="eff4f-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="eff4f-106">Если **онексенаблед** имеет значение true, служба автоматической настройки пытается выполнить проверку подлинности порта с помощью 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="eff4f-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="eff4f-107">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="eff4f-107">This element is optional.</span></span> <span data-ttu-id="eff4f-108">Значение по умолчанию — TRUE.</span><span class="sxs-lookup"><span data-stu-id="eff4f-108">The default value is TRUE.</span></span> <span data-ttu-id="eff4f-109">Если **онексенаблед** не указан в профиле, для проверки подлинности порта может использоваться 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="eff4f-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="eff4f-110">Элемент **онексенаблед** определяется элементом [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eff4f-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff4f-111">Требования</span><span class="sxs-lookup"><span data-stu-id="eff4f-111">Requirements</span></span>



| <span data-ttu-id="eff4f-112">Требование</span><span class="sxs-lookup"><span data-stu-id="eff4f-112">Requirement</span></span> | <span data-ttu-id="eff4f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="eff4f-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eff4f-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eff4f-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eff4f-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eff4f-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eff4f-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eff4f-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eff4f-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eff4f-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eff4f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eff4f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="eff4f-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="eff4f-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eff4f-120">**бюллетеня**</span><span class="sxs-lookup"><span data-stu-id="eff4f-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="eff4f-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="eff4f-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eff4f-122">**безопасность (MSM)**</span><span class="sxs-lookup"><span data-stu-id="eff4f-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




