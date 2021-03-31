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
# <a name="incremental-serialization"></a><span data-ttu-id="3ad9c-103">Добавочная сериализация</span><span class="sxs-lookup"><span data-stu-id="3ad9c-103">Incremental Serialization</span></span>

<span data-ttu-id="3ad9c-104">При использовании добавочной сериализации стилей вы предоставляете три подпрограммы для работы с буфером.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-104">When using the incremental style serialization, you supply three routines to manipulate the buffer.</span></span> <span data-ttu-id="3ad9c-105">Эти подпрограммы: Alloc, Read и Write.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-105">These routines are: Alloc, Read, and Write.</span></span> <span data-ttu-id="3ad9c-106">Подпрограммы выделения памяти распределяют буфер требуемого размера.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-106">The Alloc routine allocates a buffer of the required size.</span></span> <span data-ttu-id="3ad9c-107">Подпрограммы записи записывают данные в буфер, а подпрограммы чтения получают буфер, содержащий упакованные данные.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-107">The Write routine writes the data into the buffer, and the Read routine retrieves a buffer that contains marshaled data.</span></span> <span data-ttu-id="3ad9c-108">Один вызов сериализации может выполнять несколько вызовов этих подпрограмм.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-108">A single serialization call can make several calls to these routines.</span></span>

<span data-ttu-id="3ad9c-109">Добавочный стиль сериализации использует следующие подпрограммы:</span><span class="sxs-lookup"><span data-stu-id="3ad9c-109">The incremental style of serialization uses the following routines:</span></span>

-   [<span data-ttu-id="3ad9c-110">**месенкодеинкременталхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-110">**MesEncodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)
-   [<span data-ttu-id="3ad9c-111">**месдекодеинкременталхандлекреате**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-111">**MesDecodeIncrementalHandleCreate**</span></span>](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [<span data-ttu-id="3ad9c-112">**месинкременталхандлересет**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-112">**MesIncrementalHandleReset**</span></span>](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset)
-   [<span data-ttu-id="3ad9c-113">**мешандлефри**</span><span class="sxs-lookup"><span data-stu-id="3ad9c-113">**MesHandleFree**</span></span>](/windows/desktop/api/Midles/nf-midles-meshandlefree)

<span data-ttu-id="3ad9c-114">Ниже приведены прототипы функций Alloc, Read и Write, которые необходимо предоставить.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-114">The prototypes for the Alloc, Read, and Write functions that you must provide are shown below:</span></span>

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

<span data-ttu-id="3ad9c-115">Входные данные состояния. параметр для всех трех функций является определяемым приложением указателем, связанным с маркером служб кодирования.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-115">The State input a parameter for all three functions is the application-defined pointer that was associated with the encoding services handle.</span></span> <span data-ttu-id="3ad9c-116">Приложение может использовать этот указатель для доступа к структуре, содержащей сведения о конкретном приложении, такие как маркер файла или указатель потока.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-116">The application can use this pointer to access the structure containing application-specific information, such as a file handle or stream pointer.</span></span> <span data-ttu-id="3ad9c-117">Обратите внимание, что заглушки не изменяют указатель состояния, кроме передачи его в функции Alloc, Read и Write.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-117">Note that the stubs do not modify the State pointer other than to pass it to the Alloc, Read, and Write functions.</span></span> <span data-ttu-id="3ad9c-118">Во время кодирования вызывается метод Alloc для получения буфера, в который сериализуются данные.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-118">During encoding, Alloc is called to obtain a buffer into which the data is serialized.</span></span> <span data-ttu-id="3ad9c-119">Затем вызывается запись, чтобы позволить приложению управлять моментом и местом хранения сериализованных данных.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-119">Then, Write is called to enable the application to control when and where the serialized data is stored.</span></span> <span data-ttu-id="3ad9c-120">Во время декодирования вызывается метод Read, который возвращает запрошенное число байтов сериализованных данных, из которых было сохранено приложение.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-120">During decoding, Read is called to return the requested number of bytes of serialized data from where the application stored it.</span></span>

<span data-ttu-id="3ad9c-121">Важной функцией инкрементного стиля является то, что обработчик сохраняет указатель состояния.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-121">An important feature of the incremental style is that the handle keeps the state pointer for you.</span></span> <span data-ttu-id="3ad9c-122">Этот указатель поддерживает состояние и никогда не затрагивается функциями RPC, за исключением случаев передачи указателя на функцию Alloc, Write или Read.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-122">This pointer maintains the state and is never touched by the RPC functions, except when passing the pointer to Alloc, Write, or Read function.</span></span> <span data-ttu-id="3ad9c-123">Этот обработчик также поддерживает внутреннее состояние, которое позволяет кодировать и декодировать несколько экземпляров типа в один и тот же буфер путем добавления заполнения по мере необходимости для выравнивания.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-123">The handle also maintains an internal state that makes it possible to encode and decode several type instances to the same buffer by adding padding as needed for alignment.</span></span> <span data-ttu-id="3ad9c-124">Функция [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) сбрасывает обработчик в исходное состояние, чтобы разрешить чтение или запись с начала буфера.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-124">The [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) function resets a handle to its initial state to enable reading or writing from the beginning of the buffer.</span></span>

<span data-ttu-id="3ad9c-125">Функции Alloc и Write, а также определяемый приложением указатель связаны с обработчиком кодирования-служб путем вызова функции [**месенкодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) .</span><span class="sxs-lookup"><span data-stu-id="3ad9c-125">The Alloc and Write functions, along with an application-defined pointer, are associated with an encoding-services handle by a call to the [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate) function.</span></span> <span data-ttu-id="3ad9c-126">**Месенкодеинкременталхандлекреате** выделяет память, необходимую для обработчика, а затем инициализирует ее.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-126">**MesEncodeIncrementalHandleCreate** allocates the memory needed for the handle and then initializes it.</span></span>

<span data-ttu-id="3ad9c-127">Приложение может вызвать [**месдекодеинкременталхандлекреате**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) для создания маркера декодирования, [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) для повторной инициализации этого обработчика или [**мешандлефри**](/windows/desktop/api/Midles/nf-midles-meshandlefree) для освобождения памяти обработчика.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-127">The application can call [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate) to create a decoding handle, [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) to reinitialize the handle, or [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree) to free the handle's memory.</span></span> <span data-ttu-id="3ad9c-128">Функция Read вместе с параметром, определяемым приложением, связана с маркером декодирования путем вызова подпрограммы **месдекодеинкременталхандлекреате** .</span><span class="sxs-lookup"><span data-stu-id="3ad9c-128">The Read function, along with an application-defined parameter, is associated with a decoding handle by a call to the **MesDecodeIncrementalHandleCreate** routine.</span></span> <span data-ttu-id="3ad9c-129">Функция создает и инициализирует этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-129">The function creates the handle and initializes it.</span></span>

<span data-ttu-id="3ad9c-130">Параметры UserState, Alloc, Write и Read [**месинкременталхандлересет**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) могут иметь **значение NULL** , чтобы не указывать никаких изменений.</span><span class="sxs-lookup"><span data-stu-id="3ad9c-130">The UserState, Alloc, Write, and Read parameters of [**MesIncrementalHandleReset**](/windows/desktop/api/Midles/nf-midles-mesincrementalhandlereset) can be **NULL** to indicate no change.</span></span>

 

 




