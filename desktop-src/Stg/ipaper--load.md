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
# <a name="ipaperload"></a><span data-ttu-id="383db-104">Ипапер:: Load</span><span class="sxs-lookup"><span data-stu-id="383db-104">IPaper::Load</span></span>

<span data-ttu-id="383db-105">В следующем примере кода C++ показано, как открыть существующий поток в хранилище, прочитать свойства новой бумаги в и установить их в качестве текущих значений для собумаги.</span><span class="sxs-lookup"><span data-stu-id="383db-105">The following C++ sample code shows how to open the existing stream in the storage, read new paper properties in and then set them as the current values for COPaper.</span></span>

<span data-ttu-id="383db-106">Ниже приведен метод **ипапер:: Load** из paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="383db-106">The following is the **IPaper::Load** method from Paper.cpp.</span></span>


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



<span data-ttu-id="383db-107">Теперь вызывается метод [**IStorage:: опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) , чтобы открыть существующий поток в хранилище с именем "папердата".</span><span class="sxs-lookup"><span data-stu-id="383db-107">Now, the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method is called to open the existing stream in the storage called "PAPERDATA".</span></span> <span data-ttu-id="383db-108">Флаги режима доступа доступны только для чтения, прямого и без общего доступа.</span><span class="sxs-lookup"><span data-stu-id="383db-108">Access mode flags are for read-only, direct, and non-shared exclusive access.</span></span> <span data-ttu-id="383db-109">Когда поток открыт, вызывается метод [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) для чтения \_ структуры свойств бумаги.</span><span class="sxs-lookup"><span data-stu-id="383db-109">When the stream is open, the [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) method is called to read the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="383db-110">Если фактически считанная сумма не соответствует запрошенной сумме, операция загрузки прерывается и \_ возвращается ошибка E.</span><span class="sxs-lookup"><span data-stu-id="383db-110">If the amount actually read does not equal the amount requested, the load operation is aborted, and E\_FAIL is returned.</span></span> <span data-ttu-id="383db-111">Если версия формата в свойствах только что прочитанного документа \_ не распознана, операция загрузки прерывается, а **Load** возвращает E \_ Fail.</span><span class="sxs-lookup"><span data-stu-id="383db-111">If the format version in the newly read PAPER\_PROPERTIES is not recognized, then the load operation is aborted and **Load** returns E\_FAIL.</span></span>

<span data-ttu-id="383db-112">При наличии допустимой версии формата данных рукописного ввода размер нового массива данных рукописного ввода из \_ свойств бумаги, считанного в, используется для выделения нового массива рукописных данных требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="383db-112">With a valid ink data format version, the size of the new ink data array from the PAPER\_PROPERTIES that was read in is used to allocate a new ink data array of the required size.</span></span> <span data-ttu-id="383db-113">Существующие рукописные данные удаляются, и их данные теряются.</span><span class="sxs-lookup"><span data-stu-id="383db-113">The existing ink data is deleted, and its data is lost.</span></span> <span data-ttu-id="383db-114">Если эти данные были ценными, они должны быть сохранены до вызова **загрузки** .</span><span class="sxs-lookup"><span data-stu-id="383db-114">If this data was valuable, it should have been saved before **Load** was called.</span></span> <span data-ttu-id="383db-115">После выделения нового массива снова вызывается метод [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) для считывания данных в массив из потока.</span><span class="sxs-lookup"><span data-stu-id="383db-115">After the new array is allocated, [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) is called again to read the data into the array from the stream.</span></span> <span data-ttu-id="383db-116">Если этот вызов будет выполнен, значения в свойствах только для чтения документа будут приняты в качестве текущих значений для собумаги.</span><span class="sxs-lookup"><span data-stu-id="383db-116">If this call succeeds, the values in the newly read paper properties are adopted as the current values for COPaper.</span></span>

<span data-ttu-id="383db-117">Во время этой операции загрузки \_ для хранения новых свойств, считываемых в, используется временная структура свойств бумаги невпропс.</span><span class="sxs-lookup"><span data-stu-id="383db-117">During this load operation, a temporary PAPER\_PROPERTIES structure, NewProps, was used to hold the new properties read in.</span></span> <span data-ttu-id="383db-118">Если все прошло успешную загрузку, Невпропс копируется в \_ структуру свойств бумаги m \_ паперпропертиес.</span><span class="sxs-lookup"><span data-stu-id="383db-118">If all succeeds with the load, NewProps is copied into the PAPER\_PROPERTIES structure, m\_PaperProperties.</span></span> <span data-ttu-id="383db-119">Как и раньше, после завершения загрузки и удаления [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) указатель **IStream** освобождается.</span><span class="sxs-lookup"><span data-stu-id="383db-119">As before, after Load is done and the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) is no longer required, the **IStream** pointer is released.</span></span>

<span data-ttu-id="383db-120">Если в конце **загрузки** возникает ошибка, то массив рукописных данных удаляется, так как он может содержать поврежденные данные.</span><span class="sxs-lookup"><span data-stu-id="383db-120">If there is an error at the end of **Load**, the ink data array is erased, because it may contain damaged data.</span></span>

<span data-ttu-id="383db-121">Если в конце **загрузки** нет ошибок, вызывается метод Client [**Ипаперсинк:: Loaded**](ipapersink-methods.md) в методе Internal нотифисинкс, чтобы уведомить клиента о завершении операции загрузки.</span><span class="sxs-lookup"><span data-stu-id="383db-121">If there is no error at the end of **Load**, the client [**IPaperSink::Loaded**](ipapersink-methods.md) method is called, in the COPaper internal NotifySinks method, to notify the client that the load operation is completed.</span></span> <span data-ttu-id="383db-122">Это важное уведомление для клиента, так как оно должно отображать новые загруженные данные рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="383db-122">This is an important notification for the client, because it must display this new loaded ink data.</span></span> <span data-ttu-id="383db-123">Это уведомление существенно использует возможности подключаемых объектов в содокументе.</span><span class="sxs-lookup"><span data-stu-id="383db-123">This notification makes significant use of connectable object features in COPaper.</span></span>

 

 




