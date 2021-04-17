---
description: саферелеасе
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: саферелеасе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711406"
---
# <a name="saferelease"></a><span data-ttu-id="691f4-103">саферелеасе</span><span class="sxs-lookup"><span data-stu-id="691f4-103">SafeRelease</span></span>


<span data-ttu-id="691f4-104">Во многих примерах кода в этой документации для освобождения указателей COM-интерфейса используется следующая функция.</span><span class="sxs-lookup"><span data-stu-id="691f4-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="691f4-105">Эта функция не определена в заголовке пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="691f4-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="691f4-106">Чтобы использовать эту функцию, необходимо определить ее в собственном коде.</span><span class="sxs-lookup"><span data-stu-id="691f4-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="691f4-107">Эта функция освобождает указатель *PPT* и устанавливает его равным **null**.</span><span class="sxs-lookup"><span data-stu-id="691f4-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="691f4-108">Другим вариантом является использование класса интеллектуального указателя, такого как **CComPtr**, который определен в библиотеке активных шаблонов (ATL).</span><span class="sxs-lookup"><span data-stu-id="691f4-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="691f4-109">См. также</span><span class="sxs-lookup"><span data-stu-id="691f4-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="691f4-110">О Media Foundation</span><span class="sxs-lookup"><span data-stu-id="691f4-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="691f4-111">**IUnknown:: Release**</span><span class="sxs-lookup"><span data-stu-id="691f4-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
