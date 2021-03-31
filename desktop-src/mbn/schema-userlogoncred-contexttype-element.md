---
description: Содержит учетные данные входа для подключения.
ms.assetid: 79c1d277-6284-4adb-a1bd-6c207b37e33e
title: Усерлогонкред (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UserLogonCred
api_type:
- Schema
ms.openlocfilehash: d3dc0c22d6242ee894545bd61f839574afd06141
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145622"
---
# <a name="userlogoncred-contexttype-element"></a><span data-ttu-id="ddbb3-103">Усерлогонкред (contextType), элемент</span><span class="sxs-lookup"><span data-stu-id="ddbb3-103">UserLogonCred (contextType) Element</span></span>

<span data-ttu-id="ddbb3-104">Элемент **усерлогонкред (ContextType)** содержит учетные данные входа для подключения.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-104">The **UserLogonCred (contextType)** element contains logon credentials for a connection.</span></span>

<span data-ttu-id="ddbb3-105">Этот элемент может иметь следующие дочерние элементы.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-105">This element can have the following child elements.</span></span>

-   [<span data-ttu-id="ddbb3-106">**Имен**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-106">**UserName**</span></span>](schema-username-userlogoncred-element.md)
-   [<span data-ttu-id="ddbb3-107">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-107">**Password**</span></span>](schema-password-userlogoncred-element.md)
-   [<span data-ttu-id="ddbb3-108">**игнорепассворд**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-108">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md)

<span data-ttu-id="ddbb3-109">Этот элемент может иметь максимум одно вхождение.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-109">This element can have a maximum of one occurrence.</span></span>

<span data-ttu-id="ddbb3-110">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-110">This element is optional.</span></span>

``` syntax
<xs:element name="UserLogonCred">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="UserName"
                type="nameType"
             />
            <xs:element name="IgnorePassword"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="Password"
                type="string"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="ddbb3-111">Элемент **усерлогонкред** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ddbb3-111">The **UserLogonCred** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ddbb3-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ddbb3-112">Child elements</span></span>



| <span data-ttu-id="ddbb3-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="ddbb3-113">Element</span></span>                                                               | <span data-ttu-id="ddbb3-114">Тип</span><span class="sxs-lookup"><span data-stu-id="ddbb3-114">Type</span></span>                                           | <span data-ttu-id="ddbb3-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ddbb3-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------|------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="ddbb3-116">**игнорепассворд**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-116">**IgnorePassword**</span></span>](schema-ignorepassword-userlogoncred-element.md) | <span data-ttu-id="ddbb3-117">Логическое</span><span class="sxs-lookup"><span data-stu-id="ddbb3-117">boolean</span></span>                                        | <span data-ttu-id="ddbb3-118">Как работать с паролями при обновлении профилей.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-118">How to handle passwords when upgrading profiles.</span></span><br/> |
| [<span data-ttu-id="ddbb3-119">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-119">**Password**</span></span>](schema-password-userlogoncred-element.md)             | <span data-ttu-id="ddbb3-120">строка</span><span class="sxs-lookup"><span data-stu-id="ddbb3-120">string</span></span>                                         | <span data-ttu-id="ddbb3-121">Пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-121">User password.</span></span><br/>                                   |
| [<span data-ttu-id="ddbb3-122">**Имен**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-122">**UserName**</span></span>](schema-username-userlogoncred-element.md)             | [<span data-ttu-id="ddbb3-123">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-123">**nameType**</span></span>](schema-nametype-simpletype.md) | <span data-ttu-id="ddbb3-124">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="ddbb3-124">User name.</span></span><br/>                                       |



## <a name="requirements"></a><span data-ttu-id="ddbb3-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ddbb3-125">Requirements</span></span>



| <span data-ttu-id="ddbb3-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ddbb3-126">Requirement</span></span> | <span data-ttu-id="ddbb3-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ddbb3-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ddbb3-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ddbb3-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ddbb3-129">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="ddbb3-129">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="ddbb3-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ddbb3-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ddbb3-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ddbb3-131">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="ddbb3-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ddbb3-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="ddbb3-133">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-133">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ddbb3-134">**contextType**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-134">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="ddbb3-135">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-135">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ddbb3-136">**Контекст (Мбнпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="ddbb3-136">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




