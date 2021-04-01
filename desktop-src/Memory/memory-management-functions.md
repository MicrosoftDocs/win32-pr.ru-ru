---
description: В этом разделе описываются функции управления памятью.
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Функции управления памятью
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: 43aef65e6563a56f35c019c5202827ab65772186
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/23/2020
ms.locfileid: "103797232"
---
# <a name="memory-management-functions"></a>Функции управления памятью

- [Общие функции памяти](#general-memory-functions)
- [Функции предотвращения выполнения данных](#data-execution-prevention-functions)
- [Функции сопоставления файлов](#file-mapping-functions)
- [Функции AWE](#awe-functions)
- [Функции кучи](#heap-functions)
- [Функции виртуальной памяти](#virtual-memory-functions)
- [Глобальные и локальные функции](#global-and-local-functions)
- [Неправильные функции памяти](#bad-memory-functions)
- [Функции анклава](#enclave-functions)
- [Функции преобразователей ATL](#atl-thunk-functions)
- [Устаревшие функции](#obsolete-functions)

## <a name="general-memory-functions"></a>Общие функции памяти

| Функция | Описание |
|-|-|
| [**аддсекуремеморикачекаллбакк**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Регистрирует функцию обратного вызова, вызываемую при освобождении диапазона защищенной памяти или изменении его защиты. |
| [**копимемори**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Копирует блок памяти из одного расположения в другое. |
| [**креатемемориресаурценотификатион**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Создает объект уведомления ресурса памяти. |
| [**филлмемори**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Заполняет блок памяти указанным значением. |
| [**жетларжепажеминимум**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Возвращает минимальный размер большой страницы. |
| [**жетфисикаллинсталледсистеммемори**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Возвращает объем ОЗУ, физически установленный на компьютере. |
| [**жетсистемфилекачесизе**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Извлекает ограничения текущего размера для рабочего набора системного кэша. |
| [**жетвритеватч**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Извлекает адреса страниц, которые были записаны в область виртуальной памяти. |
| [**глобалмемористатусекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Получает сведения о текущем использовании системы как физической, так и виртуальной памяти. |
| [**мовемемори**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Перемещает блок памяти из одного расположения в другое. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Возвращает состояние указанного объекта ресурса памяти. |
| [**ремовесекуремеморикачекаллбакк**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Отменяет регистрацию функции обратного вызова, которая была ранее зарегистрирована в функции [**аддсекуремеморикачекаллбакк**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) . |
| [**ресетвритеватч**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Сбрасывает состояние отслеживания записи для региона виртуальной памяти. |
| [**секуремеморикачекаллбакк**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Определяемая приложением функция, которая вызывается при освобождении диапазона защищенной памяти или изменении его защиты. |
| [**секурезеромемори**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Заполняет блок памяти нулями. |
| [**сетсистемфилекачесизе**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Ограничивает размер рабочего набора для кэша файловой системы. |
| [**зеромемори**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Заполняет блок памяти нулями. |

## <a name="data-execution-prevention-functions"></a>Функции предотвращения выполнения данных

Эти функции используются с [предотвращением выполнения данных](data-execution-prevention.md) (DEP).

| Функция | Описание |
|-|-|
| [**жетпроцессдепполици**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Возвращает параметры DEP для процесса. |
| [**жетсистемдепполици**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Получает параметры DEP для системы. |
| [**сетпроцессдепполици**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Изменяет параметры DEP для процесса. |

## <a name="file-mapping-functions"></a>Функции сопоставления файлов

Эти функции используются в [сопоставлении файлов](file-mapping.md).

| Функция | Описание |
|-|-|
| [**креатефилемаппинга**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла. |
| [**креатефилемаппингв**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла. Можно указать предпочитаемый узел NUMA для физической памяти в качестве расширенного параметра; см. параметр *екстендедпараметерс* . |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла из приложения Магазина Windows. |
| [**креатефилемаппингнума**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Создает или открывает именованный или безымянный объект сопоставления файлов для указанного файла и указывает узел NUMA для физической памяти. |
| [**флушвиевоффиле**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Записывает на диск диапазон байтов в сопоставленном представлении файла. |
| [**жетмаппедфиленаме**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Проверяет, находится ли указанный адрес в размещенном в памяти файле в адресном пространстве указанного процесса. Если это так, функция возвращает имя отображенного в память файла. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Сопоставляет представление файла или раздела с файлом подкачки в адресном пространстве указанного процесса. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Сопоставляет представление файла или раздела с файлом подкачки в адресном пространстве указанного процесса. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса из приложения Магазина Windows. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса. Вызывающий объект может дополнительно указать рекомендуемый адрес памяти для представления. |
| [**мапвиевоффиликснума**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса и указывает узел NUMA для физической памяти. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Сопоставляет представление сопоставления файлов с адресным пространством вызывающего процесса из приложения Магазина Windows. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Сопоставляет представление файла или раздела с файлом подкачки в адресном пространстве указанного процесса. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Открывает именованный объект сопоставления файлов. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Открывает именованный объект сопоставления файлов. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Отменяет сопоставление сопоставленного представления файла с адресным пространством вызывающего процесса. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Отменяет сопоставление ранее отображенного представления файла или раздела, сохраненного в файле подкачки. |
| [**унмапвиевоффиликс**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Отменяет сопоставление ранее отображенного представления файла или раздела, сохраненного в файле подкачки. |

## <a name="awe-functions"></a>Функции AWE

Это [функции AWE](address-windowing-extensions.md).

| Функция | Описание |
|-|-|
| [**аллокатеусерфисикалпажес**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Выделяет страницы физической памяти, которые должны быть сопоставлены и отменяться в любой области расширений AWE процесса. |
| [**аллокатеусерфисикалпажеснума**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Выделяет страницы физической памяти, которые должны быть сопоставлены и не сопоставлены в любом регионе AWE процесса, и указывает узел NUMA для физической памяти. |
| [**фриусерфисикалпажес**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Освобождает страницы физической памяти, выделенные ранее с помощью [**аллокатеусерфисикалпажес**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages). |
| [**мапусерфисикалпажес**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Сопоставляет ранее выделенные страницы физической памяти по указанному адресу в области AWE. |
| [**мапусерфисикалпажесскаттер**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Сопоставляет ранее выделенные страницы физической памяти по указанному адресу в области AWE. |

## <a name="heap-functions"></a>Функции кучи

Это [функции кучи](heap-functions.md).

| Функция | Описание |
|-|-|
| [**жетпроцесшеап**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Получает маркер для кучи вызывающего процесса. |
| [**жетпроцесшеапс**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Получает дескрипторы всех куч, допустимых для вызывающего процесса. |
| [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Выделяет блок памяти из кучи. |
| [**хеапкомпакт**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Объединяет смежные свободные блоки памяти в куче. |
| [**хеапкреате**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Создает объект heap. |
| [**хеапдестрой**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Уничтожает указанный объект кучи. |
| [**хеапфри**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Освобождает блок памяти, выделенный из кучи. |
| [**хеаплокк**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Пытается получить блокировку, связанную с указанной кучей. |
| [**хеапкуеринформатион**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Извлекает сведения о указанной куче. |
| [**хеапреаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Перераспределяет блок памяти из кучи. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Задает сведения о куче для указанной кучи. |
| [**хеапсизе**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Возвращает размер блока памяти, выделенного из кучи. |
| [**хеапунлокк**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Освобождает владение блокировкой, связанной с указанной кучей. |
| [**хеапвалидате**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Пытается проверить указанную кучу. |
| [**хеапвалк**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Перечисляет блоки памяти в указанной куче. |

## <a name="virtual-memory-functions"></a>Функции виртуальной памяти

Это [функции виртуальной памяти](virtual-memory-functions.md).

| Функция | Описание |
|-|-|
| [**дискардвиртуалмемори**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Отменяет содержимое памяти диапазона страниц памяти, не выполняя выделение памяти. Содержимое отброшенной памяти не определено и должно быть перезаписано приложением. |
| [**оффервиртуалмемори**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Указывает, что данные, содержащиеся в диапазоне страниц памяти, больше не требуются приложению и могут быть отклонены системой при необходимости. |
| [**префетчвиртуалмемори**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Выберет диапазоны виртуальных адресов в физическую память. |
| [**куеривиртуалмеморинформатион**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Возвращает сведения о странице или наборе страниц в пределах виртуального адресного пространства указанного процесса. |
| [**реклаимвиртуалмемори**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Освобождает ряд страниц памяти, которые были предложены системе с помощью [**оффервиртуалмемори**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory). |
| [**сетпроцессвалидкаллтаржетс**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Предоставляет CFG со списком допустимых целей косвенного вызова и указывает, должны ли они быть помечены как допустимые или нет. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Резервирует или фиксирует область страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Резервирует, фиксирует или изменяет состояние области памяти в пределах виртуального адресного пространства указанного процесса. Функция инициализирует выделенную память до нуля. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Резервирует, фиксирует или изменяет состояние области страниц в виртуальном адресном пространстве вызывающего процесса. Память, выделенная этой функцией, автоматически инициализируется значением 0. |
| [**виртуалаллоцекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Резервирует или фиксирует область страниц в виртуальном адресном пространстве указанного процесса. |
| [**виртуалаллоцекснума**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Резервирует или фиксирует область памяти в пределах виртуального адресного пространства указанного процесса и указывает узел NUMA для физической памяти. |
| [**виртуалаллокфромапп**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Резервирует, фиксирует или изменяет состояние области страниц в виртуальном адресном пространстве вызывающего процесса. Память, выделенная этой функцией, автоматически инициализируется значением 0. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Выпускают или отменяет выделение области страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**виртуалфриекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Освобождает или снимает область памяти в пределах виртуального адресного пространства указанного процесса. |
| [**виртуаллокк**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Блокирует заданную область виртуального адресного пространства процесса в физической памяти. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Изменяет защиту доступа для области зафиксированных страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**виртуалпротектекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Изменяет защиту доступа для области зафиксированных страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Изменяет защиту в области зафиксированных страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Предоставляет сведения о диапазоне страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**виртуалкуерекс**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Предоставляет сведения о диапазоне страниц в виртуальном адресном пространстве вызывающего процесса. |
| [**виртуалунлокк**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Разблокирует указанный диапазон страниц в виртуальном адресном пространстве процесса. |

## <a name="global-and-local-functions"></a>Глобальные и локальные функции

См. также [глобальные и локальные функции](global-and-local-functions.md). Эти функции предоставляются для обеспечения совместимости с 16-разрядной ОС Windows и используются с платформа динамических данных Exchange (DDE), функциями буфера обмена и объектами данных OLE. Если в документации специально не указано, что следует использовать глобальную или локальную функцию, новые приложения должны использовать соответствующую [функцию кучи](heap-functions.md) с маркером, возвращаемым функцией [**жетпроцесшеап**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Для эквивалентной функциональности глобальной или локальной функции установите для параметра *dwFlags* функции кучи значение 0.

| Функция | Описание | Соответствующая функция кучи |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **локалаллок**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Выделяет указанное число байтов из кучи. | [**хеапаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**Глобалдискард**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard), [ **локалдискард**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Отменяет указанный глобальный блок памяти. | Не применяется |
| [**Глобалфлагс**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **локалфлагс**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Возвращает сведения об указанном объекте глобальной памяти. | Не применяется Используйте [**хеапвалидате**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) для проверки кучи. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **функции LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Освобождает указанный объект глобальной памяти. | [**хеапфри**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**Глобалхандле**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **локалхандле**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Извлекает маркер, связанный с указанным указателем, в глобальный блок памяти. Эта функция должна использоваться только с функциями OLE и буфера обмена, которым он необходим. | Не применяется |
| [**Глобаллокк**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **локаллокк**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Блокирует объект глобальной памяти и возвращает указатель на первый байт блока памяти объекта. | Не применяется |
| [**LocalLock**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **локалреаллок**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Изменяет размер или атрибуты указанного объекта глобальной памяти. | [**хеапреаллок**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**Глобалсизе**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **локалсизе**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Извлекает текущий размер указанного объекта глобальной памяти. | [**хеапсизе**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**Глобалунлокк**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **локалунлокк**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Уменьшает счетчик блокировок, связанный с объектом памяти. Эта функция должна использоваться только с функциями OLE и буфера обмена, которым он необходим. | Не применяется |

## <a name="bad-memory-functions"></a>Неправильные функции памяти

| Функция | Описание |
|-|-|
| [**бадмеморикаллбаккраутине**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Определяемая приложением функция, зарегистрированная с помощью функции [**регистербадмеморинотификатион**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) , которая вызывается при обнаружении одной или нескольких страниц с поврежденной памятью. |
| [**жетмемореррорхандлингкапабилитиес**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Возвращает возможности системы по обработке ошибок памяти. |
| [**регистербадмеморинотификатион**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Регистрирует уведомление о неправильной памяти, которое вызывается при обнаружении одной или нескольких страниц с поврежденной памятью. |
| [**унрегистербадмеморинотификатион**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Закрывает указанный маркер уведомления о неправильной памяти. |

## <a name="enclave-functions"></a>Функции анклава

| Функция | Описание |
|-|-|
| [**креатинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Создает новый неинициализированный анклава. Анклава — это изолированная область кода и данных в адресном пространстве для приложения. Только код, который выполняется в анклава, может обращаться к данным в одном анклава. |
| [**инитиализинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Инициализирует анклава, созданный и загруженный с данными. |
| [**исенклаветипесуппортед**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Возвращает значение, определяющее, поддерживается ли указанный тип анклава. |
| [**лоаденклаведата**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Загружает данные в неинициализированную анклава, созданную путем вызова [**креатинклаве**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave). |

## <a name="atl-thunk-functions"></a>Функции преобразователей ATL

| Функция | Описание |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Выделяет место в памяти для преобразователя ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Возвращает исполняемую функцию, соответствующую параметру AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Освобождает память, связанную с преобразователем ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Инициализирует преобразователь ATL. |

## <a name="obsolete-functions"></a>Устаревшие функции

Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows:

- [**исбадкодептр**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**исбадреадптр**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**исбадстрингптр**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**исбадвритептр**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

Функция ниже может возвращать неверные сведения и не должна использоваться. Вместо этого используйте функцию [**глобалмемористатусекс**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) .

- [**глобалмемористатус**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)