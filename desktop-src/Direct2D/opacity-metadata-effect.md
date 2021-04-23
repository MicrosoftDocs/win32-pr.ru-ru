---
title: Эффекты непрозрачности метаданных
description: Этот результат можно использовать для пометки области входного изображения как непрозрачной, поэтому возможна внутренняя оптимизация отрисовки графа.
ms.assetid: 25B34A31-8533-4339-BBF7-2D7E5488E301
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84d90ba1c4b1186e3e682ec94a0c9c17bdfc73e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137078"
---
# <a name="opacity-metadata-effect"></a><span data-ttu-id="13064-103">Эффекты непрозрачности метаданных</span><span class="sxs-lookup"><span data-stu-id="13064-103">Opacity metadata effect</span></span>

<span data-ttu-id="13064-104">Этот результат можно использовать для пометки области входного изображения как непрозрачной, поэтому возможна внутренняя оптимизация отрисовки графа.</span><span class="sxs-lookup"><span data-stu-id="13064-104">You can use this effect to mark an area of an input image as opaque, so internal rendering optimizations to the graph are possible.</span></span>

> [!Note]  
> <span data-ttu-id="13064-105">Этот результат не изменяет сам образ, чтобы он был непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="13064-105">This effect doesn't modify the image itself to be opaque.</span></span> <span data-ttu-id="13064-106">Он изменяет данные, связанные с изображением, поэтому модуль подготовки отчетов считает, что указанная область непрозрачна.</span><span class="sxs-lookup"><span data-stu-id="13064-106">It modifies data associated with the image so the renderer assumes the specified region is opaque.</span></span>

 

<span data-ttu-id="13064-107">Идентификатором CLSID для этого действия является CLSID \_ D2D1OpacityMetadata.</span><span class="sxs-lookup"><span data-stu-id="13064-107">The CLSID for this effect is CLSID\_D2D1OpacityMetadata.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="13064-108">Свойства эффектов</span><span class="sxs-lookup"><span data-stu-id="13064-108">Effect properties</span></span>



| <span data-ttu-id="13064-109">Отображаемое имя и перечисление индекса</span><span class="sxs-lookup"><span data-stu-id="13064-109">Display name and index enumeration</span></span>                                                 | <span data-ttu-id="13064-110">Тип и значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="13064-110">Type and default value</span></span>                                                             | <span data-ttu-id="13064-111">Описание</span><span class="sxs-lookup"><span data-stu-id="13064-111">Description</span></span>                                                                                       |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13064-112">аутпутрект</span><span class="sxs-lookup"><span data-stu-id="13064-112">OutputRect</span></span><br/> <span data-ttu-id="13064-113">\_Непрозрачный \_ \_ входной \_ \_ прямоугольник D2D1 опаЦитиметадата</span><span class="sxs-lookup"><span data-stu-id="13064-113">D2D1\_OPACITYMETADATA\_PROP\_INPUT\_OPAQUE\_RECT</span></span> <br/> | <span data-ttu-id="13064-114">D2D1 \_ vector \_ 4F</span><span class="sxs-lookup"><span data-stu-id="13064-114">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="13064-115">(-ФЛТ \_ Max,-ФЛТ \_ Max, ФЛТ \_ Max, ФЛТ \_ max)</span><span class="sxs-lookup"><span data-stu-id="13064-115">(-FLT\_MAX, -FLT\_MAX, FLT\_MAX, FLT\_MAX)</span></span> <br/> | <span data-ttu-id="13064-116">Часть исходного изображения, которая является непрозрачной.</span><span class="sxs-lookup"><span data-stu-id="13064-116">The portion of the source image that is opaque.</span></span> <span data-ttu-id="13064-117">По умолчанию используется весь входной образ.</span><span class="sxs-lookup"><span data-stu-id="13064-117">The default is the entire input image.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13064-118">Требования</span><span class="sxs-lookup"><span data-stu-id="13064-118">Requirements</span></span>



| <span data-ttu-id="13064-119">Требование</span><span class="sxs-lookup"><span data-stu-id="13064-119">Requirement</span></span> | <span data-ttu-id="13064-120">Значение</span><span class="sxs-lookup"><span data-stu-id="13064-120">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="13064-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13064-121">Minimum supported client</span></span> | <span data-ttu-id="13064-122">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="13064-122">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="13064-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13064-123">Minimum supported server</span></span> | <span data-ttu-id="13064-124">Windows 8 и обновление платформы для \[ классических приложений Windows 7 \| приложения для Магазина Windows\]</span><span class="sxs-lookup"><span data-stu-id="13064-124">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="13064-125">Header</span><span class="sxs-lookup"><span data-stu-id="13064-125">Header</span></span>                   | <span data-ttu-id="13064-126">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="13064-126">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="13064-127">Библиотека</span><span class="sxs-lookup"><span data-stu-id="13064-127">Library</span></span>                  | <span data-ttu-id="13064-128">D2D1. lib, дксгуид. lib</span><span class="sxs-lookup"><span data-stu-id="13064-128">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="13064-129">См. также</span><span class="sxs-lookup"><span data-stu-id="13064-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13064-130">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="13064-130">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

