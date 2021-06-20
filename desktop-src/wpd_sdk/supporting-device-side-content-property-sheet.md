---
title: Поддержка содержимого на стороне устройства (страница свойств)
description: Узнайте, как использовать API оболочки Windows или API-интерфейс WPD для получения данных объектов устройств, недоступных в файловой системе Windows Vista.
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aeade3745c37296b334c54af9edcc768fb8c93e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404197"
---
# <a name="supporting-device-side-content"></a><span data-ttu-id="ade92-103">Поддержка содержимого на стороне устройства</span><span class="sxs-lookup"><span data-stu-id="ade92-103">Supporting device-side content</span></span>

<span data-ttu-id="ade92-104">Поскольку содержимое на стороне устройства недоступно в файловой системе Windows Vista, для получения данных об объектах устройств необходимо использовать API оболочки Windows или API-интерфейс WPD.</span><span class="sxs-lookup"><span data-stu-id="ade92-104">Because device-side content is not accessible through the file system in Windows Vista, you'll need to use either the Windows Shell API or the WPD API to retrieve data for device objects.</span></span> <span data-ttu-id="ade92-105">Это основное различие между обычным обработчиком страницы свойств и обработчиком страницы свойств WPD.</span><span class="sxs-lookup"><span data-stu-id="ade92-105">This is the primary difference between a normal property sheet handler and a WPD property sheet handler.</span></span> <span data-ttu-id="ade92-106">В следующем примере кода демонстрируется получение содержимого на стороне устройства с помощью API оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="ade92-106">The following sample code demonstrates the retrieval of device-side content using the Windows Shell API.</span></span>

<span data-ttu-id="ade92-107">Первым шагом является инициализация списка идентификаторов элементов или ПИДЛ.</span><span class="sxs-lookup"><span data-stu-id="ade92-107">The first step is the initialization of the item identifier list or PIDL.</span></span> <span data-ttu-id="ade92-108">(Этот список содержит уникальный идентификатор для данного объекта устройства.)</span><span class="sxs-lookup"><span data-stu-id="ade92-108">(This list contains the unique identifier for the given device object.)</span></span>


```C++
HRESULT CWPDPropSheet::_InitializePIDLArray(IDataObject *pDataObj)
{
    if (m_cfHIDA == 0)
    {
        m_cfHIDA = (CLIPFORMAT)RegisterClipboardFormat(CFSTR_SHELLIDLIST);
    }

    STGMEDIUM   medium;
    FORMATETC   fmte = {m_cfHIDA, NULL, DVASPECT_CONTENT, -1, TYMED_HGLOBAL};

    m_pPropInfo = (PROPINFO*)LocalAlloc(LPTR, sizeof(PROPINFO));
    if (m_pPropInfo == NULL)
        return E_OUTOFMEMORY;

    AddRef_PropInfo(m_pPropInfo);

    HRESULT hr = pDataObj->GetData(&fmte, &medium);
    if (SUCCEEDED(hr))
    {
        SIZE_T cb = GlobalSize(medium.hGlobal);
        CIDA *pida = (CIDA*)GlobalAlloc(GPTR, cb);
        if (pida)
        {
            void *pv = GlobalLock(medium.hGlobal);
            if (pv != NULL)
            {
                CopyMemory(pida, pv, cb);
                GlobalUnlock(medium.hGlobal);
                m_pPropInfo->pida = pida;
                _ExaminePIDLArray();
            }
            else
            {
                hr = E_UNEXPECTED;
            }
        }
        else
        {
            hr = E_OUTOFMEMORY;
        }
        ReleaseStgMedium(&medium);
    }

    return hr;
}
```



<span data-ttu-id="ade92-109">Функция инициализации вызывает \_ функцию ексаминепидларрай, которая получает свойства объекта, идентифицируемого Пидл в массиве Пидл.</span><span class="sxs-lookup"><span data-stu-id="ade92-109">The initialization function calls the \_ExaminePIDLArray function, which retrieves the properties for object identified by a PIDL in the PIDL array.</span></span>


```C++
HRESULT CWPDPropSheet::_ExaminePIDLArray()
{
    CComPtr<IShellFolder2> spParentFolder;

    CComVariant  variant;

    LPITEMIDLIST pidl = NULL;
    HRESULT      hr = S_OK;
    UINT         index = 0;

    pidl = GetPIDL(m_pPropInfo->pida, index);
    if (pidl)
    {
        hr = SHBindToParent(pidl, IID_PPV_ARGS(&spParentFolder), NULL);
        IF_FAILED_JUMP(hr, Exit);
    }

    do
    {
        CComPtr<IPropertySetStorage> spSetStorage;
        CComPtr<IPropertyStorage>    spPropStorage;

        // Get the IpropertySetStorage interface for this PIDL. This method could also
        // be used to retrieve an IPortableDevice interface to allow more low-level interaction
        // with the WPD API.
        hr = spParentFolder->BindToObject(ILFindLastID(pidl), NULL, IID_PPV_ARGS(&spSetStorage));
        if (SUCCEEDED(hr))
        {
            hr = spSetStorage->Open(WPD_FUNCTIONAL_OBJECT_PROPERTIES_V1, STGM_READ, &spPropStorage);
            if (SUCCEEDED(hr))
            {
                PROPVARIANT PropVar = {0};
                PROPSPEC    PropSpec = {0};

                PropSpec.ulKind = PRSPEC_PROPID;
                PropSpec.propid = 2; // WPD_FUNCTIONAL_OBJECT_CATEGORY

                PropVariantInit(&PropVar);

                hr = spPropStorage->ReadMultiple(1, &PropSpec, &PropVar);
                if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                {
                    // The PIDL array contains a non-file object.
                    // This means we don't want to take over the
                    // default menu action.
                    m_bPIDAContainsOnlyFiles = FALSE;
                    PropVariantClear(&PropVar);
                    break;
                }
                else
                {
                    CComPtr<IPropertyStorage>    spObjectProperties;
                    hr = spSetStorage->Open(WPD_OBJECT_PROPERTIES_V1, STGM_READ, &spObjectProperties);
                    if (SUCCEEDED(hr))
                    {
                        PropSpec.ulKind = PRSPEC_PROPID;
                        PropSpec.propid = 7; // WPD_OBJECT_CONTENT_TYPE
                        
                        PropVariantClear(&PropVar);
                        hr = spObjectProperties->ReadMultiple(1, &PropSpec, &PropVar);
                        if (SUCCEEDED(hr) && PropVar.vt == VT_CLSID)
                        {
                            if (IsEqualGUID(*PropVar.puuid, WPD_CONTENT_TYPE_FOLDER))
                            {
                                // The PIDL array contains a folder object.
                                // This means we don't want to take over the
                                // default menu action.
                                m_bPIDAContainsOnlyFiles = FALSE;
                                PropVariantClear(&PropVar);
                                break;
                            }
                        }
                    }
                }

                PropVariantClear(&PropVar);
            }
        }

        UI_SAFE_ILFREE(pidl);

        pidl = GetPIDL(m_pPropInfo->pida, ++index);
    } while (pidl != NULL && index < m_pPropInfo->pida->cidl);

Exit:
    UI_SAFE_ILFREE(pidl);
    return hr;
}
```



<span data-ttu-id="ade92-110">Помимо инициализации и обработки списка идентификаторов элементов, приложению потребуется реализовать метод Ишеллпропшитекст:: Реплацепаже и вставить соответствующие обработчики замены.</span><span class="sxs-lookup"><span data-stu-id="ade92-110">In addition to the initialization and processing of the item identifier list, your application will need to implement the IShellPropSheetExt::ReplacePage method and insert the appropriate replacement handlers.</span></span> <span data-ttu-id="ade92-111">Оболочка Windows вызывает этот метод каждый раз, когда он собирается отобразить заменяемую страницу свойств, давая приложению возможность вызвать соответствующий обработчик замены.</span><span class="sxs-lookup"><span data-stu-id="ade92-111">The Windows Shell calls this method each time it is about to display a replaceable property sheet, giving your application a chance to invoke a corresponding replacement handler.</span></span> <span data-ttu-id="ade92-112">Младшее слово первого параметра в методе Реплацепаже — это идентификатор для данной вкладки свойств, который будет отображаться в Windows.</span><span class="sxs-lookup"><span data-stu-id="ade92-112">The low word of the first parameter to the ReplacePage method is an identifier for the given property sheet that Windows is about to display.</span></span> <span data-ttu-id="ade92-113">Значения, передаваемые в нижнем слове первого параметра, соответствуют значениям, определенным в файле Впдшеллекстенсион. h.</span><span class="sxs-lookup"><span data-stu-id="ade92-113">The values passed in the low word of the first parameter correspond to values defined in the file WpdShellExtension.h.</span></span> <span data-ttu-id="ade92-114">Эти значения и их описания приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ade92-114">These values and their descriptions appear in the following table.</span></span>



| <span data-ttu-id="ade92-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ade92-115">Value</span></span>                                  | <span data-ttu-id="ade92-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ade92-116">Description</span></span>                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="ade92-117">\_ \_ Общее устройство впднсе \_ пропшит</span><span class="sxs-lookup"><span data-stu-id="ade92-117">WPDNSE\_PROPSHEET\_DEVICE\_GENERAL</span></span>     | <span data-ttu-id="ade92-118">Соответствует вкладке "Общие" для устройства.</span><span class="sxs-lookup"><span data-stu-id="ade92-118">Corresponds to the general tab for the device.</span></span>                              |
| <span data-ttu-id="ade92-119">Общие сведения о \_ хранилище впднсе пропшит \_ \_</span><span class="sxs-lookup"><span data-stu-id="ade92-119">WPDNSE\_PROPSHEET\_STORAGE\_GENERAL</span></span>    | <span data-ttu-id="ade92-120">Соответствует вкладке "Общие" для объекта хранилища, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade92-120">Corresponds to the general tab for a storage object found on the device.</span></span>    |
| <span data-ttu-id="ade92-121">\_ \_ Общие сведения о содержимом впднсе пропшит \_</span><span class="sxs-lookup"><span data-stu-id="ade92-121">WPDNSE\_PROPSHEET\_CONTENT\_GENERAL</span></span>    | <span data-ttu-id="ade92-122">Соответствует вкладке "Общие" для объекта содержимого, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade92-122">Corresponds to the general tab for content object found on the device.</span></span>      |
| <span data-ttu-id="ade92-123">\_ \_ ссылки на содержимое впднсе пропшит \_</span><span class="sxs-lookup"><span data-stu-id="ade92-123">WPDNSE\_PROPSHEET\_CONTENT\_REFERENCES</span></span> | <span data-ttu-id="ade92-124">Соответствует вкладке "ссылки" для объекта содержимого, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade92-124">Corresponds to the references tab for a content object found on the device.</span></span> |
| <span data-ttu-id="ade92-125">\_ \_ ресурсы содержимого впднсе \_ пропшит</span><span class="sxs-lookup"><span data-stu-id="ade92-125">WPDNSE\_PROPSHEET\_CONTENT\_RESOURCES</span></span>  | <span data-ttu-id="ade92-126">Соответствует вкладке "ресурсы" для объекта содержимого, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade92-126">Corresponds to the resources tab for a content object found on the device.</span></span>  |
| <span data-ttu-id="ade92-127">\_ \_ сведения о содержимом впднсе пропшит \_</span><span class="sxs-lookup"><span data-stu-id="ade92-127">WPDNSE\_PROPSHEET\_CONTENT\_DETAILS</span></span>    | <span data-ttu-id="ade92-128">Соответствует вкладке сведений для объекта содержимого, найденного на устройстве.</span><span class="sxs-lookup"><span data-stu-id="ade92-128">Corresponds to a details tab for a content object found on the device.</span></span>      |



 

<span data-ttu-id="ade92-129">В примере расширения страницы свойств метод Реплацепаже вызывает два обработчика замены: \_ реплацедевицеженерал и \_ реплацеконтентреференцес.</span><span class="sxs-lookup"><span data-stu-id="ade92-129">In the sample property sheet extension, the ReplacePage method invokes two replacement handlers: \_ReplaceDeviceGeneral and \_ReplaceContentReferences.</span></span> <span data-ttu-id="ade92-130">Эти обработчики заменяют вкладки Общие устройства и ссылки на содержимое на вкладках расширяемых свойств.</span><span class="sxs-lookup"><span data-stu-id="ade92-130">These handlers replace the general device and the content references tabs in the extensible property sheets.</span></span>


```C++
STDMETHODIMP CWPDPropSheet::ReplacePage(UINT uPageID, LPFNADDPROPSHEETPAGE lpfnReplacePage, LPARAM lParam)
{
    HRESULT       hr = S_OK;

    if (LOWORD(uPageID) == WPDNSE_PROPSHEET_DEVICE_GENERAL)
    {
        hr = _ReplaceDeviceGeneral(HIWORD(uPageID), lpfnReplacePage, lParam);
    }
    else if (LOWORD(uPageID) == WPDNSE_PROPSHEET_CONTENT_REFERENCES)
    {
        hr = _ReplaceContentReferences(HIWORD(uPageID), lpfnReplacePage, lParam);
    }

    return hr;
}
```



<span data-ttu-id="ade92-131">Так как пользователь может выбрать несколько устройств, приложению потребуется сохранить массив ПИДЛ, возвращенный Ишеллекстинит:: Initialize, а затем проверить старшее слово первого параметра в Реплацепаже.</span><span class="sxs-lookup"><span data-stu-id="ade92-131">Because it is possible for a user to select multiple devices, an application will need to save the PIDL array returned by IShellExtInit::Initialize and then examine the high word of the first parameter to ReplacePage.</span></span> <span data-ttu-id="ade92-132">Нулевое значение в этом высоком слове соответствует первому элементу в массиве ПИДЛ, значение One соответствует второму элементу и т. д.</span><span class="sxs-lookup"><span data-stu-id="ade92-132">A value of zero in this high word corresponds to the first element in the PIDL array, a value of one corresponds to the second element, and so on.</span></span> <span data-ttu-id="ade92-133">В примере функции Реплацепаже приложения это большое значение слова передается в обработчики замены.</span><span class="sxs-lookup"><span data-stu-id="ade92-133">In the sample application's ReplacePage function, this high word value is passed to both replacement handlers.</span></span> <span data-ttu-id="ade92-134">Эти обработчики, в свою очередь, используют это значение для задания конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="ade92-134">These handlers, in turn, use this value to identify a particular device.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ade92-135">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ade92-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ade92-136">**Инструкции по программированию**</span><span class="sxs-lookup"><span data-stu-id="ade92-136">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



