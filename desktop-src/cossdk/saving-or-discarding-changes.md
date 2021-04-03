---
description: Сохранение или Отмена изменений
ms.assetid: eba4e794-0929-450c-a172-6de6c2f2f2c4
title: Сохранение или Отмена изменений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4946574facd0d41d68f4de8cf2f2f48410eb6e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895617"
---
# <a name="saving-or-discarding-changes"></a><span data-ttu-id="f0069-103">Сохранение или Отмена изменений</span><span class="sxs-lookup"><span data-stu-id="f0069-103">Saving or Discarding Changes</span></span>

<span data-ttu-id="f0069-104">При задании свойств элемента никакие изменения фактически не записываются в каталог COM+, пока не будут явно сохранены изменения.</span><span class="sxs-lookup"><span data-stu-id="f0069-104">When you set properties on an item, no changes are actually recorded to the COM+ catalog until you explicitly save changes.</span></span> <span data-ttu-id="f0069-105">Это делается с помощью метода [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) в объекте [**комадминкаталогколлектион**](comadmincatalogcollection.md) для коллекции, содержащей элемент.</span><span class="sxs-lookup"><span data-stu-id="f0069-105">You do this using the [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object for the collection containing the item.</span></span>

<span data-ttu-id="f0069-106">Если вы хотите отменить изменения, которые еще не были зафиксированы, можно вызвать метод [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) для объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f0069-106">If you want to discard changes that have not yet been committed, you can call the [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) method on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span> <span data-ttu-id="f0069-107">Это считывает все постоянные данные из каталога COM+ для всех элементов в коллекции, фактически удаляя все ожидающие изменения.</span><span class="sxs-lookup"><span data-stu-id="f0069-107">This reads in all persistent data from the COM+ catalog for all items in the collection, effectively deleting any pending changes.</span></span>

<span data-ttu-id="f0069-108">При использовании [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)все несоответствия в выбранных параметрах свойств приводят к ошибке, и **SaveChanges** не может записать объект, который вернул ошибку.</span><span class="sxs-lookup"><span data-stu-id="f0069-108">When you use [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), any inconsistencies in property settings that you have chosen result in an error, and **SaveChanges** fails to write the object that returned the error.</span></span> <span data-ttu-id="f0069-109">Все свойства данного элемента либо записываются, либо не могут быть записаны как единое целое.</span><span class="sxs-lookup"><span data-stu-id="f0069-109">All properties on a given item either are written or fail to be written as a whole.</span></span>

<span data-ttu-id="f0069-110">Однако при возникновении ошибок записи они могут не быть из-за несовместимых параметров. возможно, произошли другие ошибки.</span><span class="sxs-lookup"><span data-stu-id="f0069-110">However, when write errors occur, they might not be due to incompatible settings; some other failure might have occurred.</span></span> <span data-ttu-id="f0069-111">Необходимо проверить сведения о сбое.</span><span class="sxs-lookup"><span data-stu-id="f0069-111">You need to inspect the details of the failure to be certain.</span></span> <span data-ttu-id="f0069-112">Дополнительные сведения см. в разделе [Обработка ошибок администрирования com+](handling-com--administration-errors.md) и [взаимозависимости между свойствами](interdependencies-between-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f0069-112">For more information, see [Handling COM+ Administration Errors](handling-com--administration-errors.md) and [Interdependencies Between Properties](interdependencies-between-properties.md).</span></span>

<span data-ttu-id="f0069-113">Как правило, чем больше изменений вы пытаетесь сохранить одновременно, в частности, изменения в нескольких объектах, тем больше вероятность, что вы получаете сообщение об ошибке, а тем сложнее.</span><span class="sxs-lookup"><span data-stu-id="f0069-113">As a general rule, the more changes you attempt to save at once, particularly changes to multiple objects, the more likely you are to get an error and the more difficult it is to track down.</span></span>

<span data-ttu-id="f0069-114">Кроме того, между вызовами функций [**заполнения**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) и [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges)нет блокировки на элементы в коллекции; состязание возможно.</span><span class="sxs-lookup"><span data-stu-id="f0069-114">Additionally, between calls to [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges), you do not have a lock on the items in the collection; contention is possible.</span></span> <span data-ttu-id="f0069-115">Дополнительные сведения см. в разделе [Получение и Настройка свойств](getting-and-setting-properties.md).</span><span class="sxs-lookup"><span data-stu-id="f0069-115">For more details, see [Getting and Setting Properties](getting-and-setting-properties.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f0069-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f0069-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0069-117">Получение и задание свойств</span><span class="sxs-lookup"><span data-stu-id="f0069-117">Getting and Setting Properties</span></span>](getting-and-setting-properties.md)
</dt> <dt>

[<span data-ttu-id="f0069-118">Взаимозависимости между свойствами</span><span class="sxs-lookup"><span data-stu-id="f0069-118">Interdependencies Between Properties</span></span>](interdependencies-between-properties.md)
</dt> <dt>

[<span data-ttu-id="f0069-119">Запрос доступных свойств</span><span class="sxs-lookup"><span data-stu-id="f0069-119">Querying for Available Properties</span></span>](querying-for-available-properties.md)
</dt> </dl>

 

 



