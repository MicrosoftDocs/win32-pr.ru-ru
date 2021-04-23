---
description: Обращается к данным, хранящимся в каталоге COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Класс Комадминкаталог (Комадмин. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496464"
---
# <a name="comadmincatalog-class"></a><span data-ttu-id="96773-103">Класс Комадминкаталог</span><span class="sxs-lookup"><span data-stu-id="96773-103">COMAdminCatalog class</span></span>

<span data-ttu-id="96773-104">Обращается к данным, хранящимся в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="96773-104">Accesses the data that is stored in the COM+ catalog.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="96773-105">Когда следует реализовывать</span><span class="sxs-lookup"><span data-stu-id="96773-105">When to implement</span></span>

<span data-ttu-id="96773-106">Этот класс реализуется с помощью COM+.</span><span class="sxs-lookup"><span data-stu-id="96773-106">This class is implemented by COM+.</span></span>



| <span data-ttu-id="96773-107">Требование</span><span class="sxs-lookup"><span data-stu-id="96773-107">Requirement</span></span> | <span data-ttu-id="96773-108">Значение</span><span class="sxs-lookup"><span data-stu-id="96773-108">Value</span></span> |
|------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96773-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="96773-109">CLSID</span></span>      | <span data-ttu-id="96773-110">\_КОМАДМИНКАТАЛОГ CLSID</span><span class="sxs-lookup"><span data-stu-id="96773-110">CLSID\_COMAdminCatalog</span></span>                                                                                            |
| <span data-ttu-id="96773-111">ProgID:</span><span class="sxs-lookup"><span data-stu-id="96773-111">ProgID</span></span>     | <span data-ttu-id="96773-112">L "Комадмин. Комадминкаталог"</span><span class="sxs-lookup"><span data-stu-id="96773-112">L"COMAdmin.COMAdminCatalog"</span></span>                                                                                       |
| <span data-ttu-id="96773-113">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="96773-113">Interfaces</span></span> | [<span data-ttu-id="96773-114">**икомадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="96773-114">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [<span data-ttu-id="96773-115">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="96773-115">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a><span data-ttu-id="96773-116">Назначение</span><span class="sxs-lookup"><span data-stu-id="96773-116">When to use</span></span>

<span data-ttu-id="96773-117">Объекты, созданные из класса **комадминкаталог** , используются для запуска программного доступа к данным конфигурации com+, хранящимся в каталоге COM+.</span><span class="sxs-lookup"><span data-stu-id="96773-117">You use objects created from the **COMAdminCatalog** class to begin programmatic access to COM+ configuration data stored in the COM+ catalog.</span></span> <span data-ttu-id="96773-118">Эти сведения полагаются на папки и элементы в дереве консоли средства администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="96773-118">This information underlies the folders and items in the console tree of the Component Services administration tool.</span></span> <span data-ttu-id="96773-119">Класс **комадминкаталог** позволяет получать доступ к коллекциям в каталоге, устанавливать приложения и компоненты COM+, запускать и прекращать работу служб, а также подключаться к удаленным серверам и администрировать их.</span><span class="sxs-lookup"><span data-stu-id="96773-119">The **COMAdminCatalog** class enables you to access collections in the catalog, install COM+ applications and components, start and stop services, and connect to and administer remote servers.</span></span>

<span data-ttu-id="96773-120">Папки в средстве администрирования служб компонентов соответствуют коллекциям в каталоге, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="96773-120">Folders in the Component Services administration tool correspond to collections in the catalog, which you can represent by using objects created from the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) class.</span></span> <span data-ttu-id="96773-121">Элементы в папках соответствуют элементам в коллекциях, которые можно представить с помощью объектов, созданных из класса [**комадминкаталогобжект**](comadmincatalogobject.md) .</span><span class="sxs-lookup"><span data-stu-id="96773-121">Items in the folders correspond to items in the collections, which you can represent by using objects created from the [**COMAdminCatalogObject**](comadmincatalogobject.md) class.</span></span>

<span data-ttu-id="96773-122">Не все коллекции и элементы, предоставляемые через [**комадминкаталогколлектион**](comadmincatalogcollection.md) и [**комадминкаталогобжект**](comadmincatalogobject.md) , доступны в средстве администрирования служб компонентов.</span><span class="sxs-lookup"><span data-stu-id="96773-122">Not all of the collections and items exposed through [**COMAdminCatalogCollection**](comadmincatalogcollection.md) and [**COMAdminCatalogObject**](comadmincatalogobject.md) are available in the Component Services administration tool.</span></span>

<span data-ttu-id="96773-123">Сведения о конкретных коллекциях и их свойствах см. в разделе [com+ Administration Collections](com--administration-collections.md).</span><span class="sxs-lookup"><span data-stu-id="96773-123">For information regarding specific collections and their properties, see [COM+ Administration Collections](com--administration-collections.md).</span></span>

<span data-ttu-id="96773-124">Общие сведения о программном администрировании COM+ см. в разделе [Автоматизация администрирования com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="96773-124">For an introduction to programmatic administration of COM+, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="96773-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96773-125">Remarks</span></span>

<span data-ttu-id="96773-126">Чтобы создать этот объект, вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="96773-126">To create this object, call [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="96773-127">Чтобы использовать этот класс из Visual Basic Майкрософт, добавьте ссылку на библиотеку типов администрирования COM+.</span><span class="sxs-lookup"><span data-stu-id="96773-127">To use this class from Microsoft Visual Basic, add a reference to the COM+ Admin Type Library.</span></span> <span data-ttu-id="96773-128">Объект Комадминкаталог можно объявить с помощью "Комадмин. Комадминкаталог" в качестве имени класса.</span><span class="sxs-lookup"><span data-stu-id="96773-128">A COMAdminCatalog object can be declared using "COMAdmin.COMAdminCatalog" as the class name.</span></span>

<span data-ttu-id="96773-129">В COM+ 1,5, выпущенном в Windows XP, класс **комадминкаталог** реализует интерфейс [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) .</span><span class="sxs-lookup"><span data-stu-id="96773-129">In COM+ 1.5, released with Windows XP, the **COMAdminCatalog** class implements the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface.</span></span> <span data-ttu-id="96773-130">Однако в COM+ 1,0, выпущенном с Windows 2000, класс **комадминкаталог** реализует только интерфейс [**икомадминкаталог**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .</span><span class="sxs-lookup"><span data-stu-id="96773-130">However, in COM+ 1.0, released with Windows 2000, the **COMAdminCatalog** class implements only the [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="96773-131">Требования</span><span class="sxs-lookup"><span data-stu-id="96773-131">Requirements</span></span>



| <span data-ttu-id="96773-132">Требование</span><span class="sxs-lookup"><span data-stu-id="96773-132">Requirement</span></span> | <span data-ttu-id="96773-133">Значение</span><span class="sxs-lookup"><span data-stu-id="96773-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96773-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96773-134">Minimum supported client</span></span><br/> | <span data-ttu-id="96773-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96773-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="96773-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96773-136">Minimum supported server</span></span><br/> | <span data-ttu-id="96773-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="96773-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96773-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="96773-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="96773-139"><dt>Комадмин. h</dt></span><span class="sxs-lookup"><span data-stu-id="96773-139"><dt>ComAdmin.h</dt></span></span> </dl>   |
| <span data-ttu-id="96773-140">IDL</span><span class="sxs-lookup"><span data-stu-id="96773-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96773-141"><dt>Комадмин. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96773-141"><dt>ComAdmin.Idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96773-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96773-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96773-143">**комадминкаталогколлектион**</span><span class="sxs-lookup"><span data-stu-id="96773-143">**COMAdminCatalogCollection**</span></span>](comadmincatalogcollection.md)
</dt> <dt>

[<span data-ttu-id="96773-144">**комадминкаталогобжект**</span><span class="sxs-lookup"><span data-stu-id="96773-144">**COMAdminCatalogObject**</span></span>](comadmincatalogobject.md)
</dt> <dt>

[<span data-ttu-id="96773-145">**икомадминкаталог**</span><span class="sxs-lookup"><span data-stu-id="96773-145">**ICOMAdminCatalog**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[<span data-ttu-id="96773-146">**ICOMAdminCatalog2**</span><span class="sxs-lookup"><span data-stu-id="96773-146">**ICOMAdminCatalog2**</span></span>](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

