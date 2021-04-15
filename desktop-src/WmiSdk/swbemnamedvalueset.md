---
description: Объект Свбемнамедвалуесет — это коллекция объектов Свбемнамедвалуе.
ms.assetid: 7d1c3a28-d0d3-4108-9628-74ad483e328e
ms.tgt_platform: multiple
title: Объект Свбемнамедвалуесет (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet
- ISWbemNamedValueSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b3048b8589666a07958251ed4c0d56100132fd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701961"
---
# <a name="swbemnamedvalueset-object"></a><span data-ttu-id="5c037-103">Объект Свбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="5c037-103">SWbemNamedValueSet object</span></span>

<span data-ttu-id="5c037-104">Объект **свбемнамедвалуесет** — это коллекция объектов [**свбемнамедвалуе**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="5c037-104">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) objects.</span></span> <span data-ttu-id="5c037-105">Методы и свойства **свбемнамедвалуесет** используются для отправки дополнительных сведений поставщикам при отправке определенных вызовов WMI.</span><span class="sxs-lookup"><span data-stu-id="5c037-105">The methods and properties of **SWbemNamedValueSet** are used principally to send more information to providers when submitting certain calls to WMI.</span></span> <span data-ttu-id="5c037-106">Все вызовы в [**SwbemServices**](swbemservices.md)и некоторые вызовы в [**SWbemObject**](swbemobject.md)принимают необязательный параметр, который является объектом этого типа.</span><span class="sxs-lookup"><span data-stu-id="5c037-106">All calls in [**SWbemServices**](swbemservices.md), and some calls in [**SWbemObject**](swbemobject.md), take an optional parameter that is an object of this type.</span></span> <span data-ttu-id="5c037-107">Клиент может добавить сведения в объект **свбемнамедвалуесет** и отправить объект **свбемнамедвалуесет** с вызовом в качестве одного из параметров.</span><span class="sxs-lookup"><span data-stu-id="5c037-107">A client can add information to an **SWbemNamedValueSet** object, and send the **SWbemNamedValueSet** object with the call as one of the parameters.</span></span> <span data-ttu-id="5c037-108">Этот объект может быть создан вызовом метода **CreateObject** VBScript.</span><span class="sxs-lookup"><span data-stu-id="5c037-108">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="5c037-109">Дополнительные сведения см. [в разделе доступ к коллекции](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="5c037-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

> [!Note]  
> <span data-ttu-id="5c037-110">Важно! если возможно, не используйте этот механизм, так как он может нарушить унифицированную модель доступа, которая является основанием инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="5c037-110">Important - If possible, do not use this mechanism because it can break the uniform access model that is the basis of WMI.</span></span> <span data-ttu-id="5c037-111">Если поставщик использует этот механизм, важно, чтобы этот механизм использовался как можно реже.</span><span class="sxs-lookup"><span data-stu-id="5c037-111">If a provider does use this mechanism, it is important that this mechanism is used as sparingly as possible.</span></span> <span data-ttu-id="5c037-112">Если поставщику требуется большой объем строго специфической контекстной информации для ответа на запрос, все клиенты должны быть написаны для предоставления этих сведений.</span><span class="sxs-lookup"><span data-stu-id="5c037-112">If a provider requires a large amount of highly specific context information to respond to a request, all clients must be coded to provide this information.</span></span> <span data-ttu-id="5c037-113">Этот механизм позволяет при необходимости получить доступ к таким поставщикам.</span><span class="sxs-lookup"><span data-stu-id="5c037-113">This mechanism allows you to access such providers, if necessary.</span></span>

 

<span data-ttu-id="5c037-114">Объект **свбемнамедвалуесет** — это коллекция элементов [**свбемнамедвалуе**](swbemnamedvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="5c037-114">An **SWbemNamedValueSet** object is a collection of [**SWbemNamedValue**](swbemnamedvalue.md) elements.</span></span> <span data-ttu-id="5c037-115">Эти элементы добавляются в коллекцию с помощью метода [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="5c037-115">These items are added to the collection using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span> <span data-ttu-id="5c037-116">Они удаляются с помощью метода [**свбемнамедвалуесет. Remove**](swbemnamedvalueset-remove.md) и извлекаются с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="5c037-116">They are removed using the [**SWbemNamedValueSet.Remove**](swbemnamedvalueset-remove.md) method and retrieved using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="5c037-117">Вы можете получить доступ к методам, чтобы заполнить любые сведения о контексте, необходимые для динамического поставщика.</span><span class="sxs-lookup"><span data-stu-id="5c037-117">You can access the methods to fill in any context information that is required by a dynamic provider.</span></span> <span data-ttu-id="5c037-118">После вызова одного из методов [**SwbemServices**](swbemservices.md) можно повторно использовать объект **свбемнамедвалуесет** для другого вызова.</span><span class="sxs-lookup"><span data-stu-id="5c037-118">After you call one of the [**SWbemServices**](swbemservices.md) methods, you can reuse the **SWbemNamedValueSet** object for another call.</span></span>

<span data-ttu-id="5c037-119">Базовый поставщик определяет сведения, содержащиеся в объекте **свбемнамедвалуесет** .</span><span class="sxs-lookup"><span data-stu-id="5c037-119">The underlying provider determines the information that is contained in an **SWbemNamedValueSet** object.</span></span> <span data-ttu-id="5c037-120">Инструментарий WMI не использует эти сведения, но просто пересылает его поставщику.</span><span class="sxs-lookup"><span data-stu-id="5c037-120">WMI makes no use of the information, but simply forwards it to the provider.</span></span> <span data-ttu-id="5c037-121">Поставщики должны публиковать сведения о контексте, необходимые им для запросов на обслуживание.</span><span class="sxs-lookup"><span data-stu-id="5c037-121">Providers must publish the context information they require to service requests.</span></span>

## <a name="members"></a><span data-ttu-id="5c037-122">Элементы</span><span class="sxs-lookup"><span data-stu-id="5c037-122">Members</span></span>

<span data-ttu-id="5c037-123">Объект **свбемнамедвалуесет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5c037-123">The **SWbemNamedValueSet** object has these types of members:</span></span>

-   [<span data-ttu-id="5c037-124">Методы</span><span class="sxs-lookup"><span data-stu-id="5c037-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="5c037-125">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c037-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5c037-126">Методы</span><span class="sxs-lookup"><span data-stu-id="5c037-126">Methods</span></span>

<span data-ttu-id="5c037-127">Объект **свбемнамедвалуесет** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="5c037-127">The **SWbemNamedValueSet** object has these methods.</span></span>



| <span data-ttu-id="5c037-128">Метод</span><span class="sxs-lookup"><span data-stu-id="5c037-128">Method</span></span>                                            | <span data-ttu-id="5c037-129">Описание</span><span class="sxs-lookup"><span data-stu-id="5c037-129">Description</span></span>                                                                                                                              |
|:--------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c037-130">**Включить**</span><span class="sxs-lookup"><span data-stu-id="5c037-130">**Add**</span></span>](swbemnamedvalueset-add.md)             | <span data-ttu-id="5c037-131">Добавляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="5c037-131">Adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span><br/>                                                  |
| [<span data-ttu-id="5c037-132">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="5c037-132">**Clone**</span></span>](swbemnamedvalueset-clone.md)         | <span data-ttu-id="5c037-133">Создает копию этой коллекции **свбемнамедвалуесет** .</span><span class="sxs-lookup"><span data-stu-id="5c037-133">Makes a copy of this **SWbemNamedValueSet** collection.</span></span><br/>                                                                       |
| [<span data-ttu-id="5c037-134">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="5c037-134">**DeleteAll**</span></span>](swbemnamedvalueset-deleteall.md) | <span data-ttu-id="5c037-135">Удаляет все элементы из коллекции, делая объект **свбемнамедвалуесет** пустым.</span><span class="sxs-lookup"><span data-stu-id="5c037-135">Removes all items from the collection, making the **SWbemNamedValueSet** object empty.</span></span><br/>                                        |
| [<span data-ttu-id="5c037-136">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="5c037-136">**Item**</span></span>](swbemnamedvalueset-item.md)           | <span data-ttu-id="5c037-137">Извлекает объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="5c037-137">Retrieves an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span> <span data-ttu-id="5c037-138">Это метод объекта по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5c037-138">This is the default method of the object.</span></span><br/> |
| [<span data-ttu-id="5c037-139">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="5c037-139">**Remove**</span></span>](swbemnamedvalueset-remove.md)       | <span data-ttu-id="5c037-140">Удаляет объект [**свбемнамедвалуе**](swbemnamedvalue.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="5c037-140">Removes an [**SWbemNamedValue**](swbemnamedvalue.md) object from the collection.</span></span><br/>                                             |



 

### <a name="properties"></a><span data-ttu-id="5c037-141">Свойства</span><span class="sxs-lookup"><span data-stu-id="5c037-141">Properties</span></span>

<span data-ttu-id="5c037-142">Объект **свбемнамедвалуесет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c037-142">The **SWbemNamedValueSet** object has these properties.</span></span>



| <span data-ttu-id="5c037-143">Свойство</span><span class="sxs-lookup"><span data-stu-id="5c037-143">Property</span></span>                                             | <span data-ttu-id="5c037-144">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5c037-144">Access type</span></span>          | <span data-ttu-id="5c037-145">Описание</span><span class="sxs-lookup"><span data-stu-id="5c037-145">Description</span></span>                                       |
|:-----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="5c037-146">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="5c037-146">**Count**</span></span>](swbemnamedvalueset-count.md)<br/> | <span data-ttu-id="5c037-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5c037-147">Read-only</span></span><br/> | <span data-ttu-id="5c037-148">Количество элементов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="5c037-148">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="5c037-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="5c037-149">Examples</span></span>

<span data-ttu-id="5c037-150">В следующем примере VBScript демонстрируется работа с именованными наборами значений в случае, если именованное значение является типом массива.</span><span class="sxs-lookup"><span data-stu-id="5c037-150">The following VBScript sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```VB
Set Context = CreateObject("WbemScripting.SWbemNamedValueSet")

On Error Resume Next

Context.Add "n1", Array (1, 2, 3)
str = "The initial value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

WScript.Echo ""

' report the value of an element of the context value
v = Context("n1")
WScript.Echo "By indirection the first element of n1 has value:",v(0)

' report the value directly
WScript.Echo "By direct access the first element of n1 has value:", Context("n1")(0)

' set the value of a single named value element
Context("n1")(1) = 11 
WScript.Echo "After direct assignment the first element of n1 has value:", Context("n1")(1)

' set the value of a single named value element
Set v = Context("n1")
v(1) = 345
WScript.Echo "After indirect assignment the first element of n1 has value:", Context("n1")(1)

' set the value of an entire context value
Context("n1") = Array (5, 34, 178871)
WScript.Echo "After direct array assignment the first element of n1 has value:", Context("n1")(1)

str = "After direct assignment the entire value of n1 is {"
for x=LBound(Context("n1")) to UBound(Context("n1"))
 str = str & Context("n1")(x)
 if x <> UBound(Context("n1")) Then
  str = str & ", "
 End if
next
str = str & "}"
WScript.Echo str

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="5c037-151">В следующем образце Perl показано управление именованными наборами значений в случае, если именованное значение является типом массива.</span><span class="sxs-lookup"><span data-stu-id="5c037-151">The following Perl sample demonstrates the manipulation of named value sets, in the case that the named value is an array type.</span></span>


```
use strict;
use Win32::OLE;

my ( $Context, $str, $x, @v);

eval {$Context = new Win32::OLE 'WbemScripting.SWbemNamedValueSet'; };
unless($@)
{
 $Context->Add("n1", [1, 2, 3]);
 $str = "The initial value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n\n";

 # report the value of an element of the context value
 @v = @{$Context->Item("n1")->{Value}};
 print "By indirection the first element of n1 has value:", $v[0], "\n";

 # report the value directly
 print "By direct access the first element of n1 has value:", @{$Context->Item("n1")->{Value}}[0], "\n";

 # set the value of a single named value element
 @{$Context->Item("n1")->{Value}}[1] = 11;
 print "After direct assignment the first element of n1 has value:", 
       @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of a single named value element
 @v = @{$Context->Item("n1")->{Value}};
 $v[1] = 345;
 print "After indirect assignment the first element of n1 has value:", 
    @{$Context->Item("n1")->{Value}}[1], "\n";

 # set the value of an entire context value
 $Context->Item("n1")->{Value} = [5, 34, 178871];
 print "After direct array assignment the first element of n1 has value:", 
   @{$Context->Item("n1")->{Value}}[1], "\n";

 $str = "After direct assignment the entire value of n1 is {";
 for ($x = 0; $x < @{$Context->Item("n1")->{Value}}; $x++)
 {
  $str = $str.@{$Context->Item("n1")->{Value}}[$x];
  if ($x != (@{$Context->Item("n1")->{Value}}) - 1 )
  {
   $str = $str.", ";
  }
 }
 $str = $str."}";
 print $str,"\n";
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="5c037-152">Требования</span><span class="sxs-lookup"><span data-stu-id="5c037-152">Requirements</span></span>



| <span data-ttu-id="5c037-153">Требование</span><span class="sxs-lookup"><span data-stu-id="5c037-153">Requirement</span></span> | <span data-ttu-id="5c037-154">Значение</span><span class="sxs-lookup"><span data-stu-id="5c037-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c037-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c037-155">Minimum supported client</span></span><br/> | <span data-ttu-id="5c037-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c037-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c037-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c037-157">Minimum supported server</span></span><br/> | <span data-ttu-id="5c037-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c037-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c037-159">Header</span><span class="sxs-lookup"><span data-stu-id="5c037-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c037-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c037-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c037-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="5c037-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c037-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5c037-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5c037-163">DLL</span><span class="sxs-lookup"><span data-stu-id="5c037-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c037-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c037-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5c037-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="5c037-165">CLSID</span></span><br/>                    | <span data-ttu-id="5c037-166">\_СВБЕМНАМЕДВАЛУЕСЕТ CLSID</span><span class="sxs-lookup"><span data-stu-id="5c037-166">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="5c037-167">IID</span><span class="sxs-lookup"><span data-stu-id="5c037-167">IID</span></span><br/>                      | <span data-ttu-id="5c037-168">IID \_ исвбемнамедвалуесет</span><span class="sxs-lookup"><span data-stu-id="5c037-168">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="5c037-169">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5c037-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c037-170">Создание скриптов для объектов API</span><span class="sxs-lookup"><span data-stu-id="5c037-170">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




