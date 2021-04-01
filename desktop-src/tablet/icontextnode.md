---
description: Представляет узел в дереве объектов, созданных в ходе анализа рукописного ввода.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Интерфейс Иконтекстноде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072779"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="754d2-103">Интерфейс Иконтекстноде</span><span class="sxs-lookup"><span data-stu-id="754d2-103">IContextNode interface</span></span>

<span data-ttu-id="754d2-104">Представляет узел в дереве объектов, созданных в ходе анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="754d2-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="754d2-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="754d2-105">Members</span></span>

<span data-ttu-id="754d2-106">Интерфейс **иконтекстноде** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="754d2-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="754d2-107">**Иконтекстноде** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="754d2-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="754d2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="754d2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="754d2-109">Методы</span><span class="sxs-lookup"><span data-stu-id="754d2-109">Methods</span></span>

<span data-ttu-id="754d2-110">Интерфейс **иконтекстноде** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="754d2-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="754d2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="754d2-111">Method</span></span>                                                                                  | <span data-ttu-id="754d2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="754d2-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="754d2-113">**аддконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="754d2-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="754d2-114">Добавляет новый [**иконтекстлинк**](icontextlink.md) в коллекцию ссылок контекста объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="754d2-115">**аддпропертидата**</span><span class="sxs-lookup"><span data-stu-id="754d2-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="754d2-116">Добавляет часть данных для конкретного приложения.</span><span class="sxs-lookup"><span data-stu-id="754d2-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="754d2-117">**Уточнит**</span><span class="sxs-lookup"><span data-stu-id="754d2-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="754d2-118">Изменяет тип подтверждения, который управляет тем, что объект [**иинканализер**](iinkanalyzer.md) может измениться о **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="754d2-119">**контаинспропертидата**</span><span class="sxs-lookup"><span data-stu-id="754d2-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="754d2-120">Определяет, содержит ли объект **иконтекстноде** данные, хранящиеся по указанному идентификатору.</span><span class="sxs-lookup"><span data-stu-id="754d2-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="754d2-121">**креатепартиаллипопулатедсубноде**</span><span class="sxs-lookup"><span data-stu-id="754d2-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="754d2-122">Создает дочерний объект **иконтекстноде** , который содержит только сведения о типе, идентификаторе и расположении.</span><span class="sxs-lookup"><span data-stu-id="754d2-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="754d2-123">**креатесубноде**</span><span class="sxs-lookup"><span data-stu-id="754d2-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="754d2-124">Создает новый дочерний объект **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="754d2-125">**делетеконтекстлинк**</span><span class="sxs-lookup"><span data-stu-id="754d2-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="754d2-126">Удаляет объект [**иконтекстлинк**](icontextlink.md) из коллекции ссылок объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="754d2-127">**делетесубноде**</span><span class="sxs-lookup"><span data-stu-id="754d2-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="754d2-128">Удаляет дочерний элемент **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="754d2-129">**жетконтекстлинкс**</span><span class="sxs-lookup"><span data-stu-id="754d2-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="754d2-130">Извлекает коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="754d2-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="754d2-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="754d2-132">Возвращает идентификатор для объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="754d2-133">**Нахождения**</span><span class="sxs-lookup"><span data-stu-id="754d2-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="754d2-134">Извлекает расположение и размер объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="754d2-135">**жетпарентноде**</span><span class="sxs-lookup"><span data-stu-id="754d2-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="754d2-136">Возвращает родительский узел этого **иконтекстноде** в дереве узлов контекста.</span><span class="sxs-lookup"><span data-stu-id="754d2-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="754d2-137">**жетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="754d2-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="754d2-138">Получает значение, указывающее, является ли объект **иконтекстноде** частично заполнен или полностью заполнен.</span><span class="sxs-lookup"><span data-stu-id="754d2-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="754d2-139">**жетпропертидата**</span><span class="sxs-lookup"><span data-stu-id="754d2-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="754d2-140">Извлекает данные конкретного приложения или другие данные свойств по заданному идентификатору.</span><span class="sxs-lookup"><span data-stu-id="754d2-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="754d2-141">**жетпропертидатаидс**</span><span class="sxs-lookup"><span data-stu-id="754d2-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="754d2-142">Возвращает идентификаторы, для которых имеются данные свойств.</span><span class="sxs-lookup"><span data-stu-id="754d2-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="754d2-143">**жетстрокекаунт**</span><span class="sxs-lookup"><span data-stu-id="754d2-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="754d2-144">Возвращает число штрихов, связанных с объектом **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="754d2-145">**жетстрокеид**</span><span class="sxs-lookup"><span data-stu-id="754d2-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="754d2-146">Извлекает идентификатор штриха для штриха, на который ссылается значение индекса в объекте **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="754d2-147">**жетстрокеидс**</span><span class="sxs-lookup"><span data-stu-id="754d2-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="754d2-148">Извлекает массив идентификаторов для штрихов в объекте **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="754d2-149">**жетстрокепаккетдатабид**</span><span class="sxs-lookup"><span data-stu-id="754d2-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="754d2-150">Извлекает массив, содержащий данные свойства пакета для указанного штриха.</span><span class="sxs-lookup"><span data-stu-id="754d2-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="754d2-151">**жетстрокепаккетдескриптионбид**</span><span class="sxs-lookup"><span data-stu-id="754d2-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="754d2-152">Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.</span><span class="sxs-lookup"><span data-stu-id="754d2-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="754d2-153">**жетсубнодес**</span><span class="sxs-lookup"><span data-stu-id="754d2-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="754d2-154">Возвращает прямые дочерние узлы объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="754d2-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="754d2-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="754d2-156">Возвращает тип объекта **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="754d2-157">**Имя_типа**</span><span class="sxs-lookup"><span data-stu-id="754d2-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="754d2-158">Возвращает удобное для чтения имя типа этого **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="754d2-159">**Подтверждено**</span><span class="sxs-lookup"><span data-stu-id="754d2-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="754d2-160">Получает значение, указывающее, подтвержден ли объект **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="754d2-161">[**Иинканализер**](iinkanalyzer.md) не может изменить тип узла и связанные штрихи для подтвержденных объектов **иконтекстноде** .</span><span class="sxs-lookup"><span data-stu-id="754d2-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="754d2-162">**лоадпропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="754d2-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="754d2-163">Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью [**иконтекстноде:: савепропертиесдата**](icontextnode-savepropertiesdata.md).</span><span class="sxs-lookup"><span data-stu-id="754d2-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="754d2-164">**мовесубнодетопоситион**</span><span class="sxs-lookup"><span data-stu-id="754d2-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="754d2-165">Переупорядочивает указанный дочерний объект **иконтекстноде** по указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="754d2-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="754d2-166">**ремовепропертидата**</span><span class="sxs-lookup"><span data-stu-id="754d2-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="754d2-167">Удаляет часть данных, зависящих от приложения.</span><span class="sxs-lookup"><span data-stu-id="754d2-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="754d2-168">**Переподчинить**</span><span class="sxs-lookup"><span data-stu-id="754d2-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="754d2-169">Перемещает этот объект **иконтекстноде** из коллекции подузлов родительского узла контекста в коллекцию подузлов указанного узла контекста.</span><span class="sxs-lookup"><span data-stu-id="754d2-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="754d2-170">**репарентстрокебидтоноде**</span><span class="sxs-lookup"><span data-stu-id="754d2-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="754d2-171">Перемещает данные штриха из этого **иконтекстнодеа** в указанный **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="754d2-172">**савепропертиесдата**</span><span class="sxs-lookup"><span data-stu-id="754d2-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="754d2-173">Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="754d2-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="754d2-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="754d2-175">Обновляет расположение и размер этого **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="754d2-176">**сетпартиаллипопулатед**</span><span class="sxs-lookup"><span data-stu-id="754d2-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="754d2-177">Изменяет значение, указывающее, является ли **иконтекстноде** частично или полностью заполненным.</span><span class="sxs-lookup"><span data-stu-id="754d2-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="754d2-178">**сетстрокес**</span><span class="sxs-lookup"><span data-stu-id="754d2-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="754d2-179">Связывает указанные штрихи с этим **иконтекстноде**.</span><span class="sxs-lookup"><span data-stu-id="754d2-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="754d2-180">Комментарии</span><span class="sxs-lookup"><span data-stu-id="754d2-180">Remarks</span></span>

<span data-ttu-id="754d2-181">Типы узлов описаны в константах [типов узлов контекста](context-node-types.md) .</span><span class="sxs-lookup"><span data-stu-id="754d2-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="754d2-182">Примеры</span><span class="sxs-lookup"><span data-stu-id="754d2-182">Examples</span></span>

<span data-ttu-id="754d2-183">В следующем примере показан метод, который проверяет **иконтекстноде**; метод выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="754d2-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="754d2-184">Возвращает тип узла контекста.</span><span class="sxs-lookup"><span data-stu-id="754d2-184">Gets the context node's type.</span></span> <span data-ttu-id="754d2-185">Если контекстный узел является неклассифицированным рукописным вводом, указанием анализа или узлом пользовательского распознавателя, он вызывает вспомогательный метод для проверки конкретных свойств типа узла.</span><span class="sxs-lookup"><span data-stu-id="754d2-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="754d2-186">Если узел содержит подузлы, он проверяет каждый подузел, вызывая сам себя.</span><span class="sxs-lookup"><span data-stu-id="754d2-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="754d2-187">Если узел является листовым узлом рукописного ввода, он проверяет данные штриха для узла, вызывая вспомогательный метод.</span><span class="sxs-lookup"><span data-stu-id="754d2-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="754d2-188">API положение Инканалисис позволяет создать узел линии, содержащий рукописные слова и текстовые слова.</span><span class="sxs-lookup"><span data-stu-id="754d2-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="754d2-189">Однако синтаксический анализатор будет игнорировать эти смешанные узлы и будет обрабатывать их как внешние узлы.</span><span class="sxs-lookup"><span data-stu-id="754d2-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="754d2-190">Это повлияет на точность анализа при обнаружении рукописных заметок, когда пользователь выполняет запись или вокруг этого смешанного узла.</span><span class="sxs-lookup"><span data-stu-id="754d2-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="754d2-191">Требования</span><span class="sxs-lookup"><span data-stu-id="754d2-191">Requirements</span></span>



| <span data-ttu-id="754d2-192">Требование</span><span class="sxs-lookup"><span data-stu-id="754d2-192">Requirement</span></span> | <span data-ttu-id="754d2-193">Значение</span><span class="sxs-lookup"><span data-stu-id="754d2-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="754d2-194">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="754d2-194">Minimum supported client</span></span><br/> | <span data-ttu-id="754d2-195">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="754d2-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="754d2-196">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="754d2-196">Minimum supported server</span></span><br/> | <span data-ttu-id="754d2-197">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="754d2-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="754d2-198">Header</span><span class="sxs-lookup"><span data-stu-id="754d2-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="754d2-199"><dt>Иаком. h (также требуется Иаком \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="754d2-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="754d2-200">DLL</span><span class="sxs-lookup"><span data-stu-id="754d2-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="754d2-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="754d2-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="754d2-202">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="754d2-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="754d2-203">**иконтекстнодес**</span><span class="sxs-lookup"><span data-stu-id="754d2-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="754d2-204">Типы узлов контекста</span><span class="sxs-lookup"><span data-stu-id="754d2-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="754d2-205">**иинканализер**</span><span class="sxs-lookup"><span data-stu-id="754d2-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="754d2-206">Справочник по анализу рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="754d2-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

