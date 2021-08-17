---
description: выбор декодера в службах DirectShow editing Services
ms.assetid: dc6b0445-7fc1-4331-9000-a652b44a8364
title: выбор декодера в службах DirectShow editing Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcff63d44918a189f49e11527fe6fef35d108b7f20c1dadefa0a045e2c895b0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119341274"
---
# <a name="selecting-a-decoder-in-directshow-editing-services"></a>выбор декодера в службах DirectShow editing Services

\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]

когда [службы DirectShow редактирования](directshow-editing-services.md) данных (DES) визуализируют проект редактирования видео, механизм визуализации автоматически выбирает необходимые декодеры. Это может произойти внутри метода [**ирендеренгине:: коннектфронтенд**](irenderengine-connectfrontend.md) или динамически во время подготовки к просмотру.

Пользователь может установить несколько декодеров, способных декодировать определенный файл. если доступно несколько декодеров, DES использует алгоритм [интеллектуального Подключение](intelligent-connect.md) для выбора декодера.

В приложении нет способа указать, какой декодер следует использовать. Однако декодер можно выбрать опосредованно через интерфейс обратного вызова [**иамграфбуилдеркаллбакк**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) . Реализуя этот интерфейс в приложении, вы можете получать уведомления во время процесса построения графа и отклонять определенные фильтры из графа.

Начните с реализации класса, предоставляющего интерфейс [**иамграфбуилдеркаллбакк**](/windows/desktop/api/Strmif/nn-strmif-iamgraphbuildercallback) :


```C++
class GraphBuilderCB : public IAMGraphBuilderCallback
{
public:
     // Method declarations (not shown).
};
```



затем создайте экземпляр фильтра Graph Manager и зарегистрируйте свой класс для получения уведомлений обратного вызова:


```C++
// Declare an instance of the callback object.
GraphBuilderCB GraphCB; 

// Create the Filter Graph Manager.
CComPtr<IGraphBuilder> pGraph;
hr = pGraph.CoCreateInstance(CLSID_FilterGraph);
if (FAILED(hr))
{
    // Handle error (not shown).
}
// Register to receive the callbacks.
CComQIPtr<IObjectWithSite> pSite(pGraph);
if (pSite)
{
    hr = pSite->SetSite((IUnknown*)&GraphCB);
}
```



затем создайте подсистему визуализации и вызовите метод [**ирендеренгине:: сетфилтерграф**](irenderengine-setfiltergraph.md) с указателем на фильтр Graph Manager. это гарантирует, что модуль визуализации не создаст собственный фильтр Graph Manager, но вместо этого использует экземпляр, настроенный для обратных вызовов.


```C++
CComPtr<IRenderEngine> pRender;
hr = pRender.CoCreateInstance(CLSID_RenderEngine);
if (FAILED(hr))
{
    // Handle error (not shown).
}

hr = pRender->SetFilterGraph(pGraph);
```



при подготовке к просмотру проекта метод [**иамграфбуилдеркаллбакк:: селектедфилтер**](/windows/desktop/api/Strmif/nf-strmif-iamgraphbuildercallback-selectedfilter) приложения вызывается непосредственно перед тем, как фильтр Graph Manager создает новый фильтр. Метод **селектедфилтер** получает указатель на интерфейс **IMoniker** , представляющий моникер для фильтра. Проверьте моникер и, если вы решили отклонить фильтр, возвратите код ошибки из метода **селектедфилтер** .

Сложная часть состоит в том, чтобы определить, какие моникеры представляют декодеры — и в частности, какие моникеры представляют декодеры, которые нужно отклонить. Одним из решений является следующее:

-   Перед визуализацией проекта используйте метод [**IFilterMapper2:: енумматчингфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) , чтобы создать список фильтров, зарегистрированных как принимающий нужный тип входных данных. Для типов сжатия видео или аудио этот список должен сопоставляться с набором декодеров.
-   Метод **енумматчингфилтерс** Возвращает коллекцию моникеров. Для каждого моникера в коллекции следует получить свойство **DisplayName** , как описано в разделе [Использование модуля сопоставления фильтров](using-the-filter-mapper.md).
-   Сохраните список отображаемых имен, но не указывайте отображаемое имя, соответствующее фильтру, который вы хотите использовать для декодирования. Отображаемые имена для фильтров программного обеспечения имеют следующую форму:

    ```C++
    OLESTR("@device:sw:{CategoryGUID}\{FilterCLSID}");
    ```

    

    where

    ```C++
    CategoryGUID
    ```

    

    Идентификатор GUID категории фильтра.

    ```C++
    FilterCLSID
    ```

    

    Идентификатор CLSID фильтра. Для дмос формат совпадает, но измените `sw` на `dmo` .

    Теперь список содержит отображаемые имена для каждого фильтра, который выводит нужный тип мультимедиа, но не является предпочтительным фильтром.

-   В методе **селектедфилтер** получите свойство **DisplayName** в предложенном моникере и проверьте его на соответствие сохраненному списку. Если отображаемое имя совпадает с записью в списке, отклоните этот фильтр. В противном случае примите его, вернувшись в значение S \_ ОК.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Подготовка Project](rendering-a-project.md)
</dt> </dl>

 

 



