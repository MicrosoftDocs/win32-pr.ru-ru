---
description: ICE92 проверяет, что компонент без GUID идентификатора компонента также не указан как постоянный компонент.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910707"
---
# <a name="ice92"></a><span data-ttu-id="55a5b-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="55a5b-103">ICE92</span></span>

<span data-ttu-id="55a5b-104">ICE92 проверяет, что компонент без GUID идентификатора компонента также не указан как постоянный компонент.</span><span class="sxs-lookup"><span data-stu-id="55a5b-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="55a5b-105">Это настраиваемое действие ICE проверяет [таблицу компонентов](component-table.md) на наличие компонентов без [идентификатора GUID](guid.md) , указанных в поле ComponentID, и проверяет, не был ли установлен флаг **мсидбкомпонентаттрибутесперманент** в поле Attributes.</span><span class="sxs-lookup"><span data-stu-id="55a5b-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="55a5b-106">ICE92 также проверяет отсутствие у компонента атрибутов **мсидбкомпонентаттрибутесперманент** и **мсидбкомпонентаттрибутесунинсталлонсуперседенце** .</span><span class="sxs-lookup"><span data-stu-id="55a5b-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="55a5b-107">Если столбец ComponentId имеет значение null, установщик не регистрирует компонент, и компонент не может быть удален или восстановлен с помощью установщика.</span><span class="sxs-lookup"><span data-stu-id="55a5b-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="55a5b-108">Результат</span><span class="sxs-lookup"><span data-stu-id="55a5b-108">Result</span></span>

<span data-ttu-id="55a5b-109">ICE92 отправляет следующую ошибку.</span><span class="sxs-lookup"><span data-stu-id="55a5b-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="55a5b-110">ICE92, ошибка</span><span class="sxs-lookup"><span data-stu-id="55a5b-110">ICE92 error</span></span>                                                          | <span data-ttu-id="55a5b-111">Описание</span><span class="sxs-lookup"><span data-stu-id="55a5b-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a5b-112">Компонент " \[ 1 \] " не имеет ИД компонента и помечен как постоянный.</span><span class="sxs-lookup"><span data-stu-id="55a5b-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="55a5b-113">Запись для этого компонента в таблице Component имеет значение NULL в столбце ComponentId и содержит **мсидбкомпонентаттрибутесперманент** в столбце Attributes.</span><span class="sxs-lookup"><span data-stu-id="55a5b-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="55a5b-114">ICE92 отправляет следующее предупреждение.</span><span class="sxs-lookup"><span data-stu-id="55a5b-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="55a5b-115">Предупреждение ICE92</span><span class="sxs-lookup"><span data-stu-id="55a5b-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="55a5b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="55a5b-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55a5b-117">Компонент " \[ 1 \] " помечен как "постоянный" и "удаление" в случае замены.</span><span class="sxs-lookup"><span data-stu-id="55a5b-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="55a5b-118">Атрибут uninstall-on-reзамены будет проигнорирован, так как компонент является постоянным.</span><span class="sxs-lookup"><span data-stu-id="55a5b-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="55a5b-119">В записи для этого компонента в [таблице Component](component-table.md) указаны атрибуты **мсидбкомпонентаттрибутесперманент** и **мсидбкомпонентаттрибутесунинсталлонсуперседенце** .</span><span class="sxs-lookup"><span data-stu-id="55a5b-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="55a5b-120">Пример</span><span class="sxs-lookup"><span data-stu-id="55a5b-120">Example</span></span>

<span data-ttu-id="55a5b-121">ICE92 сообщает о следующей ошибке в примере:</span><span class="sxs-lookup"><span data-stu-id="55a5b-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="55a5b-122">[Таблица Component](component-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="55a5b-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="55a5b-123">Компонент</span><span class="sxs-lookup"><span data-stu-id="55a5b-123">Component</span></span>  | <span data-ttu-id="55a5b-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="55a5b-124">ComponentId</span></span> | <span data-ttu-id="55a5b-125">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="55a5b-125">Directory\_</span></span> | <span data-ttu-id="55a5b-126">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="55a5b-126">Attributes</span></span> | <span data-ttu-id="55a5b-127">Путь</span><span class="sxs-lookup"><span data-stu-id="55a5b-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="55a5b-128">Component1</span><span class="sxs-lookup"><span data-stu-id="55a5b-128">Component1</span></span> |             | <span data-ttu-id="55a5b-129">Каталог а</span><span class="sxs-lookup"><span data-stu-id="55a5b-129">DirectoryA</span></span>  | <span data-ttu-id="55a5b-130">16</span><span class="sxs-lookup"><span data-stu-id="55a5b-130">16</span></span>         | <span data-ttu-id="55a5b-131">Файл а</span><span class="sxs-lookup"><span data-stu-id="55a5b-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="55a5b-132">См. также</span><span class="sxs-lookup"><span data-stu-id="55a5b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55a5b-133">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="55a5b-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



