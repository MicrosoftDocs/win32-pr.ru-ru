---
title: Анатомия IDL-файла
description: В этих примерах файлов IDL демонстрируются фундаментальные конструкции определения интерфейса.
ms.assetid: 9c276b8a-5342-4c09-91a7-c9a9f0f83c73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acbcfbf5c145a1fb389cc26543cf75d8cc75a107
ms.sourcegitcommit: 5ebaf3a456bc68cd0c6bd46c8135b67b1bf6fa54
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "104351012"
---
# <a name="anatomy-of-an-idl-file"></a><span data-ttu-id="88c72-103">Анатомия IDL-файла</span><span class="sxs-lookup"><span data-stu-id="88c72-103">Anatomy of an IDL File</span></span>

<span data-ttu-id="88c72-104">В этих примерах файлов IDL демонстрируются фундаментальные конструкции определения интерфейса.</span><span class="sxs-lookup"><span data-stu-id="88c72-104">These example IDL files demonstrate the fundamental constructs of interface definition.</span></span> <span data-ttu-id="88c72-105">Выделение памяти, Пользовательский маршалирование и асинхронный обмен сообщениями — всего лишь несколько функций, которые можно реализовать в пользовательском интерфейсе COM.</span><span class="sxs-lookup"><span data-stu-id="88c72-105">Memory allocation, custom marshaling, and asynchronous messaging are just a few of the features you can implement in a custom COM interface.</span></span> <span data-ttu-id="88c72-106">Атрибуты MIDL используются для определения COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="88c72-106">MIDL attributes are used to define COM interfaces.</span></span> <span data-ttu-id="88c72-107">Дополнительные сведения о реализации интерфейсов и библиотек типов, включая сводку по атрибутам MIDL, см. в разделе [определения интерфейсов и библиотеки типов](/windows/desktop/Midl/interface-definitions-and-type-libraries) в руководстве и Справочнике программиста по MIDL.</span><span class="sxs-lookup"><span data-stu-id="88c72-107">For more information about implementing interfaces and type libraries, including a summary of MIDL attributes, see [Interface Definitions and Type Libraries](/windows/desktop/Midl/interface-definitions-and-type-libraries) in the MIDL Programmer's Guide and Reference.</span></span> <span data-ttu-id="88c72-108">Полный справочник по всем атрибутам, ключевым словам и директивам MIDL см. в [справочнике по языку MIDL](/windows/desktop/Midl/midl-language-reference).</span><span class="sxs-lookup"><span data-stu-id="88c72-108">For a complete reference of all MIDL attributes, keywords, and directives, see the [MIDL Language Reference](/windows/desktop/Midl/midl-language-reference).</span></span>

## <a name="exampleidl"></a><span data-ttu-id="88c72-109">Пример. idl</span><span class="sxs-lookup"><span data-stu-id="88c72-109">Example.idl</span></span>

<span data-ttu-id="88c72-110">В следующем примере файла IDL определяются два COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="88c72-110">The following example IDL file defines two COM interfaces.</span></span> <span data-ttu-id="88c72-111">Из этого IDL-файла Midl.exe создаст прокси-сервер/заглушку и маршалирует код и файлы заголовков.</span><span class="sxs-lookup"><span data-stu-id="88c72-111">From this IDL file, Midl.exe will generate proxy/stub and marshaling code and header files.</span></span> <span data-ttu-id="88c72-112">В этом примере следуют построчные разрывы.</span><span class="sxs-lookup"><span data-stu-id="88c72-112">A line-by-line dissection follows the example.</span></span>

``` syntax
//
// Example.idl 
//
import "mydefs.h","unknwn.idl"; 
[
object,
uuid(a03d1420-b1ec-11d0-8c3a-00c04fc31d2f),
] interface IFace1 : IUnknown
{
HRESULT MethodA([in] short Bread, [out] BKFST * pBToast);
HRESULT MethodB([in, out] BKFST * pBPoptart);
};
 
[
object,
uuid(a03d1421-b1ec-11d0-8c3a-00c04fc31d2f),
pointer_default(unique)
] interface IFace2 : IUnknown
{
HRESULT MethodC([in] long Max,
                [in, max_is(Max)] BkfstStuff[ ],
                [out] long * pSize,
                [out, size_is( , *pSize)] BKFST ** ppBKFST);
}; 
 
```

<span data-ttu-id="88c72-113">Здесь используется оператор [**импорта**](/windows/desktop/Midl/import) IDL, чтобы поместить в файл заголовка мидефс. h, который содержит определяемые пользователем типы, и ункнвн. idl, который содержит определение [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), от которого наследуется IFace1 и IFace2.</span><span class="sxs-lookup"><span data-stu-id="88c72-113">The IDL [**import**](/windows/desktop/Midl/import) statement is used here to bring in a header file, Mydefs.h, which contains user-defined types, and Unknwn.idl, which contains the definition of [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), from which IFace1 and IFace2 derive.</span></span>

<span data-ttu-id="88c72-114">Атрибут [**Object**](/windows/desktop/Midl/object) определяет интерфейс как объектный интерфейс и сообщает КОМПИЛЯТОРу MIDL, что вместо заглушек клиента и сервера RPC создается код прокси-сервера или заглушки.</span><span class="sxs-lookup"><span data-stu-id="88c72-114">The [**object**](/windows/desktop/Midl/object) attribute identifies the interface as an object interface and tells the MIDL compiler to generate proxy/stub code instead of RPC client and server stubs.</span></span> <span data-ttu-id="88c72-115">Методы объектного интерфейса должны иметь возвращаемый тип [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), чтобы базовый механизм RPC выдать сообщение об ошибках для вызовов, которые не удалось завершить из-за проблем с сетью.</span><span class="sxs-lookup"><span data-stu-id="88c72-115">Object interface methods must have a return type of [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), to allow the underlying RPC mechanism to report errors for calls that fail to complete due to network problems.</span></span>

<span data-ttu-id="88c72-116">Атрибут [**UUID**](/windows/desktop/Midl/uuid) задает идентификатор интерфейса (IID).</span><span class="sxs-lookup"><span data-stu-id="88c72-116">The [**uuid**](/windows/desktop/Midl/uuid) attribute specifies the interface identifier (IID).</span></span> <span data-ttu-id="88c72-117">Каждый интерфейс, класс и библиотека типов должны быть идентифицированы с помощью собственного уникального идентификатора.</span><span class="sxs-lookup"><span data-stu-id="88c72-117">Each interface, class, and type library must be identified with its own unique identifier.</span></span> <span data-ttu-id="88c72-118">Используйте Uuidgen.exe служебной программы для создания набора уникальных идентификаторов для интерфейсов и других компонентов.</span><span class="sxs-lookup"><span data-stu-id="88c72-118">Use the utility Uuidgen.exe to generate a set of unique IDs for your interfaces and other components.</span></span>

<span data-ttu-id="88c72-119">Ключевое слово [**Interface**](/windows/desktop/Midl/interface) определяет имя интерфейса.</span><span class="sxs-lookup"><span data-stu-id="88c72-119">The [**interface**](/windows/desktop/Midl/interface) keyword defines the interface name.</span></span> <span data-ttu-id="88c72-120">Все интерфейсы объектов должны прямо или косвенно наследовать от [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="88c72-120">All object interfaces must derive, directly or indirectly, from [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).</span></span>

<span data-ttu-id="88c72-121">Параметр [**в**](/windows/desktop/Midl/in) направлении задает параметр, заданный только вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="88c72-121">The [**in**](/windows/desktop/Midl/in) directional parameter specifies a parameter that is set only by the caller.</span></span> <span data-ttu-id="88c72-122">Параметр [**out**](/windows/desktop/Midl/out-idl) указывает данные, которые передаются обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="88c72-122">The [**out**](/windows/desktop/Midl/out-idl) parameter specifies data that is passed back to the caller.</span></span> <span data-ttu-id="88c72-123">Использование обоих атрибутов направления в одном параметре указывает, что параметр используется как для отправки данных в метод, так и для передачи данных обратно вызывающему объекту.</span><span class="sxs-lookup"><span data-stu-id="88c72-123">Using both directional attributes on one parameter specifies that the parameter is used both to send data to the method and to pass data back to the caller.</span></span>

<span data-ttu-id="88c72-124">Атрибут [**указателя \_ по умолчанию**](/windows/desktop/Midl/pointer-default) задает тип указателя по умолчанию ([**UNIQUE**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)или [**ptr**](/windows/desktop/Midl/ptr)) для всех указателей, за исключением тех, которые входят в списки параметров.</span><span class="sxs-lookup"><span data-stu-id="88c72-124">The [**pointer\_default**](/windows/desktop/Midl/pointer-default) attribute specifies the default pointer type ([**unique**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref), or [**ptr**](/windows/desktop/Midl/ptr)) for all pointers except for those included in parameter lists.</span></span> <span data-ttu-id="88c72-125">Если тип по умолчанию не указан, то MIDL предполагает, что одиночные указатели являются **уникальными**.</span><span class="sxs-lookup"><span data-stu-id="88c72-125">If no default type is specified, MIDL assumes that single pointers are **unique**.</span></span> <span data-ttu-id="88c72-126">Однако при наличии нескольких уровней указателей необходимо явно указать тип указателя по умолчанию, даже если требуется, чтобы тип по умолчанию был **уникальным**.</span><span class="sxs-lookup"><span data-stu-id="88c72-126">However, when you have multiple levels of pointers, you must explicitly specify a default pointer type, even if you want the default type to be **unique**.</span></span>

<span data-ttu-id="88c72-127">В предыдущем примере массив Бкфстстуфф \[ \] является *согласованным массивом*, размер которого определяется во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="88c72-127">In the preceding example, the array BkfstStuff\[ \] is a *conformant array*, the size of which is determined at run time.</span></span> <span data-ttu-id="88c72-128">Атрибут [**Max \_ —**](/windows/desktop/Midl/max-is) указывает переменную, которая содержит максимальное значение для индекса массива.</span><span class="sxs-lookup"><span data-stu-id="88c72-128">The [**max\_is**](/windows/desktop/Midl/max-is) attribute specifies the variable that contains the maximum value for the array index.</span></span>

<span data-ttu-id="88c72-129">Атрибут [**size \_**](/windows/desktop/Midl/size-is) также используется для указания размера массива или, как в предыдущем примере, нескольких уровней указателей.</span><span class="sxs-lookup"><span data-stu-id="88c72-129">The [**size\_is**](/windows/desktop/Midl/size-is) attribute is also used to specify the size of an array or, as in the preceding example, multiple levels of pointers.</span></span> <span data-ttu-id="88c72-130">В этом примере вызов можно выполнить без предварительного знания того, сколько данных будет возвращено.</span><span class="sxs-lookup"><span data-stu-id="88c72-130">In the example, the call can be made without knowing in advance how much data will be returned.</span></span>

## <a name="example2idl"></a><span data-ttu-id="88c72-131">Example2. idl</span><span class="sxs-lookup"><span data-stu-id="88c72-131">Example2.idl</span></span>

<span data-ttu-id="88c72-132">В следующем примере IDL (который повторно использует интерфейсы, описанные в предыдущем примере IDL) показаны различные способы создания сведений о библиотеке типов для интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="88c72-132">The following IDL example (which reuses the interfaces described in the previous IDL example) shows the various ways to generate type library information for interfaces.</span></span>

``` syntax
//
// Example2.idl
//

import "example.idl","oaidl.idl"; 

[
uuid(a03d1422-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace3 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace3 : IDispatch
{
   HRESULT MethodD([in] BSTR OrderIn,
                   [out, retval] * pTakeOut);
}; //end IFace3 def

[
uuid(a03d1423-b1ec-11d0-8c3a-00c04fc31d2f),
version(1.0),
helpstring("Example Type Library"),
] library ExampleLib
{
  importlib("stdole32.tlb");
  interface IFace3;
  [
  uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
  helpstring("Breakfast Component Class")
  ] coclass BkfstComponent
    {
    [default]interface IFace1;
    interfaceIFace2
    }; //end coclass def

[
uuid(a03d1424-b1ec-11d0-8c3a-00c04fc31d2f),
helpstring("IFace4 interface"),
pointer_default(unique);
dual,
oleautomation
] 
interface IFace4 : IDispatch
{
[propput] HRESULT MethodD([in] BSTR OrderIn);
[propget] HRESULT MethodE([out, retval] * pTakeOut);
}; //end IFace4 def
 
}; //end library def
 
```

<span data-ttu-id="88c72-133">Атрибут [**helpString**](/windows/desktop/Midl/helpstring) является необязательным. Он используется для краткого описания объекта или для предоставления строки состояния.</span><span class="sxs-lookup"><span data-stu-id="88c72-133">The [**helpstring**](/windows/desktop/Midl/helpstring) attribute is optional; you use it to briefly describe the object or to provide a status line.</span></span> <span data-ttu-id="88c72-134">Эти строки справки могут быть доступны для чтения с помощью обозревателя объектов, например, предоставленного в Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="88c72-134">These help strings are readable with an object browser such as the one provided with Microsoft Visual Basic.</span></span>

<span data-ttu-id="88c72-135">[**Двойной**](/windows/desktop/Midl/dual) атрибут в IFace3 создает интерфейс, который является интерфейсом диспетчеризации и COM-интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="88c72-135">The [**dual**](/windows/desktop/Midl/dual) attribute on IFace3 creates an interface that is both a dispatch interface and a COM interface.</span></span> <span data-ttu-id="88c72-136">Так как он является производным от **IDispatch**, сдвоенный интерфейс поддерживает автоматизацию, что указывает атрибут [**oleautomation**](/windows/desktop/Midl/oleautomation) .</span><span class="sxs-lookup"><span data-stu-id="88c72-136">Because it is derived from **IDispatch**, a dual interface supports Automation, which is what the [**oleautomation**](/windows/desktop/Midl/oleautomation) attribute specifies.</span></span> <span data-ttu-id="88c72-137">IFace3 импортирует Оаидл. idl, чтобы получить определение **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="88c72-137">IFace3 imports Oaidl.idl to get the definition of **IDispatch**.</span></span>

<span data-ttu-id="88c72-138">Оператор [**Library**](/windows/desktop/Midl/library) определяет библиотеку типов ексамплелиб, которая имеет собственные атрибуты [**UUID**](/windows/desktop/Midl/uuid), [**helpString**](/windows/desktop/Midl/helpstring)и [**Version**](/windows/desktop/Midl/version) .</span><span class="sxs-lookup"><span data-stu-id="88c72-138">The [**library**](/windows/desktop/Midl/library) statement defines the ExampleLib type library, which has its own [**uuid**](/windows/desktop/Midl/uuid), [**helpstring**](/windows/desktop/Midl/helpstring), and [**version**](/windows/desktop/Midl/version) attributes.</span></span>

<span data-ttu-id="88c72-139">В определении библиотеки типов директива [**importlib**](/windows/desktop/Midl/importlib) переносит в скомпилированную библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="88c72-139">Within the type library definition, the [**importlib**](/windows/desktop/Midl/importlib) directive brings in a compiled type library.</span></span> <span data-ttu-id="88c72-140">Все определения библиотек типов должны переноситься в базовую библиотеку типов, определенную в Stdole32. tlb.</span><span class="sxs-lookup"><span data-stu-id="88c72-140">All type library definitions should bring in the base type library defined in Stdole32.tlb.</span></span>

<span data-ttu-id="88c72-141">Это определение библиотеки типов демонстрирует три разных способа включения интерфейсов в библиотеку типов.</span><span class="sxs-lookup"><span data-stu-id="88c72-141">This type library definition demonstrates three different ways to include interfaces in the type library.</span></span> <span data-ttu-id="88c72-142">IFace3 включается просто путем ссылки на него в операторе Library.</span><span class="sxs-lookup"><span data-stu-id="88c72-142">IFace3 is included merely by referencing it within the library statement.</span></span>

<span data-ttu-id="88c72-143">Оператор [**coclass**](/windows/desktop/Midl/coclass) определяет полностью новый класс компонента бкфсткомпонент, который включает два ранее определенных интерфейса, IFace1 и IFace2.</span><span class="sxs-lookup"><span data-stu-id="88c72-143">The [**coclass**](/windows/desktop/Midl/coclass) statement defines an entirely new component class, BkfstComponent, that includes two previously defined interfaces, IFace1 and IFace2.</span></span> <span data-ttu-id="88c72-144">Атрибут по умолчанию обозначает IFace1 как интерфейс по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="88c72-144">The default attribute designates IFace1 as the default interface.</span></span>

<span data-ttu-id="88c72-145">IFace4 описывается в операторе Library.</span><span class="sxs-lookup"><span data-stu-id="88c72-145">IFace4 is described within the library statement.</span></span> <span data-ttu-id="88c72-146">Атрибут [**propput**](/windows/desktop/Midl/propput) в методе указывает, что метод выполняет действие Set над свойством с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="88c72-146">The [**propput**](/windows/desktop/Midl/propput) attribute on MethodD indicates that the method performs a set action on a property of the same name.</span></span> <span data-ttu-id="88c72-147">Атрибут [**propget**](/windows/desktop/Midl/propget) указывает, что метод получает сведения из свойства с тем же именем, что и у метода.</span><span class="sxs-lookup"><span data-stu-id="88c72-147">The [**propget**](/windows/desktop/Midl/propget) attribute indicates that the method retrieves information from a property of the same name as the method.</span></span> <span data-ttu-id="88c72-148">Атрибут [**retval**](/windows/desktop/Midl/retval) в методе обозначает выходной параметр, который содержит возвращаемое значение функции.</span><span class="sxs-lookup"><span data-stu-id="88c72-148">The [**retval**](/windows/desktop/Midl/retval) attribute in MethodD designates an output parameter that contains the return value of the function.</span></span>

 

 
