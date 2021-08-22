---
description: Чтение оглавления из файла видео
ms.assetid: 10c4f4ca-cb30-453c-b18d-0470bfecc14e
title: Чтение оглавления из файла видео
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bee379b0c50263463b0aa56e7ebb86bba447e70ef94ff82a6ba89e025d450bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034942"
---
# <a name="reading-a-table-of-contents-from-a-video-file"></a>Чтение оглавления из файла видео

В этом разделе показано, как прочитать оглавление, которое уже было внедрено в видеофайл.

Начните с вызова [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать объект средства синтаксического анализа оглавления и получить интерфейс [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) . Затем получите следующие интерфейсы, вызвав методы.

-   [**иток**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc)
-   [**итоцентрилист**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist)
-   [**итоцентри**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry)

Используйте методы [**итоцентри**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) для проверки отдельной записи в содержании. Например, можно проверить заголовок, время начала и время окончания записи.

В следующем списке приведены более подробные инструкции.

1.  Вызовите [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) , чтобы создать объект средства синтаксического анализа оглавления и получить на нем интерфейс [**итокпарсер**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocparser) .
2.  Вызовите [**итокпарсер:: init**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-init) , чтобы инициализировать средство синтаксического анализа оглавления и связать его с видеофайлом.
3.  Получите интерфейс [**Иток**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itoc) путем вызова [**Итокпарсер:: жеттокбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocparser-gettocbyindex).
4.  Получите интерфейс [**итоцентрилист**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentrylist) путем вызова [**Иток:: жетентрилистбиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itoc-getentrylistbyindex).
5.  Получите интерфейс [**итоцентри**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-itocentry) путем вызова [**Итоцентрилист:: жетентрибиндекс**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentrylist-getentrybyindex).
6.  Выделить структуру [**\_ \_ дескриптора записи оглавления**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) .
7.  Заполните [**структуру \_ \_ дескриптора записи оглавления**](/windows/desktop/api/wmcodecdsp/ns-wmcodecdsp-toc_entry_descriptor) , вызвав [**итоцентри:: двухбайтовый**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-itocentry-getdescriptor).

В следующем коде показаны шаги, описанные в предыдущем списке.


```C++
#include <stdio.h>
#include <wmcodecdsp.h>

HRESULT ShowEntryInfo(ITocEntry* pEntry);

void main()
{
   HRESULT hr = CoInitialize(NULL);
   
   if(SUCCEEDED(hr))
   {    
      ITocParser* pTocParser = NULL;

      hr = CoCreateInstance(CLSID_CTocParser, NULL, CLSCTX_INPROC_SERVER, 
         IID_ITocParser, (VOID**)&pTocParser);  
      
      if(SUCCEEDED(hr))
      {  
         hr = pTocParser->Init(L"\\\\?\\c:\\experiment\\seattle.wmv");

         if(SUCCEEDED(hr))
         {
            IToc* pToc = NULL;
            hr = pTocParser->GetTocByIndex(TOC_POS_TOPLEVELOBJECT, 0, &pToc);

            if(SUCCEEDED(hr))
            {
               ITocEntryList* pEntryList = NULL;
               hr = pToc->GetEntryListByIndex(0, &pEntryList);

               if(SUCCEEDED(hr))
               {
                  ITocEntry* pEntry = NULL;
                  hr = pEntryList->GetEntryByIndex(0, &pEntry);

                  if(SUCCEEDED(hr))
                  {
                     hr = ShowEntryInfo(pEntry);
                     pEntry->Release();
                     pEntry = NULL;
                  }

                  pEntryList->Release();
                  pEntryList = NULL;
               }

               pToc->Release();
               pToc = NULL;
            }
         }

         pTocParser->Release();
         pTocParser = NULL;  
      }
                   
      CoUninitialize();
   }
}

HRESULT ShowEntryInfo(ITocEntry* pEntry)
{
   HRESULT hr = E_FAIL;

   TOC_ENTRY_DESCRIPTOR entryDesc = {0};
   hr = pEntry->GetDescriptor(&entryDesc);

   if(SUCCEEDED(hr))
   {
      printf_s("qwStartTime: %x\n", entryDesc.qwStartTime);
      printf_s("qwEndTime: %x\n", entryDesc.qwEndTime);
      printf_s("qwStartStartPacketOffset: %x\n", entryDesc.qwStartPacketOffset);
      printf_s("qwEndPacketOffset: %x\n", entryDesc.qwEndPacketOffset);
      printf_s("qwRepresentativeFrameTime: %x\n", entryDesc.qwRepresentativeFrameTime);
   }

   return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Внедрение оглавления в видеофайл](embedding-a-table-of-contents-in-a-video-file.md)
</dt> <dt>

[Таблица объектов средства синтаксического анализа содержимого](toc-parser-objects.md)
</dt> <dt>

[Справочное руководством по программированию синтаксического анализатора содержимого](toc-parser-programming-guide.md)
</dt> </dl>

 

 
