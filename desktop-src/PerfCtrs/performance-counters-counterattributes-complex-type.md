---
description: Определяет список, содержащий до пяти атрибутов счетчика.
ms.assetid: d710c3d2-2886-4f1a-bd27-f11451d2f3c6
title: Сложный тип Каунтераттрибутес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfcb94b131e1343565d5763ae2ea4d95e53f1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998516"
---
# <a name="counterattributes-complex-type"></a><span data-ttu-id="dce21-103">Сложный тип Каунтераттрибутес</span><span class="sxs-lookup"><span data-stu-id="dce21-103">counterAttributes Complex Type</span></span>

<span data-ttu-id="dce21-104">Определяет список, содержащий до пяти атрибутов счетчика.</span><span class="sxs-lookup"><span data-stu-id="dce21-104">Defines a list that contains up to five counter attributes.</span></span>

``` syntax
<xs:complexType name="counterAttributes">
    <xs:choice
        minOccurs="1"
        maxOccurs="5"
    >
        <xs:element name="counterAttribute"
            type="man:counterAttribute"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="dce21-105">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dce21-105">Child elements</span></span>



| <span data-ttu-id="dce21-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="dce21-106">Element</span></span>              | <span data-ttu-id="dce21-107">Тип</span><span class="sxs-lookup"><span data-stu-id="dce21-107">Type</span></span>                                                                               | <span data-ttu-id="dce21-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dce21-108">Description</span></span>                                                                                                |
|----------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dce21-109">**каунтераттрибуте**</span><span class="sxs-lookup"><span data-stu-id="dce21-109">**counterAttribute**</span></span> | [<span data-ttu-id="dce21-110">**мужчина: Каунтераттрибуте**</span><span class="sxs-lookup"><span data-stu-id="dce21-110">**man:counterAttribute**</span></span>](performance-counters-counterattribute-complex-type.md) | <span data-ttu-id="dce21-111">Атрибут счетчика, указывающий способ отображения данных счетчиков в приложении-потребителе.</span><span class="sxs-lookup"><span data-stu-id="dce21-111">A counter attribute that specifies how the counter data is displayed in a consumer application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="dce21-112">Требования</span><span class="sxs-lookup"><span data-stu-id="dce21-112">Requirements</span></span>



| <span data-ttu-id="dce21-113">Требование</span><span class="sxs-lookup"><span data-stu-id="dce21-113">Requirement</span></span> | <span data-ttu-id="dce21-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dce21-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dce21-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dce21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="dce21-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dce21-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dce21-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dce21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="dce21-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dce21-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




