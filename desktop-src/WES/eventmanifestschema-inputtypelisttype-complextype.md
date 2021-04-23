---
title: Сложный тип Инпуттипелисттипе
description: Определяет список входных типов.
ms.assetid: e6bba894-7c17-411e-92e5-9276728a5e4b
keywords:
- Журнал событий сложных типов Инпуттипелисттипе
topic_type:
- apiref
api_name:
- InputTypeListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e68b4077bfb08b69a31f18d81aa55d0b5ac54f78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137470"
---
# <a name="inputtypelisttype-complex-type"></a><span data-ttu-id="61b73-104">Сложный тип Инпуттипелисттипе</span><span class="sxs-lookup"><span data-stu-id="61b73-104">InputTypeListType Complex Type</span></span>

<span data-ttu-id="61b73-105">Определяет список входных типов.</span><span class="sxs-lookup"><span data-stu-id="61b73-105">Defines a list of input types.</span></span>

``` syntax
<xs:complexType name="InputTypeListType">
    <xs:sequence>
        <xs:element name="inType"
            type="InputType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="61b73-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="61b73-106">Child elements</span></span>



| <span data-ttu-id="61b73-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="61b73-107">Element</span></span>                                                                | <span data-ttu-id="61b73-108">Тип</span><span class="sxs-lookup"><span data-stu-id="61b73-108">Type</span></span>                                                           | <span data-ttu-id="61b73-109">Описание</span><span class="sxs-lookup"><span data-stu-id="61b73-109">Description</span></span>                       |
|------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------|
| [<span data-ttu-id="61b73-110">**Тип**</span><span class="sxs-lookup"><span data-stu-id="61b73-110">**inType**</span></span>](eventmanifestschema-intype-inputtypelisttype-element.md) | [<span data-ttu-id="61b73-111">**InputType**</span><span class="sxs-lookup"><span data-stu-id="61b73-111">**InputType**</span></span>](eventmanifestschema-inputtype-complextype.md) | <span data-ttu-id="61b73-112">Определяет тип входных данных.</span><span class="sxs-lookup"><span data-stu-id="61b73-112">Defines an input type.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="61b73-113">Требования</span><span class="sxs-lookup"><span data-stu-id="61b73-113">Requirements</span></span>



| <span data-ttu-id="61b73-114">Требование</span><span class="sxs-lookup"><span data-stu-id="61b73-114">Requirement</span></span> | <span data-ttu-id="61b73-115">Значение</span><span class="sxs-lookup"><span data-stu-id="61b73-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="61b73-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61b73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="61b73-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="61b73-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="61b73-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61b73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="61b73-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="61b73-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





