---
title: Интерфейс Идвритефонтфаллбаккбуилдер
description: Позволяет создавать сопоставления отката шрифта в Юникоде и создавать объекты возврата шрифта из этих сопоставлений.
ms.assetid: 462AC12E-C856-4D8F-83AF-FAC3221425C2
keywords:
- Непосредственная запись интерфейса Идвритефонтфаллбаккбуилдер
- Непосредственная запись интерфейса Идвритефонтфаллбаккбуилдер, описание
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38cd1770bdd9617f53bb48d725b55c466b12c263
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988891"
---
# <a name="idwritefontfallbackbuilder-interface"></a><span data-ttu-id="e333d-105">Интерфейс Идвритефонтфаллбаккбуилдер</span><span class="sxs-lookup"><span data-stu-id="e333d-105">IDWriteFontFallbackBuilder interface</span></span>

<span data-ttu-id="e333d-106">Позволяет создавать сопоставления отката шрифта в Юникоде и создавать объекты возврата шрифта из этих сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="e333d-106">Allows you to create Unicode font fallback mappings and create a font fall back object from those mappings.</span></span>

## <a name="members"></a><span data-ttu-id="e333d-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="e333d-107">Members</span></span>

<span data-ttu-id="e333d-108">Интерфейс **идвритефонтфаллбаккбуилдер** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e333d-108">The **IDWriteFontFallbackBuilder** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e333d-109">**Идвритефонтфаллбаккбуилдер** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e333d-109">**IDWriteFontFallbackBuilder** also has these types of members:</span></span>

-   [<span data-ttu-id="e333d-110">Методы</span><span class="sxs-lookup"><span data-stu-id="e333d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e333d-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e333d-111">Methods</span></span>

<span data-ttu-id="e333d-112">Интерфейс **идвритефонтфаллбаккбуилдер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e333d-112">The **IDWriteFontFallbackBuilder** interface has these methods.</span></span>



| <span data-ttu-id="e333d-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e333d-113">Method</span></span>                                                                      | <span data-ttu-id="e333d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e333d-114">Description</span></span>                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e333d-115">**аддмаппинг**</span><span class="sxs-lookup"><span data-stu-id="e333d-115">**AddMapping**</span></span>](idwritefontfallbackbuilder-addmapping.md)                 | <span data-ttu-id="e333d-116">Добавляет одно сопоставление в список.</span><span class="sxs-lookup"><span data-stu-id="e333d-116">Appends a single mapping to the list.</span></span> <span data-ttu-id="e333d-117">Вызывайте его один раз для каждого дополнительного сопоставления.</span><span class="sxs-lookup"><span data-stu-id="e333d-117">Call this once for each additional mapping.</span></span><br/> |
| [<span data-ttu-id="e333d-118">**аддмаппингс**</span><span class="sxs-lookup"><span data-stu-id="e333d-118">**AddMappings**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-addmappings)               | <span data-ttu-id="e333d-119">Добавьте все сопоставления из существующего объекта резервного шрифта.</span><span class="sxs-lookup"><span data-stu-id="e333d-119">Add all the mappings from an existing font fallback object.</span></span><br/>                       |
| [<span data-ttu-id="e333d-120">**креатефонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e333d-120">**CreateFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefontfallbackbuilder-createfontfallback) | <span data-ttu-id="e333d-121">Создает окончательный объект резерва из добавленных сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="e333d-121">Creates the finalized fallback object from the mappings added.</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="e333d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="e333d-122">Requirements</span></span>



| <span data-ttu-id="e333d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="e333d-123">Requirement</span></span> | <span data-ttu-id="e333d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e333d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e333d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e333d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e333d-126">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="e333d-126">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="e333d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e333d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e333d-128">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="e333d-128">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e333d-129">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="e333d-129">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e333d-130">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="e333d-130">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="e333d-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e333d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e333d-132"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e333d-132"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e333d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e333d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e333d-134"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e333d-134"><dt>Dwrite.dll</dt></span></span> </dl>   |



 

