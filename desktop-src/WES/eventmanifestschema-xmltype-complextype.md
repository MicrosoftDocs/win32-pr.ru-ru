---
title: Сложный тип XmlType
description: Определяет фрагмент XML.
ms.assetid: ac6ce2a2-4584-4181-9a39-aceab85d5c51
keywords:
- Журнал событий сложных типов XmlType
topic_type:
- apiref
api_name:
- XmlType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a4d71d7f4f2685d6c5f1c0626392c79436b68d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415496"
---
# <a name="xmltype-complex-type"></a><span data-ttu-id="9c908-104">Сложный тип XmlType</span><span class="sxs-lookup"><span data-stu-id="9c908-104">XmlType Complex Type</span></span>

<span data-ttu-id="9c908-105">Определяет фрагмент XML.</span><span class="sxs-lookup"><span data-stu-id="9c908-105">Defines an XML fragment.</span></span> <span data-ttu-id="9c908-106">Любой экземпляр схемы разрешен; узел верхнего уровня в фрагменте должен содержать атрибут Namespace.</span><span class="sxs-lookup"><span data-stu-id="9c908-106">Any schema instance is allowed; the top-level node in the fragment must contain a namespace attribute.</span></span>

``` syntax
<xs:complexType name="XmlType">
    <xs:sequence>
        <xs:any
            processContents="skip"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="9c908-107">Требования</span><span class="sxs-lookup"><span data-stu-id="9c908-107">Requirements</span></span>



| <span data-ttu-id="9c908-108">Требование</span><span class="sxs-lookup"><span data-stu-id="9c908-108">Requirement</span></span> | <span data-ttu-id="9c908-109">Значение</span><span class="sxs-lookup"><span data-stu-id="9c908-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9c908-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c908-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9c908-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c908-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9c908-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c908-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9c908-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c908-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





