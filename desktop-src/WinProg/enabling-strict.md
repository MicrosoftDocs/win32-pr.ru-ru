---
title: Включение параметра
description: При определении символа «символ» вы включаете функции, требующие более тщательного использования при объявлении и использовании типов.
ms.assetid: 4029c7a7-108a-40cb-8600-eb23968e9d8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0400b67025f11dc9c58553f6835b2a8e2b36b4c
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "105703409"
---
# <a name="enabling-strict"></a><span data-ttu-id="0271b-103">Включение параметра</span><span class="sxs-lookup"><span data-stu-id="0271b-103">Enabling STRICT</span></span>

<span data-ttu-id="0271b-104">При **определении символа «символ» вы** включаете функции, требующие более тщательного использования при объявлении и использовании типов.</span><span class="sxs-lookup"><span data-stu-id="0271b-104">When you define the **STRICT** symbol, you enable features that require more care in declaring and using types.</span></span> <span data-ttu-id="0271b-105">Это поможет вам написать более переносимый код.</span><span class="sxs-lookup"><span data-stu-id="0271b-105">This helps you write more portable code.</span></span> <span data-ttu-id="0271b-106">Это также позволит сократить время отладки.</span><span class="sxs-lookup"><span data-stu-id="0271b-106">This extra care will also reduce your debugging time.</span></span> <span data-ttu-id="0271b-107">Включение параметра **строго** переопределяет определенные типы данных, чтобы компилятор не допускать присваивания от одного типа к другому без явного приведения.</span><span class="sxs-lookup"><span data-stu-id="0271b-107">Enabling **STRICT** redefines certain data types so that the compiler does not permit assignment from one type to another without an explicit cast.</span></span> <span data-ttu-id="0271b-108">Это особенно полезно в коде Windows.</span><span class="sxs-lookup"><span data-stu-id="0271b-108">This is especially helpful with Windows code.</span></span> <span data-ttu-id="0271b-109">Ошибки в передачах типов данных выводятся во время компиляции, а не вызывают неустранимые ошибки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="0271b-109">Errors in passing data types are reported at compile time instead of causing fatal errors at run time.</span></span>

<span data-ttu-id="0271b-110">С Visual C++ по умолчанию определена **строгое** проверка типов.</span><span class="sxs-lookup"><span data-stu-id="0271b-110">With Visual C++, **STRICT** type checking is defined by default.</span></span>

<span data-ttu-id="0271b-111">Чтобы определить **значение по** отдельности для каждого файла, вставьте инструкцию **\# define** перед включением Windows. h:</span><span class="sxs-lookup"><span data-stu-id="0271b-111">To define **STRICT** on a file-by-file basis, insert a **\#define** statement before including Windows.h:</span></span>


```C++
#define STRICT
#include <windows.h>
```



<span data-ttu-id="0271b-112">При определении **строгости** определения [типов данных](windows-data-types.md) изменяются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="0271b-112">When **STRICT** is defined, [data type](windows-data-types.md) definitions change as follows:</span></span>

-   <span data-ttu-id="0271b-113">Определенные типы обработчиков определяются как взаимоисключающие. Например, вы не сможете передать **HWND** , где требуется аргумент типа **HDC** .</span><span class="sxs-lookup"><span data-stu-id="0271b-113">Specific handle types are defined to be mutually exclusive; for example, you will not be able to pass an **HWND** where an **HDC** type argument is required.</span></span> <span data-ttu-id="0271b-114">Без **строгости** все дескрипторы определяются как **дескриптор**, поэтому компилятор не препятствует использованию дескриптора одного типа, где ожидается другой тип.</span><span class="sxs-lookup"><span data-stu-id="0271b-114">Without **STRICT**, all handles are defined as **HANDLE**, so the compiler does not prevent you from using one type of handle where another type is expected.</span></span>
-   <span data-ttu-id="0271b-115">Все типы функций обратного вызова (такие как процедуры диалоговых окон, процедуры и процедуры-обработчики) определяются полными прототипами.</span><span class="sxs-lookup"><span data-stu-id="0271b-115">All callback function types (such as dialog procedures, window procedures, and hook procedures) are defined with full prototypes.</span></span> <span data-ttu-id="0271b-116">Это не позволяет объявлять функции обратного вызова с неверными списками параметров.</span><span class="sxs-lookup"><span data-stu-id="0271b-116">This prevents you from declaring callback functions with incorrect parameter lists.</span></span>
-   <span data-ttu-id="0271b-117">Типы параметров и возвращаемых значений, которые должны использовать универсальный указатель, объявляются правильно как **лпвоид** , а не как **LPSTR** или другой тип указателя.</span><span class="sxs-lookup"><span data-stu-id="0271b-117">Parameter and return value types that should use a generic pointer are declared correctly as **LPVOID** instead of as **LPSTR** or another pointer type.</span></span>
-   <span data-ttu-id="0271b-118">Структура [**КОМСТАТ**](/windows/desktop/api/winbase/ns-winbase-comstat) объявляется в соответствии со стандартом ANSI.</span><span class="sxs-lookup"><span data-stu-id="0271b-118">The [**COMSTAT**](/windows/desktop/api/winbase/ns-winbase-comstat) structure is declared according to the ANSI standard.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0271b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="0271b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0271b-120">Отключение</span><span class="sxs-lookup"><span data-stu-id="0271b-120">Disabling STRICT</span></span>](disabling-strict.md)
</dt> <dt>

[<span data-ttu-id="0271b-121">ЖЕСТКОЕ соответствие</span><span class="sxs-lookup"><span data-stu-id="0271b-121">STRICT Compliance</span></span>](strict-compliance.md)
</dt> </dl>

 

 
