---
title: Обход списка кучи
description: Примеры, показывающие, как получить список куч для текущего процесса.
ms.assetid: cfa1d2a4-fec0-4089-9351-e0a26f9ecfe3
ms.topic: article
ms.date: 03/23/2021
ms.openlocfilehash: 5cc555f9a94166fa181309985d8a49c686baf06c
ms.sourcegitcommit: 4af3e9ec3142ba499d20ed8b174c2b219c5eacd2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/30/2021
ms.locfileid: "105994498"
---
# <a name="traversing-the-heap-list"></a><span data-ttu-id="47950-103">Обход списка кучи</span><span class="sxs-lookup"><span data-stu-id="47950-103">Traversing the Heap List</span></span>

<span data-ttu-id="47950-104">В следующем примере получается список куч для текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="47950-104">The following example obtains a list of heaps for the current process.</span></span> <span data-ttu-id="47950-105">Он создает моментальный снимок куч с помощью функции [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , а затем проходит по списку с помощью функций [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) и [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) .</span><span class="sxs-lookup"><span data-stu-id="47950-105">It takes a snapshot of the heaps using the [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) function, and then walks through the list using the [**Heap32ListFirst**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst) and [**Heap32ListNext**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext) functions.</span></span> <span data-ttu-id="47950-106">Для каждой кучи используются функции [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) для прохода по блокам кучи.</span><span class="sxs-lookup"><span data-stu-id="47950-106">For each heap, it uses the [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) functions to walk the heap blocks.</span></span>

> [!NOTE]
> <span data-ttu-id="47950-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) являются неэффективными, особенно для больших куч.</span><span class="sxs-lookup"><span data-stu-id="47950-107">[**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) are inefficient, particularly for large heaps.</span></span> <span data-ttu-id="47950-108">Однако они полезны для запроса других процессов, где, как правило, приходится внедрять поток в другой процесс для сбора информации (эти API делают это за вас).</span><span class="sxs-lookup"><span data-stu-id="47950-108">However, they are useful for querying other processes where you'd typically have to inject a thread into the other process to gather the information (these APIs do this for you).</span></span>

<span data-ttu-id="47950-109">См. Второй пример для эквивалентного, гораздо более эффективного, альтернативного использования [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) вместо [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) и [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span><span class="sxs-lookup"><span data-stu-id="47950-109">See the second example for an equivalent, much more efficient, alternative that uses [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) instead of [**Heap32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first) and [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next).</span></span> <span data-ttu-id="47950-110">Обратите внимание, что [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) можно использовать только для одного процесса.</span><span class="sxs-lookup"><span data-stu-id="47950-110">Note that [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) can only be used for the same process.</span></span>

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

<span data-ttu-id="47950-111">В следующем фрагменте кода используется функция [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) для прохода по кучам процесса, создавая идентичные выходные данные в предыдущем примере, но гораздо эффективнее:</span><span class="sxs-lookup"><span data-stu-id="47950-111">The following code snippet uses the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function to walk the process heaps, producing identical output to the previous example, but much more efficiently:</span></span>

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

<span data-ttu-id="47950-112">Анализ кучи с помощью функции [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) приблизительно линейный в размере кучи, в то время как в результате прохода кучи с функцией [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) примерно в квадрате в размере кучи.</span><span class="sxs-lookup"><span data-stu-id="47950-112">Walking a heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function is roughly linear in the size of the heap, whereas walking a heap with the [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) function is roughly quadratic in the size of the heap.</span></span>
<span data-ttu-id="47950-113">Даже для небольших куч с 10 000 выделения памяти [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) выполняется 10 000 быстрее, чем [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) , и предоставляет более подробную информацию.</span><span class="sxs-lookup"><span data-stu-id="47950-113">Even for a modest heap with 10,000 allocations, [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) runs 10,000 times faster than [**Heap32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next) while providing more detailed information.</span></span> <span data-ttu-id="47950-114">Разница в производительности становится еще более резкой по мере увеличения размера кучи.</span><span class="sxs-lookup"><span data-stu-id="47950-114">The difference in performance becomes even more dramatic as the heap size increases.</span></span>

<span data-ttu-id="47950-115">Более подробный пример прохода кучи с помощью функции [**хеапвалк**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) см. в разделе [перечисление кучи](/windows/win32/memory/enumerating-a-heap).</span><span class="sxs-lookup"><span data-stu-id="47950-115">For a more detailed example of walking the heap with the [**HeapWalk**](/windows/desktop/api/heapapi/nf-heapapi-heapwalk) function, see [Enumerating a Heap](/windows/win32/memory/enumerating-a-heap).</span></span>
