---
description: Использование базовых классов DirectShow
ms.assetid: 7eab0e55-1566-4b4c-b37c-32c5a1f37363
title: Использование базовых классов DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 870c910505d6df42d0b9a6094470bf803b83d6b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265262"
---
# <a name="using-the-directshow-base-classes"></a><span data-ttu-id="2293a-103">Использование базовых классов DirectShow</span><span class="sxs-lookup"><span data-stu-id="2293a-103">Using the DirectShow Base Classes</span></span>

<span data-ttu-id="2293a-104">Чтобы использовать базовые классы в DirectShow, необходимо создать и связать библиотеку базовых классов.</span><span class="sxs-lookup"><span data-stu-id="2293a-104">To use the base classes in DirectShow, you must build and link the base class library.</span></span>

<span data-ttu-id="2293a-105">Библиотека базовых классов предоставляется как образец пакета SDK в пакете средств разработки программного обеспечения (SDK) для Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="2293a-105">The base class library is provided as a SDK sample in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span> <span data-ttu-id="2293a-106">Точное расположение зависит от версии установленного пакета SDK, но относительный путь:</span><span class="sxs-lookup"><span data-stu-id="2293a-106">The exact location depends on the version of the SDK that you have installed, but the relative path is:</span></span>

<span data-ttu-id="2293a-107">*(Корень примеров пакета SDK)* \\ \\Басеклассес DirectShow</span><span class="sxs-lookup"><span data-stu-id="2293a-107">*(SDK samples root)*\\DirectShow\\BaseClasses</span></span>

<span data-ttu-id="2293a-108">Заголовок: Streams. h</span><span class="sxs-lookup"><span data-stu-id="2293a-108">Header: Streams.h</span></span>

<span data-ttu-id="2293a-109">Библиотека. Пример сборки розничной и отладочной версий библиотеки:</span><span class="sxs-lookup"><span data-stu-id="2293a-109">Library: The sample builds retail and debug versions of the library:</span></span>

-   <span data-ttu-id="2293a-110">Розничная версия: Стрмбасе. lib</span><span class="sxs-lookup"><span data-stu-id="2293a-110">Retail version: Strmbase.lib</span></span>
-   <span data-ttu-id="2293a-111">Отладочная версия: Стрмбасд. lib.</span><span class="sxs-lookup"><span data-stu-id="2293a-111">Debug version: Strmbasd.lib.</span></span>

<span data-ttu-id="2293a-112">Дополнительные сведения о настройке среды сборки см. в разделе [Настройка среды сборки](setting-up-the-build-environment.md).</span><span class="sxs-lookup"><span data-stu-id="2293a-112">For more information on setting up your build environment, see [Setting Up the Build Environment](setting-up-the-build-environment.md).</span></span>

## <a name="preprocessor-symbols"></a><span data-ttu-id="2293a-113">Символы препроцессора</span><span class="sxs-lookup"><span data-stu-id="2293a-113">Preprocessor Symbols</span></span>

<span data-ttu-id="2293a-114">При включении файла заголовка Streams. h следующие символы препроцессора имеют особое значение:</span><span class="sxs-lookup"><span data-stu-id="2293a-114">When you include the header file Streams.h, the following preprocessor symbols have special meaning:</span></span>

-   <span data-ttu-id="2293a-115">PERF: reserved.</span><span class="sxs-lookup"><span data-stu-id="2293a-115">PERF: Reserved.</span></span> <span data-ttu-id="2293a-116">Не используйте этот символ препроцессора.</span><span class="sxs-lookup"><span data-stu-id="2293a-116">Do not use this preprocessor symbol.</span></span>
-   <span data-ttu-id="2293a-117">ВФВРОБУСТ: включает проверку указателя в розницу.</span><span class="sxs-lookup"><span data-stu-id="2293a-117">VFWROBUST: Enables pointer validation in retail.</span></span> <span data-ttu-id="2293a-118">Дополнительные сведения см. в разделе [макросы проверки указателя](pointer-validation-macros.md).</span><span class="sxs-lookup"><span data-stu-id="2293a-118">For more information, see [Pointer Validation Macros](pointer-validation-macros.md).</span></span> <span data-ttu-id="2293a-119">В отладочных сборках необязательно определять ВФВРОБУСТ.</span><span class="sxs-lookup"><span data-stu-id="2293a-119">In debug builds, it is not necessary to define VFWROBUST.</span></span>

> [!Note]  
> <span data-ttu-id="2293a-120">В Windows Vista и более поздних версиях макросы проверки указателя пусты.</span><span class="sxs-lookup"><span data-stu-id="2293a-120">In Windows Vista and later, the pointer validation macros are empty.</span></span>

 

 

 



