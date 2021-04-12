---
title: Назначение заглушек для конкретных 32-разрядных или 64-разрядных платформ
description: Некоторые функции Microsoft RPC и компиляторов MIDL 3,0 и более поздних версий являются специфичными для платформы.
ms.assetid: bb1bee56-7f39-406c-bdbf-b73bda568247
keywords:
- 32-разрядные платформы MIDL
- 64-разрядные платформы MIDL
- заглушки MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526265a60f8b2ef2f31d19d0356d4ec3a3ae8c8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331379"
---
# <a name="targeting-stubs-for-specific-32-bit-or-64-bit-platforms"></a><span data-ttu-id="541ac-106">Назначение заглушек для конкретных 32-разрядных или 64-разрядных платформ</span><span class="sxs-lookup"><span data-stu-id="541ac-106">Targeting Stubs for Specific 32-bit or 64-bit Platforms</span></span>

<span data-ttu-id="541ac-107">Некоторые функции Microsoft RPC и компиляторов MIDL 3,0 и более поздних версий являются специфичными для платформы.</span><span class="sxs-lookup"><span data-stu-id="541ac-107">Some of the features of Microsoft RPC and the MIDL 3.0 and later compilers are platform-specific.</span></span>

<span data-ttu-id="541ac-108">В качестве меры предосторожности компиляторы MIDL 3,0 и более поздних версий создают условия, которые упрощают проверку совместимости на этапе C-compilation.</span><span class="sxs-lookup"><span data-stu-id="541ac-108">As a precaution, the MIDL 3.0 and later compilers generate guards that facilitate compatibility checking during the C-compilation phase.</span></span> <span data-ttu-id="541ac-109">MIDL создает два типа условий: зависимый от платформы (32-разрядный и 64-бит) и зависимый от выпуска предохранитель (зависимость набора функций).</span><span class="sxs-lookup"><span data-stu-id="541ac-109">MIDL generates two types of guards: a platform-dependent guard (32-bit versus 64-bit) and a release-dependent guard (feature set dependency).</span></span> <span data-ttu-id="541ac-110">Например, MIDL создает следующее условие, чтобы предотвратить компиляцию 32-разрядной заглушки для других платформ с помощью C:</span><span class="sxs-lookup"><span data-stu-id="541ac-110">For example, MIDL generates the following guard to prevent C-compiling of a 32-bit stub for other platforms:</span></span>

``` syntax
#if !defined(__RPC_WIN32__)
#error  Invalid build platform for this stub.
#endif
```

<span data-ttu-id="541ac-111">Зависимый от выпуска предохранитель активируется набором компонентов, найденных в обрабатываемых IDL-файлах, и параметром [**/Target**](-target.md) .</span><span class="sxs-lookup"><span data-stu-id="541ac-111">The release-dependent guard is triggered by a set of features found in the processed IDL file(s) and by the [**/target**](-target.md) switch.</span></span> <span data-ttu-id="541ac-112">Например, если интерфейс использует функции, поддерживаемые только в Windows 2000 или более поздней версии, MIDL создает защиту с ЦЕЛЕВЫМ \_ объектом \_ \_ \_ макроса NT50 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="541ac-112">For example, if the interface uses features supported only on WindowsÂ 2000 or later, MIDL generates a guard with the TARGET\_IS\_NT50\_OR\_LATER macro.</span></span>

<span data-ttu-id="541ac-113">Макросы Guard, определенные в Рпкндр. h, зависят от настройки WINVER и \_ Win32 \_ Winnt и оцениваются компилятором C/C++.</span><span class="sxs-lookup"><span data-stu-id="541ac-113">The guard macros, defined in Rpcndr.h, depend on the setting of WINVER and \_WIN32\_WINNT and are evaluated by the C/C++ compiler.</span></span>

<span data-ttu-id="541ac-114">Если во время компиляции на языке C вы получаете сообщение об ошибке, указывающее, что для запуска заглушки требуется определенная платформа, сначала убедитесь, что вы не использовали функцию, недоступную на этой платформе.</span><span class="sxs-lookup"><span data-stu-id="541ac-114">If, at C-compile time, you get an error message indicating that you need a specific platform to run a stub, first check to make sure you have not used a feature that is not available on this platform.</span></span> <span data-ttu-id="541ac-115">Функции, активируемые определенным условием, перечислены в тексте средства защиты.</span><span class="sxs-lookup"><span data-stu-id="541ac-115">The features triggering a particular guard are listed in the body of the guard.</span></span> <span data-ttu-id="541ac-116">В предыдущем примере параметр компилятора-Оикф активировал условие.</span><span class="sxs-lookup"><span data-stu-id="541ac-116">In the previous example, the -Oicf compiler switch triggered the guard.</span></span> <span data-ttu-id="541ac-117">Важные функции такого рода включают параметр [**/robust**](-robust.md) и \[ атрибут [**Async**](async.md) , \] доступный в Windows 2000 и более поздних версиях, конструктор типа [**канала**](pipe.md) , параметр компилятора/OIF, а также атрибуты маршалирования и передачи данных \[ [**пользователя \_**](user-marshal.md) \] \[ [**\_**](wire-marshal.md) \] .</span><span class="sxs-lookup"><span data-stu-id="541ac-117">Notable features of this kind include the [**/robust**](-robust.md) switch and the \[[**async**](async.md)\] attribute available on WindowsÂ 2000 and later, the [**pipe**](pipe.md) type constructor, the /Oif compiler option, and the \[[**user\_marshal**](user-marshal.md)\] and \[[**wire\_marshal**](wire-marshal.md)\] attributes.</span></span> <span data-ttu-id="541ac-118">Заглушки, использующие эти функции, не будут работать в более ранних системах.</span><span class="sxs-lookup"><span data-stu-id="541ac-118">Stubs using these features will not run on earlier systems.</span></span>

<span data-ttu-id="541ac-119">Если вы уверены, что Целевая платформа правильна для используемых Вами функций и по-прежнему получает сообщение об ошибке, может потребоваться задать соответствующие переменные среды.</span><span class="sxs-lookup"><span data-stu-id="541ac-119">If you know that your target platform is correct for the features you are using and still receive an error, you may need to set the environment variables appropriately.</span></span>

<span data-ttu-id="541ac-120">**Сборка для Windows 2000 или более поздних версий**</span><span class="sxs-lookup"><span data-stu-id="541ac-120">**To build for WindowsÂ 2000 or later releases**</span></span>

-   <span data-ttu-id="541ac-121">Добавьте следующую строку в файл Makefile:</span><span class="sxs-lookup"><span data-stu-id="541ac-121">Add this line to your makefile:</span></span>

    ``` syntax
    CFLAGS = $(CFLAGS) -D_WIN32_WINNT=0x500
    ```

## <a name="related-topics"></a><span data-ttu-id="541ac-122">См. также</span><span class="sxs-lookup"><span data-stu-id="541ac-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="541ac-123">**/Target**</span><span class="sxs-lookup"><span data-stu-id="541ac-123">**/target**</span></span>](-target.md)
</dt> <dt>

[<span data-ttu-id="541ac-124">**/robust**</span><span class="sxs-lookup"><span data-stu-id="541ac-124">**/robust**</span></span>](-robust.md)
</dt> <dt>

[<span data-ttu-id="541ac-125">**async**</span><span class="sxs-lookup"><span data-stu-id="541ac-125">**async**</span></span>](async.md)
</dt> <dt>

[<span data-ttu-id="541ac-126">**асинхронный \_ UUID**</span><span class="sxs-lookup"><span data-stu-id="541ac-126">**async\_uuid**</span></span>](async-uuid.md)
</dt> <dt>

[<span data-ttu-id="541ac-127">**/Oi**</span><span class="sxs-lookup"><span data-stu-id="541ac-127">**/Oi**</span></span>](-oi.md)
</dt> <dt>

[<span data-ttu-id="541ac-128">**дать**</span><span class="sxs-lookup"><span data-stu-id="541ac-128">**pipe**</span></span>](pipe.md)
</dt> <dt>

[<span data-ttu-id="541ac-129">**проводное \_ маршалирование**</span><span class="sxs-lookup"><span data-stu-id="541ac-129">**wire\_marshal**</span></span>](wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="541ac-130">**Пользовательская \_ Упаковка**</span><span class="sxs-lookup"><span data-stu-id="541ac-130">**user\_marshal**</span></span>](user-marshal.md)
</dt> <dt>

[<span data-ttu-id="541ac-131">Маршалирование типов данных OLE</span><span class="sxs-lookup"><span data-stu-id="541ac-131">Marshaling OLE Data Types</span></span>](marshaling-ole-data-types.md)
</dt> </dl>

 

 




