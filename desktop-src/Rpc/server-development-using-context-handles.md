---
title: Разработка сервера с помощью дескрипторов контекста
description: С точки зрения разработки серверной программы, маркер контекста является нетипизированным указателем. Серверные программы инициализируют дескрипторы контекста, указывая их на данные в памяти или в другой форме хранилища (например, файлы на дисках).
ms.assetid: 6a1aabca-4cb9-401c-90c7-0cff7a69b7b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f743a4a6aa4a2aa7b6987bb54dc56e55cffbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068418"
---
# <a name="server-development-using-context-handles"></a><span data-ttu-id="635de-104">Разработка сервера с помощью дескрипторов контекста</span><span class="sxs-lookup"><span data-stu-id="635de-104">Server Development Using Context Handles</span></span>

<span data-ttu-id="635de-105">С точки зрения разработки серверной программы, маркер контекста является нетипизированным указателем.</span><span class="sxs-lookup"><span data-stu-id="635de-105">From the perspective of server program development, a context handle is an untyped pointer.</span></span> <span data-ttu-id="635de-106">Серверные программы инициализируют дескрипторы контекста, указывая их на данные в памяти или в другой форме хранилища (например, файлы на дисках).</span><span class="sxs-lookup"><span data-stu-id="635de-106">Server programs initialize context handles by pointing them at data in memory or on some other form of storage (such as files on disks).</span></span>

<span data-ttu-id="635de-107">Например, предположим, что клиент использует маркер контекста для запроса ряда обновлений записи в базе данных.</span><span class="sxs-lookup"><span data-stu-id="635de-107">For instance, suppose that a client uses a context handle to request a series of updates to a record in a database.</span></span> <span data-ttu-id="635de-108">Клиент вызывает удаленную процедуру на сервере и передает ей ключ поиска.</span><span class="sxs-lookup"><span data-stu-id="635de-108">The client calls a remote procedure on the server and passes it a search key.</span></span> <span data-ttu-id="635de-109">Серверная программа ищет ключ поиска в базе данных и получает целочисленный номер записи для соответствующей записи.</span><span class="sxs-lookup"><span data-stu-id="635de-109">The server program searches the database for the search key and obtains the integer record number of the matching record.</span></span> <span data-ttu-id="635de-110">Затем сервер может указать указатель на void в расположении в памяти, содержащем номер записи.</span><span class="sxs-lookup"><span data-stu-id="635de-110">The server can then point a pointer to void at a memory location containing the record number.</span></span> <span data-ttu-id="635de-111">При возврате удаленной процедуре потребуется возврат указателя в виде контекстного контекста через его возвращаемое значение или список параметров.</span><span class="sxs-lookup"><span data-stu-id="635de-111">When it returns, the remote procedure would need to return the pointer as a context handle through its return value or its parameter list.</span></span> <span data-ttu-id="635de-112">Клиенту необходимо передать указатель на сервер каждый раз, когда он вызывал удаленные процедуры для обновления записи.</span><span class="sxs-lookup"><span data-stu-id="635de-112">The client would need to pass the pointer to the server each time it called remote procedures to update the record.</span></span> <span data-ttu-id="635de-113">Во время каждой из этих операций обновления сервер преобразует указатель void в указатель на целое число.</span><span class="sxs-lookup"><span data-stu-id="635de-113">During each of these update operations, the server would cast the void pointer to be a pointer to an integer.</span></span>

<span data-ttu-id="635de-114">После того как серверная программа указывает на контекстные данные, этот маркер считается открытым.</span><span class="sxs-lookup"><span data-stu-id="635de-114">After the server program points the context handle at context data, the handle is considered opened.</span></span> <span data-ttu-id="635de-115">Дескрипторы, содержащие значение **null** , закрываются.</span><span class="sxs-lookup"><span data-stu-id="635de-115">Handles containing a **NULL** value are closed.</span></span> <span data-ttu-id="635de-116">Сервер поддерживает открытый обработчик контекста до тех пор, пока клиент не вызовет удаленную процедуру, которая его закрывает.</span><span class="sxs-lookup"><span data-stu-id="635de-116">The server maintains an opened context handle until the client calls a remote procedure that closes it.</span></span> <span data-ttu-id="635de-117">Если сеанс клиента завершается, пока открыт маркер, то во время выполнения RPC вызывается подпрограммы запуска сервера для освобождения маркера.</span><span class="sxs-lookup"><span data-stu-id="635de-117">If the client session terminates while the handle is open, the RPC run time calls the server run-down routine to free the handle.</span></span>

<span data-ttu-id="635de-118">В следующем фрагменте кода показано, как сервер может реализовать контекстный маркер.</span><span class="sxs-lookup"><span data-stu-id="635de-118">The following code fragment demonstrates how a server might implement a context handle.</span></span> <span data-ttu-id="635de-119">В этом примере сервер поддерживает файл данных, который клиент записывает на использование удаленных процедур.</span><span class="sxs-lookup"><span data-stu-id="635de-119">In this example, the server maintains a data file that the client writes to using remote procedures.</span></span> <span data-ttu-id="635de-120">Контекстная информация — это файловый обработчик, который отслеживает текущее расположение в файле, в котором сервер будет записывать данные.</span><span class="sxs-lookup"><span data-stu-id="635de-120">The context information is a file handle that keeps track of the current location in the file where the server will write data.</span></span> <span data-ttu-id="635de-121">Этот файл упаковывается как обработчик контекста в список параметров для удаленных вызовов процедур.</span><span class="sxs-lookup"><span data-stu-id="635de-121">The file handle is packaged as a context handle in the parameter list to remote procedure calls.</span></span> <span data-ttu-id="635de-122">Структура содержит имя файла и файловый обработчик.</span><span class="sxs-lookup"><span data-stu-id="635de-122">A structure contains the file name and the file handle.</span></span> <span data-ttu-id="635de-123">Определение интерфейса для этого примера показано в области [разработки интерфейса с использованием дескрипторов контекста](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="635de-123">The interface definition for this example is shown in [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span>


```C++
/* cxhndlp.c (fragment of file containing remote procedures) */
typedef struct 
{
     FILE* hFile;
     char   achFile[256];
} FILE_CONTEXT_TYPE;
```



<span data-ttu-id="635de-124">Функция Ремотеопен открывает файл на сервере:</span><span class="sxs-lookup"><span data-stu-id="635de-124">The function RemoteOpen opens a file on the server:</span></span>


```C++
short RemoteOpen(
    PPCONTEXT_HANDLE_TYPE pphContext,
    unsigned char *pszFileName)
{
    FILE               *hFile;
    FILE_CONTEXT_TYPE  *pFileContext;
 
    if ((hFile = fopen(pszFileName, "r")) == NULL) 
    {
        *pphContext = (PCONTEXT_HANDLE_TYPE) NULL;
        return(-1);
    }
    else 
    {
        pFileContext = (FILE_CONTEXT_TYPE *) 
                       MIDL_user_allocate(sizeof(FILE_CONTEXT_TYPE));
        pFileContext->hFile = hFile;
        // check if pszFileName is longer than 256 and if yes, return
        // an error
        strcpy_s(pFileContext->achFile, srlen(pszFileName), pszFileName);
        *pphContext = (PCONTEXT_HANDLE_TYPE) pFileContext;
        return(0);
    }
}
```



<span data-ttu-id="635de-125">Функция Ремотереад считывает файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="635de-125">The function RemoteRead reads a file on the server.</span></span>


```C++
short RemoteRead(
    PCONTEXT_HANDLE_TYPE phContext, 
    unsigned char *pbBuf, 
    short *pcbBuf) 
{ 
    FILE_CONTEXT_TYPE *pFileContext; 
    printf("in RemoteRead\n"); 
    pFileContext = (FILE_CONTEXT_TYPE *) phContext; 
    *pcbBuf = (short) fread(pbBuf, sizeof(char), 
                            BUFSIZE, 
                            pFileContext->hFile); 
    return(*pcbBuf); 
}
```



<span data-ttu-id="635de-126">Функция Ремотеклосе закрывает файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="635de-126">The function RemoteClose closes a file on the server.</span></span> <span data-ttu-id="635de-127">Обратите внимание, что серверному приложению необходимо назначить **значение NULL** для контекстного контекста как часть функции Close.</span><span class="sxs-lookup"><span data-stu-id="635de-127">Note that the server application has to assign **NULL** to the context handle as part of the close function.</span></span> <span data-ttu-id="635de-128">Это подключается к заглушке сервера и библиотеке времени выполнения RPC, которая была удалена с помощью маркера контекста.</span><span class="sxs-lookup"><span data-stu-id="635de-128">This communicates to the server stub and the RPC run-time library that the context handle has been deleted.</span></span> <span data-ttu-id="635de-129">В противном случае соединение будет оставаться открытым, и в конечном итоге будет выполняться контекст.</span><span class="sxs-lookup"><span data-stu-id="635de-129">Otherwise, the connection will be kept open and eventually a context run-down will occur.</span></span>


```C++
void RemoteClose(PPCONTEXT_HANDLE_TYPE pphContext)
{
    FILE_CONTEXT_TYPE *pFileContext;
 
    if (*pphContext == NULL)
    {
        //Log error, client tried to close a NULL handle.
        return;
    }
    pFileContext = (FILE_CONTEXT_TYPE *)*pphContext;
    printf("File %s closed.\n", pFileContext->achFile);
    fclose(pFileConext->hFile);
    MIDL_user_free(pFileContext);
 
    // This tells the run-time, when it is marshalling the out 
    // parameters, that the context handle has been closed normally.
    *pphContext = NULL;
}
```



> [!Note]  
> <span data-ttu-id="635de-130">Хотя ожидается, что клиент передает допустимый дескриптор контекста в вызов с \[ \] атрибутами направления in, RPC не отклоняет дескрипторы контекста **null** для этого сочетания атрибутов направления.</span><span class="sxs-lookup"><span data-stu-id="635de-130">While it is expected the client passes a valid context handle to a call with \[in, out\] directional attributes, RPC does not reject **NULL** context handles for this combination of directional attributes.</span></span> <span data-ttu-id="635de-131">**Нулевой** маркер контекста передается на сервер в качестве указателя **null** .</span><span class="sxs-lookup"><span data-stu-id="635de-131">The **NULL** context handle is passed to the server as a **NULL** pointer.</span></span> <span data-ttu-id="635de-132">\[ \] Чтобы избежать нарушения прав доступа при получении указателя **null** , необходимо написать серверный код для вызовов, содержащих in, выходной обработчик контекста.</span><span class="sxs-lookup"><span data-stu-id="635de-132">The server code for calls containing an \[in, out\] context handle should be written to avoid an access violation when a **NULL** pointer is received.</span></span>

 

 

 




