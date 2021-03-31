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
# <a name="anatomy-of-an-idl-file"></a>Анатомия IDL-файла

В этих примерах файлов IDL демонстрируются фундаментальные конструкции определения интерфейса. Выделение памяти, Пользовательский маршалирование и асинхронный обмен сообщениями — всего лишь несколько функций, которые можно реализовать в пользовательском интерфейсе COM. Атрибуты MIDL используются для определения COM-интерфейсов. Дополнительные сведения о реализации интерфейсов и библиотек типов, включая сводку по атрибутам MIDL, см. в разделе [определения интерфейсов и библиотеки типов](/windows/desktop/Midl/interface-definitions-and-type-libraries) в руководстве и Справочнике программиста по MIDL. Полный справочник по всем атрибутам, ключевым словам и директивам MIDL см. в [справочнике по языку MIDL](/windows/desktop/Midl/midl-language-reference).

## <a name="exampleidl"></a>Пример. idl

В следующем примере файла IDL определяются два COM-интерфейса. Из этого IDL-файла Midl.exe создаст прокси-сервер/заглушку и маршалирует код и файлы заголовков. В этом примере следуют построчные разрывы.

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

Здесь используется оператор [**импорта**](/windows/desktop/Midl/import) IDL, чтобы поместить в файл заголовка мидефс. h, который содержит определяемые пользователем типы, и ункнвн. idl, который содержит определение [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), от которого наследуется IFace1 и IFace2.

Атрибут [**Object**](/windows/desktop/Midl/object) определяет интерфейс как объектный интерфейс и сообщает КОМПИЛЯТОРу MIDL, что вместо заглушек клиента и сервера RPC создается код прокси-сервера или заглушки. Методы объектного интерфейса должны иметь возвращаемый тип [**HRESULT**](/openspecs/windows_protocols/ms-erref/0642cb2f-2075-4469-918c-4441e69c548a), чтобы базовый механизм RPC выдать сообщение об ошибках для вызовов, которые не удалось завершить из-за проблем с сетью.

Атрибут [**UUID**](/windows/desktop/Midl/uuid) задает идентификатор интерфейса (IID). Каждый интерфейс, класс и библиотека типов должны быть идентифицированы с помощью собственного уникального идентификатора. Используйте Uuidgen.exe служебной программы для создания набора уникальных идентификаторов для интерфейсов и других компонентов.

Ключевое слово [**Interface**](/windows/desktop/Midl/interface) определяет имя интерфейса. Все интерфейсы объектов должны прямо или косвенно наследовать от [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown).

Параметр [**в**](/windows/desktop/Midl/in) направлении задает параметр, заданный только вызывающим объектом. Параметр [**out**](/windows/desktop/Midl/out-idl) указывает данные, которые передаются обратно вызывающему объекту. Использование обоих атрибутов направления в одном параметре указывает, что параметр используется как для отправки данных в метод, так и для передачи данных обратно вызывающему объекту.

Атрибут [**указателя \_ по умолчанию**](/windows/desktop/Midl/pointer-default) задает тип указателя по умолчанию ([**UNIQUE**](/windows/desktop/Midl/unique), [**ref**](/windows/desktop/Midl/ref)или [**ptr**](/windows/desktop/Midl/ptr)) для всех указателей, за исключением тех, которые входят в списки параметров. Если тип по умолчанию не указан, то MIDL предполагает, что одиночные указатели являются **уникальными**. Однако при наличии нескольких уровней указателей необходимо явно указать тип указателя по умолчанию, даже если требуется, чтобы тип по умолчанию был **уникальным**.

В предыдущем примере массив Бкфстстуфф \[ \] является *согласованным массивом*, размер которого определяется во время выполнения. Атрибут [**Max \_ —**](/windows/desktop/Midl/max-is) указывает переменную, которая содержит максимальное значение для индекса массива.

Атрибут [**size \_**](/windows/desktop/Midl/size-is) также используется для указания размера массива или, как в предыдущем примере, нескольких уровней указателей. В этом примере вызов можно выполнить без предварительного знания того, сколько данных будет возвращено.

## <a name="example2idl"></a>Example2. idl

В следующем примере IDL (который повторно использует интерфейсы, описанные в предыдущем примере IDL) показаны различные способы создания сведений о библиотеке типов для интерфейсов.

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

Атрибут [**helpString**](/windows/desktop/Midl/helpstring) является необязательным. Он используется для краткого описания объекта или для предоставления строки состояния. Эти строки справки могут быть доступны для чтения с помощью обозревателя объектов, например, предоставленного в Microsoft Visual Basic.

[**Двойной**](/windows/desktop/Midl/dual) атрибут в IFace3 создает интерфейс, который является интерфейсом диспетчеризации и COM-интерфейсом. Так как он является производным от **IDispatch**, сдвоенный интерфейс поддерживает автоматизацию, что указывает атрибут [**oleautomation**](/windows/desktop/Midl/oleautomation) . IFace3 импортирует Оаидл. idl, чтобы получить определение **IDispatch**.

Оператор [**Library**](/windows/desktop/Midl/library) определяет библиотеку типов ексамплелиб, которая имеет собственные атрибуты [**UUID**](/windows/desktop/Midl/uuid), [**helpString**](/windows/desktop/Midl/helpstring)и [**Version**](/windows/desktop/Midl/version) .

В определении библиотеки типов директива [**importlib**](/windows/desktop/Midl/importlib) переносит в скомпилированную библиотеку типов. Все определения библиотек типов должны переноситься в базовую библиотеку типов, определенную в Stdole32. tlb.

Это определение библиотеки типов демонстрирует три разных способа включения интерфейсов в библиотеку типов. IFace3 включается просто путем ссылки на него в операторе Library.

Оператор [**coclass**](/windows/desktop/Midl/coclass) определяет полностью новый класс компонента бкфсткомпонент, который включает два ранее определенных интерфейса, IFace1 и IFace2. Атрибут по умолчанию обозначает IFace1 как интерфейс по умолчанию.

IFace4 описывается в операторе Library. Атрибут [**propput**](/windows/desktop/Midl/propput) в методе указывает, что метод выполняет действие Set над свойством с тем же именем. Атрибут [**propget**](/windows/desktop/Midl/propget) указывает, что метод получает сведения из свойства с тем же именем, что и у метода. Атрибут [**retval**](/windows/desktop/Midl/retval) в методе обозначает выходной параметр, который содержит возвращаемое значение функции.

 

 
