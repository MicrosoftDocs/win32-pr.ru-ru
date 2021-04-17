---
title: IStream — реализация составного файла
description: Интерфейс IStream поддерживает чтение и запись данных в объекты Stream. В структурированном объекте хранилища объекты-потоки содержат данные и хранилища, которые предоставляют структуру.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Стрктд STG, реализация составного файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/04/2021
ms.locfileid: "105664785"
---
# <a name="istream---compound-file-implementation"></a>IStream — реализация составного файла

Интерфейс [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) поддерживает чтение и запись данных в объекты Stream. В структурированном объекте хранилища объекты-потоки содержат данные и хранилища, которые предоставляют структуру. Простые данные можно записывать непосредственно в поток, но чаще потоки — это элементы, вложенные в объект хранилища. Они похожи на стандартные файлы.

Спецификация [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) определяет больше функций, чем поддерживается реализацией com. Например, интерфейс **IStream** определяет потоки длиной до 2 ⁶ ⁴ байт, что требует 64-разрядный указатель поиска. Однако реализация COM поддерживает только потоки длиной до 2 ³ ² байт (4 ГБ), а операции чтения и записи всегда ограничены 2 ³ ² байтами. Реализация COM также не поддерживает транзакционную блокировку в потоках или в области.

Чтобы создать простой поток на основе глобальной памяти, получите указатель [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , вызвав функцию API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Чтобы получить указатель **IStream** внутри объекта составного файла, вызовите либо [**Стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , либо [**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Эти функции извлекают указатель [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , с помощью которого можно вызвать [**креатестреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) или [**опенстреам**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) для указателя **IStream** . В любом случае используется один и тот же код реализации **IStream** .

> [!Note]  
> Реализация составного файла в структурированном хранилище не выполняется в методе [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) для [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), но включает методы [**чтения**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) и [**записи**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) через указатель интерфейса [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .

 

## <a name="when-to-use"></a>Назначение

Вызывайте методы [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) для чтения и записи данных в поток.

Поскольку объекты потока могут быть упакованы в другие процессы, приложения могут совместно использовать данные в объектах хранилища, не используя глобальную память. В реализации составного файла COM для объектов потоков пользовательская функция упаковки в COM создает удаленную версию исходного объекта в новом процессе, когда два процесса имеют доступ к общей памяти. Таким же удаленная версия не должна взаимодействовать с исходным процессом для выполнения своих функций.

Удаленная версия объекта Stream использует тот же указатель поиска, что и исходный поток. Если вы не хотите совместно использовать указатель поиска, используйте метод [**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) , чтобы предоставить копию объекта потока для удаленного процесса.

> [!Note]
> Если создается объект потока, превышающий кучу в памяти компьютера, и вы используете обработчик **хглобал** для объекта глобальной памяти, объект Stream вызывает метод [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) внутренне вхе он требует больше памяти. Поскольку **LocalLock** всегда копирует данные из источника в место назначения, увеличение объекта потока с 20 МБ до 25 МБ, например, требует большого количества времени. Это связано с размером скопированных приращений и усугубить, если на компьютере установлено менее 45 МБ памяти из-за переключения дисков.
>
> Предпочтительным решением является реализация метода [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , который использует память, выделенную [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) , а не [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Это может зарезервировать большой фрагмент виртуального адресного пространства, а затем зафиксировать память в этом адресном пространстве по мере необходимости. Копирование данных не происходит, и память зафиксирована только по мере необходимости.
>
> Альтернативой [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) является вызов метода [**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) объекта Stream для увеличения объема выделяемой памяти заранее. Однако это не так эффективно, как использование [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), как описано выше.

 

## <a name="methods"></a>Методы

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream:: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Считывает указанное число байтов из объекта потока в память, начиная с текущего указателя поиска. Эта реализация возвращает значение \_ ОК, если конец потока был достигнут во время чтения. (Это аналогично поведению "конец файла", обнаруженному в файловой системе MS-DOS FAT).

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream:: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Записывает указанное число из байтов в объект потока, начиная с текущего указателя поиска. В этой реализации объекты потока не имеют разреженных объектов. Все байты заполнения в конечном итоге выделяются на диске и назначаются потоку.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream:: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Изменяет указатель поиска на новое расположение относительно начала потока до конца потока или текущего положения поиска.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream:: SetSize**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Изменяет размер объекта-потока. В этой реализации нет никакой гарантии, что выделенное пространство будет непрерывным.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Копирует указанное число байтов из текущего указателя поиска в потоке до текущего указателя поиска в другом потоке.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

Реализация составного файла для [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) поддерживает открытие потоков только в режиме Direct, а не в режиме транзакций. Поэтому метод не действует при вызове, отличном от сброса всех буферов памяти до следующего уровня хранилища.

В этой реализации не имеет значения, следует ли зафиксировать изменения в потоках, необходимо только внести изменения в объекты хранилища.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream:: revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Эта реализация не поддерживает транзакционные потоки, поэтому вызов этого метода не оказывает никакого влияния.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Блокировка диапазона не поддерживается этой реализацией, поэтому вызов этого метода не оказывает никакого влияния.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream:: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Удаляет ограничение доступа для диапазона байтов, которые ранее были ограничены с помощью [**IStream:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream:: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Получает структуру [**статстг**](/windows/win32/api/objidl/ns-objidl-statstg) для этого потока

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream:: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Создает новый объект потока с собственным указателем, который ссылается на те же байты, что и исходный поток.

</dd> </dl>

Для простого режима [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) действуют следующие ограничения.

-   Поток является простым режимом, если он был создан или открыт из хранилища в простом режиме. Хранилище имеет простой режим, если он создан или открыт с помощью \_ простого флага стгм, установленного в параметре *грфмоде* .
-   Методы [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) и [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) не поддерживаются.
-   Поддерживается метод [**stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) , однако \_ должно быть указано значение статфлаг.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**Метод IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**стгкреатедокфиле**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**стгопенстораже**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 