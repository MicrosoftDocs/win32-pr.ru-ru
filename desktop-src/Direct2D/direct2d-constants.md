---
title: Константы Direct2D
description: Direct2D определяет следующий список констант.
ms.assetid: 98a443af-4bb7-486d-bc87-ff34c3671bdd
topic_type:
- apiref
api_name:
- D2D1_APPEND_ALIGNED_ELEMENT
- D2D1_DEFAULT_FLATTENING_TOLERANCE
- D2D1_INVALID_PROPERTY_INDEX
- D2D1_INVALID_TAG
- D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL
api_location:
- d2d1.h
- d2d1effects_2.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 09/19/2019
ms.openlocfilehash: bc25bf1055b923a383fc580a622e96d787ed13e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654583"
---
# <a name="direct2d-constants"></a><span data-ttu-id="02a5c-103">Константы Direct2D</span><span class="sxs-lookup"><span data-stu-id="02a5c-103">Direct2D constants</span></span>

<span data-ttu-id="02a5c-104">Следующие константы объявляются в `d2d1effectauthor.h` `d2d1.h` `d2d1_1.h` `d2d1effects_2.h` файлах заголовков,, и.</span><span class="sxs-lookup"><span data-stu-id="02a5c-104">The following constants are declared in the `d2d1effectauthor.h`, `d2d1.h`, `d2d1_1.h`, and `d2d1effects_2.h` header files.</span></span>

## <a name="d2d1_append_aligned_element--1"></a><span data-ttu-id="02a5c-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span><span class="sxs-lookup"><span data-stu-id="02a5c-105">D2D1_APPEND_ALIGNED_ELEMENT (-1)</span></span>
<span data-ttu-id="02a5c-106">Используется при упаковке входных элементов макета.</span><span class="sxs-lookup"><span data-stu-id="02a5c-106">Used when packing input layout elements.</span></span> <span data-ttu-id="02a5c-107">Указывает, что элементы должны упаковываться непрерывно.</span><span class="sxs-lookup"><span data-stu-id="02a5c-107">It indicates that the elements must be packed contiguously.</span></span>

## <a name="d2d1_default_flattening_tolerance-025f"></a><span data-ttu-id="02a5c-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0,25 f)</span><span class="sxs-lookup"><span data-stu-id="02a5c-108">D2D1_DEFAULT_FLATTENING_TOLERANCE (0.25f)</span></span>
<span data-ttu-id="02a5c-109">Допуск по умолчанию для геометрических операций спрямления.</span><span class="sxs-lookup"><span data-stu-id="02a5c-109">The default tolerance for geometric flattening operations.</span></span>

## <a name="d2d1_invalid_property_index-uint_max"></a><span data-ttu-id="02a5c-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span><span class="sxs-lookup"><span data-stu-id="02a5c-110">D2D1_INVALID_PROPERTY_INDEX (UINT_MAX)</span></span>
<span data-ttu-id="02a5c-111">Определяет недопустимый индекс свойства.</span><span class="sxs-lookup"><span data-stu-id="02a5c-111">Defines an invalid property index.</span></span>

<span data-ttu-id="02a5c-112">Эта константа возвращается из [**ID2D1Properties:: жетпропертиндекс**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) , чтобы указать, что указанное именованное свойство не имеет индекса в интерфейсе свойства.</span><span class="sxs-lookup"><span data-stu-id="02a5c-112">This constant is returned from [**ID2D1Properties::GetPropertyIndex**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getpropertyindex) to indicate that the named property that you provided doesn't have an index in the property interface.</span></span>

<span data-ttu-id="02a5c-113">Если передать эту константу в [**ID2D1Properties:: GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) или [**ID2D1Properties:: жетвалуебинаме**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), то вызов завершается ошибкой, а выходной буфер заполняется нулем.</span><span class="sxs-lookup"><span data-stu-id="02a5c-113">If you pass this constant to [**ID2D1Properties::GetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvalue(uint32_byte_uint32)) or [**ID2D1Properties::GetValueByName**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-getvaluebyname(pcwstr_byte_uint32)), then the call fails, and the output buffer is zero-filled.</span></span>

## <a name="d2d1_invalid_tag-ulonglong_max"></a><span data-ttu-id="02a5c-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span><span class="sxs-lookup"><span data-stu-id="02a5c-114">D2D1_INVALID_TAG (ULONGLONG_MAX)</span></span>
<span data-ttu-id="02a5c-115">Процессу не используйте.</span><span class="sxs-lookup"><span data-stu-id="02a5c-115">Reserved; don't use.</span></span>

## <a name="d2d1_scene_referred_sdr_white_level-800f"></a><span data-ttu-id="02a5c-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0 f)</span><span class="sxs-lookup"><span data-stu-id="02a5c-116">D2D1_SCENE_REFERRED_SDR_WHITE_LEVEL (80.0f)</span></span>
<span data-ttu-id="02a5c-117">Число НИТС, которое используется для цветового пространства sRGB или scRGB для белого SDR, или значений с плавающей точкой 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="02a5c-117">The number of nits that sRGB or scRGB color space uses for SDR white, or floating point values of 1.0f.</span></span> <span data-ttu-id="02a5c-118">Это значение является константой только в том случае, если цветовое пространство использует освещенность, основанную на сцене, что относится к содержимому с большим динамическим диапазоном (HDR).</span><span class="sxs-lookup"><span data-stu-id="02a5c-118">This value is constant only when the color space uses scene-referred luminance, which is true for high dynamic range (HDR) content.</span></span> <span data-ttu-id="02a5c-119">Если цветовая область использует светимость, связанную с отображением, то на экране должны быть запрошены белые уровни SDR.</span><span class="sxs-lookup"><span data-stu-id="02a5c-119">If the color space uses display-referred luminance instead, then the SDR white level should be queried from the display.</span></span>

## <a name="requirements"></a><span data-ttu-id="02a5c-120">Требования</span><span class="sxs-lookup"><span data-stu-id="02a5c-120">Requirements</span></span>

| <span data-ttu-id="02a5c-121">Требование</span><span class="sxs-lookup"><span data-stu-id="02a5c-121">Requirement</span></span> | <span data-ttu-id="02a5c-122">Значение</span><span class="sxs-lookup"><span data-stu-id="02a5c-122">Value</span></span> |
|-|-|
| <span data-ttu-id="02a5c-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02a5c-123">Minimum supported client</span></span> | <span data-ttu-id="02a5c-124">Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы для \[ классических приложений Windows Vista \| приложения UWP\]</span><span class="sxs-lookup"><span data-stu-id="02a5c-124">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="02a5c-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02a5c-125">Minimum supported server</span></span> | <span data-ttu-id="02a5c-126">Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 классические \[ приложения \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="02a5c-126">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span> |
| <span data-ttu-id="02a5c-127">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="02a5c-127">Minimum supported phone</span></span> | <span data-ttu-id="02a5c-128">Windows Phone 8,1 \[ Windows Phone silverlight 8,1 и среда выполнения Windows приложения \] Windows Phone 8,1 \[ Windows Phone silverlight 8,1 и среда выполнения Windows Apps\]</span><span class="sxs-lookup"><span data-stu-id="02a5c-128">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\], Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span> |
| <span data-ttu-id="02a5c-129">Header</span><span class="sxs-lookup"><span data-stu-id="02a5c-129">Header</span></span> | <span data-ttu-id="02a5c-130">d2d1effectauthor. h, D2D1. h, d2d1_1. h, d2d1effects_2. h</span><span class="sxs-lookup"><span data-stu-id="02a5c-130">d2d1effectauthor.h, d2d1.h, d2d1_1.h, d2d1effects_2.h</span></span> |
