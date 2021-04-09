---
title: Распределитель памяти OLE
description: Распределитель памяти OLE
ms.assetid: 026c62e5-c296-4059-b028-77c98fdb77ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64fedd610fd8fd6dab0bcd14deb37e04f6df74d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134631"
---
# <a name="the-ole-memory-allocator"></a><span data-ttu-id="4bf8c-103">Распределитель памяти OLE</span><span class="sxs-lookup"><span data-stu-id="4bf8c-103">The OLE Memory Allocator</span></span>

<span data-ttu-id="4bf8c-104">Библиотека COM предоставляет реализацию механизма выделения памяти, который является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="4bf8c-104">The COM library provides an implementation of a memory allocator that is thread-safe.</span></span> <span data-ttu-id="4bf8c-105">(То есть это не может вызвать проблемы в многопоточных ситуациях.) Всякий раз, когда владение выделенным блоком памяти передается через COM-интерфейс или между клиентом и библиотекой COM, необходимо использовать этот распределитель COM для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="4bf8c-105">(That is, it cannot cause problems in multithreaded situations.) Whenever ownership of an allocated chunk of memory is passed through a COM interface or between a client and the COM library, you must use this COM allocator to allocate the memory.</span></span> <span data-ttu-id="4bf8c-106">Внутреннее выделение объекта может использовать любую схему распределения, но распределитель памяти COM — это удобный, эффективный и потокобезопасный распределитель.</span><span class="sxs-lookup"><span data-stu-id="4bf8c-106">Allocation internal to an object can use any allocation scheme desired, but the COM memory allocator is a handy, efficient, and thread-safe allocator.</span></span>

<span data-ttu-id="4bf8c-107">Вызов функции API [**кожетмаллок**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) предоставляет указатель на распределитель OLE, который является реализацией [**интерфейса выделения**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) .</span><span class="sxs-lookup"><span data-stu-id="4bf8c-107">A call to the API function [**CoGetMalloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc) provides a pointer to the OLE allocator, which is an implementation of the [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc) interface.</span></span> <span data-ttu-id="4bf8c-108">Однако более эффективно вызывать вспомогательные функции [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**котаскмемреаллок**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc)и [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), которые заключают указатель на распределитель памяти задачи, вызывая **соответствующий метод выделения** , а затем освобождая указатель на распределитель.</span><span class="sxs-lookup"><span data-stu-id="4bf8c-108">However, it is more efficient to call the helper functions [**CoTaskMemAlloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc), [**CoTaskMemRealloc**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemrealloc), and [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree), which wrap getting a pointer to the task memory allocator, calling the corresponding **IMalloc** method, and then releasing the pointer to the allocator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4bf8c-109">См. также</span><span class="sxs-lookup"><span data-stu-id="4bf8c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4bf8c-110">Управление выделением памяти</span><span class="sxs-lookup"><span data-stu-id="4bf8c-110">Managing Memory Allocation</span></span>](managing-memory-allocation.md)
</dt> <dt>

[<span data-ttu-id="4bf8c-111">Библиотека COM</span><span class="sxs-lookup"><span data-stu-id="4bf8c-111">The COM Library</span></span>](the-com-library.md)
</dt> </dl>

 

 