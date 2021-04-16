---
title: Сложный тип Филтерлисттипе
description: Определяет список фильтров, которые контроллер ETW может передать поставщику для дальнейшего ограничения числа записываемых событий.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- Журнал событий сложных типов Филтерлисттипе
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341215"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="e7fdd-104">Сложный тип Филтерлисттипе</span><span class="sxs-lookup"><span data-stu-id="e7fdd-104">FilterListType Complex Type</span></span>

<span data-ttu-id="e7fdd-105">Определяет список фильтров, которые контроллер ETW может передать поставщику для дальнейшего ограничения числа записываемых событий.</span><span class="sxs-lookup"><span data-stu-id="e7fdd-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e7fdd-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e7fdd-106">Child elements</span></span>



| <span data-ttu-id="e7fdd-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="e7fdd-107">Element</span></span>    | <span data-ttu-id="e7fdd-108">Тип</span><span class="sxs-lookup"><span data-stu-id="e7fdd-108">Type</span></span>                                                             | <span data-ttu-id="e7fdd-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e7fdd-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="e7fdd-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="e7fdd-110">**filter**</span></span> | [<span data-ttu-id="e7fdd-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="e7fdd-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="e7fdd-112">Список фильтров.</span><span class="sxs-lookup"><span data-stu-id="e7fdd-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e7fdd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7fdd-113">Remarks</span></span>

<span data-ttu-id="e7fdd-114">Контроллер ETW — это приложение, которое вызывает функцию [**старттраце**](/windows/desktop/ETW/starttrace) для создания сеанса ETW.</span><span class="sxs-lookup"><span data-stu-id="e7fdd-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="e7fdd-115">Дополнительные сведения см. в разделе [Управление сеансами трассировки событий](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="e7fdd-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="e7fdd-116">Контроллер может использовать функцию [**тдхенумератепровидерфилтерс**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) для перечисления определенных фильтров.</span><span class="sxs-lookup"><span data-stu-id="e7fdd-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="e7fdd-117">Контроллер может затем передать один или несколько фильтров при вызове функции [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) для включения поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7fdd-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="e7fdd-118">Поставщик получает фильтры вместе с остальными параметрами включения в функции обратного вызова [*енаблекаллбакк*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .</span><span class="sxs-lookup"><span data-stu-id="e7fdd-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7fdd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e7fdd-119">Requirements</span></span>



| <span data-ttu-id="e7fdd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="e7fdd-120">Requirement</span></span> | <span data-ttu-id="e7fdd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="e7fdd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="e7fdd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7fdd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e7fdd-123">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e7fdd-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e7fdd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7fdd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e7fdd-125">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7fdd-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

