---
title: Коды возврата Direct3D 12
description: Ниже приведены коды возврата из функций API.
ms.assetid: 5F6CC962-7DB7-489F-82A4-9388313014D3
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd04c0c7702f00f1338ce884adc745522390c8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105700919"
---
# <a name="direct3d-12-return-codes"></a><span data-ttu-id="7ed4d-103">Коды возврата Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7ed4d-103">Direct3D 12 Return Codes</span></span>

<span data-ttu-id="7ed4d-104">Ниже приведены коды возврата из функций API.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-104">The following are return codes from API functions.</span></span> <span data-ttu-id="7ed4d-105">Дополнительные коды возврата см. в [разделе \_ Ошибка DXGI](/windows/desktop/direct3ddxgi/dxgi-error).</span><span class="sxs-lookup"><span data-stu-id="7ed4d-105">For more return codes, see [DXGI\_ERROR](/windows/desktop/direct3ddxgi/dxgi-error).</span></span>



| <span data-ttu-id="7ed4d-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="7ed4d-106">HRESULT</span></span>                                                                  | <span data-ttu-id="7ed4d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7ed4d-107">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ed4d-108">\_Адаптер ошибок \_ D3D12 \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="7ed4d-108">D3D12\_ERROR\_ADAPTER\_NOT\_FOUND</span></span>                                        | <span data-ttu-id="7ed4d-109">Указанный кэшированный PSO был создан на другом адаптере и не может быть использован повторно на текущем адаптере.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-109">The specified cached PSO was created on a different adapter and cannot be reused on the current adapter.</span></span>          |
| <span data-ttu-id="7ed4d-110">\_Несоответствие \_ версии драйвера ошибки \_ D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="7ed4d-110">D3D12\_ERROR\_DRIVER\_VERSION\_MISMATCH</span></span>                                  | <span data-ttu-id="7ed4d-111">Указанный кэшированный PSO был создан в другой версии драйвера и не может быть использован повторно на текущем адаптере.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-111">The specified cached PSO was created on a different driver version and cannot be reused on the current adapter.</span></span>  |
| <span data-ttu-id="7ed4d-112">D3DERR \_ инвалидкалл (заменяется \_ \_ недопустимым \_ вызовом ошибки DXGI)</span><span class="sxs-lookup"><span data-stu-id="7ed4d-112">D3DERR\_INVALIDCALL (replaced with DXGI\_ERROR\_INVALID\_CALL)</span></span>           | <span data-ttu-id="7ed4d-113">Недопустимый вызов метода.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-113">The method call is invalid.</span></span> <span data-ttu-id="7ed4d-114">Например, параметр метода не может быть допустимым указателем.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-114">For example, a method's parameter may not be a valid pointer.</span></span>                             |
| <span data-ttu-id="7ed4d-115">D3DERR \_ васстиллдравинг (не удалось выполнить замену с \_ ошибкой DXGI \_ \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="7ed4d-115">D3DERR\_WASSTILLDRAWING (replaced with DXGI\_ERROR\_WAS\_STILL\_DRAWING)</span></span> | <span data-ttu-id="7ed4d-116">Предыдущая операция Блит, которая передает информацию в эту область или из нее, является неполной.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-116">The previous blit operation that is transferring information to or from this surface is incomplete.</span></span>                   |
| <span data-ttu-id="7ed4d-117">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="7ed4d-117">E\_FAIL</span></span>                                                                  | <span data-ttu-id="7ed4d-118">Попытка создать устройство с включенным уровнем отладки, и этот слой не установлен.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-118">Attempted to create a device with the debug layer enabled and the layer is not installed.</span></span>                             |
| <span data-ttu-id="7ed4d-119">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7ed4d-119">E\_INVALIDARG</span></span>                                                            | <span data-ttu-id="7ed4d-120">Функции, возвращающей, передан недопустимый параметр.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-120">An invalid parameter was passed to the returning function.</span></span>                                                             |
| <span data-ttu-id="7ed4d-121">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="7ed4d-121">E\_OUTOFMEMORY</span></span>                                                           | <span data-ttu-id="7ed4d-122">Direct3D не удалось выделить достаточно памяти для завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-122">Direct3D could not allocate sufficient memory to complete the call.</span></span>                                                   |
| <span data-ttu-id="7ed4d-123">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="7ed4d-123">E\_NOTIMPL</span></span>                                                               | <span data-ttu-id="7ed4d-124">Вызов метода не реализован с переданным сочетанием параметров.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-124">The method call isn't implemented with the passed parameter combination.</span></span>                                               |
| <span data-ttu-id="7ed4d-125">S \_ false</span><span class="sxs-lookup"><span data-stu-id="7ed4d-125">S\_FALSE</span></span>                                                                 | <span data-ttu-id="7ed4d-126">Альтернативное значение успеха, указывающее на успешное, но нестандартное завершение (точное значение зависит от контекста).</span><span class="sxs-lookup"><span data-stu-id="7ed4d-126">Alternate success value, indicating a successful but nonstandard completion (the precise meaning depends on context).</span></span> |
| <span data-ttu-id="7ed4d-127">\_ОК</span><span class="sxs-lookup"><span data-stu-id="7ed4d-127">S\_OK</span></span>                                                                    | <span data-ttu-id="7ed4d-128">Без ошибок.</span><span class="sxs-lookup"><span data-stu-id="7ed4d-128">No error occurred.</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="7ed4d-129">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed4d-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed4d-130">Справочник по Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="7ed4d-130">Direct3D 12 Reference</span></span>](direct3d-12-reference.md)
</dt> </dl>

 

 