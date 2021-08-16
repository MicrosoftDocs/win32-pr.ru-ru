---
title: Ипапер сохранить
description: Основное внимание в этом примере кода заключается в том, как собумага может загружать и сохранять свои бумажные данные в составных файлах. Реализации методов Ипапер, Load и Save подробно обсуждаются.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52772002fe8f0ed234a4f430eaff4328f96f9d1ef151e83da3f4aa3e255dba09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961374"
---
# <a name="ipapersave"></a>Ипапер:: Save

Основное внимание в этом примере кода заключается в том, как собумага может загружать и сохранять свои бумажные данные в составных файлах. Реализации методов [**ипапер**](ipaper-methods.md), [**Load**](ipaper--load.md)и **Save** подробно обсуждаются.

Ниже приведен метод **ипапер:: Save из файла** paper. cpp.


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



В этой связи между клиентом и сервером собумага не создает составной файл, используемый для хранения бумажных данных. Для методов **Save** и [**Load**](ipaper--load.md) клиент передает указатель интерфейса [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) для существующего составного файла. Затем он использует **IStorage** для записи и чтения данных в этом составном файле. В **ипапер:: Save** выше хранятся несколько типов данных.

CLSID для Дллпапер, CLSID \_ дллпапер сериализуется и хранится в специальном потоке, управляемом com, в объекте хранилища с именем " \\ 001CompObj". Функция [**вритеклассстг**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) Service выполняет это хранилище. Эти сохраненные данные CLSID можно использовать для связывания содержимого хранилища с компонентом Дллпапер, который создал и может интерпретировать его. В этом примере корневое хранилище передается **стоклиен**, и, таким же, весь составной файл связывается с компонентом дллпапер. Эти данные CLSID можно получить позже с помощью вызова функции службы [**реадклассстг**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .

Поскольку Дллпапер работает с редактируемыми данными, также можно записать в хранилище формат буфера обмена. Функция службы [**вритефмтусертипестг**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) вызывается для сохранения формата буфера обмена и понятного для пользователя имени в формате. Имя, доступное для чтения, предназначено для показа графического пользовательского интерфейса в списках выбора. Переданное выше имя использует макрос КЛИПБДФМТ \_ str, который определен как "дллпапер 1,0" в paper. h. Эти сохраненные данные в буфере обмена можно получить позже, вызвав функцию службы [**реадфмтусертипестг**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Эта функция возвращает строковое значение, выделенное с помощью распределителя памяти задачи. Вызывающий объект отвечает за освобождение строки.

**Сохранить** далее — создает поток в хранилище для бумажных данных. Поток называется "ПАПЕРДАТА" и передается с помощью \_ \_ макроса Stream папердата устр. Метод [**IStorage:: креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) требует, чтобы эта строка была в Юникоде. Так как строка фиксируется во время компиляции, макрос определяется как Unicode в формате paper. h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

Оператор L перед строкой, указывающий на LONG, достигает этого.

Метод [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) создает и открывает поток в указанном хранилище. Указатель интерфейса [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для нового потока передается в переменную указателя вызывающего интерфейса. Метод AddRef вызывается для этого указателя интерфейса в **креатестреам**, и вызывающий объект должен освободить этот указатель после его использования. Методу **креатестреам** передается множество флагов режима доступа, как показано ниже.

СТГМ \_ Создание \| стгм \_ запись \| стгм \_ Direct \| стгм \_ \_ монопольный доступ

[**Стгм \_ CREATE**](stgm-constants.md) создает новый поток или перезаписывает существующий с тем же именем. [**Стгм \_ WRITE**](stgm-constants.md) открывает поток с разрешением на запись. [**Стгм \_ DIRECT**](stgm-constants.md) открывает поток для прямого доступа в отличие от транзакционного доступа. [**Стгм \_ \_Монопольный доступ**](stgm-constants.md) открывает файл для монопольного использования, не являющегося общим для вызывающего.

После успешного создания потока ПАПЕРДАТА интерфейс [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) используется для записи в поток. Метод **IStream:: Write** используется для первого хранения содержимого \_ структуры свойств бумаги. По сути, это заголовок свойств в начале потока. Поскольку номер версии является первым в файле, его можно прочитать независимо, чтобы определить, как работать с данными, приведенными ниже. Если фактически записанный объем данных не равен запрошенному объему, метод Save прерывается и возвращается значение STG \_ E \_ кантсаве.

Сохранение всего массива рукописных данных в потоке выполняется просто.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Поскольку метод [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) работает с массивом байтов, число байтов сохраненных рукописных данных в массиве вычисляется, а операция записи начинается с начала массива. Если фактически записанный объем данных не равен запрошенному объему, метод **Save** возвращает STG \_ E \_ кантсаве.

После того как поток записан, метод **ипапер:: Save** освобождает указатель [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , который он использовал.

Метод **Save** также вызывает [**ипаперсинк**](ipapersink-methods.md) клиента (во внутреннем методе нотифисинкс), чтобы уведомить клиента о завершении операции сохранения. На этом этапе метод **Save** возвращается вызывающему клиенту, который обычно освобождает указатель [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

 

 




