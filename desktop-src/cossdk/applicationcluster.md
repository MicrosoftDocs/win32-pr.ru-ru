---
description: Содержит список серверных компьютеров в кластере приложений. Он содержит объект для каждого сервера.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Коллекция Аппликатионклустер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141383"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="1e317-104">Коллекция Аппликатионклустер</span><span class="sxs-lookup"><span data-stu-id="1e317-104">ApplicationCluster collection</span></span>

<span data-ttu-id="1e317-105">Содержит список серверных компьютеров в кластере приложений.</span><span class="sxs-lookup"><span data-stu-id="1e317-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="1e317-106">Он содержит объект для каждого сервера.</span><span class="sxs-lookup"><span data-stu-id="1e317-106">It contains an object for each server.</span></span> <span data-ttu-id="1e317-107">Это коллекция верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="1e317-107">This is a top-level collection.</span></span>

<span data-ttu-id="1e317-108">Кластер приложений определяется в целях службы балансировки нагрузки компонентов (распределения загрузки).</span><span class="sxs-lookup"><span data-stu-id="1e317-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="1e317-109">Для использования коллекции кластеров приложений на компьютере должна быть установлена служба распределения загрузки.</span><span class="sxs-lookup"><span data-stu-id="1e317-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="1e317-110">Вы назначаете маршрутизатор в кластере приложений с помощью свойства IsCollection в объекте коллекции [**локалкомпутер**](localcomputer.md) , и вы указываете, что заданный компонент должен быть сбалансирован с помощью свойства лоадбаланЦингсуппортед в объекте коллекции [**компонентов**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="1e317-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="1e317-111">Эта коллекция поддерживает методы [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) и [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) объекта [**комадминкаталогколлектион**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="1e317-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="1e317-112">Элементы</span><span class="sxs-lookup"><span data-stu-id="1e317-112">Members</span></span>

<span data-ttu-id="1e317-113">Коллекция **аппликатионклустер** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , но не содержит дополнительных элементов.</span><span class="sxs-lookup"><span data-stu-id="1e317-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="1e317-114">Связанные коллекции</span><span class="sxs-lookup"><span data-stu-id="1e317-114">Related Collections</span></span>

<span data-ttu-id="1e317-115">Можно переходить от этой коллекции к любой из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1e317-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="1e317-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="1e317-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="1e317-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="1e317-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="1e317-118">**релатедколлектионинфо**</span><span class="sxs-lookup"><span data-stu-id="1e317-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="1e317-119">Вы можете переходить к этой коллекции из следующих коллекций:</span><span class="sxs-lookup"><span data-stu-id="1e317-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="1e317-120">**Корневой**</span><span class="sxs-lookup"><span data-stu-id="1e317-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="1e317-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="1e317-121">Properties</span></span>

<span data-ttu-id="1e317-122">Объект [**комадминкаталогобжект**](comadmincatalogobject.md) в коллекции поддерживает следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1e317-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="1e317-123">Name</span><span class="sxs-lookup"><span data-stu-id="1e317-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="1e317-124">Имя</span><span class="sxs-lookup"><span data-stu-id="1e317-124">Name</span></span>



| <span data-ttu-id="1e317-125">Ввод</span><span class="sxs-lookup"><span data-stu-id="1e317-125">Entry</span></span> | <span data-ttu-id="1e317-126">Значение</span><span class="sxs-lookup"><span data-stu-id="1e317-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e317-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1e317-127">Description</span></span>    | <span data-ttu-id="1e317-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="1e317-128">The name of the server.</span></span> <span data-ttu-id="1e317-129">Лишние пробелы в начале и конце строки удаляются. Это свойство возвращается при вызове метода свойства [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) или [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) для объекта этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="1e317-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="1e317-130">Access</span><span class="sxs-lookup"><span data-stu-id="1e317-130">Access</span></span>         | <span data-ttu-id="1e317-131">Флагом writeonce</span><span class="sxs-lookup"><span data-stu-id="1e317-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="1e317-132">Тип</span><span class="sxs-lookup"><span data-stu-id="1e317-132">Type</span></span>           | <span data-ttu-id="1e317-133">Строка</span><span class="sxs-lookup"><span data-stu-id="1e317-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1e317-134">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e317-134">Default</span></span>        | <span data-ttu-id="1e317-135">"Новый компьютер"</span><span class="sxs-lookup"><span data-stu-id="1e317-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="1e317-136">Минимальная система</span><span class="sxs-lookup"><span data-stu-id="1e317-136">Minimum system</span></span> | <span data-ttu-id="1e317-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="1e317-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="1e317-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e317-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e317-139">Коллекции администрирования COM+</span><span class="sxs-lookup"><span data-stu-id="1e317-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
