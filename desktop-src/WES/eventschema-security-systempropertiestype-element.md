---
title: Элемент Security (Системпропертиестипе)
description: Указывает пользователя, который записал в журнал событие.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Журнал событий элемента безопасности
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137310"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="49d84-104">Элемент Security (Системпропертиестипе)</span><span class="sxs-lookup"><span data-stu-id="49d84-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="49d84-105">Указывает пользователя, который записал в журнал событие.</span><span class="sxs-lookup"><span data-stu-id="49d84-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="49d84-106">Элемент **Security** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="49d84-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="49d84-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="49d84-107">Attributes</span></span>



| <span data-ttu-id="49d84-108">Имя</span><span class="sxs-lookup"><span data-stu-id="49d84-108">Name</span></span>   | <span data-ttu-id="49d84-109">Тип</span><span class="sxs-lookup"><span data-stu-id="49d84-109">Type</span></span>   | <span data-ttu-id="49d84-110">Описание</span><span class="sxs-lookup"><span data-stu-id="49d84-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="49d84-111">UserID</span><span class="sxs-lookup"><span data-stu-id="49d84-111">UserID</span></span> | <span data-ttu-id="49d84-112">строка</span><span class="sxs-lookup"><span data-stu-id="49d84-112">string</span></span> | <span data-ttu-id="49d84-113">Идентификатор безопасности (SID) пользователя в строковой форме.</span><span class="sxs-lookup"><span data-stu-id="49d84-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="49d84-114">Требования</span><span class="sxs-lookup"><span data-stu-id="49d84-114">Requirements</span></span>



| <span data-ttu-id="49d84-115">Требование</span><span class="sxs-lookup"><span data-stu-id="49d84-115">Requirement</span></span> | <span data-ttu-id="49d84-116">Значение</span><span class="sxs-lookup"><span data-stu-id="49d84-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="49d84-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49d84-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49d84-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="49d84-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="49d84-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49d84-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49d84-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="49d84-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="49d84-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49d84-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="49d84-122">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="49d84-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="49d84-123">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="49d84-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





