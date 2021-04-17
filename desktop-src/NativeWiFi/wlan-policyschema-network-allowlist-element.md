---
description: Определяет разрешенную сеть.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Элемент Network (разрешенных)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684446"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="dbd9e-103">Элемент Network (разрешенных)</span><span class="sxs-lookup"><span data-stu-id="dbd9e-103">network (allowList) Element</span></span>

<span data-ttu-id="dbd9e-104">Элемент Network (разрешенных) определяет разрешенную сеть.</span><span class="sxs-lookup"><span data-stu-id="dbd9e-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="dbd9e-105">Компьютеру должно быть разрешено подключаться к разрешенной сети.</span><span class="sxs-lookup"><span data-stu-id="dbd9e-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="dbd9e-106">Элемент **Network** определяется элементом [**разрешенных**](wlan-policyschema-allowlist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="dbd9e-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbd9e-107">Требования</span><span class="sxs-lookup"><span data-stu-id="dbd9e-107">Requirements</span></span>



| <span data-ttu-id="dbd9e-108">Требование</span><span class="sxs-lookup"><span data-stu-id="dbd9e-108">Requirement</span></span> | <span data-ttu-id="dbd9e-109">Значение</span><span class="sxs-lookup"><span data-stu-id="dbd9e-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dbd9e-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dbd9e-110">Minimum supported client</span></span><br/> | <span data-ttu-id="dbd9e-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dbd9e-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dbd9e-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dbd9e-112">Minimum supported server</span></span><br/> | <span data-ttu-id="dbd9e-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dbd9e-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dbd9e-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbd9e-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="dbd9e-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="dbd9e-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="dbd9e-116">**Разрешенных**</span><span class="sxs-lookup"><span data-stu-id="dbd9e-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="dbd9e-117">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="dbd9e-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="dbd9e-118">**Разрешенных (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="dbd9e-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




