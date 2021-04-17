---
title: Синтаксис объекта (DS-DN)
description: Строка, содержащая различающееся имя (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса object (DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535663"
---
# <a name="objectds-dn-syntax"></a><span data-ttu-id="6998a-104">Синтаксис объекта (DS-DN)</span><span class="sxs-lookup"><span data-stu-id="6998a-104">Object(DS-DN) syntax</span></span>

<span data-ttu-id="6998a-105">Строка, содержащая различающееся имя (DN).</span><span class="sxs-lookup"><span data-stu-id="6998a-105">String that contains a distinguished name (DN).</span></span> <span data-ttu-id="6998a-106">Для атрибутов с этим синтаксисом Active Directory обрабатывает значения атрибутов как ссылки на объект, идентифицируемый DN, и автоматически обновляет значение при перемещении или переименовании объекта.</span><span class="sxs-lookup"><span data-stu-id="6998a-106">For attributes with this syntax, Active Directory handles attribute values as references to the object identified by the DN and automatically updates the value if the object is moved or renamed.</span></span> <span data-ttu-id="6998a-107">Для запросов, содержащих атрибуты синтаксиса DN в фильтре, укажите полные различающиеся имена.</span><span class="sxs-lookup"><span data-stu-id="6998a-107">For queries that include attributes of DN syntax in a filter, specify full distinguished names.</span></span> <span data-ttu-id="6998a-108">Подстановочные знаки (например, CN = John \* ) не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6998a-108">Wildcards (for example, cn=John\*) are not supported.</span></span>



| <span data-ttu-id="6998a-109">Ввод</span><span class="sxs-lookup"><span data-stu-id="6998a-109">Entry</span></span> | <span data-ttu-id="6998a-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6998a-110">Value</span></span> |
|--------------|------------------------------------------------------------------------|
| <span data-ttu-id="6998a-111">Имя</span><span class="sxs-lookup"><span data-stu-id="6998a-111">Name</span></span>         | <span data-ttu-id="6998a-112">Object(DS-DN)</span><span class="sxs-lookup"><span data-stu-id="6998a-112">Object(DS-DN)</span></span>                                                          |
| <span data-ttu-id="6998a-113">Идентификатор синтаксиса</span><span class="sxs-lookup"><span data-stu-id="6998a-113">Syntax ID</span></span>    | <span data-ttu-id="6998a-114">2.5.5.1</span><span class="sxs-lookup"><span data-stu-id="6998a-114">2.5.5.1</span></span>                                                                |
| <span data-ttu-id="6998a-115">ИДЕНТИФИКАТОР OM</span><span class="sxs-lookup"><span data-stu-id="6998a-115">OM ID</span></span>        | <span data-ttu-id="6998a-116">127</span><span class="sxs-lookup"><span data-stu-id="6998a-116">127</span></span>                                                                    |
| <span data-ttu-id="6998a-117">Тип MAPI</span><span class="sxs-lookup"><span data-stu-id="6998a-117">MAPI Type</span></span>    | <span data-ttu-id="6998a-118">OBJECT</span><span class="sxs-lookup"><span data-stu-id="6998a-118">OBJECT</span></span>                                                                 |
| <span data-ttu-id="6998a-119">Тип ADS</span><span class="sxs-lookup"><span data-stu-id="6998a-119">ADS Type</span></span>     | <span data-ttu-id="6998a-120">\_строка различающегося имени адстипе \_</span><span class="sxs-lookup"><span data-stu-id="6998a-120">ADSTYPE\_DN\_STRING</span></span>                                                    |
| <span data-ttu-id="6998a-121">Тип варианта</span><span class="sxs-lookup"><span data-stu-id="6998a-121">Variant Type</span></span> | <span data-ttu-id="6998a-122">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="6998a-122">VT\_BSTR</span></span>                                                               |
| <span data-ttu-id="6998a-123">Тип SDS</span><span class="sxs-lookup"><span data-stu-id="6998a-123">SDS Type</span></span>     | [<span data-ttu-id="6998a-124">System.String</span><span class="sxs-lookup"><span data-stu-id="6998a-124">System.String</span></span>](/dotnet/api/system.string) |



## <a name="see-also"></a><span data-ttu-id="6998a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6998a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6998a-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6998a-126">System.String</span></span>](/dotnet/api/system.string)
</dt> </dl>

 

 
