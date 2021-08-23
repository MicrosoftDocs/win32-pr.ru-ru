---
description: Отображение страниц свойств фильтра
ms.assetid: 4a5f6938-7b33-4350-b8fa-cf78c5c44bcd
title: Отображение страниц свойств фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f0e29654983ee51b98666411a11f7130eb896c380ec754b5576862c313dcbc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016141"
---
# <a name="displaying-a-filters-property-pages"></a>Отображение страниц свойств фильтра

Страница свойств является одним из способов, с помощью которых фильтр поддерживает свойства, которые пользователь может задать. В этой статье описывается, как отобразить страницы свойств фильтра в приложении. Дополнительные сведения о страницах свойств см. в документации по пакету SDK для платформы.

> [!Note]  
> несмотря на то, что многие фильтры, предоставляемые со страницами свойств, поддерживаются DirectShow, они предназначены для отладки и не рекомендуются для использования приложением. В большинстве случаев Аналогичная функциональность предоставляется через пользовательский интерфейс фильтра. Приложение должно управлять этими фильтрами программным способом, а не предоставлять пользователям страницы свойств.

 

Фильтры со страницами свойств предоставляют интерфейс **испеЦифипропертипажес** . Чтобы определить, определяет ли фильтр страницу свойств, запросите фильтр для этого интерфейса с помощью **QueryInterface**.

Если вы непосредственно создали экземпляр фильтра (путем вызова **CoCreateInstance**), у вас уже есть указатель на фильтр. В противном случае можно перечислить фильтры в графе с помощью метода [**ифилтерграф:: енумфилтерс**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) . Дополнительные сведения см. [в разделе Перечисление объектов в фильтре Graph](enumerating-objects-in-a-filter-graph.md).

Получив указатель интерфейса **испеЦифипропертипажес** , извлеките страницы свойств фильтра, вызвав метод **испеЦифипропертипажес::** . Этот метод заполняет считанный массив глобально уникальных идентификаторов (GUID) с помощью идентификатора класса (CLSID) каждой страницы свойств. Подсчет массива определяется структурой **каууид** , которую необходимо выделить, но не нужно инициализировать. Метод **IsArray** выделяет массив, который содержится в элементе **пелемс** структуры **каууид** . По завершении Освободите массив, вызвав функцию **CoTaskMemFree** .

Функция **олекреатепропертифраме** предоставляет простой способ отобразить страницы свойств в модальном диалоговом окне.


```C++
IBaseFilter *pFilter;
/* Obtain the filter's IBaseFilter interface. (Not shown) */
ISpecifyPropertyPages *pProp;
HRESULT hr = pFilter->QueryInterface(IID_ISpecifyPropertyPages, (void **)&pProp);
if (SUCCEEDED(hr)) 
{
    // Get the filter's name and IUnknown pointer.
    FILTER_INFO FilterInfo;
    hr = pFilter->QueryFilterInfo(&FilterInfo); 
    IUnknown *pFilterUnk;
    pFilter->QueryInterface(IID_IUnknown, (void **)&pFilterUnk);

    // Show the page. 
    CAUUID caGUID;
    pProp->GetPages(&caGUID);
    pProp->Release();
    OleCreatePropertyFrame(
        hWnd,                   // Parent window
        0, 0,                   // Reserved
        FilterInfo.achName,     // Caption for the dialog box
        1,                      // Number of objects (just the filter)
        &pFilterUnk,            // Array of object pointers. 
        caGUID.cElems,          // Number of property pages
        caGUID.pElems,          // Array of property page CLSIDs
        0,                      // Locale identifier
        0, NULL                 // Reserved
    );

    // Clean up.
    pFilterUnk->Release();
    FilterInfo.pGraph->Release(); 
    CoTaskMemFree(caGUID.pElems);
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[основные задачи DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 



