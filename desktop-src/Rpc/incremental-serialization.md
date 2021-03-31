---
title: Добавочная сериализация
description: При использовании добавочной сериализации стилей вы предоставляете три подпрограммы для работы с буфером.
ms.assetid: c7383b4d-94d1-4edd-ac29-c11fb5343156
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 409f8da0881719ec9273f4dd12cc99e3d36c35a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532402"
---
# <a name="incremental-serialization"></a>Добавочная сериализация

При использовании добавочной сериализации стилей вы предоставляете три подпрограммы для работы с буфером. Эти подпрограммы: Alloc, Read и Write. Подпрограммы выделения памяти распределяют буфер требуемого размера. Подпрограммы записи записывают данные в буфер, а подпрограммы чтения получают буфер, содержащий упакованные данные. Один вызов сериализации может выполнять несколько вызовов этих подпрограмм.

Добавочный стиль сериализации использует следующие подпрограммы:

-   [**месенкодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [**месдекодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree)

Ниже приведены прототипы функций Alloc, Read и Write, которые необходимо предоставить.

``` syntax
void __RPC_USER Alloc (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returns pointer to allocated buffer */
   unsigned int *pSize); /* inputs requested bytes; outputs 
                         /* pBuffer size */

void __RPC_USER Write (
   void *State,          /* application-defined pointer */
   char *Buffer,         /* buffer with serialized data */
   unsigned int Size);   /* number of bytes to write from Buffer */

void __RPC_USER Read (
   void *State,          /* application-defined pointer */
   char **pBuffer,       /* returned pointer to buffer with data */
   unsigned int *pSize); /* number of bytes to read into pBuffer */
```

Входные данные состояния. параметр для всех трех функций является определяемым приложением указателем, связанным с маркером служб кодирования. Приложение может использовать этот указатель для доступа к структуре, содержащей сведения о конкретном приложении, такие как маркер файла или указатель потока. Обратите внимание, что заглушки не изменяют указатель состояния, кроме передачи его в функции Alloc, Read и Write. Во время кодирования вызывается метод Alloc для получения буфера, в который сериализуются данные. Затем вызывается запись, чтобы позволить приложению управлять моментом и местом хранения сериализованных данных. Во время декодирования вызывается метод Read, который возвращает запрошенное число байтов сериализованных данных, из которых было сохранено приложение.

Важной функцией инкрементного стиля является то, что обработчик сохраняет указатель состояния. Этот указатель поддерживает состояние и никогда не затрагивается функциями RPC, за исключением случаев передачи указателя на функцию Alloc, Write или Read. Этот обработчик также поддерживает внутреннее состояние, которое позволяет кодировать и декодировать несколько экземпляров типа в один и тот же буфер путем добавления заполнения по мере необходимости для выравнивания. Функция [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) сбрасывает обработчик в исходное состояние, чтобы разрешить чтение или запись с начала буфера.

Функции Alloc и Write, а также определяемый приложением указатель связаны с обработчиком кодирования-служб путем вызова функции [**месенкодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) . **Месенкодеинкременталхандлекреате** выделяет память, необходимую для обработчика, а затем инициализирует ее.

Приложение может вызвать [**месдекодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) для создания маркера декодирования, [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) для повторной инициализации этого обработчика или [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика. Функция Read вместе с параметром, определяемым приложением, связана с маркером декодирования путем вызова подпрограммы **месдекодеинкременталхандлекреате** . Функция создает и инициализирует этот обработчик.

Параметры UserState, Alloc, Write и Read [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) могут иметь **значение NULL** , чтобы не указывать никаких изменений.

 

 




