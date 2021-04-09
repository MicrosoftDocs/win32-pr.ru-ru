---
description: Внедрение оглавления в видеофайл
ms.assetid: 1546388a-7868-4411-be20-34d28becbe76
title: Внедрение оглавления в видеофайл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a8303082e454dde181de336ee0f64ff9d583312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143120"
---
# <a name="embedding-a-table-of-contents-in-a-video-file"></a>Внедрение оглавления в видеофайл

В этом разделе показано, как создать оглавление и внедрить его в видеофайл. Чтобы избежать краткого примера кода, оглавление очень просто. Он содержит только одну запись, а запись заполняется как минимум информацией.

Чтобы создать оглавление и внедрить его в файл, необходимо создать следующие четыре объекта, вызвав **CoCreateInstance**.

-   Запись ОГЛАВЛЕНИя
-   Список записей ОГЛАВЛЕНИя
-   ОГЛАВЛЕНИЕ
-   Средство синтаксического анализа ОГЛАВЛЕНИя

Идентификаторы классов для объектов задаются в [идентификаторах классов для средства синтаксического анализа содержимого](class-identifiers-for-toc-parser.md).

Сначала заполните запись ОГЛАВЛЕНИя информацией, описывающей одну часть видеофайла. Добавьте запись ОГЛАВЛЕНИя в список элементов ОГЛАВЛЕНИя, а затем добавьте список записей ОГЛАВЛЕНИя в ОГЛАВЛЕНИе. Наконец, добавьте ОГЛАВЛЕНИе в средство синтаксического анализа TOC, которое предоставляет функциональные возможности для внедрения ОГЛАВЛЕНИя в видеофайл. В следующем списке приведены более подробные инструкции.

1.  Создайте объект элемента ОГЛАВЛЕНИя и получите на нем интерфейс [**итоцентри**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) .
2.  Заполните [**структуру \_ \_ дескриптора записи оглавления**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) и передайте ее в [**итоцентри:: сетдескриптор**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-setdescriptor).
3.  Создайте объект списка записей ОГЛАВЛЕНИя и получите на нем интерфейс [**итоцентрилист**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) .
4.  Добавьте объект записи ОГЛАВЛЕНИя, созданный на шаге 1, в объект списка записей ОГЛАВЛЕНИя, вызвав [**итоцентрилист:: аддентрибиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-addentrybyindex).
5.  Создайте объект TOC и получите на нем интерфейс [**Иток**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) .
6.  Добавьте объект списка записей ОГЛАВЛЕНИя, созданный на шаге 3, в объект TOC, вызвав [**Иток:: аддентрилистбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-addentrylistbyindex).
7.  Создайте объект средства синтаксического анализа ОГЛАВЛЕНИя и получите на нем интерфейс [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .
8.  Вызовите метод [**итокпарсер:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , чтобы инициализировать объект средства синтаксического анализа оглавления и связать его с видеофайлом.
9.  Добавьте объект TOC, созданный на шаге 5, в объект средства синтаксического анализа ОГЛАВЛЕНИя, вызвав [**итокпарсер:: аддток**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-addtoc).
10. Внедрите оглавление в видеофайл, вызвав [**итокпарсер:: Commit**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-commit).

В следующем коде показаны шаги, приведенные в предыдущем списке.


```C++
#include <wmcodecdsp.h>
HRESULT InitTocParserAndCommit(IToc* pToc);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocEntry* pEntry = NULL;
      hr = CoCreateInstance(CLSID_CTocEntry, NULL, 
         CLSCTX_INPROC_SERVER, IID_ITocEntry, (VOID**)&pEntry); 

      if(SUCCEEDED(hr))
      {
         TOC_ENTRY_DESCRIPTOR tocDesc = {0};
         tocDesc.qwStartTime = 4; 
         tocDesc.qwEndTime = 8;
         pEntry->SetDescriptor(&tocDesc); // HRESULT ignored for simplicity.    
    
         ITocEntryList* pEntryList = NULL;
         hr = CoCreateInstance(CLSID_CTocEntryList, NULL, 
            CLSCTX_INPROC_SERVER, IID_ITocEntryList, (VOID**)&pEntryList);

         if(SUCCEEDED(hr))
         {
            pEntryList->AddEntryByIndex(0, pEntry); // HRESULT ignored.
      
            IToc* pToc = NULL;
            hr = CoCreateInstance(CLSID_CToc, NULL, 
               CLSCTX_INPROC_SERVER, IID_IToc, (VOID**)&pToc);

            if(SUCCEEDED(hr))
            {
               pToc->AddEntryListByIndex(0, pEntryList); // HRESULT ignored.
               hr = InitTocParserAndCommit(pToc);
            }
         }
      }
     
      CoUninitialize();
   }
}

HRESULT InitTocParserAndCommit(IToc* pToc)
{
   ITocParser* pTocParser = NULL;
   HRESULT hr = CoCreateInstance(CLSID_CTocParser, NULL, 
      CLSCTX_INPROC_SERVER, IID_ITocParser, (VOID**)&pTocParser);

   if(SUCCEEDED(hr))
   {
      hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

      if(SUCCEEDED(hr))
      {
         DWORD tocIndex = 0;
         hr = pTocParser->AddToc(TOC_POS_TOPLEVELOBJECT, pToc, &tocIndex);

         if(SUCCEEDED(hr))
         {
            hr = pTocParser->Commit();
         }
      }

      pTocParser->Release();
      pTocParser = NULL;
   }

   return hr;
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Чтение оглавления из файла видео](reading-a-table-of-contents-from-a-video-file.md)
</dt> <dt>

[Таблица объектов средства синтаксического анализа содержимого](toc-parser-objects.md)
</dt> <dt>

[Справочное руководством по программированию синтаксического анализатора содержимого](toc-parser-programming-guide.md)
</dt> </dl>

 

 



