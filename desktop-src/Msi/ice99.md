---
description: ICE99 проверяет, что имя свойства, указанное в таблице каталога, дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.
ms.assetid: a7657c14-6542-4a7b-a8f7-727b109cfc39
title: ICE99
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d70aeaf6480e45db5b47f76434f93e49adf317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814409"
---
# <a name="ice99"></a><span data-ttu-id="7e11a-103">ICE99</span><span class="sxs-lookup"><span data-stu-id="7e11a-103">ICE99</span></span>

<span data-ttu-id="7e11a-104">ICE99 проверяет, что имя свойства, указанное в таблице [каталога](directory-table.md) , дублирует имя, зарезервированное для открытого или закрытого использования установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="7e11a-104">ICE99 verifies that no property name entered in the [Directory](directory-table.md) table duplicates a name reserved for the public or private use of the Windows Installer.</span></span>

## <a name="result"></a><span data-ttu-id="7e11a-105">Результат</span><span class="sxs-lookup"><span data-stu-id="7e11a-105">Result</span></span>

<span data-ttu-id="7e11a-106">ICE99 отправляет следующую ошибку.</span><span class="sxs-lookup"><span data-stu-id="7e11a-106">ICE99 posts the following error.</span></span>



| <span data-ttu-id="7e11a-107">ICE99, ошибка</span><span class="sxs-lookup"><span data-stu-id="7e11a-107">ICE99 error</span></span>                                                                                                      | <span data-ttu-id="7e11a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7e11a-108">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e11a-109">Имя каталога: 1 совпадает с \[ \] одним из открытых свойств MSI и может привести к непредвиденным побочным эффектам.</span><span class="sxs-lookup"><span data-stu-id="7e11a-109">The directory name: \[1\] is the same as one of the MSI Public Properties and can cause unforeseen side effects.</span></span> | <span data-ttu-id="7e11a-110">Значение в столбце Directory таблицы [Directory](directory-table.md) дублирует имя свойства, зарезервированное установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="7e11a-110">The value in the Directory column of the [Directory](directory-table.md) table duplicates a property name reserved by the Windows Installer.</span></span> |



 

## <a name="example"></a><span data-ttu-id="7e11a-111">Пример</span><span class="sxs-lookup"><span data-stu-id="7e11a-111">Example</span></span>

<span data-ttu-id="7e11a-112">ICE99 сообщает о следующей ошибке в примере:</span><span class="sxs-lookup"><span data-stu-id="7e11a-112">ICE99 reports the following error for the example:</span></span>

``` syntax
CustomActionData is the same as one of the MSI Public Properties and can cause unforeseen side effects.
```

<span data-ttu-id="7e11a-113">[Каталог](directory-table.md) (частичный)</span><span class="sxs-lookup"><span data-stu-id="7e11a-113">[Directory](directory-table.md) (partial)</span></span>



| <span data-ttu-id="7e11a-114">Каталог</span><span class="sxs-lookup"><span data-stu-id="7e11a-114">Directory</span></span>        | <span data-ttu-id="7e11a-115">\_Родительский каталог</span><span class="sxs-lookup"><span data-stu-id="7e11a-115">Directory\_Parent</span></span> | <span data-ttu-id="7e11a-116">дефаултдир</span><span class="sxs-lookup"><span data-stu-id="7e11a-116">DefaultDir</span></span> |
|------------------|-------------------|------------|
| <span data-ttu-id="7e11a-117">CustomActionData</span><span class="sxs-lookup"><span data-stu-id="7e11a-117">CustomActionData</span></span> |                   |            |



 

<span data-ttu-id="7e11a-118">Чтобы исправить это предупреждение, измените имя CustomActionData.</span><span class="sxs-lookup"><span data-stu-id="7e11a-118">To correct this warning you should change the name of CustomActionData.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e11a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7e11a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e11a-120">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="7e11a-120">ICE Reference</span></span>](ice-reference.md)
</dt> <dt>

[<span data-ttu-id="7e11a-121">Таблица каталога</span><span class="sxs-lookup"><span data-stu-id="7e11a-121">Directory Table</span></span>](directory-table.md)
</dt> <dt>

[<span data-ttu-id="7e11a-122">Не поддерживается в установщик Windows 3,0 и более ранних версиях</span><span class="sxs-lookup"><span data-stu-id="7e11a-122">Not Supported in Windows Installer 3.0 and earlier</span></span>](not-supported-in-windows-installer-version-3-0.md)
</dt> </dl>

 

 



