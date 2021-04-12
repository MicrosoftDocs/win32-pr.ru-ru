---
title: Сложный тип Ексектипе
description: Определяет дочерние элементы и сведения о последовательности элемента exec (actionGroup).
ms.assetid: ab23801a-453d-4fab-8584-30c5c9d57dff
keywords:
- планировщик задач сложного типа Ексектипе
topic_type:
- apiref
api_name:
- execType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f6186c15e8bbe059abaa6cc33580fca45286cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489543"
---
# <a name="exectype-complex-type"></a><span data-ttu-id="09866-104">Сложный тип Ексектипе</span><span class="sxs-lookup"><span data-stu-id="09866-104">execType Complex Type</span></span>

<span data-ttu-id="09866-105">Определяет дочерние элементы и сведения о последовательности элемента [**exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) .</span><span class="sxs-lookup"><span data-stu-id="09866-105">Defines the child elements and sequencing information of the [**Exec (actionGroup)**](taskschedulerschema-exec-actiongroup-element.md) element.</span></span>

``` syntax
<xs:complexType name="execType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Command"
                    type="pathType"
                 />
                <xs:element name="Arguments"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="WorkingDirectory"
                    type="pathType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="09866-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="09866-106">Child elements</span></span>



| <span data-ttu-id="09866-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="09866-107">Element</span></span>                                                                           | <span data-ttu-id="09866-108">Тип</span><span class="sxs-lookup"><span data-stu-id="09866-108">Type</span></span>                                                        | <span data-ttu-id="09866-109">Описание</span><span class="sxs-lookup"><span data-stu-id="09866-109">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09866-110">**Аргументы**</span><span class="sxs-lookup"><span data-stu-id="09866-110">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="09866-111">**string**</span><span class="sxs-lookup"><span data-stu-id="09866-111">**string**</span></span>                                                  | <span data-ttu-id="09866-112">Задает аргументы, связанные с операцией командной строки.</span><span class="sxs-lookup"><span data-stu-id="09866-112">Specifies the arguments associated with the command-line operation.</span></span> <br/>                              |
| [<span data-ttu-id="09866-113">**Get-Help**</span><span class="sxs-lookup"><span data-stu-id="09866-113">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | [<span data-ttu-id="09866-114">**пастипе**</span><span class="sxs-lookup"><span data-stu-id="09866-114">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="09866-115">Указывает исполняемый файл или документ для запуска.</span><span class="sxs-lookup"><span data-stu-id="09866-115">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="09866-116">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="09866-116">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | [<span data-ttu-id="09866-117">**пастипе**</span><span class="sxs-lookup"><span data-stu-id="09866-117">**pathType**</span></span>](taskschedulerschema-pathtype-simpletype.md) | <span data-ttu-id="09866-118">Указывает каталог, в котором существует исполняемый файл или файлы, используемые исполняемым объектом.</span><span class="sxs-lookup"><span data-stu-id="09866-118">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="09866-119">Требования</span><span class="sxs-lookup"><span data-stu-id="09866-119">Requirements</span></span>



| <span data-ttu-id="09866-120">Требование</span><span class="sxs-lookup"><span data-stu-id="09866-120">Requirement</span></span> | <span data-ttu-id="09866-121">Значение</span><span class="sxs-lookup"><span data-stu-id="09866-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09866-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09866-122">Minimum supported client</span></span><br/> | <span data-ttu-id="09866-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="09866-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="09866-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09866-124">Minimum supported server</span></span><br/> | <span data-ttu-id="09866-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="09866-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09866-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09866-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09866-127">планировщик задач сложные типы схемы</span><span class="sxs-lookup"><span data-stu-id="09866-127">Task Scheduler Schema Complex Types</span></span>](task-scheduler-schema-complex-types.md)
</dt> <dt>

[<span data-ttu-id="09866-128">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="09866-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





