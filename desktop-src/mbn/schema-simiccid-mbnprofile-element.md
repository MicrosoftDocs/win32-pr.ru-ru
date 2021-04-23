---
description: Определяет идентификационный номер SIM-карты для устройств GSM.
ms.assetid: 980afba4-fc31-4da0-ba01-6eb8e3db0ac8
title: СимикЦид (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SimIccID
api_type:
- Schema
ms.openlocfilehash: f566253ad3e86b4f7ee7317cf125d9e649034847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662392"
---
# <a name="simiccid-mbnprofile-element"></a><span data-ttu-id="bc733-103">СимикЦид (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="bc733-103">SimIccID (MBNProfile) Element</span></span>

<span data-ttu-id="bc733-104">Элемент **симикЦид (мбнпрофиле)** определяет идентификационный номер SIM-карты для устройств GSM.</span><span class="sxs-lookup"><span data-stu-id="bc733-104">The **SimIccID (MBNProfile)** element identifies the SIM Identification number for GSM devices.</span></span>

<span data-ttu-id="bc733-105">Этот элемент является необязательным и задается службой мобильного широкополосного подключения для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="bc733-105">This element is optional and is set by the Mobile Broadband service for internal use.</span></span> <span data-ttu-id="bc733-106">Приложение не должно задавать это поле при создании или обновлении профиля.</span><span class="sxs-lookup"><span data-stu-id="bc733-106">An application should not set this field while creating or updating a profile.</span></span>

``` syntax
<xs:element name="SimIccID"
    type="simIccIDType"
 />
```

<span data-ttu-id="bc733-107">Элемент **симикЦид** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bc733-107">The **SimIccID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc733-108">Требования</span><span class="sxs-lookup"><span data-stu-id="bc733-108">Requirements</span></span>



| <span data-ttu-id="bc733-109">Требование</span><span class="sxs-lookup"><span data-stu-id="bc733-109">Requirement</span></span> | <span data-ttu-id="bc733-110">Значение</span><span class="sxs-lookup"><span data-stu-id="bc733-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bc733-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bc733-111">Minimum supported client</span></span><br/> | <span data-ttu-id="bc733-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bc733-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bc733-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bc733-113">Minimum supported server</span></span><br/> | <span data-ttu-id="bc733-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bc733-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bc733-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bc733-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="bc733-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="bc733-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bc733-117">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="bc733-117">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="bc733-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="bc733-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bc733-119">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="bc733-119">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




