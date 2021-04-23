---
title: Сложный тип Опкоделисттипе
description: Определяет список кодов операций, которые используются для определения операций компонента приложения.
ms.assetid: 0cbca036-b32e-4fc4-96ee-1dd5bee019bf
keywords:
- Журнал событий сложных типов Опкоделисттипе
topic_type:
- apiref
api_name:
- OpcodeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dce0942ef0268f50b25987a6be0fd4fffeebd614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490419"
---
# <a name="opcodelisttype-complex-type"></a><span data-ttu-id="db790-104">Сложный тип Опкоделисттипе</span><span class="sxs-lookup"><span data-stu-id="db790-104">OpcodeListType Complex Type</span></span>

<span data-ttu-id="db790-105">Определяет список кодов операций, которые используются для определения операций компонента приложения.</span><span class="sxs-lookup"><span data-stu-id="db790-105">Defines a list of opcodes that are used to identify the operations of a component of the application.</span></span>

``` syntax
<xs:complexType name="OpcodeListType">
    <xs:sequence>
        <xs:element name="opcode"
            type="OpcodeType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="db790-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="db790-106">Child elements</span></span>



| <span data-ttu-id="db790-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="db790-107">Element</span></span>                                                             | <span data-ttu-id="db790-108">Тип</span><span class="sxs-lookup"><span data-stu-id="db790-108">Type</span></span>                                                             | <span data-ttu-id="db790-109">Описание</span><span class="sxs-lookup"><span data-stu-id="db790-109">Description</span></span>                                                            |
|---------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="db790-110">**транслируют**</span><span class="sxs-lookup"><span data-stu-id="db790-110">**opcode**</span></span>](eventmanifestschema-opcode-opcodelisttype-element.md) | [<span data-ttu-id="db790-111">**опкодетипе**</span><span class="sxs-lookup"><span data-stu-id="db790-111">**OpcodeType**</span></span>](eventmanifestschema-opcodetype-complextype.md) | <span data-ttu-id="db790-112">Определяет операцию в компоненте приложения.</span><span class="sxs-lookup"><span data-stu-id="db790-112">Defines an operation within a component of the application.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="db790-113">Требования</span><span class="sxs-lookup"><span data-stu-id="db790-113">Requirements</span></span>



| <span data-ttu-id="db790-114">Требование</span><span class="sxs-lookup"><span data-stu-id="db790-114">Requirement</span></span> | <span data-ttu-id="db790-115">Значение</span><span class="sxs-lookup"><span data-stu-id="db790-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="db790-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db790-116">Minimum supported client</span></span><br/> | <span data-ttu-id="db790-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="db790-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="db790-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db790-118">Minimum supported server</span></span><br/> | <span data-ttu-id="db790-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="db790-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





