---
description: В этом разделе описываются требования к реализации выходного ПИН-кода для фильтра записи DirectShow.
ms.assetid: cb9cda1c-efa2-4abb-934b-21ba8cb80f30
title: Требования к ПИН-коду для фильтров захвата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2a97d3e5c0f7fe0f5a9a341899651685df1cdd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682214"
---
# <a name="pin-requirements-for-capture-filters"></a>Требования к ПИН-коду для фильтров захвата

В этом разделе описываются требования к реализации выходного ПИН-кода для фильтра записи DirectShow.

## <a name="pin-name"></a>Название контакта

Можно задать ПИН-код любого имени. Если имя ПИН-кода начинается с символа тильды (~), диспетчер графа фильтров не будет автоматически отображать этот ПИН-код, когда приложение вызывает [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile). Например, если фильтр имеет ПИН-код захвата и ПИН-код для предварительного просмотра, вы можете присвоить им имя "~ Capture" и "Preview" соответственно. Если приложение визуализирует этот фильтр в графе, то предварительный ПИН-код будет подключаться к своему модулю подготовки отчетов по умолчанию, и к нему не будет подключаться запись, что является разумным поведением по умолчанию. Это также может применяться к контактам, которые доставляют информационные данные, не предназначенные для подготовки к просмотру, или ПИН-коды, для которых требуется задать настраиваемые свойства. Обратите внимание, что контакты с префиксом тильды (~) по-прежнему могут быть подключены приложением вручную.

## <a name="pin-category"></a>Категория закрепления

Фильтр записи всегда имеет ПИН-код записи и может иметь предварительный ПИН-код. Некоторые фильтры захвата могут иметь другие выходные сигналы для доставки других типов данных, таких как управляющая информация. Каждый выходной ПИН-код должен предоставлять интерфейс [**икспропертисет**](ikspropertyset.md) . Приложения используют этот интерфейс для определения категории закрепления. ПИН-код обычно возвращает либо \_ запись категории закрепления \_ , либо \_ \_ Предварительный просмотр категории закрепления. Дополнительные сведения см. в разделе [закрепить набор свойств](pin-property-set.md).

В следующем примере показано, как реализовать [**икспропертисет**](ikspropertyset.md) , чтобы вернуть категорию закрепления для ПИН-кода захвата.


```C++
// Set: Cannot set any properties.
HRESULT CMyCapturePin::Set(REFGUID guidPropSet, DWORD dwID,
    void *pInstanceData, DWORD cbInstanceData, void *pPropData, 
    DWORD cbPropData)
{
    return E_NOTIMPL;
}

// Get: Return the pin category (our only property). 
HRESULT CMyCapturePin::Get(
    REFGUID guidPropSet,   // Which property set.
    DWORD dwPropID,        // Which property in that set.
    void *pInstanceData,   // Instance data (ignore).
    DWORD cbInstanceData,  // Size of the instance data (ignore).
    void *pPropData,       // Buffer to receive the property data.
    DWORD cbPropData,      // Size of the buffer.
    DWORD *pcbReturned     // Return the size of the property.
)
{
    if (guidPropSet != AMPROPSETID_Pin) 
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pPropData == NULL && pcbReturned == NULL)
        return E_POINTER;
    if (pcbReturned)
        *pcbReturned = sizeof(GUID);
    if (pPropData == NULL)  // Caller just wants to know the size.
        return S_OK;
    if (cbPropData < sizeof(GUID)) // The buffer is too small.
        return E_UNEXPECTED;
    *(GUID *)pPropData = PIN_CATEGORY_CAPTURE;
    return S_OK;
}

// QuerySupported: Query whether the pin supports the specified property.
HRESULT CMyCapturePin::QuerySupported(REFGUID guidPropSet, DWORD dwPropID,
    DWORD *pTypeSupport)
{
    if (guidPropSet != AMPROPSETID_Pin)
        return E_PROP_SET_UNSUPPORTED;
    if (dwPropID != AMPROPERTY_PIN_CATEGORY)
        return E_PROP_ID_UNSUPPORTED;
    if (pTypeSupport)
        // We support getting this property, but not setting it.
        *pTypeSupport = KSPROPERTY_SUPPORT_GET; 
    return S_OK;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Запись фильтров записи](writing-capture-filters.md)
</dt> </dl>

 

 



