---
description: Указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.
ms.assetid: 2aee93e4-d124-43cb-b974-19f00eb4d6a6
title: Элемент Compression (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Compression
api_type:
- Schema
ms.openlocfilehash: 0da6665f69c2791669f75b91e847081dbcc351e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897530"
---
# <a name="compression-contexttype-element"></a><span data-ttu-id="50ea7-103">Элемент Compression (contextType)</span><span class="sxs-lookup"><span data-stu-id="50ea7-103">Compression (contextType) Element</span></span>

<span data-ttu-id="50ea7-104">Элемент **Compression (ContextType)** указывает, будет ли использоваться сжатие по каналу данных для заголовка и передачи данных.</span><span class="sxs-lookup"><span data-stu-id="50ea7-104">The **Compression (contextType)** element specifies if compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="50ea7-105">Этот элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="50ea7-105">This element can be one of the following values.</span></span>

| <span data-ttu-id="50ea7-106">Значение</span><span class="sxs-lookup"><span data-stu-id="50ea7-106">Value</span></span>     | <span data-ttu-id="50ea7-107">Значение</span><span class="sxs-lookup"><span data-stu-id="50ea7-107">Meaning</span></span>                       |
|-----------|-------------------------------|
| <span data-ttu-id="50ea7-108">ПАРАМЕТР</span><span class="sxs-lookup"><span data-stu-id="50ea7-108">"ENABLE"</span></span>  | <span data-ttu-id="50ea7-109">Будет использоваться сжатие.</span><span class="sxs-lookup"><span data-stu-id="50ea7-109">Compression will be used.</span></span>     |
| <span data-ttu-id="50ea7-110">ВКЛЮЧЕН</span><span class="sxs-lookup"><span data-stu-id="50ea7-110">"DISABLE"</span></span> | <span data-ttu-id="50ea7-111">Сжатие не будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="50ea7-111">Compression will not be used.</span></span> |



 

<span data-ttu-id="50ea7-112">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="50ea7-112">This element is optional.</span></span> <span data-ttu-id="50ea7-113">Если этот элемент не указан, то система мобильной широкополосной связи не будет использовать сжатие.</span><span class="sxs-lookup"><span data-stu-id="50ea7-113">If this element is not specified, then the Mobile Broadband system will not use compression.</span></span>

``` syntax
<xs:element name="Compression">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="DISABLE"
             />
            <xs:enumeration
                value="ENABLE"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="50ea7-114">Элемент **Compression** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="50ea7-114">The **Compression** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="50ea7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="50ea7-115">Requirements</span></span>



| <span data-ttu-id="50ea7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="50ea7-116">Requirement</span></span> | <span data-ttu-id="50ea7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="50ea7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="50ea7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50ea7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="50ea7-119">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="50ea7-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="50ea7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50ea7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="50ea7-121">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50ea7-121">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="50ea7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50ea7-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="50ea7-123">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="50ea7-123">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="50ea7-124">**contextType**</span><span class="sxs-lookup"><span data-stu-id="50ea7-124">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="50ea7-125">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="50ea7-125">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="50ea7-126">**Контекст (Мбнпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="50ea7-126">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




