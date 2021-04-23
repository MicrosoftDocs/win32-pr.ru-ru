---
description: Так как API установки не предоставляет подпрограмму обратного вызова CAB-файла по умолчанию, необходимо предоставить подпрограмму. Подпрограммы обратного вызова, необходимые функции Сетупитератекабинет, должны иметь ту же форму, что и, на которую указывает Филекаллбакк.
ms.assetid: 45a2690e-1db6-4a09-a141-9e68ebc2a6d8
title: Создание подпрограммы обратного вызова CAB-файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f25d59515a6afdd68cef4458868fbfb62335aed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264815"
---
# <a name="creating-a-cabinet-callback-routine"></a><span data-ttu-id="29e62-104">Создание подпрограммы обратного вызова CAB-файла</span><span class="sxs-lookup"><span data-stu-id="29e62-104">Creating a Cabinet Callback Routine</span></span>

<span data-ttu-id="29e62-105">Так как API установки не предоставляет подпрограмму обратного вызова CAB-файла по умолчанию, необходимо предоставить подпрограмму.</span><span class="sxs-lookup"><span data-stu-id="29e62-105">Because the Setup API does not supply a default cabinet callback routine, you need to supply a routine.</span></span> <span data-ttu-id="29e62-106">Подпрограммы обратного вызова, необходимые функции [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) , должны иметь ту же форму, что и, на которую указывает [филекаллбакк](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="29e62-106">The callback routine that the [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function requires must have the same form as those pointed to by [FileCallback](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span>

<span data-ttu-id="29e62-107">Ниже приведен синтаксис, который [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) использует для отправки уведомления в подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="29e62-107">Following is the syntax that [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) uses to send a notification to the callback routine.</span></span>

``` syntax
MsgHandler(          //the specified callback routine
    Context,         //context used by the callback routine
    Notification,    //cabinet notification
    Param1,          //additional notification information
    Param2           //additional notification information
);
```

<span data-ttu-id="29e62-108">Параметр *контекста* является указателем void на переменную контекста или структуру, которую может использовать подпрограммы обратного вызова для хранения информации, которая должна сохраняться между последовательными вызовами подпрограммы обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="29e62-108">The *Context* parameter is a void pointer to a context variable or structure that can be used by the callback routine to store information that needs to persist between subsequent calls to the callback routine.</span></span>

<span data-ttu-id="29e62-109">Реализация этого контекста задается подделом обратного вызова и никогда не указывается или не изменяется с помощью [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span><span class="sxs-lookup"><span data-stu-id="29e62-109">This context's implementation is specified by the callback routine, and it is never referenced or altered by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).</span></span>

<span data-ttu-id="29e62-110">Параметр *уведомления* является целым числом без знака и может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29e62-110">The *Notification* parameter is an unsigned integer and will be one of the following values.</span></span>



| <span data-ttu-id="29e62-111">Уведомление</span><span class="sxs-lookup"><span data-stu-id="29e62-111">Notification</span></span>                                                        | <span data-ttu-id="29e62-112">Описание</span><span class="sxs-lookup"><span data-stu-id="29e62-112">Description</span></span>                                        |
|---------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="29e62-113">**СПФИЛЕНОТИФИ \_ филикстрактед**</span><span class="sxs-lookup"><span data-stu-id="29e62-113">**SPFILENOTIFY\_FILEEXTRACTED**</span></span>](spfilenotify-fileextracted.md)   | <span data-ttu-id="29e62-114">Файл был извлечен из CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="29e62-114">The file has been extracted from the cabinet.</span></span>      |
| [<span data-ttu-id="29e62-115">**СПФИЛЕНОТИФИ \_ филеинкабинет**</span><span class="sxs-lookup"><span data-stu-id="29e62-115">**SPFILENOTIFY\_FILEINCABINET**</span></span>](spfilenotify-fileincabinet.md)   | <span data-ttu-id="29e62-116">В CAB-файле обнаружен файл.</span><span class="sxs-lookup"><span data-stu-id="29e62-116">A file is encountered in the cabinet.</span></span>              |
| [<span data-ttu-id="29e62-117">**СПФИЛЕНОТИФИ \_ нидневкабинет**</span><span class="sxs-lookup"><span data-stu-id="29e62-117">**SPFILENOTIFY\_NEEDNEWCABINET**</span></span>](spfilenotify-neednewcabinet.md) | <span data-ttu-id="29e62-118">Текущий файл продолжает работу в следующем CAB-файле.</span><span class="sxs-lookup"><span data-stu-id="29e62-118">The current file is continued in the next cabinet.</span></span> |



 

<span data-ttu-id="29e62-119">Последние два параметра, *param1* и *Param2*, являются также целыми числами без знака и содержат дополнительные сведения, относящиеся к уведомлению.</span><span class="sxs-lookup"><span data-stu-id="29e62-119">The final two parameters, *Param1* and *Param2*, are also unsigned integers and contain additional information relevant to the notification.</span></span> <span data-ttu-id="29e62-120">Дополнительные сведения об уведомлениях, отправляемых [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), см. в разделе [уведомления о CAB-файлах](cabinet-file-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="29e62-120">For more information about the notifications sent by [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta), see [Cabinet File Notifications](cabinet-file-notifications.md).</span></span>

<span data-ttu-id="29e62-121">\_ \_ Процедура обратного вызова для уведомления о файле SP \_ возвращает целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="29e62-121">A SP\_FILE\_NOTIFY\_CALLBACK routine returns an unsigned integer.</span></span> <span data-ttu-id="29e62-122">Подпрограммы обратного вызова CAB-файла должны возвращать одно из следующих значений в зависимости от уведомления.</span><span class="sxs-lookup"><span data-stu-id="29e62-122">The cabinet callback routine should return one of the following values depending on the notification.</span></span>

<span data-ttu-id="29e62-123">Для уведомления СПФИЛЕНОТИФИ \_ Филеинкабинет [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) ожидает, что подпрограммы обратного вызова возвращают одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29e62-123">For the SPFILENOTIFY\_FILEINCABINET notification, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="29e62-124">Значение</span><span class="sxs-lookup"><span data-stu-id="29e62-124">Value</span></span>         | <span data-ttu-id="29e62-125">Значение</span><span class="sxs-lookup"><span data-stu-id="29e62-125">Meaning</span></span>                   |
|---------------|---------------------------|
| <span data-ttu-id="29e62-126">прервать ФИЛЕОП \_</span><span class="sxs-lookup"><span data-stu-id="29e62-126">FILEOP\_ABORT</span></span> | <span data-ttu-id="29e62-127">Прервать обработку CAB-файлов.</span><span class="sxs-lookup"><span data-stu-id="29e62-127">Abort cabinet processing.</span></span> |
| <span data-ttu-id="29e62-128">ФИЛЕОП \_ доит</span><span class="sxs-lookup"><span data-stu-id="29e62-128">FILEOP\_DOIT</span></span>  | <span data-ttu-id="29e62-129">Извлеките текущий файл.</span><span class="sxs-lookup"><span data-stu-id="29e62-129">Extract the current file.</span></span> |
| <span data-ttu-id="29e62-130">ФИЛЕОП \_ пропустить</span><span class="sxs-lookup"><span data-stu-id="29e62-130">FILEOP\_SKIP</span></span>  | <span data-ttu-id="29e62-131">Пропустить текущий файл.</span><span class="sxs-lookup"><span data-stu-id="29e62-131">Skip the current file.</span></span>    |



 

<span data-ttu-id="29e62-132">Для СПФИЛЕНОТИФИ \_ нидневкабинет и спфиленотифи \_ Филикстрактед уведомлений **сетупитератекабинет** ожидает, что подпрограммы обратного вызова возвращают одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="29e62-132">For SPFILENOTIFY\_NEEDNEWCABINET and SPFILENOTIFY\_FILEEXTRACTED notifications, **SetupIterateCabinet** expects one of the following values to be returned by the callback routine.</span></span>



| <span data-ttu-id="29e62-133">Значение</span><span class="sxs-lookup"><span data-stu-id="29e62-133">Value</span></span>      | <span data-ttu-id="29e62-134">Значение</span><span class="sxs-lookup"><span data-stu-id="29e62-134">Meaning</span></span>                                                                                                                                                                                                                           |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e62-135">БЕЗ \_ ошибок</span><span class="sxs-lookup"><span data-stu-id="29e62-135">NO\_ERROR</span></span>  | <span data-ttu-id="29e62-136">Ошибок не обнаружено, продолжить обработку CAB-файла.</span><span class="sxs-lookup"><span data-stu-id="29e62-136">No error was encountered, continue processing the cabinet.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="29e62-137">Ошибка \_ xxx</span><span class="sxs-lookup"><span data-stu-id="29e62-137">ERROR\_XXX</span></span> | <span data-ttu-id="29e62-138">Произошла ошибка указанного типа.</span><span class="sxs-lookup"><span data-stu-id="29e62-138">An error of the specified type occurred.</span></span> <span data-ttu-id="29e62-139">Функция [**сетупитератекабинет**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) вернет **значение false**, а указанный код ошибки будет возвращен вызовом [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="29e62-139">The [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) function will return **FALSE**, and the specified error code will be returned by a call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span> |



 

<span data-ttu-id="29e62-140">Если подпрограммы обратного вызова возвращают ФИЛЕОП \_ доит, подпрограммы также должны предоставлять полный целевой путь.</span><span class="sxs-lookup"><span data-stu-id="29e62-140">If the callback routine returns FILEOP\_DOIT, the routine must also provide a full target path.</span></span> <span data-ttu-id="29e62-141">Дополнительные сведения см. в разделе [**спфиленотифи \_ филеинкабинет**](spfilenotify-fileincabinet.md).</span><span class="sxs-lookup"><span data-stu-id="29e62-141">For more information see [**SPFILENOTIFY\_FILEINCABINET**](spfilenotify-fileincabinet.md).</span></span>

 

 
