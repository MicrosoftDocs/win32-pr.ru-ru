---
title: Ипапер Загрузка
description: В следующем примере кода C++ показано, как открыть существующий поток в хранилище, прочитать свойства новой бумаги в и установить их в качестве текущих значений для собумаги.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Ипапер Загрузка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986712"
---
# <a name="ipaperload"></a>Ипапер:: Load

В следующем примере кода C++ показано, как открыть существующий поток в хранилище, прочитать свойства новой бумаги в и установить их в качестве текущих значений для собумаги.

Ниже приведен метод **ипапер:: Load** из paper. cpp.


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



Теперь вызывается метод [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) , чтобы открыть существующий поток в хранилище с именем "папердата". Флаги режима доступа доступны только для чтения, прямого и без общего доступа. Когда поток открыт, вызывается метод [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) для чтения \_ структуры свойств бумаги. Если фактически считанная сумма не соответствует запрошенной сумме, операция загрузки прерывается и \_ возвращается ошибка E. Если версия формата в свойствах только что прочитанного документа \_ не распознана, операция загрузки прерывается, а **Load** возвращает E \_ Fail.

При наличии допустимой версии формата данных рукописного ввода размер нового массива данных рукописного ввода из \_ свойств бумаги, считанного в, используется для выделения нового массива рукописных данных требуемого размера. Существующие рукописные данные удаляются, и их данные теряются. Если эти данные были ценными, они должны быть сохранены до вызова **загрузки** . После выделения нового массива снова вызывается метод [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) для считывания данных в массив из потока. Если этот вызов будет выполнен, значения в свойствах только для чтения документа будут приняты в качестве текущих значений для собумаги.

Во время этой операции загрузки \_ для хранения новых свойств, считываемых в, используется временная структура свойств бумаги невпропс. Если все прошло успешную загрузку, Невпропс копируется в \_ структуру свойств бумаги m \_ паперпропертиес. Как и раньше, после завершения загрузки и удаления [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) указатель **IStream** освобождается.

Если в конце **загрузки** возникает ошибка, то массив рукописных данных удаляется, так как он может содержать поврежденные данные.

Если в конце **загрузки** нет ошибок, вызывается метод Client [**Ипаперсинк:: Loaded**](ipapersink-methods.md) в методе Internal нотифисинкс, чтобы уведомить клиента о завершении операции загрузки. Это важное уведомление для клиента, так как оно должно отображать новые загруженные данные рукописного ввода. Это уведомление существенно использует возможности подключаемых объектов в содокументе.

 

 




