---
description: Определяет уникальный идентификатор профиля.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Субскриберид (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542183"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="015b6-103">Субскриберид (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="015b6-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="015b6-104">Элемент **субскриберид (мбнпрофиле)** определяет уникальный идентификатор профиля.</span><span class="sxs-lookup"><span data-stu-id="015b6-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="015b6-105">Для сети GSM оно должно содержать IMSI (Международный идентификатор мобильного подписчика) SIM-карты и устройства CDMA, которые должны содержать минимальное значение (мобильный идентификационный номер) устройства.</span><span class="sxs-lookup"><span data-stu-id="015b6-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="015b6-106">Элемент — это числовая строка с максимальной длиной 15 цифр.</span><span class="sxs-lookup"><span data-stu-id="015b6-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="015b6-107">Элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="015b6-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="015b6-108">Элемент **субскриберид** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="015b6-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="015b6-109">Требования</span><span class="sxs-lookup"><span data-stu-id="015b6-109">Requirements</span></span>



| <span data-ttu-id="015b6-110">Требование</span><span class="sxs-lookup"><span data-stu-id="015b6-110">Requirement</span></span> | <span data-ttu-id="015b6-111">Значение</span><span class="sxs-lookup"><span data-stu-id="015b6-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="015b6-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="015b6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="015b6-113">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="015b6-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="015b6-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="015b6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="015b6-115">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="015b6-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="015b6-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="015b6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="015b6-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="015b6-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="015b6-118">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="015b6-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="015b6-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="015b6-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="015b6-120">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="015b6-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




