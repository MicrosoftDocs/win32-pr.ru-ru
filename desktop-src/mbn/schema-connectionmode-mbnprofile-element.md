---
description: Задает параметр автоматического подключения, используемый для устройства мобильной широкополосной связи.
ms.assetid: 789016d5-47f1-4506-bcb9-1a4019d236fd
title: ConnectionMode (Мбнпрофиле), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectionMode
api_type:
- Schema
ms.openlocfilehash: d9c92227e26bb8858aef28d2f030ac2f84bed06d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991096"
---
# <a name="connectionmode-mbnprofile-element"></a><span data-ttu-id="bf85b-103">ConnectionMode (Мбнпрофиле), элемент</span><span class="sxs-lookup"><span data-stu-id="bf85b-103">ConnectionMode (MBNProfile) Element</span></span>

<span data-ttu-id="bf85b-104">Элемент **ConnectionMode (мбнпрофиле)** задает параметр автоматического подключения, который будет использоваться для устройства мобильной широкополосной связи.</span><span class="sxs-lookup"><span data-stu-id="bf85b-104">The **ConnectionMode (MBNProfile)** element specifies the auto connection setting to be used for a Mobile Broadband device.</span></span>

<span data-ttu-id="bf85b-105">Этот элемент может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="bf85b-105">This element can have one of the following values.</span></span>



| <span data-ttu-id="bf85b-106">Значение</span><span class="sxs-lookup"><span data-stu-id="bf85b-106">Value</span></span>       | <span data-ttu-id="bf85b-107">Значение</span><span class="sxs-lookup"><span data-stu-id="bf85b-107">Meaning</span></span>                                                                |
|-------------|------------------------------------------------------------------------|
| <span data-ttu-id="bf85b-108">документации</span><span class="sxs-lookup"><span data-stu-id="bf85b-108">"manual"</span></span>    | <span data-ttu-id="bf85b-109">Никогда не подключайтесь к сети автоматически.</span><span class="sxs-lookup"><span data-stu-id="bf85b-109">Never automatically connect to the network.</span></span>                            |
| <span data-ttu-id="bf85b-110">Выбор</span><span class="sxs-lookup"><span data-stu-id="bf85b-110">"auto"</span></span>      | <span data-ttu-id="bf85b-111">Всегда автоматически подключаться к сети.</span><span class="sxs-lookup"><span data-stu-id="bf85b-111">Always automatically connect to the network.</span></span>                           |
| <span data-ttu-id="bf85b-112">"Авто-Домашняя"</span><span class="sxs-lookup"><span data-stu-id="bf85b-112">"auto-home"</span></span> | <span data-ttu-id="bf85b-113">Автоматически подключаться к сети, кроме случаев, когда в роуминге сеть.</span><span class="sxs-lookup"><span data-stu-id="bf85b-113">Automatically connect to the network except when in a roaming network.</span></span> |



 

<span data-ttu-id="bf85b-114">Этот элемент может иметь максимум одно вхождение.</span><span class="sxs-lookup"><span data-stu-id="bf85b-114">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="bf85b-115">Этот обязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="bf85b-115">This is a required element.</span></span>

``` syntax
<xs:element name="ConnectionMode">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="manual"
             />
            <xs:enumeration
                value="auto"
             />
            <xs:enumeration
                value="auto-home"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="bf85b-116">Элемент **ConnectionMode** определяется элементом [**мбнпрофиле**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bf85b-116">The **ConnectionMode** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf85b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf85b-117">Requirements</span></span>



| <span data-ttu-id="bf85b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bf85b-118">Requirement</span></span> | <span data-ttu-id="bf85b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bf85b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="bf85b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf85b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf85b-121">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="bf85b-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="bf85b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf85b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf85b-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bf85b-123">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="bf85b-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf85b-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="bf85b-125">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="bf85b-125">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bf85b-126">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="bf85b-126">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="bf85b-127">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="bf85b-127">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bf85b-128">**мбнпрофиле**</span><span class="sxs-lookup"><span data-stu-id="bf85b-128">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




