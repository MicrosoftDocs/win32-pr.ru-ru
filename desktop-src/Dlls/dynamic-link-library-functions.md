---
description: В динамической компоновке используются следующие функции.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Функции библиотеки Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47ce37b6f91570ce9f3314fc329b5e85cde310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912876"
---
# <a name="dynamic-link-library-functions"></a>Функции библиотеки Dynamic-Link

В динамической компоновке используются следующие функции.



| Функция                                                       | Описание                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**адддллдиректори**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)                     | Добавляет каталог в путь поиска DLL процесса.                                                                                                               |
| [**дисаблесреадлибрарикаллс**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) | Отключает присоединение потоков и уведомления об отсоединении потоков для указанной библиотеки DLL.                                                                                  |
| [**DllMain**](dllmain.md)                                     | Необязательная точка входа в библиотеку DLL.                                                                                                                            |
| [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)                             | Уменьшает значение счетчика ссылок загруженной библиотеки DLL. Когда счетчик ссылок достигает нуля, модуль не сопоставляется с адресным пространством вызывающего процесса. |
| [**фрилибраряндекситсреад**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread)   | Уменьшает значение счетчика ссылок загруженной библиотеки DLL на единицу, а затем вызывает [**ExitThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitthread) для завершения вызывающего потока.                       |
| [**жетдллдиректори**](/windows/desktop/api/WinBase/nf-winbase-getdlldirectorya)                     | Извлекает часть пути поиска, относящуюся к приложению, используемую для поиска библиотек DLL для приложения.                                                         |
| [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)                 | Возвращает полный путь к файлу, содержащему указанный модуль.                                                                               |
| [**жетмодулефиленамикс**](/windows/desktop/api/psapi/nf-psapi-getmodulefilenameexa)            | Возвращает полный путь к файлу, содержащему указанный модуль.                                                                               |
| [**Ошибка GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)                     | Извлекает маркер модуля для указанного модуля.                                                                                                            |
| [**жетмодулехандликс**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandleexa)                 | Извлекает маркер модуля для указанного модуля.                                                                                                            |
| [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)                       | Извлекает адрес экспортированной функции или переменной из указанной библиотеки DLL.                                                                              |
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Сопоставляет указанный исполняемый модуль с адресным пространством вызывающего процесса.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Сопоставляет указанный исполняемый модуль с адресным пространством вызывающего процесса.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Сопоставляет указанный упакованный модуль и его зависимости с адресным пространством вызывающего процесса. Эту функцию могут вызывать только приложения из Магазина Windows.         |
| [**ремоведллдиректори**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Удаляет каталог, добавленный в путь поиска DLL процесса с помощью [**адддллдиректори**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**сетдефаултдллдиректориес**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Указывает набор каталогов по умолчанию для поиска, когда вызывающий процесс загружает библиотеку DLL.                                                                         |
| [**сетдллдиректори**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Изменяет путь поиска, используемый для поиска библиотек DLL для приложения.                                                                                              |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
