---
description: Описывает, как инициализировать объектную модель XPS, которая позволяет программе создавать документы XPS.
ms.assetid: 920d940f-5ae2-4376-8c7b-0cef04f21df7
title: Инициализация объектной модели XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cac44a69d171c1d38633512b0e275dcdeaea8738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344832"
---
# <a name="initialize-an-xps-om"></a>Инициализация объектной модели XPS

Описывает, как инициализировать объектную модель XPS, которая позволяет программе создавать документы XPS.

Интерфейсы API документа XPS создаются интерфейсом [**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) . Чтобы получить указатель на **икспсомобжектфактори** , который можно использовать в программе, вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

Прежде чем использовать приведенные ниже примеры кода в программе, ознакомьтесь со сведениями об отказе в [типичных задачах программирования документов XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Пример кода

В следующем примере создается фабрика объектов, которая будет использоваться для создания интерфейсов OM-модели XPS в других примерах.


```C++
    IXpsOMObjectFactory *xpsFactory;

    HRESULT hr = S_OK;

    // Init COM for this thread if it hasn't 
    //  been initialized, yet.
    hr = CoInitializeEx(0, COINIT_MULTITHREADED);

    hr = CoCreateInstance(
        __uuidof(XpsOMObjectFactory),
        NULL, 
        CLSCTX_INPROC_SERVER,
        __uuidof(IXpsOMObjectFactory),
        reinterpret_cast<LPVOID*>(&xpsFactory));

    if (SUCCEEDED(hr))
    {
        // Make sure that you got a pointer 
        //  to the interface.

        // Use object factory...

        // ... and release when done
        xpsFactory->Release();
    }

    // Uninitialize COM when finished
    CoUninitialize();
```



## <a name="best-practices"></a>Рекомендации

Чтобы сделать программу более эффективной, можно получить указатель на интерфейс [**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory) в первый раз, когда необходимо вызвать **икспсомобжектфактори** для создания интерфейса, а затем сохранить указатель для использования в других областях программы. Если программе больше не требуется фабрика объектов или она не понадобится в течение определенного времени, указатель может быть освобожден.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Следующие шаги**
</dt> <dt>

[Создание пустой объектной модели XPS](create-a-blank-xps-om.md)
</dt> <dt>

**Используется в этом разделе**
</dt> <dt>

[**икспсомобжектфактори**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)
</dt> <dt>

**Дополнительные сведения**
</dt> <dt>

[Упаковка](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Справочник по API документов XPS](xps-programming-reference.md)
</dt> <dt>

[XPS](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
