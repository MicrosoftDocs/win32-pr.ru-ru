---
title: Запрос объекта для интерфейса
description: Запрос объекта для интерфейса
ms.assetid: 04296372-4897-426e-9be3-e6862a530ac6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a173342c7dba59c09cdef05c6b20d9d4d37da9d6971e6a7c26c1787b708121bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680750"
---
# <a name="asking-an-object-for-an-interface"></a>Запрос объекта для интерфейса

Ранее мы видели, что объект может реализовать более одного интерфейса. Объект диалогового окна общих элементов является реальным примером этого. Для поддержки наиболее типичных применений объект реализует интерфейс [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Этот интерфейс определяет основные методы для отображения диалогового окна и получения сведений о выбранном файле. Однако для более сложного использования объект также реализует интерфейс с именем [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize). Программа может использовать этот интерфейс для настройки внешнего вида и поведения диалогового окна путем добавления новых элементов управления пользовательского интерфейса.

Вспомним, что каждый COM-интерфейс должен прямо или косвенно наследовать от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . На следующей схеме показано наследование объекта диалогового окна общих элементов.

![Схема, показывающая интерфейсы, предоставляемые объектом диалогового окна общих элементов](images/com06.png)

Как видно из схемы, прямым предком [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) является интерфейс [**ифиледиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialog) , который, в свою очередь, наследует [**имодалвиндов**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-imodalwindow). Когда вы переходите к цепочке наследования от **ифилеопендиалог** к **имодалвиндов**, интерфейсы определяют все более обобщенные функциональные возможности окна. Наконец, интерфейс **имодалвиндов** наследует [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown). Объект диалогового окна общего элемента также реализует [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize), который существует в отдельной цепочке наследования.

Теперь предположим, что у вас есть указатель на интерфейс [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) . Как можно получить указатель на интерфейс [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) ?

![Схема, в которой показаны два указателя интерфейса на интерфейсы в одном объекте](images/com07.png)

Простое приведение указателя [**ифилеопендиалог**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) к указателю [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) не будет работать. В иерархии наследования нет надежного способа «перекрестное приведение» без какой-либо формы информации о типах во время выполнения (RTTI), что является очень зависимым от языка функцией.

Подход COM заключается *в том, чтобы предоставить* объекту указатель [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) , используя первый интерфейс в качестве программы передачи в объект. Это делается путем вызова метода [**IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) из первого указателя интерфейса. **QueryInterface** можно считать независимым от языка версией ключевого слова **Dynamic \_ Cast** в C++.

Метод [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) имеет следующую сигнатуру:

``` syntax
HRESULT QueryInterface(REFIID riid, void **ppvObject);
```

В зависимости от того, что вы уже знаете о [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), вы можете угадать, как работает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

-   Параметр *riid* — это идентификатор GUID, определяющий интерфейс, который вы запрашиваете. Тип данных **рефиид** является **typedef** для `const GUID&` . Обратите внимание, что идентификатор класса (CLSID) не является обязательным, поскольку объект уже был создан. Требуется только идентификатор интерфейса.
-   Параметр *ппвобжект* получает указатель на интерфейс. Тип данных этого параметра — **\* \* void**, по той же причине, что [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) использует этот тип данных: [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) может использоваться для запроса любого COM-интерфейса, поэтому параметр не может быть строго типизирован.

Вот как можно вызвать [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для получения указателя [**ифиледиалогкустомизе**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifiledialogcustomize) :


```C++
hr = pFileOpen->QueryInterface(IID_IFileDialogCustomize, 
    reinterpret_cast<void**>(&pCustom));
if (SUCCEEDED(hr))
{
    // Use the interface. (Not shown.)
    // ...

    pCustom->Release();
}
else
{
    // Handle the error.
}
```



Как всегда, проверьте возвращаемое значение **HRESULT** в случае сбоя метода. Если метод завершится с ошибкой, необходимо вызвать метод [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) , когда вы завершите работу с указателем, как описано в разделе [Управление временем существования объекта](managing-the-lifetime-of-an-object.md).

## <a name="next"></a>Следующая

[Выделение памяти в COM](memory-allocation-in-com.md)

 

 