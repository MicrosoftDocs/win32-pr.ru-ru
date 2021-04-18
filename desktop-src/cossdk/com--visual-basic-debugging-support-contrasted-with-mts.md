---
description: Поддержка отладки Visual Basic COM+ отличается от MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Поддержка отладки Visual Basic COM+ отличается от MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710761"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Поддержка отладки Visual Basic COM+ отличается от MTS

COM+ удаляет или сокращает некоторые ограничения на отладку с помощью Microsoft Visual Basic 6,0 и MTS. В следующем списке перечислены изменения, которые можно выполнять с помощью COM+:

-   Отладка нескольких компонентов — в COM+ можно выполнять отладку сценариев, в которых клиент, работающий в одном экземпляре интегрированной среды разработки, выполняет вызовы к любому числу библиотек DLL, выполняющихся в другой, в качестве группы проектов. Объекты в проектах с группировкой библиотек DLL могут вызывать друг друга произвольно, переносящий контекст по мере необходимости. Конечно, это также работает, если библиотеки DLL и клиент находятся в одной группе проектов в одном и том же экземпляре интегрированной среды разработки.

-   Ограничения на отладку для \_ инициализации класса и \_ событий прекращения класса — с помощью COM+ можно размещать код в \_ событиях инициализации и \_ прекращения класса в компоненте приложения COM+, даже если этот код пытается получить доступ к объекту или соответствующему ему контекстному объекту. В нем можно установить точки останова и использовать контрольные значения. Можно также задать точки останова в \_ событии класса Terminate.

    Хотя в качестве обходного пути больше не требуется, можно по-прежнему реализовать интерфейс [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) и использовать методы [**активации**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) и [**деактивации**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) , если необходимо выполнить код во время запуска и завершения работы компонента. Кроме того, теперь можно размещать точки останова в коде для методов **Deactivate** или [**канбепулед**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) .

-   Наблюдение за объектами MTS. с помощью COM+ можно добавлять контрольные значения для переменных объектов, возвращаемых COM+, в том числе возвращаемых значений из методов [**сафереф**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**ObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)и [**иобжектконтекст:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) .

-   Повышенная стабильность при сбое компонентов — в COM+ сбой компонента больше не всегда останавливается Visual Basic (который выполняется в том же процессе, что и отлаживаемый компонент). Например, поддержка ошибок повторной активации JIT теперь позволяет просматривать контекст объекта во время отладки.

-   Отладчик может повторно активировать объекты, выпущенные COM+ — как и MTS, Visual Basic 6,0 может повторно активировать объекты COM+ при отладке одного шага через клиент. Из-за способа, которым Visual Basic 6,0 обнаруживает сведения об объектах, это ожидаемое поведение. Рассмотрим следующий пример кода:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Значение, если obj. Метод теста вызывает [**иобжектконтекст:: сеткомплете**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), com+ немедленно освобождает obj из памяти, но для OBJ еще не задано значение Nothing. При использовании obj. Возвращаемые тесты. отладчик Visual Basic вызывает [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) на obj-интерфейсе для интерфейса [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) . Обертка контекста, связанная с OBJ, создает новый экземпляр MyApp. MyClass для обслуживания вызова **QueryInterface** . В результате этот неинициализированный объект будет отображаться в отладчике после obj. Тест возвращен. Этот объект отображается только в отладчике и удаляется последующей инструкцией, чтобы присвоить параметру obj значение Nothing.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Отладка скомпилированных компонентов Visual Basic](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Отладка в интегрированной среде разработки Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
