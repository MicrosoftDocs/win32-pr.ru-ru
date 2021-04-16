---
description: Когда приложение вызывает функции LoadLibrary или LoadLibraryEx, система пытается найти библиотеку DLL (Дополнительные сведения см. в разделе порядок поиска в библиотеке Dynamic-Link).
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Run-Time динамическая компоновка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662613"
---
# <a name="run-time-dynamic-linking"></a>Run-Time динамическая компоновка

Когда приложение вызывает функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , система пытается найти библиотеку DLL (Дополнительные сведения см. в статье [Порядок поиска библиотек динамической компоновки](dynamic-link-library-search-order.md)). Если поиск выполняется, система сопоставляет модуль DLL с виртуальным адресным пространством процесса и увеличивает значение счетчика ссылок. Если при вызове **LoadLibrary** или **LoadLibraryEx** указана библиотека DLL, код которой уже сопоставлен с виртуальным адресным пространством вызывающего процесса, функция просто возвращает маркер в библиотеку DLL и увеличивает счетчик ссылок DLL. Обратите внимание, что две библиотеки DLL с одинаковыми базовыми именами и расширениями файлов, но находятся в разных каталогах, не считаются одной и той же библиотекой DLL.

Система вызывает функцию точки входа в контексте потока, который вызвал [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Функция точки входа не вызывается, если библиотека DLL уже была загружена процессом посредством вызова **LoadLibrary** или **LoadLibraryEx** без соответствующего вызова функции [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

Если системе не удается найти библиотеку DLL или если функция точки входа возвращает значение FALSE, то [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) возвращает значение null. Если **LoadLibrary** или **LoadLibraryEx** завершается, возвращается маркер модуля DLL. Процесс может использовать этот обработчик для обнаружения библиотеки DLL при вызове функции [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)или [**фрилибраряндекситсреад**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) .

Функция [**Ошибка GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) возвращает маркер, используемый в [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)или [**фрилибраряндекситсреад**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Функция **Ошибка GetModuleHandle** выполняется, только если модуль DLL уже сопоставлен с адресным пространством процесса путем компоновки во время загрузки или путем предыдущего вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). В отличие от **LoadLibrary** или **LoadLibraryEx**, **Ошибка GetModuleHandle** не увеличивает счетчик ссылок на модуль. Функция [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) извлекает полный путь к модулю, связанному с маркером, возвращаемым **Ошибка GetModuleHandle**, **LoadLibrary** или **LoadLibraryEx**.

Процесс может использовать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для получения адреса экспортированной функции в библиотеке DLL с помощью обработчика модуля DLL, возвращаемого [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**Ошибка GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

Если модуль DLL больше не нужен, процесс может вызвать [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) или [**фрилибраряндекситсреад**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Эти функции уменьшают число ссылок на модули и отменяют сопоставление кода DLL из виртуального адресного пространства процесса, если число ссылок равно нулю.

Динамическая компоновка среды выполнения позволяет продолжить выполнение процесса, даже если библиотека DLL недоступна. Затем процесс может использовать альтернативный метод для выполнения своей цели. Например, если процессу не удается разместить одну библиотеку DLL, он может попытаться использовать другой или уведомить пользователя об ошибке. Если пользователь может предоставить полный путь к отсутствующей библиотеке DLL, процесс может использовать эти сведения для загрузки библиотеки DLL, несмотря на то, что она не находится в нормальном пути поиска. Эта ситуация отличается от связывания во время загрузки, при которой система просто завершает процесс, если не удается найти библиотеку DLL.

Динамическая компоновка во время выполнения может вызвать проблемы, если библиотека DLL использует функцию [**DllMain**](dllmain.md) для выполнения инициализации каждого потока процесса, так как точка входа не вызывается для потоков, существовавших до вызова [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) или [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Пример решения этой проблемы см. [в разделе Использование локального хранилища потока в библиотеке Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование динамической компоновки во время выполнения](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
