---
description: В динамической компоновке используются следующие функции.
ms.assetid: 29e50bd5-1712-407f-bcb3-50a0a22ab8b5
title: Функции библиотеки Dynamic-Link
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521c9200b3fa6585ec2804d76ac385845dcd6fb56ef4e7b70a7a3d9bd59150c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070584"
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
| [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                             | Карты указанный исполняемый модуль в адресное пространство вызывающего процесса.                                                                            |
| [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)                         | Карты указанный исполняемый модуль в адресное пространство вызывающего процесса.                                                                            |
| [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)             | Карты указанный упакованный модуль и его зависимости в адресное пространство вызывающего процесса. эту функцию могут вызывать только приложения Windows Store.         |
| [**ремоведллдиректори**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-removedlldirectory)               | Удаляет каталог, добавленный в путь поиска DLL процесса с помощью [**адддллдиректори**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory).                                         |
| [**сетдефаултдллдиректориес**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)   | Указывает набор каталогов по умолчанию для поиска, когда вызывающий процесс загружает библиотеку DLL.                                                                         |
| [**сетдллдиректори**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)                     | Изменяет путь поиска, используемый для поиска библиотек DLL для приложения.                                                                                              |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows.

[**LoadModule**](/windows/desktop/api/Winbase/nf-winbase-loadmodule)

 

 
