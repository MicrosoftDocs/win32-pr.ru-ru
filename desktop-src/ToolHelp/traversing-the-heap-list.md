---
title: Обход списка куч
description: Примеры, показывающие, как получить список куч для текущего процесса.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 868526c76ee85095f5b52cc9238e9e16015bfb3a81c9888da148f1d5ecc644aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419254"
---
# <a name="traversing-the-heap-list"></a>Обход списка куч

В следующем примере получается список куч для текущего процесса. Он создает моментальный снимок куч с помощью функции [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , а затем проходит по списку с помощью функций [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) и [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) . Для каждой кучи используются функции [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) для прохода по блокам кучи.

> [!NOTE]
> [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) являются неэффективными, особенно для больших куч. Однако они полезны для запроса других процессов, где, как правило, приходится внедрять поток в другой процесс для сбора информации (эти API делают это за вас).

См. Второй пример для эквивалентного, гораздо более эффективного, альтернативного использования [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) вместо [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next). Обратите внимание, что [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) можно использовать только для одного процесса.

```C++
#include <windows.h>
#include <tlhelp32.h>
#include <stdio.h>

int main( void )
{
   HEAPLIST32 hl;
   
   HANDLE hHeapSnap = CreateToolhelp32Snapshot(TH32CS_SNAPHEAPLIST, GetCurrentProcessId());
   
   hl.dwSize = sizeof(HEAPLIST32);
   
   if ( hHeapSnap == INVALID_HANDLE_VALUE )
   {
      printf ("CreateToolhelp32Snapshot failed (%d)\n", GetLastError());
      return 1;
   }
   
   if( Heap32ListFirst( hHeapSnap, &hl ) )
   {
      do
      {
         HEAPENTRY32 he;
         ZeroMemory(&he, sizeof(HEAPENTRY32));
         he.dwSize = sizeof(HEAPENTRY32);

         if( Heap32First( &he, GetCurrentProcessId(), hl.th32HeapID ) )
         {
            printf( "\nHeap ID: %d\n", hl.th32HeapID );
            do
            {
               printf( "Block size: %d\n", he.dwBlockSize );
               
               he.dwSize = sizeof(HEAPENTRY32);
            } while( Heap32Next(&he) );
         }
         hl.dwSize = sizeof(HEAPLIST32);
      } while (Heap32ListNext( hHeapSnap, &hl ));
   }
   else printf ("Cannot list first heap (%d)\n", GetLastError());
   
   CloseHandle(hHeapSnap); 

   return 0;
}
```

В следующем фрагменте кода используется функция [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) для прохода по кучам процесса, создавая идентичные выходные данные в предыдущем примере, но гораздо эффективнее:

```C++
#include <windows.h>
#include <stdio.h>

int main( void )
{
    DWORD heapIndex;
    DWORD heapCount = 0;
    PHANDLE heaps = NULL;
    while (TRUE)
    {
        DWORD actualHeapCount = GetProcessHeaps(heapCount, heaps);
        if (actualHeapCount <= heapCount)
        {
            break;
        }
        heapCount = actualHeapCount;
        free(heaps);
        heaps = (HANDLE*)malloc(heapCount * sizeof(HANDLE));
        if (heaps == NULL)
        {
            printf("Unable to allocate memory for list of heaps\n");
            return 1;
        }
    }

    for (heapIndex = 0; heapIndex < heapCount; heapIndex++)
    {
        PROCESS_HEAP_ENTRY entry;

        printf("Heap ID: %d\n", (DWORD)(ULONG_PTR)heaps[heapIndex]);
        entry.lpData = NULL;
        while (HeapWalk(heaps[heapIndex], &entry))
        {
            // Heap32First and Heap32Next ignore entries
            // with the PROCESS_HEAP_REGION flag
            if (!(entry.wFlags & PROCESS_HEAP_REGION))
            {
                printf("Block size: %d\n", entry.cbData + entry.cbOverhead);
            }
        }
    }

    free(heaps);
    return 0;
}
```

Анализ кучи с помощью функции [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) приблизительно линейный в размере кучи, в то время как в результате прохода кучи с функцией [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) примерно в квадрате в размере кучи.
Даже для небольших куч с 10 000 выделения памяти [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) выполняется 10 000 быстрее, чем [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , и предоставляет более подробную информацию. Разница в производительности становится еще более резкой по мере увеличения размера кучи.

Более подробный пример прохода кучи с помощью функции [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) см. в разделе [перечисление кучи](/windows/win32/memory/enumerating-a-heap).
