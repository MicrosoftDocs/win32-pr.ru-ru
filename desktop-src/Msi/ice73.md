---
description: ICE73 проверяет, что пакет не использует коды пакетов, коды обновления или коды продуктов установщик Windows примеров пакета SDK. Пакеты никогда не должны повторно использовать коды пакета, обновления или продукта другого продукта.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662589"
---
# <a name="ice73"></a><span data-ttu-id="d0423-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="d0423-104">ICE73</span></span>

<span data-ttu-id="d0423-105">ICE73 проверяет, что пакет не использует коды пакетов, коды обновления или коды продуктов установщик Windows примеров пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="d0423-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="d0423-106">Пакеты никогда не должны повторно использовать коды пакета, обновления или продукта другого продукта.</span><span class="sxs-lookup"><span data-stu-id="d0423-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="d0423-107">Результат</span><span class="sxs-lookup"><span data-stu-id="d0423-107">Result</span></span>

<span data-ttu-id="d0423-108">ICE73 выводит предупреждение, если пакет продукта повторно использует код пакета или продукта в образце пакета SDK установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d0423-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="d0423-109">Пример</span><span class="sxs-lookup"><span data-stu-id="d0423-109">Example</span></span>

<span data-ttu-id="d0423-110">ICE73 сообщает о следующих ошибках в приведенном примере:</span><span class="sxs-lookup"><span data-stu-id="d0423-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="d0423-111">Звездочки ( \* \* \* \* ) в GUID представляют диапазон идентификаторов GUID, зарезервированных для последующих пакетов SDK установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="d0423-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="d0423-112">Чтобы устранить ошибки, создайте уникальный идентификатор GUID для продукта пакета и кодов пакетов.</span><span class="sxs-lookup"><span data-stu-id="d0423-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="d0423-113">Кроме того, вам потребуется новый уникальный идентификатор GUID для кода обновления пакета.</span><span class="sxs-lookup"><span data-stu-id="d0423-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="d0423-114">[Поток сводных данных](summary-information-stream.md) (частичный)</span><span class="sxs-lookup"><span data-stu-id="d0423-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="d0423-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="d0423-115">Property</span></span>       | <span data-ttu-id="d0423-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d0423-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="d0423-117">Идентификатор процесса \_ ревнумбер</span><span class="sxs-lookup"><span data-stu-id="d0423-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="d0423-118">{000C1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="d0423-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="d0423-119">[Таблица свойств](property-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="d0423-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="d0423-120">Свойство</span><span class="sxs-lookup"><span data-stu-id="d0423-120">Property</span></span>                           | <span data-ttu-id="d0423-121">Значение</span><span class="sxs-lookup"><span data-stu-id="d0423-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="d0423-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="d0423-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="d0423-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span><span class="sxs-lookup"><span data-stu-id="d0423-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="d0423-124">**UpgradeCode**</span><span class="sxs-lookup"><span data-stu-id="d0423-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="d0423-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span><span class="sxs-lookup"><span data-stu-id="d0423-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d0423-126">См. также</span><span class="sxs-lookup"><span data-stu-id="d0423-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0423-127">Коды пакетов</span><span class="sxs-lookup"><span data-stu-id="d0423-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="d0423-128">Коды продуктов</span><span class="sxs-lookup"><span data-stu-id="d0423-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="d0423-129">**Свойство сводки номеров редакций**</span><span class="sxs-lookup"><span data-stu-id="d0423-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="d0423-130">**UpgradeCode, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0423-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="d0423-131">**ProductCode, свойство**</span><span class="sxs-lookup"><span data-stu-id="d0423-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="d0423-132">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="d0423-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



