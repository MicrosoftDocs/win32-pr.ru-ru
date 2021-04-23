---
title: Сложный тип Левеллисттипе
description: Определяет список уровней серьезности, определяющих уровень детализации события.
ms.assetid: 82102f8a-271e-4c3d-9b0a-1e20eaa87497
keywords:
- Журнал событий сложных типов Левеллисттипе
topic_type:
- apiref
api_name:
- LevelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4456ade3977603948997304393a1c9414cb0c458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493089"
---
# <a name="levellisttype-complex-type"></a><span data-ttu-id="95f61-104">Сложный тип Левеллисттипе</span><span class="sxs-lookup"><span data-stu-id="95f61-104">LevelListType Complex Type</span></span>

<span data-ttu-id="95f61-105">Определяет список уровней серьезности, определяющих уровень детализации события.</span><span class="sxs-lookup"><span data-stu-id="95f61-105">Defines a list of severity levels that specify the verbosity of an event.</span></span>

``` syntax
<xs:complexType name="LevelListType">
    <xs:sequence>
        <xs:element name="level"
            type="LevelType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="95f61-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="95f61-106">Child elements</span></span>



| <span data-ttu-id="95f61-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="95f61-107">Element</span></span>                                                          | <span data-ttu-id="95f61-108">Тип</span><span class="sxs-lookup"><span data-stu-id="95f61-108">Type</span></span>                                                           | <span data-ttu-id="95f61-109">Описание</span><span class="sxs-lookup"><span data-stu-id="95f61-109">Description</span></span>                                                                                 |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95f61-110">**уровню**</span><span class="sxs-lookup"><span data-stu-id="95f61-110">**level**</span></span>](eventmanifestschema-level-levellisttype-element.md) | [<span data-ttu-id="95f61-111">**LevelType**</span><span class="sxs-lookup"><span data-stu-id="95f61-111">**LevelType**</span></span>](eventmanifestschema-leveltype-complextype.md) | <span data-ttu-id="95f61-112">Определяет значение серьезности, определяющее уровень детализации событий во время ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="95f61-112">Defines a severity value that determines the verbosity of events during logging.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="95f61-113">Требования</span><span class="sxs-lookup"><span data-stu-id="95f61-113">Requirements</span></span>



| <span data-ttu-id="95f61-114">Требование</span><span class="sxs-lookup"><span data-stu-id="95f61-114">Requirement</span></span> | <span data-ttu-id="95f61-115">Значение</span><span class="sxs-lookup"><span data-stu-id="95f61-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="95f61-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="95f61-116">Minimum supported client</span></span><br/> | <span data-ttu-id="95f61-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="95f61-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="95f61-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="95f61-118">Minimum supported server</span></span><br/> | <span data-ttu-id="95f61-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="95f61-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





