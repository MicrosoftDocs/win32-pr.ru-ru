---
title: Создание файлов заглушек
description: После определения интерфейса клиент/сервер обычно разрабатываются исходные файлы клиента и сервера.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Удаленный вызов процедур RPC, задачи, создание файлов заглушек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888304"
---
# <a name="generating-the-stub-files"></a><span data-ttu-id="1eaf5-104">Создание файлов заглушек</span><span class="sxs-lookup"><span data-stu-id="1eaf5-104">Generating the Stub Files</span></span>

<span data-ttu-id="1eaf5-105">После определения интерфейса клиент/сервер обычно разрабатываются исходные файлы клиента и сервера.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="1eaf5-106">Затем используйте отдельный файл makefile для создания файлов заглушек и заголовков.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="1eaf5-107">Скомпилируйте и свяжите клиентские и серверные приложения.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="1eaf5-108">Однако если это первый доступ к среде распределенных вычислений, вы можете вызвать компилятор MIDL, чтобы увидеть, что MIDL создает, прежде чем продолжить.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="1eaf5-109">Компилятор MIDL (Midl.exe) автоматически устанавливается при установке пакета SDK для платформы.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="1eaf5-110">При компиляции этих файлов убедитесь, что Hello. idl и Hello. ACF находятся в одном каталоге.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="1eaf5-111">Следующая команда создаст файл заголовка Hello. h, а также заглушки клиента и сервера, Hello \_ c. c и Hello \_ с.к.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="1eaf5-112">**MIDL Hello. idl**</span><span class="sxs-lookup"><span data-stu-id="1eaf5-112">**midl hello.idl**</span></span>

<span data-ttu-id="1eaf5-113">Обратите внимание, что Hello. h содержит прототипы функций для Хеллопрок и завершения работы, а также опережающие объявления для двух функций управления памятью, пользовательского **\_ \_ выделения MIDL** и выхода **\_ пользователя \_ MIDL**.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="1eaf5-114">Эти две функции будут предоставлены в серверном приложении.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="1eaf5-115">Если данные передаются с сервера клиенту (с помощью \[ параметра **out** \] ), необходимо также предоставить эти две функции управления памятью в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="1eaf5-116">Обратите внимание на определения для переменной глобального обработчика, Hello \_ ифхандле, а также имен обрабатывающих интерфейсов клиента и сервера: Hello \_ v1 \_ 0 \_ c \_ ифспек и Hello \_ v1 \_ 0 \_ s \_ ифспек.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="1eaf5-117">Клиентские и серверные приложения будут использовать имена обработчиков интерфейсов во время выполнения вызовов.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="1eaf5-118">На этом этапе вам не нужно ничего делать с заглушками файлов Hello \_ c. c и Hello \_ с.к.</span><span class="sxs-lookup"><span data-stu-id="1eaf5-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




