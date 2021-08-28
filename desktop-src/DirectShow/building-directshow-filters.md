---
description: создание фильтров DirectShow
ms.assetid: fb907263-e7f3-42d6-80f9-a9f16fc21033
title: создание фильтров DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d1983d3bfd42d1a1582ef696b6793acdd0856dde2bd2d589e809acc614314
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794326"
---
# <a name="building-directshow-filters"></a>создание фильтров DirectShow

для реализации фильтров DirectShow рекомендуется использовать DirectShow базовых классов. Чтобы выполнить сборку с базовыми классами, выполните следующие действия в дополнение к шагам, перечисленным в разделе [Настройка среды сборки](setting-up-the-build-environment.md):

-   создайте библиотеку базовых классов, расположенную в каталоге samples \\ мультимедиа \\ DirectShow \\ басеклассес, в корневом каталоге пакета SDK. Существует две версии библиотеки: розничная версия (Стрмбасе. lib) и отладочная версия (Стрмбасд. lib).
-   включите заголовочный файл Потоки. h.
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

для версий библиотеки базовых классов, предшествующих DirectShow 9,0, необходимо также выполнить следующие действия.

-   Для отладочных сборок определите ОТЛАДКу флага препроцессора.

этот шаг не требуется для версии библиотеки базовых классов, доступной в DirectShow 9,0 и более поздних версиях.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[DirectShow Базовые классы](directshow-base-classes.md)
</dt> <dt>

[написание фильтров DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



