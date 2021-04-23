---
description: Создание фильтров DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: Создание фильтров DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7090eed702b1abe8ee863d5fa3ac9c1fd413690e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908622"
---
# <a name="building-directshow-filters"></a>Создание фильтров DirectShow

Базовые классы DirectShow рекомендуются для реализации фильтров DirectShow. Чтобы выполнить сборку с базовыми классами, выполните следующие действия в дополнение к шагам, перечисленным в разделе [Настройка среды сборки](setting-up-the-build-environment.md):

-   Создайте библиотеку базовых классов, расположенную в каталоге Samples \\ мультимедиа \\ DirectShow \\ басеклассес, в КОРНЕВОМ каталоге пакета SDK. Существует две версии библиотеки: розничная версия (Стрмбасе. lib) и отладочная версия (Стрмбасд. lib).
-   Включите файл заголовка Streams. h.
-   Используйте \_ \_ соглашение о вызовах STDCALL.
-   Используйте многопоточность библиотеки времени выполнения C (Debug или Retail, если это необходимо).
-   Включите файл определения (DEF), который экспортирует функции DLL. Ниже приведен пример файла определения. Предполагается, что выходной файл называется MyFilter.dll.
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   Ссылка на следующие lib файлы.

| Метка | Значение |
    |--------------|--------------------------------------|
    | Отладочная сборка  | Стрмбасд. lib, MSVCRTD. lib, winmm. lib |
    | Розничная Сборка | Стрмбасе. lib, msvcrt. lib, winmm. lib  |

    

     

-   Выберите параметр "игнорировать библиотеки по умолчанию" в параметрах компоновщика.
-   Объявите точку входа DLL в исходном коде следующим образом:
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

Предыдущие версии

Для версий библиотеки базовых классов, предшествующих DirectShow 9,0, необходимо также выполнить следующие действия.

-   Для отладочных сборок определите ОТЛАДКу флага препроцессора.

Этот шаг не является обязательным для версии библиотеки базовых классов, доступной в DirectShow 9,0 и более поздних версиях.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Базовые классы DirectShow](directshow-base-classes.md)
</dt> <dt>

[Написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



