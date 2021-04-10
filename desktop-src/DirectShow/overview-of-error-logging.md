---
description: Общие сведения о ведении журнала ошибок
ms.assetid: 1037f354-0415-4a5c-a96c-20ae714981af
title: Общие сведения о ведении журнала ошибок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4af82c35cdb34a238e280641015407c7a5d6f837
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139898"
---
# <a name="overview-of-error-logging"></a><span data-ttu-id="54ba5-103">Общие сведения о ведении журнала ошибок</span><span class="sxs-lookup"><span data-stu-id="54ba5-103">Overview of Error Logging</span></span>

<span data-ttu-id="54ba5-104">\[Этот API не поддерживается и может быть изменен или недоступен в будущем.\]</span><span class="sxs-lookup"><span data-stu-id="54ba5-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="54ba5-105">Чтобы предоставить приложениям максимальную гибкость при обработке ошибок, [службы редактирования DirectShow](directshow-editing-services.md) используют механизм обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="54ba5-105">To give applications maximum flexibility in handling errors, [DirectShow Editing Services](directshow-editing-services.md) uses a callback mechanism.</span></span> <span data-ttu-id="54ba5-106">Приложение реализует метод для регистрации ошибки.</span><span class="sxs-lookup"><span data-stu-id="54ba5-106">Your application implements a method for logging an error.</span></span> <span data-ttu-id="54ba5-107">Во время выполнения, если возникает ошибка, DES вызывает предоставленный метод.</span><span class="sxs-lookup"><span data-stu-id="54ba5-107">At run time, if an error occurs, DES calls the method you have provided.</span></span> <span data-ttu-id="54ba5-108">Метод принимает параметры, описывающие ошибку.</span><span class="sxs-lookup"><span data-stu-id="54ba5-108">The method takes parameters that describe the error.</span></span> <span data-ttu-id="54ba5-109">Действия метода с этими сведениями помогут вам.</span><span class="sxs-lookup"><span data-stu-id="54ba5-109">What the method does with this information is up to you.</span></span> <span data-ttu-id="54ba5-110">(Он должен возвращать как можно быстрее, или же может мешать выполнению программы.)</span><span class="sxs-lookup"><span data-stu-id="54ba5-110">(It should return as quickly as possible, however, or it might interfere with the execution of the program.)</span></span>

<span data-ttu-id="54ba5-111">Метод обратного вызова регистрации ошибок содержится в COM-интерфейсе [**иамеррорлог**](iamerrorlog.md).</span><span class="sxs-lookup"><span data-stu-id="54ba5-111">The error logging callback method is contained in a COM interface, [**IAMErrorLog**](iamerrorlog.md).</span></span> <span data-ttu-id="54ba5-112">Приложение должно реализовать этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="54ba5-112">Your application must implement this interface.</span></span> <span data-ttu-id="54ba5-113">Как и все COM-интерфейсы, **иамеррорлог** наследует интерфейс **IUnknown** , поэтому приложение также должно его реализовать.</span><span class="sxs-lookup"><span data-stu-id="54ba5-113">Like all COM interfaces, **IAMErrorLog** inherits the **IUnknown** interface, so your application must implement that as well.</span></span>

<span data-ttu-id="54ba5-114">Существует несколько способов реализации этих COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="54ba5-114">You have several choices for implementing these COM interfaces.</span></span> <span data-ttu-id="54ba5-115">Можно использовать библиотеку активных шаблонов (ATL), которая предоставляет стандартные реализации методов **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="54ba5-115">You can use the Active Template Library (ATL), which provides stock implementations of the **IUnknown** methods.</span></span> <span data-ttu-id="54ba5-116">DirectShow также предоставляет базовый класс C++ [**кункновн**](cunknown.md), который упрощает реализацию COM-интерфейса.</span><span class="sxs-lookup"><span data-stu-id="54ba5-116">DirectShow also provides a C++ base class, [**CUnknown**](cunknown.md), that makes it easy to implement a COM interface.</span></span> <span data-ttu-id="54ba5-117">Сведения об использовании **кункновн** см. [в разделе Реализация IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="54ba5-117">For information on using **CUnknown**, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>

<span data-ttu-id="54ba5-118">Пример кода в этой статье определяет автономный класс C++, который реализует **IUnknown** и **иамеррорлог**.</span><span class="sxs-lookup"><span data-stu-id="54ba5-118">The sample code in this article defines a self-contained C++ class, which implements both **IUnknown** and **IAMErrorLog**.</span></span> <span data-ttu-id="54ba5-119">Результат не является истинным COM-объектом, так как он не поддерживает **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="54ba5-119">The result is not a true COM object, because it does not support **CoCreateInstance**.</span></span> <span data-ttu-id="54ba5-120">Однако этот подход достаточно для целей примера.</span><span class="sxs-lookup"><span data-stu-id="54ba5-120">However, this approach is adequate for the purpose of the example.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54ba5-121">См. также</span><span class="sxs-lookup"><span data-stu-id="54ba5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54ba5-122">Регистрация ошибок</span><span class="sxs-lookup"><span data-stu-id="54ba5-122">Logging Errors</span></span>](logging-errors.md)
</dt> </dl>

 

 



