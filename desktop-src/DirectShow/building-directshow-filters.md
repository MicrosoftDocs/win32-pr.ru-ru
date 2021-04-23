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
# <a name="building-directshow-filters"></a><span data-ttu-id="a1dee-103">Создание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1dee-103">Building DirectShow Filters</span></span>

<span data-ttu-id="a1dee-104">Базовые классы DirectShow рекомендуются для реализации фильтров DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a1dee-104">The DirectShow base classes are recommended for implementing DirectShow filters.</span></span> <span data-ttu-id="a1dee-105">Чтобы выполнить сборку с базовыми классами, выполните следующие действия в дополнение к шагам, перечисленным в разделе [Настройка среды сборки](setting-up-the-build-environment.md):</span><span class="sxs-lookup"><span data-stu-id="a1dee-105">To build with the base classes, perform the following steps, in addition to the steps listed in [Setting Up the Build Environment](setting-up-the-build-environment.md):</span></span>

-   <span data-ttu-id="a1dee-106">Создайте библиотеку базовых классов, расположенную в каталоге Samples \\ мультимедиа \\ DirectShow \\ басеклассес, в КОРНЕВОМ каталоге пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="a1dee-106">Build the base class library, located in the directory Samples\\Multimedia\\DirectShow\\BaseClasses, under the SDK root directory.</span></span> <span data-ttu-id="a1dee-107">Существует две версии библиотеки: розничная версия (Стрмбасе. lib) и отладочная версия (Стрмбасд. lib).</span><span class="sxs-lookup"><span data-stu-id="a1dee-107">There are two versions of the library: a retail version (Strmbase.lib) and a debug version (Strmbasd.lib).</span></span>
-   <span data-ttu-id="a1dee-108">Включите файл заголовка Streams. h.</span><span class="sxs-lookup"><span data-stu-id="a1dee-108">Include the header file Streams.h.</span></span>
-   <span data-ttu-id="a1dee-109">Используйте \_ \_ соглашение о вызовах STDCALL.</span><span class="sxs-lookup"><span data-stu-id="a1dee-109">Use the \_\_stdcall calling convention.</span></span>
-   <span data-ttu-id="a1dee-110">Используйте многопоточность библиотеки времени выполнения C (Debug или Retail, если это необходимо).</span><span class="sxs-lookup"><span data-stu-id="a1dee-110">Use the multithreaded C run-time library (debug or retail, as appropriate).</span></span>
-   <span data-ttu-id="a1dee-111">Включите файл определения (DEF), который экспортирует функции DLL.</span><span class="sxs-lookup"><span data-stu-id="a1dee-111">Include a definition (.def) file that exports the DLL functions.</span></span> <span data-ttu-id="a1dee-112">Ниже приведен пример файла определения.</span><span class="sxs-lookup"><span data-stu-id="a1dee-112">The following is an example of a definition file.</span></span> <span data-ttu-id="a1dee-113">Предполагается, что выходной файл называется MyFilter.dll.</span><span class="sxs-lookup"><span data-stu-id="a1dee-113">It assumes that the output file is named MyFilter.dll.</span></span>
    ```C++
    LIBRARY MYFILTER.DLL
    EXPORTS 
        DllMain             PRIVATE
        DllGetClassObject   PRIVATE
        DllCanUnloadNow     PRIVATE
        DllRegisterServer   PRIVATE
        DllUnregisterServer PRIVATE
    ```

    

-   <span data-ttu-id="a1dee-114">Ссылка на следующие lib файлы.</span><span class="sxs-lookup"><span data-stu-id="a1dee-114">Link to the following lib files.</span></span>

| <span data-ttu-id="a1dee-115">Метка</span><span class="sxs-lookup"><span data-stu-id="a1dee-115">Label</span></span> | <span data-ttu-id="a1dee-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a1dee-116">Value</span></span> |
    |--------------|--------------------------------------|
    | <span data-ttu-id="a1dee-117">Отладочная сборка</span><span class="sxs-lookup"><span data-stu-id="a1dee-117">Debug Build</span></span>  | <span data-ttu-id="a1dee-118">Стрмбасд. lib, MSVCRTD. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="a1dee-118">Strmbasd.lib, Msvcrtd.lib, Winmm.lib</span></span> |
    | <span data-ttu-id="a1dee-119">Розничная Сборка</span><span class="sxs-lookup"><span data-stu-id="a1dee-119">Retail Build</span></span> | <span data-ttu-id="a1dee-120">Стрмбасе. lib, msvcrt. lib, winmm. lib</span><span class="sxs-lookup"><span data-stu-id="a1dee-120">Strmbase.lib, Msvcrt.lib, Winmm.lib</span></span>  |

    

     

-   <span data-ttu-id="a1dee-121">Выберите параметр "игнорировать библиотеки по умолчанию" в параметрах компоновщика.</span><span class="sxs-lookup"><span data-stu-id="a1dee-121">Choose the "ignore default libraries" option in the linker settings.</span></span>
-   <span data-ttu-id="a1dee-122">Объявите точку входа DLL в исходном коде следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a1dee-122">Declare the DLL entry point in your source code, as follows:</span></span>
    ```C++
    extern "C" BOOL WINAPI DllEntryPoint(HINSTANCE, ULONG, LPVOID);
    BOOL APIENTRY DllMain(HANDLE hModule, DWORD dwReason, LPVOID lpReserved)
    {
        return DllEntryPoint((HINSTANCE)(hModule), dwReason, lpReserved);
    }
    ```

    

<span data-ttu-id="a1dee-123">Предыдущие версии</span><span class="sxs-lookup"><span data-stu-id="a1dee-123">Previous Versions</span></span>

<span data-ttu-id="a1dee-124">Для версий библиотеки базовых классов, предшествующих DirectShow 9,0, необходимо также выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="a1dee-124">For versions of the base class library before DirectShow 9.0, you must also do the following:</span></span>

-   <span data-ttu-id="a1dee-125">Для отладочных сборок определите ОТЛАДКу флага препроцессора.</span><span class="sxs-lookup"><span data-stu-id="a1dee-125">For debug builds, define the preprocessor flag DEBUG.</span></span>

<span data-ttu-id="a1dee-126">Этот шаг не является обязательным для версии библиотеки базовых классов, доступной в DirectShow 9,0 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="a1dee-126">This step is not required for the version of the base class library that is available in DirectShow 9.0 and later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1dee-127">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="a1dee-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1dee-128">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1dee-128">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="a1dee-129">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1dee-129">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



