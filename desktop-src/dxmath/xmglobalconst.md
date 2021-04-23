---
description: Объявляет объект как выбор любой константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке Директксмас.
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: Макрос КСМГЛОБАЛКОНСТ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711475"
---
# <a name="xmglobalconst-macro"></a><span data-ttu-id="1a6ec-103">Макрос КСМГЛОБАЛКОНСТ</span><span class="sxs-lookup"><span data-stu-id="1a6ec-103">XMGLOBALCONST macro</span></span>

<span data-ttu-id="1a6ec-104">Объявляет объект как *Выбор любой* константы, чтобы избежать избыточных перегрузок этого объекта, если он используется (и объявлен) в нескольких местах в библиотеке директксмас.</span><span class="sxs-lookup"><span data-stu-id="1a6ec-104">Declares an object to be a *pick-any* constant, to avoid redundant reloads of that object if it is used (and declared) in multiple places in the DirectXMath Library.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a6ec-105">Syntax</span></span>

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a><span data-ttu-id="1a6ec-106">Примечания</span><span class="sxs-lookup"><span data-stu-id="1a6ec-106">Remarks</span></span>

<span data-ttu-id="1a6ec-107">Использование КСМГЛОБАЛКОНСТ позволяет использовать спецификацию глобальных констант.</span><span class="sxs-lookup"><span data-stu-id="1a6ec-107">Using XMGLOBALCONST permits the specification of global constants.</span></span> <span data-ttu-id="1a6ec-108">Это позволяет уменьшить размер сегмента данных приложения, избежать создания избыточных объектов и уничтожения, а также сократить операции загрузки и сохранения.</span><span class="sxs-lookup"><span data-stu-id="1a6ec-108">This helps to reduce the size of an application's data segment, avoid redundant object creation and destruction, and reduce load and store operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6ec-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1a6ec-109">Requirements</span></span>

<span data-ttu-id="1a6ec-110">**Заголовок:** Объявлено в Директксмас. h.</span><span class="sxs-lookup"><span data-stu-id="1a6ec-110">**Header:** Declared in DirectXMath.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1a6ec-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1a6ec-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a6ec-112">Макросы библиотеки Директксмас</span><span class="sxs-lookup"><span data-stu-id="1a6ec-112">DirectXMath Library Macros</span></span>](ovw-xnamath-reference-macros.md)
</dt> <dt>

[<span data-ttu-id="1a6ec-113">Глобальные константы в библиотеке Директксмас</span><span class="sxs-lookup"><span data-stu-id="1a6ec-113">Global Constants in the DirectXMath Library</span></span>](pg-xnamath-internals.md)
</dt> <dt>

<span data-ttu-id="1a6ec-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="1a6ec-114">[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))</span></span>
</dt> <dt>

<span data-ttu-id="1a6ec-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="1a6ec-115">[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))</span></span>
</dt> </dl>

 

 
