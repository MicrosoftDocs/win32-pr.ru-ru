---
description: Задает параметры, необходимые для настройки подключения к данным.
ms.assetid: 7a3d3b9d-f799-4927-9c18-04b025788a4a
title: Элемент context (Мбнпрофиле)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Context
api_type:
- Schema
ms.openlocfilehash: dac98101dade85fbbaa63275933885241ef206fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692464"
---
# <a name="context-mbnprofile-element"></a><span data-ttu-id="1484e-103">Элемент context (Мбнпрофиле)</span><span class="sxs-lookup"><span data-stu-id="1484e-103">Context (MBNProfile) Element</span></span>

<span data-ttu-id="1484e-104">Элемент **context (мбнпрофиле)** задает параметры, необходимые для настройки подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="1484e-104">The **Context (MBNProfile)** element specifies the parameters required to setup a data connection.</span></span>

<span data-ttu-id="1484e-105">Элемент может иметь следующие дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="1484e-105">The element can have the following child elements.</span></span>

-   [<span data-ttu-id="1484e-106">**AccessString**</span><span class="sxs-lookup"><span data-stu-id="1484e-106">**AccessString**</span></span>](schema-accessstring-contexttype-element.md)
-   [<span data-ttu-id="1484e-107">**UserLogonCred**</span><span class="sxs-lookup"><span data-stu-id="1484e-107">**UserLogonCred**</span></span>](schema-userlogoncred-contexttype-element.md)
-   [<span data-ttu-id="1484e-108">**Сжатие**</span><span class="sxs-lookup"><span data-stu-id="1484e-108">**Compression**</span></span>](schema-compression-contexttype-element.md)
-   [<span data-ttu-id="1484e-109">**AuthProtocol**</span><span class="sxs-lookup"><span data-stu-id="1484e-109">**AuthProtocol**</span></span>](schema-authprotocol-contexttype-element.md)

<span data-ttu-id="1484e-110">Этот элемент может иметь максимум одно вхождение.</span><span class="sxs-lookup"><span data-stu-id="1484e-110">This element can have a maximum of one occurrence.</span></span>

``` syntax
<xs:element name="Context"
    type="contextType"
 />
```

<span data-ttu-id="1484e-111">Элемент **context** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1484e-111">The **Context** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1484e-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1484e-112">Requirements</span></span>



| <span data-ttu-id="1484e-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1484e-113">Requirement</span></span> | <span data-ttu-id="1484e-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1484e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="1484e-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1484e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1484e-116">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="1484e-116">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="1484e-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1484e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1484e-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1484e-118">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="1484e-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1484e-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="1484e-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="1484e-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1484e-121">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="1484e-121">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="1484e-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="1484e-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1484e-123">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="1484e-123">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




