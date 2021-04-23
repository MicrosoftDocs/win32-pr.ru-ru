---
title: Атрибуты многоадресной станции
description: Атрибуты многоадресной станции
ms.assetid: 24b81ccb-4030-49a4-802c-5b45f7dd5950
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, многоадресная станция
- атрибуты многоадресной станции
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f618ffa645055bf10a9247272d57c7e3f76853c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710155"
---
# <a name="multicast-station-attributes"></a><span data-ttu-id="82e29-108">Атрибуты многоадресной станции</span><span class="sxs-lookup"><span data-stu-id="82e29-108">Multicast Station Attributes</span></span>

<span data-ttu-id="82e29-109">При потоковой передаче файла с многоадресной станции станция может наложить некоторые атрибуты на файл.</span><span class="sxs-lookup"><span data-stu-id="82e29-109">When a file is streaming from a multicast station, the station can impose some attributes on the file.</span></span> <span data-ttu-id="82e29-110">Эти атрибуты, перечисленные в следующей таблице, фактически не хранятся в файле и доступны только в том случае, если файл является потоковой передачей.</span><span class="sxs-lookup"><span data-stu-id="82e29-110">These attributes, listed in the following table, are not actually stored in the file and are only available when the file is streaming.</span></span> <span data-ttu-id="82e29-111">Они содержат сведения о станции и, как правило, идентичны для всего содержимого с станции.</span><span class="sxs-lookup"><span data-stu-id="82e29-111">They contain information about the station and would typically be identical for all content from the station.</span></span>



| <span data-ttu-id="82e29-112">Атрибут многоадресной станции</span><span class="sxs-lookup"><span data-stu-id="82e29-112">Multicast station attribute</span></span>                 | <span data-ttu-id="82e29-113">Глобальный идентификатор</span><span class="sxs-lookup"><span data-stu-id="82e29-113">Global identifier</span></span>      | <span data-ttu-id="82e29-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="82e29-114">Data type</span></span>             |
|---------------------------------------------|------------------------|-----------------------|
| [<span data-ttu-id="82e29-115">**NSC \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="82e29-115">**NSC\_Address**</span></span>](nsc-address.md)         | <span data-ttu-id="82e29-116">g \_ всзвмнскаддресс</span><span class="sxs-lookup"><span data-stu-id="82e29-116">g\_wszWMNSCAddress</span></span>     | <span data-ttu-id="82e29-117">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="82e29-117">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="82e29-118">**\_Описание NSC**</span><span class="sxs-lookup"><span data-stu-id="82e29-118">**NSC\_Description**</span></span>](nsc-description.md) | <span data-ttu-id="82e29-119">g \_ всзвмнскдескриптион</span><span class="sxs-lookup"><span data-stu-id="82e29-119">g\_wszWMNSCDescription</span></span> | <span data-ttu-id="82e29-120">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="82e29-120">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="82e29-121">**NSC \_ адрес электронной почты**</span><span class="sxs-lookup"><span data-stu-id="82e29-121">**NSC\_Email**</span></span>](nsc-email.md)             | <span data-ttu-id="82e29-122">g \_ всзвмнсцемаил</span><span class="sxs-lookup"><span data-stu-id="82e29-122">g\_wszWMNSCEmail</span></span>       | <span data-ttu-id="82e29-123">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="82e29-123">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="82e29-124">**\_Имя NSC**</span><span class="sxs-lookup"><span data-stu-id="82e29-124">**NSC\_Name**</span></span>](nsc-name.md)               | <span data-ttu-id="82e29-125">g \_ всзвмнскнаме</span><span class="sxs-lookup"><span data-stu-id="82e29-125">g\_wszWMNSCName</span></span>        | <span data-ttu-id="82e29-126">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="82e29-126">**WMT\_TYPE\_STRING**</span></span> |
| [<span data-ttu-id="82e29-127">**NSC \_ Телефон**</span><span class="sxs-lookup"><span data-stu-id="82e29-127">**NSC\_Phone**</span></span>](nsc-phone.md)             | <span data-ttu-id="82e29-128">g \_ всзвмнскфоне</span><span class="sxs-lookup"><span data-stu-id="82e29-128">g\_wszWMNSCPhone</span></span>       | <span data-ttu-id="82e29-129">**\_Строка типа \_ ВМТ**</span><span class="sxs-lookup"><span data-stu-id="82e29-129">**WMT\_TYPE\_STRING**</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="82e29-130">См. также</span><span class="sxs-lookup"><span data-stu-id="82e29-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82e29-131">**Атрибуты по типу**</span><span class="sxs-lookup"><span data-stu-id="82e29-131">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="82e29-132">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="82e29-132">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




