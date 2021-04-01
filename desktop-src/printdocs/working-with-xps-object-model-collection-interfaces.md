---
description: Описывает, как использовать общие методы интерфейсов коллекции.
ms.assetid: 6ea311c0-a155-47de-ad40-62b0cbeb6e8f
title: Работа с интерфейсами коллекции OM в XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cda84243347680d91a6f3a5255f7ebf4e66932
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265109"
---
# <a name="working-with-xps-om-collection-interfaces"></a><span data-ttu-id="e5f99-103">Работа с интерфейсами коллекции OM в XPS</span><span class="sxs-lookup"><span data-stu-id="e5f99-103">Working with XPS OM Collection Interfaces</span></span>

<span data-ttu-id="e5f99-104">Описывает, как использовать общие методы интерфейсов коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-104">Describes how to use the common methods of the collection interfaces.</span></span>

## <a name="contents"></a><span data-ttu-id="e5f99-105">Содержимое</span><span class="sxs-lookup"><span data-stu-id="e5f99-105">Contents</span></span>

<span data-ttu-id="e5f99-106">Методы, описанные в этом разделе, показаны в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="e5f99-106">The methods described in this section are shown in the list that follows.</span></span> <span data-ttu-id="e5f99-107">Не все интерфейсы коллекций поддерживают каждый из этих методов, а некоторые интерфейсы также поддерживают методы, не описанные на этой странице.</span><span class="sxs-lookup"><span data-stu-id="e5f99-107">Not all collection interfaces support each of these methods, and some interfaces also support methods that are not described on this page.</span></span> <span data-ttu-id="e5f99-108">Список методов, поддерживаемых конкретным интерфейсом, см. в описании этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e5f99-108">For the list of methods supported by a specific interface, refer to the description of that interface's description.</span></span>

<dl>

[<span data-ttu-id="e5f99-109">Метод Append</span><span class="sxs-lookup"><span data-stu-id="e5f99-109">Append Method</span></span>](#append-method)  
[<span data-ttu-id="e5f99-110">Метод GetAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-110">GetAt Method</span></span>](#getat-method)  
[<span data-ttu-id="e5f99-111">Метод GetCount</span><span class="sxs-lookup"><span data-stu-id="e5f99-111">GetCount Method</span></span>](#getcount-method)  
[<span data-ttu-id="e5f99-112">Метод Инсертат</span><span class="sxs-lookup"><span data-stu-id="e5f99-112">InsertAt Method</span></span>](#insertat-method)  
[<span data-ttu-id="e5f99-113">Метод RemoveAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-113">RemoveAt Method</span></span>](#removeat-method)  
[<span data-ttu-id="e5f99-114">Метод SetAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-114">SetAt Method</span></span>](#setat-method)  
</dl>

[<span data-ttu-id="e5f99-115">См. также:</span><span class="sxs-lookup"><span data-stu-id="e5f99-115">See also</span></span>](#see-also)

## <a name="append-method"></a><span data-ttu-id="e5f99-116">Метод Append</span><span class="sxs-lookup"><span data-stu-id="e5f99-116">Append Method</span></span>

<span data-ttu-id="e5f99-117">Добавляет объект в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-117">Appends an object to the end of the collection.</span></span>

<span data-ttu-id="e5f99-118">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-118">**Generic Syntax**</span></span>


```C++
HRESULT Append(
  [in]  Object *object
);
```



<span data-ttu-id="e5f99-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-119">**Description**</span></span>

<span data-ttu-id="e5f99-120">В конец коллекции этот метод добавляет объект, который передается в список параметров, как показано на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="e5f99-120">To the end of the collection, this method appends an object that is passed in the parameter list, as shown in the following diagram.</span></span>

![Рисунок, показывающий, как Append добавляет запись в коллекцию](images/generic-append.png)

## <a name="getat-method"></a><span data-ttu-id="e5f99-122">Метод GetAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-122">GetAt Method</span></span>

<span data-ttu-id="e5f99-123">Возвращает объект из указанного расположения в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-123">Gets an object from a specified location in the collection.</span></span>

<span data-ttu-id="e5f99-124">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-124">**Generic Syntax**</span></span>


```C++
HRESULT GetAt(
  [in]           UINT32 index,
  [out, retval]  Object **object
);
```



<span data-ttu-id="e5f99-125">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-125">**Description**</span></span>

<span data-ttu-id="e5f99-126">Записывает объект, хранящийся в расположении коллекции, заданном параметром *index* , в переменную, на которую ссылается *объект*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-126">Writes the object that is stored at the collection's location specified by *index* to the variable referenced by *object*.</span></span> <span data-ttu-id="e5f99-127">Это действие не изменяет содержимое коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-127">This action does not change the collection's contents.</span></span> <span data-ttu-id="e5f99-128">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="e5f99-128">The following diagram illustrates this process.</span></span>

![Рисунок, показывающий, как GetAt извлекает запись из коллекции.](images/generic-getat.png)

## <a name="getcount-method"></a><span data-ttu-id="e5f99-130">Метод GetCount</span><span class="sxs-lookup"><span data-stu-id="e5f99-130">GetCount Method</span></span>

<span data-ttu-id="e5f99-131">Возвращает число объектов, хранящихся в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-131">Gets the number of objects stored in the collection.</span></span>

<span data-ttu-id="e5f99-132">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-132">**Generic Syntax**</span></span>


```C++
HRESULT GetCount(
  [out, retval]  UINT32 *count
);
```



<span data-ttu-id="e5f99-133">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-133">**Description**</span></span>

<span data-ttu-id="e5f99-134">Записывает количество объектов, которые в данный момент хранятся в коллекции, в переменную, на которую ссылается *Count*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-134">Writes the number of objects that are currently stored in the collection into the variable referenced by *count*.</span></span> <span data-ttu-id="e5f99-135">Это действие не изменяет содержимое коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-135">This action does not change the collection's contents.</span></span> <span data-ttu-id="e5f99-136">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="e5f99-136">The following diagram illustrates this process.</span></span>

![фигура, показывающая, как функция NOCOUNT получает количество записей в коллекции](images/generic-getcount.png)

## <a name="insertat-method"></a><span data-ttu-id="e5f99-138">Метод Инсертат</span><span class="sxs-lookup"><span data-stu-id="e5f99-138">InsertAt Method</span></span>

<span data-ttu-id="e5f99-139">Вставляет объект в указанное место коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-139">Inserts an object at a specified location of the collection.</span></span>

<span data-ttu-id="e5f99-140">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-140">**Generic Syntax**</span></span>


```C++
HRESULT InsertAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="e5f99-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-141">**Description**</span></span>

<span data-ttu-id="e5f99-142">Объект, передаваемый в *объект* , вставляется в коллекцию в расположении, указанном параметром *index*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-142">The object that is passed in *object* is inserted into the collection at the location specified by *index*.</span></span> <span data-ttu-id="e5f99-143">Перед вставкой нового *объекта* этот метод перемещается на 1 объект, который ранее занимал место в *индексе* , и перемещает все указатели интерфейса после *индекса*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-143">Before inserting the new *object*, this method moves by 1 the object that has previously occupied the location at *index* and moves all interface pointers subsequent to *index*.</span></span> <span data-ttu-id="e5f99-144">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="e5f99-144">The following diagram illustrates this process.</span></span>

![Рисунок, показывающий, как инсертат добавляет запись в коллекцию](images/generic-insertat.png)

## <a name="removeat-method"></a><span data-ttu-id="e5f99-146">Метод RemoveAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-146">RemoveAt Method</span></span>

<span data-ttu-id="e5f99-147">Удаляет объект из указанного расположения в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-147">Removes the object from a specified location in the collection.</span></span>

<span data-ttu-id="e5f99-148">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-148">**Generic Syntax**</span></span>


```C++
HRESULT RemoveAt(
  [in]  UINT32 index
);
```



<span data-ttu-id="e5f99-149">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-149">**Description**</span></span>

<span data-ttu-id="e5f99-150">Этот метод освобождает объект из расположения, заданного параметром *index*, а затем сжимает коллекцию, уменьшая на 1 индекс каждого указателя, следующего за *индексом*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-150">This method releases the object from the location specified by *index*, then compacts the collection by reducing by 1 the index of each pointer subsequent to *index*.</span></span> <span data-ttu-id="e5f99-151">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="e5f99-151">The following diagram illustrates this process.</span></span>

![Рисунок, показывающий, как метод RemoveAt удаляет запись из коллекции](images/generic-removeat.png)

## <a name="setat-method"></a><span data-ttu-id="e5f99-153">Метод SetAt</span><span class="sxs-lookup"><span data-stu-id="e5f99-153">SetAt Method</span></span>

<span data-ttu-id="e5f99-154">Заменяет объект в указанном месте в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5f99-154">Replaces the object at a specified location in the collection.</span></span>

<span data-ttu-id="e5f99-155">**Универсальный синтаксис**</span><span class="sxs-lookup"><span data-stu-id="e5f99-155">**Generic Syntax**</span></span>


```C++
HRESULT SetAt(
  [in]  UINT32 index,
  [in]  Object *object
);
```



<span data-ttu-id="e5f99-156">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e5f99-156">**Description**</span></span>

<span data-ttu-id="e5f99-157">Этот метод сначала освобождает объект в расположении, на которое ссылается *индекс*, а затем заменяет этот объект на тот, который передается в *объект*.</span><span class="sxs-lookup"><span data-stu-id="e5f99-157">This method first releases the object at the location referenced by *index*, then replaces that object with the one that is passed in *object*.</span></span> <span data-ttu-id="e5f99-158">Этот процесс представлен на схеме ниже.</span><span class="sxs-lookup"><span data-stu-id="e5f99-158">The following diagram illustrates this process.</span></span>

![Рисунок, показывающий, как SetAt заменяет запись в коллекции](images/generic-setat.png)

## <a name="see-also"></a><span data-ttu-id="e5f99-160">См. также:</span><span class="sxs-lookup"><span data-stu-id="e5f99-160">See Also</span></span>

<dl>

[<span data-ttu-id="e5f99-161">**икспсомколорпрофилересаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-161">**IXpsOMColorProfileResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomcolorprofileresourcecollection)  
[<span data-ttu-id="e5f99-162">**икспсомдашколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-162">**IXpsOMDashCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)  
[<span data-ttu-id="e5f99-163">**икспсомдокументколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-163">**IXpsOMDocumentCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)  
[<span data-ttu-id="e5f99-164">**икспсомфонтресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-164">**IXpsOMFontResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomfontresourcecollection)  
[<span data-ttu-id="e5f99-165">**икспсомжеометрифигуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-165">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)  
[<span data-ttu-id="e5f99-166">**икспсомградиентстопколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-166">**IXpsOMGradientStopCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstopcollection)  
[<span data-ttu-id="e5f99-167">**икспсомимажересаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-167">**IXpsOMImageResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimageresourcecollection)  
[<span data-ttu-id="e5f99-168">**икспсомнамеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-168">**IXpsOMNameCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)  
[<span data-ttu-id="e5f99-169">**икспсомпажереференцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-169">**IXpsOMPageReferenceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)  
[<span data-ttu-id="e5f99-170">**икспсомпартуриколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-170">**IXpsOMPartUriCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomparturicollection)  
[<span data-ttu-id="e5f99-171">**икспсомремотедиктионариресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-171">**IXpsOMRemoteDictionaryResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomremotedictionaryresourcecollection)  
[<span data-ttu-id="e5f99-172">**икспсомсигнатуреблоккресаурцеколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-172">**IXpsOMSignatureBlockResourceCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsignatureblockresourcecollection)  
[<span data-ttu-id="e5f99-173">**икспсомвисуалколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-173">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)  
[<span data-ttu-id="e5f99-174">**икспссигнатуреблоккколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-174">**IXpsSignatureBlockCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignatureblockcollection)  
[<span data-ttu-id="e5f99-175">**икспссигнатуреколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-175">**IXpsSignatureCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)  
[<span data-ttu-id="e5f99-176">**икспссигнатуререкуестколлектион**</span><span class="sxs-lookup"><span data-stu-id="e5f99-176">**IXpsSignatureRequestCollection**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturerequestcollection)  
</dl>

 

 



