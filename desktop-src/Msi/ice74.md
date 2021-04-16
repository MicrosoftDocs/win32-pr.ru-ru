---
description: ICE74 проверяет, что свойство ФАСТОЕМ не было создано в таблице свойств.
ms.assetid: 2af132f0-0ffa-405f-9d05-7cb5d5f826b8
title: ICE74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fe2762710e061f2c88f55893294a40fbac8700f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650592"
---
# <a name="ice74"></a><span data-ttu-id="c9fbd-103">ICE74</span><span class="sxs-lookup"><span data-stu-id="c9fbd-103">ICE74</span></span>

<span data-ttu-id="c9fbd-104">ICE74 проверяет, что свойство [**фастоем**](fastoem.md) не было создано в [таблице свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="c9fbd-104">ICE74 verifies that the [**FASTOEM**](fastoem.md) property has not been authored into the [Property table](property-table.md).</span></span>

<span data-ttu-id="c9fbd-105">Свойство [**фастоем**](fastoem.md) позволяет изготовителям оборудования сократить время, необходимое для установки установщик Windows приложений в первый раз.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-105">The [**FASTOEM**](fastoem.md) property enables OEMs to reduce the time required to install Windows Installer applications for the first time.</span></span> <span data-ttu-id="c9fbd-106">Его нельзя использовать после первой установки.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-106">It cannot be used after the first install.</span></span> <span data-ttu-id="c9fbd-107">Свойство **фастоем** не должно быть создано в таблице свойств, так как это влияет на последующие установки для обслуживания, удаления или восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-107">The **FASTOEM** property must not be authored in the Property table because this interferes with subsequent installations for the maintenance, removal, or repair of the application.</span></span>

<span data-ttu-id="c9fbd-108">ICE74 также проверяет, что свойство [**UpgradeCode**](upgradecode.md) создано в [таблице свойств](property-table.md), а его значение не равно NULL GUID {00000000-0000-0000-0000-000000000000} .</span><span class="sxs-lookup"><span data-stu-id="c9fbd-108">ICE74 also verifies that the [**UpgradeCode**](upgradecode.md) property is authored into the [Property table](property-table.md), and that its value is not a null GUID, {00000000-0000-0000-0000-000000000000}.</span></span>

## <a name="result"></a><span data-ttu-id="c9fbd-109">Результат</span><span class="sxs-lookup"><span data-stu-id="c9fbd-109">Result</span></span>

<span data-ttu-id="c9fbd-110">ICE74 может публиковать следующие ошибки.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-110">ICE74 can post the following errors.</span></span>



| <span data-ttu-id="c9fbd-111">ICE74, ошибка</span><span class="sxs-lookup"><span data-stu-id="c9fbd-111">ICE74 error</span></span>                                                                       | <span data-ttu-id="c9fbd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c9fbd-112">Description</span></span>                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fbd-113">Свойство [**фастоем**](fastoem.md) не может быть создано в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-113">The [**FASTOEM**](fastoem.md) property cannot be authored in the Property table.</span></span> | <span data-ttu-id="c9fbd-114">Свойство [**фастоем**](fastoem.md) было задано в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-114">The [**FASTOEM**](fastoem.md) property has been set in the Property table.</span></span>                             |
| <span data-ttu-id="c9fbd-115">" \[ 2 \] " не является допустимым [**UpgradeCode**](upgradecode.md).</span><span class="sxs-lookup"><span data-stu-id="c9fbd-115">'\[2\]' is not a valid [**UpgradeCode**](upgradecode.md).</span></span>                        | <span data-ttu-id="c9fbd-116">Для свойства [**UpgradeCode**](upgradecode.md) в таблице свойств был введен пустой GUID.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-116">A null GUID has been entered for the [**UpgradeCode**](upgradecode.md) property in the Property table.</span></span> |



 

<span data-ttu-id="c9fbd-117">ICE74 может опубликовать следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-117">ICE74 can post the following warning.</span></span>



| <span data-ttu-id="c9fbd-118">Предупреждение ICE74</span><span class="sxs-lookup"><span data-stu-id="c9fbd-118">ICE74 warning</span></span>                                                                                                                                                                                             | <span data-ttu-id="c9fbd-119">Описание</span><span class="sxs-lookup"><span data-stu-id="c9fbd-119">Description</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fbd-120">Свойство [**UpgradeCode**](upgradecode.md) не создано в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-120">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> <span data-ttu-id="c9fbd-121">Настоятельно рекомендуется, чтобы авторы установочных пакетов указали **UpgradeCode** для своего приложения.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-121">It is strongly recommended that authors of installation packages specify an **UpgradeCode** for their application.</span></span> | <span data-ttu-id="c9fbd-122">Свойство [**UpgradeCode**](upgradecode.md) не создано в таблице свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-122">The [**UpgradeCode**](upgradecode.md) property is not authored in the Property table.</span></span> |



 

## <a name="example"></a><span data-ttu-id="c9fbd-123">Пример</span><span class="sxs-lookup"><span data-stu-id="c9fbd-123">Example</span></span>

<span data-ttu-id="c9fbd-124">ICE74 сообщает о следующей ошибке, если свойство [**фастоем**](fastoem.md) задано: фастоем</span><span class="sxs-lookup"><span data-stu-id="c9fbd-124">ICE74 reports the following error if the [**FASTOEM**](fastoem.md) property is set: The FASTOEM</span></span>

``` syntax
 property cannot be authored in the Property table.
```

<span data-ttu-id="c9fbd-125">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="c9fbd-125">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="c9fbd-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="c9fbd-126">Property</span></span>                   | <span data-ttu-id="c9fbd-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c9fbd-127">Value</span></span> |
|----------------------------|-------|
| [<span data-ttu-id="c9fbd-128">**фастоем**</span><span class="sxs-lookup"><span data-stu-id="c9fbd-128">**FASTOEM**</span></span>](fastoem.md) | <span data-ttu-id="c9fbd-129">1</span><span class="sxs-lookup"><span data-stu-id="c9fbd-129">1</span></span>     |



 

<span data-ttu-id="c9fbd-130">Чтобы устранить эту ошибку, удалите свойство [**фастоем**](fastoem.md) из таблицы свойств.</span><span class="sxs-lookup"><span data-stu-id="c9fbd-130">To fix this error remove the [**FASTOEM**](fastoem.md) property from the Property Table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9fbd-131">См. также</span><span class="sxs-lookup"><span data-stu-id="c9fbd-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9fbd-132">**ФАСТОЕМ, свойство**</span><span class="sxs-lookup"><span data-stu-id="c9fbd-132">**FASTOEM property**</span></span>](fastoem.md)
</dt> <dt>

[<span data-ttu-id="c9fbd-133">Таблица свойств</span><span class="sxs-lookup"><span data-stu-id="c9fbd-133">Property table</span></span>](property-table.md)
</dt> <dt>

[<span data-ttu-id="c9fbd-134">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="c9fbd-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



