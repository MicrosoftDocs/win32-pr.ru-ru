---
title: Преобразование в C++ из Visual Basic
description: Visual Basic обрабатывает указатели неявно. В C++ приложение отвечает за выполнение всех необходимых арифметических операций с указателями.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253231"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="9d376-104">Преобразование в C++ из Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9d376-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="9d376-105">Visual Basic обрабатывает указатели неявно.</span><span class="sxs-lookup"><span data-stu-id="9d376-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="9d376-106">В C++ приложение отвечает за выполнение всех необходимых арифметических операций с указателями.</span><span class="sxs-lookup"><span data-stu-id="9d376-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="9d376-107">По умолчанию Visual Basic передает параметры по ссылке (в виде указателей).</span><span class="sxs-lookup"><span data-stu-id="9d376-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="9d376-108">Параметры, которые должны передаваться только по значению, задаются с помощью ключевого слова **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="9d376-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="9d376-109">Например, параметр **ByVal** в  **целочисленном** Visual Basic эквивалентен **короткому** параметру в C++, тогда как параметр **ByRef** в  **целочисленной** Visual Basic эквивалентен **короткому \*** параметру.</span><span class="sxs-lookup"><span data-stu-id="9d376-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="9d376-110">Параметр, объявленный **как String** в Visual Basic, объявляется как указатель на **BSTR** в C++.</span><span class="sxs-lookup"><span data-stu-id="9d376-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="9d376-111">Установка указателя строки на **null** в C++ эквивалентна установке строки константы **вбнуллстринг** в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="9d376-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="9d376-112">Передача строки нулевой длины ("") в функцию, предназначенную для получения **значения NULL** , не работает, так как она передает указатель на строку нулевой длины вместо нулевого указателя.</span><span class="sxs-lookup"><span data-stu-id="9d376-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="9d376-113">C++ и Visual Basic немного отличаются в том, как они представляют свойства.</span><span class="sxs-lookup"><span data-stu-id="9d376-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="9d376-114">В C++ свойства представлены в виде набора функций доступа, который задает значение свойства и одно из них, которое получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="9d376-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="9d376-115">В Visual Basic свойства представлены как один элемент, который можно использовать для получения или задания значения свойства.</span><span class="sxs-lookup"><span data-stu-id="9d376-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d376-116">См. также</span><span class="sxs-lookup"><span data-stu-id="9d376-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d376-117">Преобразование в C++</span><span class="sxs-lookup"><span data-stu-id="9d376-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




