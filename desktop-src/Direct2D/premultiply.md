---
title: Преумножить результат
description: Используйте этот результат для преобразования изображения из унпремултиплиед Alpha в предварительно умноженный альфа-канал.
ms.assetid: 8A5F55C6-3AC7-48B4-87D8-C19D8B4EA0DD
keywords:
- преумножить результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a01a8a9ba005ed688a96254856897b3514f05fd5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988971"
---
# <a name="premultiply-effect"></a><span data-ttu-id="277ce-104">Преумножить результат</span><span class="sxs-lookup"><span data-stu-id="277ce-104">Premultiply effect</span></span>

<span data-ttu-id="277ce-105">Используйте этот результат для преобразования изображения из унпремултиплиед Alpha в предварительно умноженный альфа-канал.</span><span class="sxs-lookup"><span data-stu-id="277ce-105">Use this effect to convert an image from unpremultiplied alpha to premultiplied alpha.</span></span> <span data-ttu-id="277ce-106">Этот результат заменяет каждый входной пиксель `P = {R, G, B, A}` `P' = {R*A, G*A, B*A, A}` на в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="277ce-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R*A, G*A, B*A, A}` in the output.</span></span>

<span data-ttu-id="277ce-107">У этого действия нет свойств.</span><span class="sxs-lookup"><span data-stu-id="277ce-107">This effect has no properties.</span></span>

<span data-ttu-id="277ce-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1Premultiply.</span><span class="sxs-lookup"><span data-stu-id="277ce-108">The CLSID for this effect is CLSID\_D2D1Premultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="277ce-109">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="277ce-109">Output bitmap</span></span>

<span data-ttu-id="277ce-110">Размер выходного растрового изображения совпадает с размером входного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="277ce-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="277ce-111">Требования</span><span class="sxs-lookup"><span data-stu-id="277ce-111">Requirements</span></span>



| <span data-ttu-id="277ce-112">Требование</span><span class="sxs-lookup"><span data-stu-id="277ce-112">Requirement</span></span> | <span data-ttu-id="277ce-113">Значение</span><span class="sxs-lookup"><span data-stu-id="277ce-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="277ce-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="277ce-114">Minimum supported client</span></span> | <span data-ttu-id="277ce-115">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="277ce-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="277ce-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="277ce-116">Minimum supported server</span></span> | <span data-ttu-id="277ce-117">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="277ce-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="277ce-118">Header</span><span class="sxs-lookup"><span data-stu-id="277ce-118">Header</span></span>                   | <span data-ttu-id="277ce-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="277ce-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="277ce-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="277ce-120">Library</span></span>                  | <span data-ttu-id="277ce-121">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="277ce-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="277ce-122">См. также</span><span class="sxs-lookup"><span data-stu-id="277ce-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="277ce-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="277ce-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
