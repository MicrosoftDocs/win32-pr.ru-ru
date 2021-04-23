---
description: Получение и задание свойств
ms.assetid: 259612e7-70df-4f0f-90bc-766008dfdce7
title: Получение и задание свойств (службы компонентов)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d151b08293cd32a35cd27bdba4dd3a37cdebfa4f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496338"
---
# <a name="getting-and-setting-properties-component-services"></a><span data-ttu-id="f1e14-103">Получение и задание свойств (службы компонентов)</span><span class="sxs-lookup"><span data-stu-id="f1e14-103">Getting and Setting Properties (Component Services)</span></span>

<span data-ttu-id="f1e14-104">Прежде чем можно будет читать или записывать определенные свойства, предоставляемые элементом коллекции, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="f1e14-104">Before you can read or write particular properties exposed by an item in a collection, you must take the following steps:</span></span>

1.  <span data-ttu-id="f1e14-105">Получение коллекции.</span><span class="sxs-lookup"><span data-stu-id="f1e14-105">Retrieve the collection.</span></span>
2.  <span data-ttu-id="f1e14-106">Заполните коллекцию данными для чтения из каталога COM+.</span><span class="sxs-lookup"><span data-stu-id="f1e14-106">Populate the collection to read in data for it from the COM+ catalog.</span></span>
3.  <span data-ttu-id="f1e14-107">Получение конкретного элемента в коллекции, представляющего его с помощью объекта из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="f1e14-107">Retrieve the specific item in the collection, representing it with an object from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="f1e14-108">Пример, демонстрирующий эти шаги, см. [в разделе Навигация по иерархии коллекции com+](navigating-the-com--collection-hierarchy.md).</span><span class="sxs-lookup"><span data-stu-id="f1e14-108">For an example that illustrates these steps, see [Navigating the COM+ Collection Hierarchy](navigating-the-com--collection-hierarchy.md).</span></span>

<span data-ttu-id="f1e14-109">Так как определенные свойства могут различаться в зависимости от того, что представляет элемент; то есть элемент, представляющий компонент, имеет разные свойства, чем одно, представляющее приложение COM+.</span><span class="sxs-lookup"><span data-stu-id="f1e14-109">Because the particular properties exposed can vary depending on what the item represents; that is, an item representing a component has different properties than one representing a COM+ application.</span></span> <span data-ttu-id="f1e14-110">Задайте любое из этих свойств, используя одно универсальное свойство, свойство Value, в [**комадминкаталогобжект**](comadmincatalogobject.md).</span><span class="sxs-lookup"><span data-stu-id="f1e14-110">Set any of these properties using a single generic property, the Value property, on [**COMAdminCatalogObject**](comadmincatalogobject.md).</span></span>

<span data-ttu-id="f1e14-111">Свойство Value позволяет получать или задавать любое конкретное именованное свойство, предоставляемое элементом, возвращая значение для именованного свойства при получении, а также при задании имени и значения.</span><span class="sxs-lookup"><span data-stu-id="f1e14-111">The Value property enables you to get or set any specific named property exposed by an item, returning a value for a named property when getting, and taking a name and value when setting.</span></span>

<span data-ttu-id="f1e14-112">Изменения фактически не записываются в каталог COM+, пока вы явно не сохраните изменения с помощью метода [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f1e14-112">No changes are actually recorded to the COM+ catalog until you explicitly save changes using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="f1e14-113">Ожидающие изменения для всех свойств всех элементов в данной коллекции сохраняются одновременно.</span><span class="sxs-lookup"><span data-stu-id="f1e14-113">Pending changes for all properties on all items in a given collection are saved all at once.</span></span> <span data-ttu-id="f1e14-114">Дополнительные сведения см. в разделе [Сохранение или удаление изменений](saving-or-discarding-changes.md).</span><span class="sxs-lookup"><span data-stu-id="f1e14-114">For details, see [Saving or Discarding Changes](saving-or-discarding-changes.md).</span></span>

<span data-ttu-id="f1e14-115">Не все внесенные изменения будут приняты.</span><span class="sxs-lookup"><span data-stu-id="f1e14-115">Not all changes that you make will be accepted.</span></span> <span data-ttu-id="f1e14-116">Каталог COM+ применяет некоторую логику согласования, чтобы обеспечить разумную настройку.</span><span class="sxs-lookup"><span data-stu-id="f1e14-116">The COM+ catalog enforces some coherency logic to ensure that you configure things in a reasonable way.</span></span> <span data-ttu-id="f1e14-117">Кроме того, при изменении некоторых свойств другие могут автоматически измениться с помощью той же логики согласования.</span><span class="sxs-lookup"><span data-stu-id="f1e14-117">Additionally, when you change some properties, others might change automatically by the same coherency logic.</span></span> <span data-ttu-id="f1e14-118">Эти эффекты отображаются при попытке сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="f1e14-118">These effects show up when you attempt to save changes.</span></span>

> [!Note]  
> <span data-ttu-id="f1e14-119">Может возникнуть состязание с другим модулем записи в каталог COM+.</span><span class="sxs-lookup"><span data-stu-id="f1e14-119">It is possible for you to be in contention with another writer to the COM+ catalog.</span></span> <span data-ttu-id="f1e14-120">Между вызовами функций [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) для заданной коллекции не существует блокировки этих данных в каталоге.</span><span class="sxs-lookup"><span data-stu-id="f1e14-120">Between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) for a given collection, you do not have a lock on any of that data in the catalog.</span></span> <span data-ttu-id="f1e14-121">Несколько сторон могут одновременно настраивать элементы в определенной коллекции и могут полагаться на них при сохранении изменений.</span><span class="sxs-lookup"><span data-stu-id="f1e14-121">Multiple parties may simultaneously be configuring items in a given collection and could be contending when they save changes.</span></span> <span data-ttu-id="f1e14-122">Это означает, что кто-то другой может изменить параметры объекта до или после того, как запускают какую-либо программу с помощью объектов Комадмин или с помощью средства администрирования "службы компонентов" локально или удаленно.</span><span class="sxs-lookup"><span data-stu-id="f1e14-122">This means that someone else might change settings on an object before or after you do, either running some kind of program using the COMAdmin objects or using the Component Services administrative tool, either locally or remotely.</span></span> <span data-ttu-id="f1e14-123">Общее правило с записью объектов в каталог состоит в том, что все свойства объекта записываются одновременно.</span><span class="sxs-lookup"><span data-stu-id="f1e14-123">The general rule with writing objects on the catalog is that all properties on an object are written at once.</span></span> <span data-ttu-id="f1e14-124">То есть последний модуль записи WINS — объект сохраняется в каталоге точно так же, как и последний настроенный модуль записи.</span><span class="sxs-lookup"><span data-stu-id="f1e14-124">That is, the last writer wins—the object is saved in the catalog precisely as the last writer configured it.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f1e14-125">См. также</span><span class="sxs-lookup"><span data-stu-id="f1e14-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1e14-126">Взаимозависимости между свойствами</span><span class="sxs-lookup"><span data-stu-id="f1e14-126">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="f1e14-127">Запрос доступных свойств</span><span class="sxs-lookup"><span data-stu-id="f1e14-127">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> <dt>

[<span data-ttu-id="f1e14-128">Сохранение или Отмена изменений</span><span class="sxs-lookup"><span data-stu-id="f1e14-128">Saving or Discarding Changes</span></span>](saving-or-discarding-changes.md)
</dt> </dl>

 

 



