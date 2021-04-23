---
title: Сложный тип Инструментатионтипе
description: Определяет содержимое раздела инструментирования манифеста.
ms.assetid: dbbb978d-50dd-44c0-8bd1-3e48b41afb88
keywords:
- Журнал событий сложных типов Инструментатионтипе
topic_type:
- apiref
api_name:
- InstrumentationType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1679ae310a996458aad3e25aba74955036094e00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691936"
---
# <a name="instrumentationtype-complex-type"></a><span data-ttu-id="a2fc0-104">Сложный тип Инструментатионтипе</span><span class="sxs-lookup"><span data-stu-id="a2fc0-104">InstrumentationType Complex Type</span></span>

<span data-ttu-id="a2fc0-105">Определяет содержимое раздела инструментирования манифеста.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-105">Defines the contents of the instrumentation section of the manifest.</span></span>

``` syntax
<xs:complexType name="InstrumentationType">
    <xs:sequence>
        <xs:element name="events"
            type="EventsType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a2fc0-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a2fc0-106">Child elements</span></span>



| <span data-ttu-id="a2fc0-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="a2fc0-107">Element</span></span>                                                                  | <span data-ttu-id="a2fc0-108">Тип</span><span class="sxs-lookup"><span data-stu-id="a2fc0-108">Type</span></span>                                                             | <span data-ttu-id="a2fc0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="a2fc0-109">Description</span></span>                                                        |
|--------------------------------------------------------------------------|------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="a2fc0-110">**событиях**</span><span class="sxs-lookup"><span data-stu-id="a2fc0-110">**events**</span></span>](eventmanifestschema-events-instrumentationtype-element.md) | [<span data-ttu-id="a2fc0-111">**евентстипе**</span><span class="sxs-lookup"><span data-stu-id="a2fc0-111">**EventsType**</span></span>](eventmanifestschema-eventstype-complextype.md) | <span data-ttu-id="a2fc0-112">Содержит список поставщиков, определяемых манифестом.</span><span class="sxs-lookup"><span data-stu-id="a2fc0-112">Contains a list of providers that the manifest defines.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a2fc0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a2fc0-113">Requirements</span></span>



| <span data-ttu-id="a2fc0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a2fc0-114">Requirement</span></span> | <span data-ttu-id="a2fc0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a2fc0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2fc0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2fc0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a2fc0-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a2fc0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2fc0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2fc0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a2fc0-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a2fc0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





