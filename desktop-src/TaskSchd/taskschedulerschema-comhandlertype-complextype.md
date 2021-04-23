---
title: Сложный тип Комхандлертипе
description: Определяет дочерние элементы и сведения о последовательности для элемента Комхандлер.
ms.assetid: 688e79f3-8b7e-4892-8119-b0a457ce9c7f
keywords:
- планировщик задач сложного типа Комхандлертипе
topic_type:
- apiref
api_name:
- comHandlerType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d36a92651fc46c0a1950ecff00fa59fe56e1d758
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071412"
---
# <a name="comhandlertype-complex-type"></a><span data-ttu-id="46632-104">Сложный тип Комхандлертипе</span><span class="sxs-lookup"><span data-stu-id="46632-104">comHandlerType Complex Type</span></span>

<span data-ttu-id="46632-105">Определяет дочерние элементы и сведения о последовательности для элемента [**комхандлер**](taskschedulerschema-comhandler-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="46632-105">Defines the child elements and sequencing information for the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="comHandlerType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="ClassId"
                    type="guidType"
                 />
                <xs:element name="Data"
                    type="dataType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="46632-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="46632-106">Child elements</span></span>



| <span data-ttu-id="46632-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="46632-107">Element</span></span>                                                               | <span data-ttu-id="46632-108">Тип</span><span class="sxs-lookup"><span data-stu-id="46632-108">Type</span></span>                                                         | <span data-ttu-id="46632-109">Описание</span><span class="sxs-lookup"><span data-stu-id="46632-109">Description</span></span>                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="46632-110">**Класса**</span><span class="sxs-lookup"><span data-stu-id="46632-110">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="46632-111">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="46632-111">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="46632-112">Задает идентификатор класса обработчика.</span><span class="sxs-lookup"><span data-stu-id="46632-112">Specifies the identifier of the handler class.</span></span><br/>          |
| [<span data-ttu-id="46632-113">**Data**</span><span class="sxs-lookup"><span data-stu-id="46632-113">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="46632-114">**Заданий**</span><span class="sxs-lookup"><span data-stu-id="46632-114">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="46632-115">Указывает дополнительные данные, связанные с обработчиком.</span><span class="sxs-lookup"><span data-stu-id="46632-115">Specifies additional data associated with the handler.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="46632-116">Требования</span><span class="sxs-lookup"><span data-stu-id="46632-116">Requirements</span></span>



| <span data-ttu-id="46632-117">Требование</span><span class="sxs-lookup"><span data-stu-id="46632-117">Requirement</span></span> | <span data-ttu-id="46632-118">Значение</span><span class="sxs-lookup"><span data-stu-id="46632-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="46632-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46632-119">Minimum supported client</span></span><br/> | <span data-ttu-id="46632-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46632-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="46632-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46632-121">Minimum supported server</span></span><br/> | <span data-ttu-id="46632-122">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46632-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="46632-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46632-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46632-124">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="46632-124">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="46632-125">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="46632-125">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





