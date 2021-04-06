---
title: Усерцерт (Еаптипе), элемент
description: Ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.
ms.assetid: 0f0fa37c-dff2-44c6-bd7c-ca54c569fcf1
keywords:
- Элемент Усерцерт EAPHost
topic_type:
- apiref
api_name:
- UserCert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c23840b489bad1e06bdd0c7eb6e0033bfb1961f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803550"
---
# <a name="usercert-eaptype-element"></a><span data-ttu-id="eede5-104">Усерцерт (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="eede5-104">UserCert (EapType) Element</span></span>

<span data-ttu-id="eede5-105">Элемент **усерцерт (еаптипе)** ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="eede5-105">The **UserCert (EapType)** element refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span>

``` syntax
<xs:element name="UserCert"
    type="hexBinary"
 />
```

<span data-ttu-id="eede5-106">Элемент **усерцерт** определяется элементом [**еаптипе**](eaptlsuserpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="eede5-106">The **UserCert** element is defined by the [**EapType**](eaptlsuserpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="eede5-107">Требования</span><span class="sxs-lookup"><span data-stu-id="eede5-107">Requirements</span></span>



| <span data-ttu-id="eede5-108">Требование</span><span class="sxs-lookup"><span data-stu-id="eede5-108">Requirement</span></span> | <span data-ttu-id="eede5-109">Значение</span><span class="sxs-lookup"><span data-stu-id="eede5-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eede5-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eede5-110">Minimum supported client</span></span><br/> | <span data-ttu-id="eede5-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eede5-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="eede5-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eede5-112">Minimum supported server</span></span><br/> | <span data-ttu-id="eede5-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eede5-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eede5-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eede5-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="eede5-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="eede5-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="eede5-116">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="eede5-116">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="eede5-117">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="eede5-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="eede5-118">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="eede5-118">**EapType**</span></span>](eaptlsuserpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="eede5-119">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="eede5-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="eede5-120">Схема eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="eede5-120">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





