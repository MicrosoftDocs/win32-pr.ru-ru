---
title: Унпремултипли, результат
description: Используйте этот результат для преобразования изображения из предварительно умноженного альфа-канала в унпремултиплиед Alpha.
ms.assetid: A4FAF899-81DA-4BDA-98B4-DE63EC1664F5
keywords:
- унпремултипли, результат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5628ea646443a08abffa4549ad25147deb609acf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415936"
---
# <a name="unpremultiply-effect"></a><span data-ttu-id="2c9ee-104">Унпремултипли, результат</span><span class="sxs-lookup"><span data-stu-id="2c9ee-104">Unpremultiply effect</span></span>

<span data-ttu-id="2c9ee-105">Используйте этот результат для преобразования изображения из предварительно умноженного альфа-канала в унпремултиплиед Alpha.</span><span class="sxs-lookup"><span data-stu-id="2c9ee-105">Use this effect to convert an image from premultiplied alpha to unpremultiplied alpha.</span></span> <span data-ttu-id="2c9ee-106">Этот результат заменяет каждый входной пиксель `P = {R, G, B, A}` `P' = {R/A, G/A, B/A, A}` на в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2c9ee-106">The effect replaces each input pixel `P = {R, G, B, A}` with `P' = {R/A, G/A, B/A, A}` in the output.</span></span>

<span data-ttu-id="2c9ee-107">У этого действия нет свойств.</span><span class="sxs-lookup"><span data-stu-id="2c9ee-107">This effect has no properties.</span></span>

<span data-ttu-id="2c9ee-108">Идентификатором CLSID для этого действия является CLSID \_ D2D1Unpremultiply.</span><span class="sxs-lookup"><span data-stu-id="2c9ee-108">The CLSID for this effect is CLSID\_D2D1Unpremultiply.</span></span>

## <a name="output-bitmap"></a><span data-ttu-id="2c9ee-109">Битовая карта вывода</span><span class="sxs-lookup"><span data-stu-id="2c9ee-109">Output bitmap</span></span>

<span data-ttu-id="2c9ee-110">Размер выходного растрового изображения совпадает с размером входного растрового изображения.</span><span class="sxs-lookup"><span data-stu-id="2c9ee-110">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c9ee-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2c9ee-111">Requirements</span></span>



| <span data-ttu-id="2c9ee-112">Требование</span><span class="sxs-lookup"><span data-stu-id="2c9ee-112">Requirement</span></span> | <span data-ttu-id="2c9ee-113">Значение</span><span class="sxs-lookup"><span data-stu-id="2c9ee-113">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2c9ee-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c9ee-114">Minimum supported client</span></span> | <span data-ttu-id="2c9ee-115">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="2c9ee-115">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2c9ee-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c9ee-116">Minimum supported server</span></span> | <span data-ttu-id="2c9ee-117">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="2c9ee-117">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="2c9ee-118">Header</span><span class="sxs-lookup"><span data-stu-id="2c9ee-118">Header</span></span>                   | <span data-ttu-id="2c9ee-119">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="2c9ee-119">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="2c9ee-120">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2c9ee-120">Library</span></span>                  | <span data-ttu-id="2c9ee-121">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="2c9ee-121">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="2c9ee-122">См. также</span><span class="sxs-lookup"><span data-stu-id="2c9ee-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c9ee-123">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="2c9ee-123">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

 
