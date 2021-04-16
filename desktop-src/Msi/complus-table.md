---
description: Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.
ms.assetid: 0c9a7469-5959-45ad-b84d-6cfd3e169ff6
title: Таблица ComPlus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2ad5b7b96044025b78bfc774ee0767c2756aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651138"
---
# <a name="complus-table"></a><span data-ttu-id="d9a03-103">Таблица ComPlus</span><span class="sxs-lookup"><span data-stu-id="d9a03-103">Complus Table</span></span>

<span data-ttu-id="d9a03-104">Таблица ComPlus содержит сведения, необходимые для установки приложений COM+.</span><span class="sxs-lookup"><span data-stu-id="d9a03-104">The Complus table contains information needed to install COM+ applications.</span></span>

<span data-ttu-id="d9a03-105">Таблица ComPlus содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="d9a03-105">The Complus table has the following columns.</span></span>



| <span data-ttu-id="d9a03-106">Столбец</span><span class="sxs-lookup"><span data-stu-id="d9a03-106">Column</span></span>      | <span data-ttu-id="d9a03-107">Type</span><span class="sxs-lookup"><span data-stu-id="d9a03-107">Type</span></span>                         | <span data-ttu-id="d9a03-108">Ключ</span><span class="sxs-lookup"><span data-stu-id="d9a03-108">Key</span></span> | <span data-ttu-id="d9a03-109">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="d9a03-109">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="d9a03-110">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="d9a03-110">Component\_</span></span> | [<span data-ttu-id="d9a03-111">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="d9a03-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="d9a03-112">Да</span><span class="sxs-lookup"><span data-stu-id="d9a03-112">Y</span></span>   | <span data-ttu-id="d9a03-113">Нет</span><span class="sxs-lookup"><span data-stu-id="d9a03-113">N</span></span>        |
| <span data-ttu-id="d9a03-114">експтипе</span><span class="sxs-lookup"><span data-stu-id="d9a03-114">ExpType</span></span>     | [<span data-ttu-id="d9a03-115">Integer</span><span class="sxs-lookup"><span data-stu-id="d9a03-115">Integer</span></span>](integer.md)       | <span data-ttu-id="d9a03-116">Нет</span><span class="sxs-lookup"><span data-stu-id="d9a03-116">N</span></span>   | <span data-ttu-id="d9a03-117">Да</span><span class="sxs-lookup"><span data-stu-id="d9a03-117">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d9a03-118">Столбцы</span><span class="sxs-lookup"><span data-stu-id="d9a03-118">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d9a03-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="d9a03-119"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="d9a03-120">Внешний ключ в первом столбце [таблицы Component](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="d9a03-120">An external key into the first column of the [Component table](component-table.md).</span></span> <span data-ttu-id="d9a03-121">Это компонент, содержащий приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="d9a03-121">This is the component that contains the COM+ application.</span></span>

</dd> <dt>

<span data-ttu-id="d9a03-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>експтипе</span><span class="sxs-lookup"><span data-stu-id="d9a03-122"><span id="ExpType"></span><span id="exptype"></span><span id="EXPTYPE"></span>ExpType</span></span>
</dt> <dd>

<span data-ttu-id="d9a03-123">Флаги экспорта, используемые при создании MSI файла.</span><span class="sxs-lookup"><span data-stu-id="d9a03-123">Export flags used during the generation of the .msi file.</span></span> <span data-ttu-id="d9a03-124">Дополнительные сведения см. в документации по COM+ в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d9a03-124">For more information see the COM+ documentation in the Microsoft Windows Software Development Kit (SDK).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9a03-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9a03-125">Remarks</span></span>

<span data-ttu-id="d9a03-126">См. действие [регистеркомплус](registercomplus-action.md) и [действие унрегистеркомплус](unregistercomplus-action.md).</span><span class="sxs-lookup"><span data-stu-id="d9a03-126">See the [RegisterComPlus action](registercomplus-action.md) and [UnregisterComPlus action](unregistercomplus-action.md).</span></span>

<span data-ttu-id="d9a03-127">См. раздел [Установка приложения COM+ с установщик Windows](installing-a-com--application-with-the-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="d9a03-127">See [Installing a COM+ Application with the Windows Installer](installing-a-com--application-with-the-windows-installer.md).</span></span>

## <a name="validation"></a><span data-ttu-id="d9a03-128">Проверка</span><span class="sxs-lookup"><span data-stu-id="d9a03-128">Validation</span></span>

<dl>

[<span data-ttu-id="d9a03-129">ICE03</span><span class="sxs-lookup"><span data-stu-id="d9a03-129">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d9a03-130">ICE06</span><span class="sxs-lookup"><span data-stu-id="d9a03-130">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d9a03-131">ICE32</span><span class="sxs-lookup"><span data-stu-id="d9a03-131">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d9a03-132">ICE66</span><span class="sxs-lookup"><span data-stu-id="d9a03-132">ICE66</span></span>](ice66.md)  
</dl>

 

 



