---
title: /Error, параметр
description: Параметр/error определяет типы проверки ошибок, которые созданные заглушки будут выполнять во время выполнения.
ms.assetid: abd3616a-2d2c-4a7d-bf3a-c84a43387894
keywords:
- MIDL/Error Switch
topic_type:
- apiref
api_name:
- /error
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84a56c1ae3d57ab1931ec175aa8dc9010ea6b8a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104411900"
---
# <a name="error-switch"></a><span data-ttu-id="074c7-104">/Error, параметр</span><span class="sxs-lookup"><span data-stu-id="074c7-104">/error switch</span></span>

<span data-ttu-id="074c7-105">Параметр **/Error** определяет типы проверки ошибок, которые созданные заглушки будут выполнять во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="074c7-105">The **/error** switch determines the types of error checking that the generated stubs will perform at run time.</span></span>

> [!Note]  
> <span data-ttu-id="074c7-106">Эта функция устарела и больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="074c7-106">This feature is obsolete and no longer supported.</span></span> <span data-ttu-id="074c7-107">Рекомендуется использовать параметр [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="074c7-107">The use of the [**/robust**](-robust.md) switch is recommended.</span></span>

 

``` syntax
midl /error { allocation | stub_data | ref | bounds_check | none | all }
```

## <a name="switch-options"></a><span data-ttu-id="074c7-108">Параметры коммутатора</span><span class="sxs-lookup"><span data-stu-id="074c7-108">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="allocation"></span><span id="ALLOCATION"></span>

<span data-ttu-id="074c7-109"><span id="allocation"></span><span id="ALLOCATION"></span>выделение \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="074c7-109"><span id="allocation"></span><span id="ALLOCATION"></span>\*\*\*\*allocation\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-110">Проверяет, возвращает ли метод [**MIDL \_ user \_ allocate**](midl-user-allocate-1.md) значение **null** , что указывает на ошибку нехватки памяти.</span><span class="sxs-lookup"><span data-stu-id="074c7-110">Checks whether [**midl\_user\_allocate**](midl-user-allocate-1.md) returns a **NULL** value, indicating an out-of-memory error.</span></span>

</dd> <dt>

<span id="stub_data"></span><span id="STUB_DATA"></span>

<span data-ttu-id="074c7-111"><span id="stub_data"></span><span id="STUB_DATA"></span>данные заглушки \* \* \* \_ \*</span><span class="sxs-lookup"><span data-stu-id="074c7-111"><span id="stub_data"></span><span id="STUB_DATA"></span>\*\*\*\*stub\_data\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-112">Создает заглушку, которая перехватывает исключения при распаковке на стороне сервера и распространяет их обратно клиенту.</span><span class="sxs-lookup"><span data-stu-id="074c7-112">Generates a stub that catches unmarshaling exceptions on the server side and propagates them back to the client.</span></span>

</dd> <dt>

<span id="ref"></span><span id="REF"></span>

<span data-ttu-id="074c7-113"><span id="ref"></span><span id="REF"></span>ref \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="074c7-113"><span id="ref"></span><span id="REF"></span>\*\*\*\*ref\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-114">Создает код, выполняющий проверку во время выполнения, чтобы убедиться, что в клиентские заглушки не передаются **пустые** указатели ссылок, и вызывает \_ исключение RPC X \_ null Pointer, \_ \_ если оно найдено.</span><span class="sxs-lookup"><span data-stu-id="074c7-114">Generates code that runs a check at run time to ensure that no **NULL** reference pointers are being passed to the client stubs and raises an RPC\_X\_NULL\_REF\_POINTER exception if it finds any.</span></span>

</dd> <dt>

<span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>

<span data-ttu-id="074c7-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>Проверка границ \_ \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="074c7-115"><span id="bounds_check"></span><span id="BOUNDS_CHECK"></span>\*\*\*\*bounds\_check\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-116">Проверяет размер одноцветных и разных массивов в соответствии со спецификацией длины передачи.</span><span class="sxs-lookup"><span data-stu-id="074c7-116">Checks size of conformant-varying and varying arrays against transmission length specification.</span></span>

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span data-ttu-id="074c7-117"><span id="none"></span><span id="NONE"></span>нет \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="074c7-117"><span id="none"></span><span id="NONE"></span>\*\*\*\*none\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-118">Не выполняет проверку ошибок.</span><span class="sxs-lookup"><span data-stu-id="074c7-118">Performs no error checking.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="074c7-119"><span id="all"></span><span id="ALL"></span>все \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="074c7-119"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="074c7-120">Выполняет все проверки ошибок.</span><span class="sxs-lookup"><span data-stu-id="074c7-120">Performs all error checking.</span></span> <span data-ttu-id="074c7-121">Действует с MIDL версии 5,0. это параметр компилятора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="074c7-121">Effective with MIDL version 5.0, this is a default compiler switch.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="074c7-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="074c7-122">Remarks</span></span>

<span data-ttu-id="074c7-123">Параметр **/Error** выбирает число проверок ошибок, которые будут выполнены для созданных файлов заглушек.</span><span class="sxs-lookup"><span data-stu-id="074c7-123">The **/error** switch selects the number of error checks that the generated stub files will perform.</span></span> <span data-ttu-id="074c7-124">Начиная с MIDL версии 5,0, значение по умолчанию — **/Error ALL**.</span><span class="sxs-lookup"><span data-stu-id="074c7-124">Effective with MIDL version 5.0, the default setting is **/error all**.</span></span>

<span data-ttu-id="074c7-125">Проверяемые ошибки перечисления (по умолчанию во всех версиях MIDL) являются ошибками усечения, которые возникают при преобразовании между типами **Long enum** (32-разрядные целые числа) и **короткими типами enum** (представлением сетевых [**данных) и**](enum.md)числом идентификаторов в перечислении, превышающим 32 767.</span><span class="sxs-lookup"><span data-stu-id="074c7-125">The enum errors that are checked (by default in all versions of MIDL) are truncation errors caused when converting between **long enum** types (32-bit integers) and **short enum** types (the network-data representation of [**enum**](enum.md)), and the number of identifiers in an enumeration exceeding 32,767.</span></span>

<span data-ttu-id="074c7-126">Проверка ошибок доступа к памяти (также по умолчанию во всех версиях MIDL) предназначена для указателей, которые выходят за пределы буфера в коде маршалирования и для согласованных массивов, размер которых меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="074c7-126">The memory-access error checking (also by default in all versions of MIDL) is for pointers that exceed the end of the buffer in marshaling code and for conformant arrays whose size is less than zero.</span></span> <span data-ttu-id="074c7-127">Используйте флаг **\_ проверки границ/Error** , чтобы проверить наличие других недопустимых границ массива.</span><span class="sxs-lookup"><span data-stu-id="074c7-127">Use the **/error bounds\_check** flag to check for other invalid array bounds.</span></span>

<span data-ttu-id="074c7-128">При указании **распределения/Error** заглушки включают код, вызывающий исключение, когда [**\_ пользователь MIDL \_ выделил**](midl-user-allocate-1.md) возвращает 0.</span><span class="sxs-lookup"><span data-stu-id="074c7-128">When you specify **/error allocation**, the stubs include code that raises an exception when [**midl\_user\_allocate**](midl-user-allocate-1.md) returns 0.</span></span>

<span data-ttu-id="074c7-129">Параметр **\_ данных заглушки/Error** предотвращает сбой сервера в данных клиента во время распаковки, что обеспечивает более надежный метод обработки операции распаковки.</span><span class="sxs-lookup"><span data-stu-id="074c7-129">The **/error stub\_data** option prevents client data from crashing the server during unmarshaling, effectively providing a more robust method of handling the unmarshaling operation.</span></span>

<span data-ttu-id="074c7-130">Начиная с Windows 2000, базовый модуль маршалирования отчета о выходе выполнения выполняет большинство этих проверок.</span><span class="sxs-lookup"><span data-stu-id="074c7-130">Effective with WindowsÂ 2000, the underlying run-time NDR marshaling engine performs most of these checks.</span></span> <span data-ttu-id="074c7-131">Это означает, что при использовании одного из полностью интерпретируемых режимов ([**/Oi**](-oi.md), **/OIF**) создания заглушки выбор разных параметров проверки на наличие ошибок не влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="074c7-131">This means that if you are using one of the fully-interpreted modes ([**/Oi**](-oi.md), **/Oif**) of stub generation, choosing different error checking options will not have a marked effect on performance.</span></span>

## <a name="examples"></a><span data-ttu-id="074c7-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="074c7-132">Examples</span></span>

<span data-ttu-id="074c7-133">**MIDL/Error выделенное имя файла. idl**</span><span class="sxs-lookup"><span data-stu-id="074c7-133">**midl /error allocation filename.idl**</span></span>

<span data-ttu-id="074c7-134">**MIDL/Error нет filename. idl**</span><span class="sxs-lookup"><span data-stu-id="074c7-134">**midl /error none filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="074c7-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="074c7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074c7-136">Общий синтаксис командной строки MIDL</span><span class="sxs-lookup"><span data-stu-id="074c7-136">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="074c7-137">**/robust**</span><span class="sxs-lookup"><span data-stu-id="074c7-137">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




