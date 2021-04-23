---
title: Ипапер сохранить
description: Основное внимание в этом примере кода заключается в том, как собумага может загружать и сохранять свои бумажные данные в составных файлах. Реализации методов Ипапер, Load и Save подробно обсуждаются.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661619"
---
# <a name="ipapersave"></a><span data-ttu-id="7b9ff-104">Ипапер:: Save</span><span class="sxs-lookup"><span data-stu-id="7b9ff-104">IPaper::Save</span></span>

<span data-ttu-id="7b9ff-105">Основное внимание в этом примере кода заключается в том, как собумага может загружать и сохранять свои бумажные данные в составных файлах.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="7b9ff-106">Реализации методов [**ипапер**](ipaper-methods.md), [**Load**](ipaper--load.md)и **Save** подробно обсуждаются.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="7b9ff-107">Ниже приведен метод **ипапер:: Save из файла** paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



<span data-ttu-id="7b9ff-108">В этой связи между клиентом и сервером собумага не создает составной файл, используемый для хранения бумажных данных.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="7b9ff-109">Для методов **Save** и [**Load**](ipaper--load.md) клиент передает указатель интерфейса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для существующего составного файла.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="7b9ff-110">Затем он использует **IStorage** для записи и чтения данных в этом составном файле.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="7b9ff-111">В **ипапер:: Save** выше хранятся несколько типов данных.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="7b9ff-112">CLSID для Дллпапер, CLSID \_ дллпапер сериализуется и хранится в специальном потоке, управляемом com, в объекте хранилища с именем " \\ 001CompObj".</span><span class="sxs-lookup"><span data-stu-id="7b9ff-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="7b9ff-113">Функция [**вритеклассстг**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) Service выполняет это хранилище.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="7b9ff-114">Эти сохраненные данные CLSID можно использовать для связывания содержимого хранилища с компонентом Дллпапер, который создал и может интерпретировать его.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="7b9ff-115">В этом примере корневое хранилище передается **стоклиен**, и, таким же, весь составной файл связывается с компонентом дллпапер.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="7b9ff-116">Эти данные CLSID можно получить позже с помощью вызова функции службы [**реадклассстг**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .</span><span class="sxs-lookup"><span data-stu-id="7b9ff-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="7b9ff-117">Поскольку Дллпапер работает с редактируемыми данными, также можно записать в хранилище формат буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="7b9ff-118">Функция службы [**вритефмтусертипестг**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) вызывается для сохранения формата буфера обмена и понятного для пользователя имени в формате.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="7b9ff-119">Имя, доступное для чтения, предназначено для показа графического пользовательского интерфейса в списках выбора.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="7b9ff-120">Переданное выше имя использует макрос КЛИПБДФМТ \_ str, который определен как "дллпапер 1,0" в paper. h.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="7b9ff-121">Эти сохраненные данные в буфере обмена можно получить позже, вызвав функцию службы [**реадфмтусертипестг**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span><span class="sxs-lookup"><span data-stu-id="7b9ff-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="7b9ff-122">Эта функция возвращает строковое значение, выделенное с помощью распределителя памяти задачи.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="7b9ff-123">Вызывающий объект отвечает за освобождение строки.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="7b9ff-124">**Сохранить** далее — создает поток в хранилище для бумажных данных.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="7b9ff-125">Поток называется "ПАПЕРДАТА" и передается с помощью \_ \_ макроса Stream папердата устр.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="7b9ff-126">Метод [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) требует, чтобы эта строка была в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="7b9ff-127">Так как строка фиксируется во время компиляции, макрос определяется как Unicode в формате paper. h.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="7b9ff-128">Оператор L перед строкой, указывающий на LONG, достигает этого.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="7b9ff-129">Метод [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) создает и открывает поток в указанном хранилище.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="7b9ff-130">Указатель интерфейса [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для нового потока передается в переменную указателя вызывающего интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="7b9ff-131">Метод AddRef вызывается для этого указателя интерфейса в **креатестреам**, и вызывающий объект должен освободить этот указатель после его использования.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="7b9ff-132">Методу **креатестреам** передается множество флагов режима доступа, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="7b9ff-133">СТГМ \_ Создание \| стгм \_ запись \| стгм \_ Direct \| стгм \_ \_ монопольный доступ</span><span class="sxs-lookup"><span data-stu-id="7b9ff-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="7b9ff-134">[**Стгм \_ CREATE**](stgm-constants.md) создает новый поток или перезаписывает существующий с тем же именем.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="7b9ff-135">[**Стгм \_ WRITE**](stgm-constants.md) открывает поток с разрешением на запись.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="7b9ff-136">[**Стгм \_ DIRECT**](stgm-constants.md) открывает поток для прямого доступа в отличие от транзакционного доступа.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="7b9ff-137">[**Стгм \_ \_Монопольный доступ**](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="7b9ff-138">После успешного создания потока ПАПЕРДАТА интерфейс [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) используется для записи в поток.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="7b9ff-139">Метод **IStream:: Write** используется для первого хранения содержимого \_ структуры свойств бумаги.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="7b9ff-140">По сути, это заголовок свойств в начале потока.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="7b9ff-141">Поскольку номер версии является первым в файле, его можно прочитать независимо, чтобы определить, как работать с данными, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="7b9ff-142">Если фактически записанный объем данных не равен запрошенному объему, метод Save прерывается и возвращается значение STG \_ E \_ кантсаве.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="7b9ff-143">Сохранение всего массива рукописных данных в потоке выполняется просто.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="7b9ff-144">Поскольку метод [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) работает с массивом байтов, число байтов сохраненных рукописных данных в массиве вычисляется, а операция записи начинается с начала массива.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="7b9ff-145">Если фактически записанный объем данных не равен запрошенному объему, метод **Save** возвращает STG \_ E \_ кантсаве.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="7b9ff-146">После того как поток записан, метод **ипапер:: Save** освобождает указатель [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , который он использовал.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="7b9ff-147">Метод **Save** также вызывает [**ипаперсинк**](ipapersink-methods.md) клиента (во внутреннем методе нотифисинкс), чтобы уведомить клиента о завершении операции сохранения.</span><span class="sxs-lookup"><span data-stu-id="7b9ff-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="7b9ff-148">На этом этапе метод **Save** возвращается вызывающему клиенту, который обычно освобождает указатель [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="7b9ff-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




