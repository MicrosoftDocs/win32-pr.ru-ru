---
title: Сложный тип Шовмессажетипе
description: Определяет элементы, представляющие действие, которое отображает окно сообщения.
ms.assetid: eb841d9f-0be2-433b-9002-5e41c6ee78f9
keywords:
- планировщик задач сложного типа Шовмессажетипе
topic_type:
- apiref
api_name:
- showMessageType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d65ed893bce63c95fffcf237d3a3a95ebb1550d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988947"
---
# <a name="showmessagetype-complex-type"></a><span data-ttu-id="d8437-104">Сложный тип Шовмессажетипе</span><span class="sxs-lookup"><span data-stu-id="d8437-104">showMessageType Complex Type</span></span>

<span data-ttu-id="d8437-105">Определяет элементы, представляющие действие, которое отображает окно сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8437-105">Defines the elements that represent an action that shows a message box.</span></span>

``` syntax
<xs:complexType name="showMessageType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Title"
                    type="nonEmptyString"
                 />
                <xs:element name="Body"
                    type="nonEmptyString"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="d8437-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d8437-106">Child elements</span></span>



| <span data-ttu-id="d8437-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="d8437-107">Element</span></span>                                                            | <span data-ttu-id="d8437-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d8437-108">Type</span></span>           | <span data-ttu-id="d8437-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d8437-109">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="d8437-110">**Текст**</span><span class="sxs-lookup"><span data-stu-id="d8437-110">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="d8437-111">нонемптистринг</span><span class="sxs-lookup"><span data-stu-id="d8437-111">nonEmptyString</span></span> | <span data-ttu-id="d8437-112">Задает текст, отображаемый в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8437-112">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="d8437-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d8437-113">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="d8437-114">нонемптистринг</span><span class="sxs-lookup"><span data-stu-id="d8437-114">nonEmptyString</span></span> | <span data-ttu-id="d8437-115">Задает заголовок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="d8437-115">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="requirements"></a><span data-ttu-id="d8437-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d8437-116">Requirements</span></span>



| <span data-ttu-id="d8437-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d8437-117">Requirement</span></span> | <span data-ttu-id="d8437-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d8437-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8437-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d8437-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d8437-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d8437-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8437-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d8437-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d8437-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d8437-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





