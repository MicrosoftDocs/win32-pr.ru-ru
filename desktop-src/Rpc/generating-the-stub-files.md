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
# <a name="generating-the-stub-files"></a>Создание файлов заглушек

После определения интерфейса клиент/сервер обычно разрабатываются исходные файлы клиента и сервера. Затем используйте отдельный файл makefile для создания файлов заглушек и заголовков. Скомпилируйте и свяжите клиентские и серверные приложения. Однако если это первый доступ к среде распределенных вычислений, вы можете вызвать компилятор MIDL, чтобы увидеть, что MIDL создает, прежде чем продолжить. Компилятор MIDL (Midl.exe) автоматически устанавливается при установке пакета SDK для платформы.

При компиляции этих файлов убедитесь, что Hello. idl и Hello. ACF находятся в одном каталоге. Следующая команда создаст файл заголовка Hello. h, а также заглушки клиента и сервера, Hello \_ c. c и Hello \_ с.к.

**MIDL Hello. idl**

Обратите внимание, что Hello. h содержит прототипы функций для Хеллопрок и завершения работы, а также опережающие объявления для двух функций управления памятью, пользовательского **\_ \_ выделения MIDL** и выхода **\_ пользователя \_ MIDL**. Эти две функции будут предоставлены в серверном приложении. Если данные передаются с сервера клиенту (с помощью \[ параметра **out** \] ), необходимо также предоставить эти две функции управления памятью в клиентском приложении.

Обратите внимание на определения для переменной глобального обработчика, Hello \_ ифхандле, а также имен обрабатывающих интерфейсов клиента и сервера: Hello \_ v1 \_ 0 \_ c \_ ифспек и Hello \_ v1 \_ 0 \_ s \_ ифспек. Клиентские и серверные приложения будут использовать имена обработчиков интерфейсов во время выполнения вызовов.

На этом этапе вам не нужно ничего делать с заглушками файлов Hello \_ c. c и Hello \_ с.к.

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

 

 




