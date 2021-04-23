---
description: В следующей таблице содержатся коды возврата из функций API.
ms.assetid: 7b67d428-d000-4c3e-adc1-b5fc67a15a6a
title: Коды возврата Direct3D 10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15a2fcdc4db5bd2d295b7cd3078ed80d401ce52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682340"
---
# <a name="direct3d-10-return-codes"></a><span data-ttu-id="bdcc8-103">Коды возврата Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="bdcc8-103">Direct3D 10 Return Codes</span></span>

<span data-ttu-id="bdcc8-104">В следующей таблице содержатся коды возврата из функций API.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-104">The following table contains return codes from API functions.</span></span>



| <span data-ttu-id="bdcc8-105">HRESULT</span><span class="sxs-lookup"><span data-stu-id="bdcc8-105">HRESULT</span></span>                                         | <span data-ttu-id="bdcc8-106">Описание</span><span class="sxs-lookup"><span data-stu-id="bdcc8-106">Description</span></span>                                                                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdcc8-107">\_Файл ошибок \_ D3D10 \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="bdcc8-107">D3D10\_ERROR\_FILE\_NOT\_FOUND</span></span>                  | <span data-ttu-id="bdcc8-108">Файл не найден.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-108">The file was not found.</span></span>                                                                                                                               |
| <span data-ttu-id="bdcc8-109">Ошибка D3D10. \_ \_ слишком \_ много \_ уникальных \_ \_ объектов состояния</span><span class="sxs-lookup"><span data-stu-id="bdcc8-109">D3D10\_ERROR\_TOO\_MANY\_UNIQUE\_STATE\_OBJECTS</span></span> | <span data-ttu-id="bdcc8-110">Слишком много уникальных экземпляров определенного типа [объекта состояния](d3d10-graphics-programming-guide-api-features-state-objects.md).</span><span class="sxs-lookup"><span data-stu-id="bdcc8-110">There are too many unique instances of a particular type of [state object](d3d10-graphics-programming-guide-api-features-state-objects.md).</span></span>          |
| <span data-ttu-id="bdcc8-111">D3DERR \_ инвалидкалл</span><span class="sxs-lookup"><span data-stu-id="bdcc8-111">D3DERR\_INVALIDCALL</span></span>                             | <span data-ttu-id="bdcc8-112">Недопустимый вызов метода.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-112">The method call is invalid.</span></span> <span data-ttu-id="bdcc8-113">Например, параметр метода не может быть допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-113">For example, a method's parameter may not be a valid pointer.</span></span>                                                             |
| <span data-ttu-id="bdcc8-114">D3DERR \_ васстиллдравинг</span><span class="sxs-lookup"><span data-stu-id="bdcc8-114">D3DERR\_WASSTILLDRAWING</span></span>                         | <span data-ttu-id="bdcc8-115">Предыдущая операция Блит, которая передает информацию в эту область или из нее, является неполной.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-115">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                                                   |
| <span data-ttu-id="bdcc8-116">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="bdcc8-116">E\_FAIL</span></span>                                         | <span data-ttu-id="bdcc8-117">Попытка создать устройство с включенным [уровнем отладки](d3d10-graphics-programming-guide-api-features-layers.md) , и этот слой не установлен.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-117">Attempted to create a device with the [debug layer](d3d10-graphics-programming-guide-api-features-layers.md) enabled and the layer is not installed.</span></span> |
| <span data-ttu-id="bdcc8-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="bdcc8-118">E\_INVALIDARG</span></span>                                   | <span data-ttu-id="bdcc8-119">Функции, возвращающей, передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-119">An invalid parameter was passed to the returning function.</span></span>                                                                                            |
| <span data-ttu-id="bdcc8-120">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="bdcc8-120">E\_OUTOFMEMORY</span></span>                                  | <span data-ttu-id="bdcc8-121">Direct3D не удалось выделить достаточно памяти для завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-121">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                                                   |
| <span data-ttu-id="bdcc8-122">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="bdcc8-122">E\_NOTIMPL</span></span>                                      | <span data-ttu-id="bdcc8-123">Вызов метода не реализован с переданным сочетанием параметров.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-123">The method call isn't implemented with the passed parameter combination.</span></span>                                                                              |
| <span data-ttu-id="bdcc8-124">S \_ false</span><span class="sxs-lookup"><span data-stu-id="bdcc8-124">S\_FALSE</span></span>                                        | <span data-ttu-id="bdcc8-125">Альтернативное значение успеха, указывающее на успешное, но нестандартное завершение (точное значение зависит от контекста).</span><span class="sxs-lookup"><span data-stu-id="bdcc8-125">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span>                                 |
| <span data-ttu-id="bdcc8-126">\_ОК</span><span class="sxs-lookup"><span data-stu-id="bdcc8-126">S\_OK</span></span>                                           | <span data-ttu-id="bdcc8-127">Без ошибок.</span><span class="sxs-lookup"><span data-stu-id="bdcc8-127">No error occurred.</span></span>                                                                                                                                    |



 

<span data-ttu-id="bdcc8-128">Чтобы создать код, который обеспечивает надежную обработку [значений HRESULT](../winprog/windows-data-types.md) , используйте макросы успешно (HR) и Failed (HR).</span><span class="sxs-lookup"><span data-stu-id="bdcc8-128">To write code that handles [HRESULT values](../winprog/windows-data-types.md) robustly, use the SUCCEEDED(hr) and FAILED(hr) macros.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdcc8-129">См. также</span><span class="sxs-lookup"><span data-stu-id="bdcc8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdcc8-130">Справочник по Direct3D</span><span class="sxs-lookup"><span data-stu-id="bdcc8-130">Direct3D Reference</span></span>](d3d10-graphics-reference-d3d10.md)
</dt> <dt>

[<span data-ttu-id="bdcc8-131">Справочник по Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="bdcc8-131">Reference for Direct3D 10</span></span>](d3d10-graphics-reference.md)
</dt> </dl>

 

 
