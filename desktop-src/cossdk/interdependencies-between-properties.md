---
description: Взаимозависимости между свойствами
ms.assetid: 1c7c7c76-ec27-4ee4-a860-24244843a1e5
title: Взаимозависимости между свойствами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6df8015c3fc49e35f5079315f6c056f680ebcc12
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990607"
---
# <a name="interdependencies-between-properties"></a><span data-ttu-id="7a131-103">Взаимозависимости между свойствами</span><span class="sxs-lookup"><span data-stu-id="7a131-103">Interdependencies Between Properties</span></span>

<span data-ttu-id="7a131-104">При задании свойств каталог COM+ применяет некоторую логику согласованности, чтобы обеспечить разумную настройку элементов.</span><span class="sxs-lookup"><span data-stu-id="7a131-104">When you set properties, the COM+ catalog enforces some coherency logic to ensure that you configure elements in a reasonable way.</span></span> <span data-ttu-id="7a131-105">Эту логику можно реализовать двумя способами, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7a131-105">This logic can be implemented in two ways, as follows:</span></span>

-   <span data-ttu-id="7a131-106">**Сборки.**</span><span class="sxs-lookup"><span data-stu-id="7a131-106">**Dependencies.**</span></span> <span data-ttu-id="7a131-107">Внесение некоторых изменений может быть заблокировано, так как другое свойство зависит от конкретного параметра для свойства, которое вы пытаетесь задать.</span><span class="sxs-lookup"><span data-stu-id="7a131-107">You might be blocked from making some changes because another property depends on a particular setting for a property you attempt to set.</span></span> <span data-ttu-id="7a131-108">Например, если для компонента заданы требуемые транзакции атрибута, и при попытке изменить параметр синхронизации на значение нет, то при попытке вызвать функцию [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) создается ошибка, так как транзакции зависят от синхронизации.</span><span class="sxs-lookup"><span data-stu-id="7a131-108">For example, if a component is set with the attribute Transactions Required and if you then attempt to change the Synchronization setting to None, an error is generated when you attempt to call [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) because transactions depend on synchronization.</span></span>
-   <span data-ttu-id="7a131-109">**Побочные эффекты.**</span><span class="sxs-lookup"><span data-stu-id="7a131-109">**Side effects.**</span></span> <span data-ttu-id="7a131-110">Некоторые свойства могут быть изменены без их явного задания.</span><span class="sxs-lookup"><span data-stu-id="7a131-110">Some properties might be changed for you without your explicitly setting them.</span></span> <span data-ttu-id="7a131-111">Например, если установить компонент с необходимыми транзакциями атрибута, для параметра синхронизация будет задано значение обязательно.</span><span class="sxs-lookup"><span data-stu-id="7a131-111">For example, if you set a component with the attribute Transactions Required, Synchronization will be set to Required as well.</span></span> <span data-ttu-id="7a131-112">На самом деле это перевернутая сторона зависимостей — одно свойство имеет приоритет над другим, а его зависимость выражается с помощью первого задания вторичного свойства и последующей блокировки изменений.</span><span class="sxs-lookup"><span data-stu-id="7a131-112">This is really the flip side of dependencies—one property takes precedence over another, and its dependency is expressed through first setting the secondary property and then blocking changes to it.</span></span>

<span data-ttu-id="7a131-113">В списке свойств, предоставляемых элементами коллекции, все перечисленные в коллекции [администрирования com+](com--administration-collections.md), зависимости и побочные эффекты задаются для каждого свойства.</span><span class="sxs-lookup"><span data-stu-id="7a131-113">In the list of properties exposed by items in a collection, all listed in [COM+ Administration Collections](com--administration-collections.md), the dependencies and side effects are stated for each property.</span></span> <span data-ttu-id="7a131-114">При настройке приложений и компонентов COM+ необходимо знать, какие ограничения накладываются на конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7a131-114">When you configure COM+ applications and components, you should be aware of what constraints are imposed on configurations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a131-115">См. также</span><span class="sxs-lookup"><span data-stu-id="7a131-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a131-116">Получение и задание свойств</span><span class="sxs-lookup"><span data-stu-id="7a131-116">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="7a131-117">Запрос доступных свойств</span><span class="sxs-lookup"><span data-stu-id="7a131-117">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="7a131-118">Сохранение или Отмена изменений</span><span class="sxs-lookup"><span data-stu-id="7a131-118">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



