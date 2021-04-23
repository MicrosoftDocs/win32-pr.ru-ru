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
# <a name="pin-requirements-for-capture-filters"></a><span data-ttu-id="e8410-103">Требования к ПИН-коду для фильтров захвата</span><span class="sxs-lookup"><span data-stu-id="e8410-103">Pin Requirements for Capture Filters</span></span>

<span data-ttu-id="e8410-104">В этом разделе описываются требования к реализации выходного ПИН-кода для фильтра записи DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e8410-104">This topic describes the requirements for implementing an output pin on a DirectShow capture filter.</span></span>

## <a name="pin-name"></a><span data-ttu-id="e8410-105">Название контакта</span><span class="sxs-lookup"><span data-stu-id="e8410-105">Pin Name</span></span>

<span data-ttu-id="e8410-106">Можно задать ПИН-код любого имени.</span><span class="sxs-lookup"><span data-stu-id="e8410-106">You can give a pin any name.</span></span> <span data-ttu-id="e8410-107">Если имя ПИН-кода начинается с символа тильды (~), диспетчер графа фильтров не будет автоматически отображать этот ПИН-код, когда приложение вызывает [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span><span class="sxs-lookup"><span data-stu-id="e8410-107">If the pin name begins with the tilde (~) character, the Filter Graph Manager does not automatically render that pin when an application calls [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile).</span></span> <span data-ttu-id="e8410-108">Например, если фильтр имеет ПИН-код захвата и ПИН-код для предварительного просмотра, вы можете присвоить им имя "~ Capture" и "Preview" соответственно.</span><span class="sxs-lookup"><span data-stu-id="e8410-108">For example, if the filter has a capture pin and a preview pin, you might name them "~Capture" and "Preview," respectively.</span></span> <span data-ttu-id="e8410-109">Если приложение визуализирует этот фильтр в графе, то предварительный ПИН-код будет подключаться к своему модулю подготовки отчетов по умолчанию, и к нему не будет подключаться запись, что является разумным поведением по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e8410-109">If an application renders that filter in a graph, the preview pin will connect to its default renderer, and nothing will connect to the capture pin, which is a reasonable default behavior.</span></span> <span data-ttu-id="e8410-110">Это также может применяться к контактам, которые доставляют информационные данные, не предназначенные для подготовки к просмотру, или ПИН-коды, для которых требуется задать настраиваемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e8410-110">This can also apply to pins that deliver informational data that is not meant to be rendered, or pins that need custom properties set.</span></span> <span data-ttu-id="e8410-111">Обратите внимание, что контакты с префиксом тильды (~) по-прежнему могут быть подключены приложением вручную.</span><span class="sxs-lookup"><span data-stu-id="e8410-111">Note that pins with the tilde (~) prefix can still be connected manually by the application.</span></span>

## <a name="pin-category"></a><span data-ttu-id="e8410-112">Категория закрепления</span><span class="sxs-lookup"><span data-stu-id="e8410-112">Pin Category</span></span>

<span data-ttu-id="e8410-113">Фильтр записи всегда имеет ПИН-код записи и может иметь предварительный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="e8410-113">A capture filter always has a capture pin, and might have a preview pin.</span></span> <span data-ttu-id="e8410-114">Некоторые фильтры захвата могут иметь другие выходные сигналы для доставки других типов данных, таких как управляющая информация.</span><span class="sxs-lookup"><span data-stu-id="e8410-114">Some capture filters might have other output pins, to deliver other types of data, such as control information.</span></span> <span data-ttu-id="e8410-115">Каждый выходной ПИН-код должен предоставлять интерфейс [**икспропертисет**](ikspropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="e8410-115">Each output pin must expose the [**IKsPropertySet**](ikspropertyset.md) interface.</span></span> <span data-ttu-id="e8410-116">Приложения используют этот интерфейс для определения категории закрепления.</span><span class="sxs-lookup"><span data-stu-id="e8410-116">Applications use this interface to determine the pin category.</span></span> <span data-ttu-id="e8410-117">ПИН-код обычно возвращает либо \_ запись категории закрепления \_ , либо \_ \_ Предварительный просмотр категории закрепления.</span><span class="sxs-lookup"><span data-stu-id="e8410-117">The pin typically returns either PIN\_CATEGORY\_CAPTURE or PIN\_CATEGORY\_PREVIEW.</span></span> <span data-ttu-id="e8410-118">Дополнительные сведения см. в разделе [закрепить набор свойств](pin-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="e8410-118">For more information, see [Pin Property Set](pin-property-set.md).</span></span>

<span data-ttu-id="e8410-119">В следующем примере показано, как реализовать [**икспропертисет**](ikspropertyset.md) , чтобы вернуть категорию закрепления для ПИН-кода захвата.</span><span class="sxs-lookup"><span data-stu-id="e8410-119">The following example shows how to implement [**IKsPropertySet**](ikspropertyset.md) to return the pin category on a capture pin:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e8410-120">См. также</span><span class="sxs-lookup"><span data-stu-id="e8410-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8410-121">Запись фильтров записи</span><span class="sxs-lookup"><span data-stu-id="e8410-121">Writing Capture Filters</span></span>](writing-capture-filters.md)
</dt> </dl>

 

 



