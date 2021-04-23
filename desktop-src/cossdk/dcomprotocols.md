---
description: Содержит список протоколов, используемых DCOM. Он содержит объект для каждого протокола.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Коллекция Дкомпротоколс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496164"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="b1873-104">Коллекция Дкомпротоколс</span><span class="sxs-lookup"><span data-stu-id="b1873-104">DCOMProtocols collection</span></span>

<span data-ttu-id="b1873-105">Содержит список протоколов, используемых DCOM.</span><span class="sxs-lookup"><span data-stu-id="b1873-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="b1873-106">Он содержит объект для каждого протокола.</span><span class="sxs-lookup"><span data-stu-id="b1873-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="b1873-107">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="b1873-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="b1873-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="b1873-108">Members</span></span>

<span data-ttu-id="b1873-109">Коллекция **дкомпротоколс** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="b1873-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="b1873-110">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="b1873-110">Related Collections</span></span>

<span data-ttu-id="b1873-111">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="b1873-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="b1873-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="b1873-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="b1873-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="b1873-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="b1873-114">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="b1873-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="b1873-115">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="b1873-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="b1873-116">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="b1873-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="b1873-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="b1873-117">Properties</span></span>

<span data-ttu-id="b1873-118">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="b1873-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="b1873-119">Name</span><span class="sxs-lookup"><span data-stu-id="b1873-119">Name</span></span>](#name)
-   [<span data-ttu-id="b1873-120">Заказ</span><span class="sxs-lookup"><span data-stu-id="b1873-120">Order</span></span>](#order)
-   [<span data-ttu-id="b1873-121">протоколкоде</span><span class="sxs-lookup"><span data-stu-id="b1873-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="b1873-122">Имя</span><span class="sxs-lookup"><span data-stu-id="b1873-122">Name</span></span>



| <span data-ttu-id="b1873-123">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1873-123">Entry</span></span> | <span data-ttu-id="b1873-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b1873-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1873-125">Описание</span><span class="sxs-lookup"><span data-stu-id="b1873-125">Description</span></span>    | <span data-ttu-id="b1873-126">Имя протокола.</span><span class="sxs-lookup"><span data-stu-id="b1873-126">The name of the protocol.</span></span> <span data-ttu-id="b1873-127">Это свойство возвращается при вызове метода свойства [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="b1873-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1873-128">Access</span><span class="sxs-lookup"><span data-stu-id="b1873-128">Access</span></span>         | <span data-ttu-id="b1873-129">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1873-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="b1873-130">Тип</span><span class="sxs-lookup"><span data-stu-id="b1873-130">Type</span></span>           | <span data-ttu-id="b1873-131">Строка</span><span class="sxs-lookup"><span data-stu-id="b1873-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="b1873-132">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b1873-132">Default</span></span>        | <span data-ttu-id="b1873-133">"Новый протокол"</span><span class="sxs-lookup"><span data-stu-id="b1873-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="b1873-134">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="b1873-134">Minimum system</span></span> | <span data-ttu-id="b1873-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1873-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="b1873-136">Заказ</span><span class="sxs-lookup"><span data-stu-id="b1873-136">Order</span></span>



| <span data-ttu-id="b1873-137">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1873-137">Entry</span></span> | <span data-ttu-id="b1873-138">Значение</span><span class="sxs-lookup"><span data-stu-id="b1873-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="b1873-139">Описание</span><span class="sxs-lookup"><span data-stu-id="b1873-139">Description</span></span>    | <span data-ttu-id="b1873-140">Порядок, в котором следует использовать протокол.</span><span class="sxs-lookup"><span data-stu-id="b1873-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="b1873-141">Access</span><span class="sxs-lookup"><span data-stu-id="b1873-141">Access</span></span>         | <span data-ttu-id="b1873-142">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b1873-142">ReadWrite</span></span>                               |
| <span data-ttu-id="b1873-143">Тип</span><span class="sxs-lookup"><span data-stu-id="b1873-143">Type</span></span>           | <span data-ttu-id="b1873-144">Long (0-65000)</span><span class="sxs-lookup"><span data-stu-id="b1873-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="b1873-145">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b1873-145">Default</span></span>        | <span data-ttu-id="b1873-146">0</span><span class="sxs-lookup"><span data-stu-id="b1873-146">0</span></span>                                       |
| <span data-ttu-id="b1873-147">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="b1873-147">Minimum system</span></span> | <span data-ttu-id="b1873-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1873-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="b1873-149">протоколкоде</span><span class="sxs-lookup"><span data-stu-id="b1873-149">ProtocolCode</span></span>



| <span data-ttu-id="b1873-150">Ввод</span><span class="sxs-lookup"><span data-stu-id="b1873-150">Entry</span></span> | <span data-ttu-id="b1873-151">Значение</span><span class="sxs-lookup"><span data-stu-id="b1873-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1873-152">Описание</span><span class="sxs-lookup"><span data-stu-id="b1873-152">Description</span></span>    | <span data-ttu-id="b1873-153">Код, указывающий последовательность протокола RPC.</span><span class="sxs-lookup"><span data-stu-id="b1873-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="b1873-154">Поддерживаемые коды протоколов включают в себя: нкакн \_ IP \_ TCP, нкакн \_ http, нкакн \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="b1873-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="b1873-155">Это свойство возвращается при вызове метода свойства [**ключа**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="b1873-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="b1873-156">Access</span><span class="sxs-lookup"><span data-stu-id="b1873-156">Access</span></span>         | <span data-ttu-id="b1873-157">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="b1873-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b1873-158">Тип</span><span class="sxs-lookup"><span data-stu-id="b1873-158">Type</span></span>           | <span data-ttu-id="b1873-159">Строка</span><span class="sxs-lookup"><span data-stu-id="b1873-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="b1873-160">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="b1873-160">Default</span></span>        | <span data-ttu-id="b1873-161">""</span><span class="sxs-lookup"><span data-stu-id="b1873-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="b1873-162">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="b1873-162">Minimum system</span></span> | <span data-ttu-id="b1873-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b1873-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="b1873-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1873-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1873-165">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="b1873-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
