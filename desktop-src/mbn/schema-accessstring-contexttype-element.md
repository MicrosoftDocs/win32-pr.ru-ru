---
description: Определяет имя APN или строку вызова, используемые для установки подключения к данным.
ms.assetid: e791ffa1-b417-480c-adb8-b1dda7547d89
title: Акцессстринг (contextType), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AccessString
api_type:
- Schema
ms.openlocfilehash: 8cf0d37b8a1870011ae6ae3ea6febf22a98cdeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682744"
---
# <a name="accessstring-contexttype-element"></a><span data-ttu-id="3b63a-103">Акцессстринг (contextType), элемент</span><span class="sxs-lookup"><span data-stu-id="3b63a-103">AccessString (contextType) Element</span></span>

<span data-ttu-id="3b63a-104">Элемент **акцессстринг (ContextType)** определяет имя APN или строку вызова для использования при установлении подключения к данным.</span><span class="sxs-lookup"><span data-stu-id="3b63a-104">The **AccessString (contextType)** element identifies the APN or dial string to be used to establish a data connection.</span></span>

<span data-ttu-id="3b63a-105">Длина этого элемента не может превышать 100 символов.</span><span class="sxs-lookup"><span data-stu-id="3b63a-105">This element can have a maximum length of 100 characters.</span></span>

<span data-ttu-id="3b63a-106">Этот элемент является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3b63a-106">This element is optional.</span></span>

``` syntax
<xs:element name="AccessString">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:minLength
                value="1"
             />
            <xs:maxLength
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="3b63a-107">Элемент **акцессстринг** определяется сложным типом [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3b63a-107">The **AccessString** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b63a-108">Требования</span><span class="sxs-lookup"><span data-stu-id="3b63a-108">Requirements</span></span>



| <span data-ttu-id="3b63a-109">Требование</span><span class="sxs-lookup"><span data-stu-id="3b63a-109">Requirement</span></span> | <span data-ttu-id="3b63a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="3b63a-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="3b63a-111">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3b63a-111">Minimum supported client</span></span><br/> | <span data-ttu-id="3b63a-112">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="3b63a-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="3b63a-113">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3b63a-113">Minimum supported server</span></span><br/> | <span data-ttu-id="3b63a-114">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3b63a-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="3b63a-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b63a-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b63a-116">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3b63a-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3b63a-117">**contextType**</span><span class="sxs-lookup"><span data-stu-id="3b63a-117">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="3b63a-118">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3b63a-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3b63a-119">**Контекст (Мбнпрофиле)**</span><span class="sxs-lookup"><span data-stu-id="3b63a-119">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




