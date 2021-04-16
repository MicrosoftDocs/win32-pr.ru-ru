---
title: Поддержка содержимого на стороне устройства (страница свойств)
description: Поддержка содержимого Device-Side
ms.assetid: ea11f8e6-fb53-46e4-b210-2dae33cdc056
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd7e054e4c545acd8f34583da5cd9ef3af347643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347415"
---
# <a name="supporting-device-side-content"></a>Поддержка содержимого на стороне устройства

Поскольку содержимое на стороне устройства недоступно в файловой системе Windows Vista, для получения данных об объектах устройств необходимо использовать API оболочки Windows или API-интерфейс WPD. Это основное различие между обычным обработчиком страницы свойств и обработчиком страницы свойств WPD. В следующем примере кода демонстрируется получение содержимого на стороне устройства с помощью API оболочки Windows.

Первым шагом является инициализация списка идентификаторов элементов или ПИДЛ. (Этот список содержит уникальный идентификатор для данного объекта устройства.)


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



Функция инициализации вызывает \_ функцию ексаминепидларрай, которая получает свойства объекта, идентифицируемого Пидл в массиве Пидл.


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



Помимо инициализации и обработки списка идентификаторов элементов, приложению потребуется реализовать метод Ишеллпропшитекст:: Реплацепаже и вставить соответствующие обработчики замены. Оболочка Windows вызывает этот метод каждый раз, когда он собирается отобразить заменяемую страницу свойств, давая приложению возможность вызвать соответствующий обработчик замены. Младшее слово первого параметра в методе Реплацепаже — это идентификатор для данной вкладки свойств, который будет отображаться в Windows. Значения, передаваемые в нижнем слове первого параметра, соответствуют значениям, определенным в файле Впдшеллекстенсион. h. Эти значения и их описания приведены в следующей таблице.



| Значение                                  | Описание                                                                 |
|----------------------------------------|-----------------------------------------------------------------------------|
| \_ \_ Общее устройство впднсе \_ пропшит     | Соответствует вкладке "Общие" для устройства.                              |
| Общие сведения о \_ хранилище впднсе пропшит \_ \_    | Соответствует вкладке "Общие" для объекта хранилища, найденного на устройстве.    |
| \_ \_ Общие сведения о содержимом впднсе пропшит \_    | Соответствует вкладке "Общие" для объекта содержимого, найденного на устройстве.      |
| \_ \_ ссылки на содержимое впднсе пропшит \_ | Соответствует вкладке "ссылки" для объекта содержимого, найденного на устройстве. |
| \_ \_ ресурсы содержимого впднсе \_ пропшит  | Соответствует вкладке "ресурсы" для объекта содержимого, найденного на устройстве.  |
| \_ \_ сведения о содержимом впднсе пропшит \_    | Соответствует вкладке сведений для объекта содержимого, найденного на устройстве.      |



 

В примере расширения страницы свойств метод Реплацепаже вызывает два обработчика замены: \_ реплацедевицеженерал и \_ реплацеконтентреференцес. Эти обработчики заменяют вкладки Общие устройства и ссылки на содержимое на вкладках расширяемых свойств.


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



Так как пользователь может выбрать несколько устройств, приложению потребуется сохранить массив ПИДЛ, возвращенный Ишеллекстинит:: Initialize, а затем проверить старшее слово первого параметра в Реплацепаже. Нулевое значение в этом высоком слове соответствует первому элементу в массиве ПИДЛ, значение One соответствует второму элементу и т. д. В примере функции Реплацепаже приложения это большое значение слова передается в обработчики замены. Эти обработчики, в свою очередь, используют это значение для задания конкретного устройства.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Инструкции по программированию**](programming-guide.md)
</dt> </dl>

 

 



