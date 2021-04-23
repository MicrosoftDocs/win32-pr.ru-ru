---
description: ICE62 выполняет расширенные проверки в таблице Исолатедкомпонент для данных, которые могут привести к непредвиденному поведению.
ms.assetid: 649d3989-8121-4303-aa3e-63bc6649f445
title: ICE62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245e205b2d004efa99ae1605ff5255ef69834a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663847"
---
# <a name="ice62"></a><span data-ttu-id="d77f9-103">ICE62</span><span class="sxs-lookup"><span data-stu-id="d77f9-103">ICE62</span></span>

<span data-ttu-id="d77f9-104">ICE62 выполняет расширенные проверки в [таблице исолатедкомпонент](isolatedcomponent-table.md) для данных, которые могут привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="d77f9-104">ICE62 performs extensive checks on the [IsolatedComponent table](isolatedcomponent-table.md) for data that may cause unexpected behavior.</span></span>

<span data-ttu-id="d77f9-105">Сбой исправления ошибки, обнаруженной ICE62, может привести к сбою системы изолированных компонентов различными способами.</span><span class="sxs-lookup"><span data-stu-id="d77f9-105">Failure to fix an error reported by ICE62 can result in a failure of the isolated component system in a wide variety of ways.</span></span> <span data-ttu-id="d77f9-106">Например, если бит Шареддллрефкаунт не задан для общего компонента, регистрация для компонента может быть удалена, когда другое приложение использует это значение ComponentId и удалено.</span><span class="sxs-lookup"><span data-stu-id="d77f9-106">For example, if the SharedDllRefCount bit is not set for a shared component, the registration for the component could be removed when another application uses that ComponentId and is uninstalled.</span></span>

## <a name="result"></a><span data-ttu-id="d77f9-107">Результат</span><span class="sxs-lookup"><span data-stu-id="d77f9-107">Result</span></span>

<span data-ttu-id="d77f9-108">ICE62 отправляет предупреждение или ошибку при обнаружении в таблице Исолатедкомпонент данных, которые могут привести к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="d77f9-108">ICE62 posts a warning or error when it finds data in the IsolatedComponent table that may produce unexpected behavior.</span></span>

## <a name="example"></a><span data-ttu-id="d77f9-109">Пример</span><span class="sxs-lookup"><span data-stu-id="d77f9-109">Example</span></span>

<span data-ttu-id="d77f9-110">ICE62 сообщает о следующих ошибках и предупреждении для приведенных примеров.</span><span class="sxs-lookup"><span data-stu-id="d77f9-110">ICE62 reports the following errors and warning for the examples shown.</span></span>

``` syntax
The component 'Component2' is listed as an isolated application 
component in the IsolatedComponent table, but the key path is not a file.
```

<span data-ttu-id="d77f9-111">Component2 указан в качестве компонента приложения для изоляции Component1.</span><span class="sxs-lookup"><span data-stu-id="d77f9-111">Component2 is listed as the application component for the isolation of component1.</span></span> <span data-ttu-id="d77f9-112">Однако Component2 имеет путь к разделу реестра и не предоставляет допустимый путь к исполняемому файлу, используемый для изоляции компонента.</span><span class="sxs-lookup"><span data-stu-id="d77f9-112">However, Component2 has a registry key path, and does not provide a valid executable path to use to isolate the component.</span></span>

<span data-ttu-id="d77f9-113">Чтобы устранить эту ошибку, используйте другой компонент в качестве приложения для изолированного компонента Component1.</span><span class="sxs-lookup"><span data-stu-id="d77f9-113">To fix this error, use a different component as the application for the isolated component Component1.</span></span>

``` syntax
The component 'Component1' is listed as an isolated shared component in the 
IsolatedComponent table, but is not marked with the SharedDllRefCount component attribute.
```

<span data-ttu-id="d77f9-114">Component1 указан как изолированный общий компонент, но не имеет установленного бита Шареддллрефкаунт.</span><span class="sxs-lookup"><span data-stu-id="d77f9-114">Component1 is listed as an isolated shared component, but does not have the SharedDllRefCount bit set.</span></span> <span data-ttu-id="d77f9-115">Это может привести к неправильному времени существования компонента.</span><span class="sxs-lookup"><span data-stu-id="d77f9-115">This could result in the lifetime of the component being incorrect.</span></span> <span data-ttu-id="d77f9-116">Если другое приложение использует этот компонент (изолированное или не установлено) и удаляется, регистрация для компонента будет удалена, но изолированная копия этого приложения останется.</span><span class="sxs-lookup"><span data-stu-id="d77f9-116">If another application uses this component (isolated or not) and is uninstalled, the registration for the component is removed but this application's isolated copy remains.</span></span> <span data-ttu-id="d77f9-117">Это приводит к проблемам с восстановлением и удалением.</span><span class="sxs-lookup"><span data-stu-id="d77f9-117">This causes repair and uninstall problems.</span></span>

<span data-ttu-id="d77f9-118">Чтобы устранить эту ошибку, установите бит Шареддллрефкаунт для компонента.</span><span class="sxs-lookup"><span data-stu-id="d77f9-118">To fix this error, set the SharedDllRefCount bit for the component.</span></span>

``` syntax
The isolated shared component 'Component1' is not installed by the same feature as 
(or a parent feature of) its isolated application component 'Component2' (which is installed by feature 'Feature2').
```

<span data-ttu-id="d77f9-119">Component1 и Component2 устанавливаются различными компонентами.</span><span class="sxs-lookup"><span data-stu-id="d77f9-119">Component1 and Component2 are installed by different features.</span></span> <span data-ttu-id="d77f9-120">Component1 устанавливается с помощью Feature1, а Component2 устанавливается с помощью Feature2.</span><span class="sxs-lookup"><span data-stu-id="d77f9-120">Component1 is installed by Feature1, and Component2 is installed by Feature2.</span></span> <span data-ttu-id="d77f9-121">Feature1 не является родителем Feature2, поэтому приложение может быть установлено, но не является изолированным компонентом, нарушая изоляцию.</span><span class="sxs-lookup"><span data-stu-id="d77f9-121">Feature1 is not a parent of Feature2, hence it is possible for the application to be installed but not the isolated component, breaking the isolation.</span></span>

<span data-ttu-id="d77f9-122">Чтобы устранить эту ошибку, добавьте запись в таблицу Феатурекомпонентс, связывающую Component1 с той же функцией, что и (или родительская функция) функции, устанавливающей Component2.</span><span class="sxs-lookup"><span data-stu-id="d77f9-122">To fix this error, add an entry to the FeatureComponents table linking Component1 to the same feature as (or a parent feature of) the feature that installs Component2.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' (referenced in the IsolatedComponent table) 
is conditionalized. Isolated shared component conditions should never change from TRUE to FALSE after the first install of the product.
```

<span data-ttu-id="d77f9-123">Component1 имеет условие в таблице Component.</span><span class="sxs-lookup"><span data-stu-id="d77f9-123">Component1 has a condition in the Component table.</span></span> <span data-ttu-id="d77f9-124">Если это условие когда-либо изменится со значения TRUE на FALSE в течение времени существования установки на компьютере, то изолированный компонент может быть потерян без сведений о регистрации.</span><span class="sxs-lookup"><span data-stu-id="d77f9-124">If this condition ever changes from TRUE to FALSE during the lifetime of an installation on a computer, the isolated component could be orphaned without registration information.</span></span>

<span data-ttu-id="d77f9-125">Чтобы устранить это предупреждение, удалите условие или создайте условие, чтобы оно никогда не изменялось с TRUE на FALSE.</span><span class="sxs-lookup"><span data-stu-id="d77f9-125">To fix this warning, remove the condition, or author the condition so that it can never change from TRUE to FALSE.</span></span>

``` syntax
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component2') that are installed to the directory 'TARGETDIR'.
WARNING: The isolated shared component 'Component1' is shared by multiple applications 
(including 'Component3') that are installed to the directory 'TARGETDIR'.
```

<span data-ttu-id="d77f9-126">Component1 изолированы как для Component2, так и для Component3, а два компонента также устанавливаются в один и тот же каталог.</span><span class="sxs-lookup"><span data-stu-id="d77f9-126">Component1 is isolated for both Component2 and Component3, and the two components are also installed to the same directory.</span></span> <span data-ttu-id="d77f9-127">Приложения совместно используют изолированный компонент, но если одно приложение удаляется, общий компонент удаляется, а другие приложения теряют изолированный компонент.</span><span class="sxs-lookup"><span data-stu-id="d77f9-127">The applications share an isolated component, but if one application is removed the shared component is removed as well causing the other applications to lose the isolated component.</span></span>

<span data-ttu-id="d77f9-128">Чтобы устранить это предупреждение, установите приложения в разные каталоги или проверьте, действительно ли для некоторых приложений требуется изолированный компонент.</span><span class="sxs-lookup"><span data-stu-id="d77f9-128">To fix this warning, install the applications to different directories or check whether some of the applications truly require an isolated component.</span></span>

[<span data-ttu-id="d77f9-129">Таблица Исолатедкомпонент</span><span class="sxs-lookup"><span data-stu-id="d77f9-129">IsolatedComponent Table</span></span>](isolatedcomponent-table.md)



| <span data-ttu-id="d77f9-130">\_Общий компонент</span><span class="sxs-lookup"><span data-stu-id="d77f9-130">Component\_Shared</span></span> | <span data-ttu-id="d77f9-131">\_Приложение компонента</span><span class="sxs-lookup"><span data-stu-id="d77f9-131">Component\_Application</span></span> |
|-------------------|------------------------|
| <span data-ttu-id="d77f9-132">Component1</span><span class="sxs-lookup"><span data-stu-id="d77f9-132">Component1</span></span>        | <span data-ttu-id="d77f9-133">Component2</span><span class="sxs-lookup"><span data-stu-id="d77f9-133">Component2</span></span>             |
| <span data-ttu-id="d77f9-134">Component1</span><span class="sxs-lookup"><span data-stu-id="d77f9-134">Component1</span></span>        | <span data-ttu-id="d77f9-135">Component3</span><span class="sxs-lookup"><span data-stu-id="d77f9-135">Component3</span></span>             |



 

[<span data-ttu-id="d77f9-136">Таблица компонентов</span><span class="sxs-lookup"><span data-stu-id="d77f9-136">Component Table</span></span>](component-table.md)



| <span data-ttu-id="d77f9-137">Компонент</span><span class="sxs-lookup"><span data-stu-id="d77f9-137">Component</span></span>  | <span data-ttu-id="d77f9-138">ComponentId</span><span class="sxs-lookup"><span data-stu-id="d77f9-138">ComponentId</span></span> | <span data-ttu-id="d77f9-139">Каталог\_</span><span class="sxs-lookup"><span data-stu-id="d77f9-139">Directory\_</span></span> | <span data-ttu-id="d77f9-140">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d77f9-140">Attributes</span></span> | <span data-ttu-id="d77f9-141">Условие</span><span class="sxs-lookup"><span data-stu-id="d77f9-141">Condition</span></span>   | <span data-ttu-id="d77f9-142">Путь</span><span class="sxs-lookup"><span data-stu-id="d77f9-142">KeyPath</span></span>   |
|------------|-------------|-------------|------------|-------------|-----------|
| <span data-ttu-id="d77f9-143">Component1</span><span class="sxs-lookup"><span data-stu-id="d77f9-143">Component1</span></span> |             | <span data-ttu-id="d77f9-144">Dir1</span><span class="sxs-lookup"><span data-stu-id="d77f9-144">Dir1</span></span>        | <span data-ttu-id="d77f9-145">0</span><span class="sxs-lookup"><span data-stu-id="d77f9-145">0</span></span>          | <span data-ttu-id="d77f9-146">микондитион</span><span class="sxs-lookup"><span data-stu-id="d77f9-146">MYCONDITION</span></span> | <span data-ttu-id="d77f9-147">Файл1</span><span class="sxs-lookup"><span data-stu-id="d77f9-147">File1</span></span>     |
| <span data-ttu-id="d77f9-148">Component2</span><span class="sxs-lookup"><span data-stu-id="d77f9-148">Component2</span></span> |             | <span data-ttu-id="d77f9-149">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="d77f9-149">TARGETDIR</span></span>   | <span data-ttu-id="d77f9-150">4</span><span class="sxs-lookup"><span data-stu-id="d77f9-150">4</span></span>          |             | <span data-ttu-id="d77f9-151">Registry2</span><span class="sxs-lookup"><span data-stu-id="d77f9-151">Registry2</span></span> |
| <span data-ttu-id="d77f9-152">Component3</span><span class="sxs-lookup"><span data-stu-id="d77f9-152">Component3</span></span> |             | <span data-ttu-id="d77f9-153">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="d77f9-153">TARGETDIR</span></span>   | <span data-ttu-id="d77f9-154">0</span><span class="sxs-lookup"><span data-stu-id="d77f9-154">0</span></span>          |             | <span data-ttu-id="d77f9-155">Файл3</span><span class="sxs-lookup"><span data-stu-id="d77f9-155">File3</span></span>     |



 

[<span data-ttu-id="d77f9-156">феатурекомпонентстабле</span><span class="sxs-lookup"><span data-stu-id="d77f9-156">FeatureComponentsTable</span></span>](featurecomponents-table.md)



| <span data-ttu-id="d77f9-157">Функция\_</span><span class="sxs-lookup"><span data-stu-id="d77f9-157">Feature\_</span></span> | <span data-ttu-id="d77f9-158">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="d77f9-158">Component\_</span></span> |
|-----------|-------------|
| <span data-ttu-id="d77f9-159">Feature1</span><span class="sxs-lookup"><span data-stu-id="d77f9-159">Feature1</span></span>  | <span data-ttu-id="d77f9-160">Component1</span><span class="sxs-lookup"><span data-stu-id="d77f9-160">Component1</span></span>  |
| <span data-ttu-id="d77f9-161">Feature2</span><span class="sxs-lookup"><span data-stu-id="d77f9-161">Feature2</span></span>  | <span data-ttu-id="d77f9-162">Component2</span><span class="sxs-lookup"><span data-stu-id="d77f9-162">Component2</span></span>  |
| <span data-ttu-id="d77f9-163">Feature1</span><span class="sxs-lookup"><span data-stu-id="d77f9-163">Feature1</span></span>  | <span data-ttu-id="d77f9-164">Component3</span><span class="sxs-lookup"><span data-stu-id="d77f9-164">Component3</span></span>  |



 

<span data-ttu-id="d77f9-165">[Таблица компонентов](feature-table.md) (частичная)</span><span class="sxs-lookup"><span data-stu-id="d77f9-165">[Feature Table](feature-table.md) (partial)</span></span>



| <span data-ttu-id="d77f9-166">Функция</span><span class="sxs-lookup"><span data-stu-id="d77f9-166">Feature</span></span>  | <span data-ttu-id="d77f9-167">\_Родительский компонент функции</span><span class="sxs-lookup"><span data-stu-id="d77f9-167">Feature\_Parent</span></span> |
|----------|-----------------|
| <span data-ttu-id="d77f9-168">Feature1</span><span class="sxs-lookup"><span data-stu-id="d77f9-168">Feature1</span></span> |                 |
| <span data-ttu-id="d77f9-169">Feature2</span><span class="sxs-lookup"><span data-stu-id="d77f9-169">Feature2</span></span> |                 |



 

## <a name="related-topics"></a><span data-ttu-id="d77f9-170">См. также</span><span class="sxs-lookup"><span data-stu-id="d77f9-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d77f9-171">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="d77f9-171">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



