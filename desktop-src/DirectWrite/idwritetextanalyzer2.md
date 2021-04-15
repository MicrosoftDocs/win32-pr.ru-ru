---
title: Интерфейс IDWriteTextAnalyzer2
description: Анализирует различные свойства текста для обработки сложных скриптов.
ms.assetid: 62DF6E71-F99D-47E9-A9BE-2A481A60AEDD
keywords:
- Непосредственная запись интерфейса IDWriteTextAnalyzer2
- Непосредственная запись интерфейса IDWriteTextAnalyzer2, описание
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer2
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2548cc7961c8d866d4067e794e033701457d5b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534493"
---
# <a name="idwritetextanalyzer2-interface"></a><span data-ttu-id="fbaf4-105">Интерфейс IDWriteTextAnalyzer2</span><span class="sxs-lookup"><span data-stu-id="fbaf4-105">IDWriteTextAnalyzer2 interface</span></span>

<span data-ttu-id="fbaf4-106">Анализирует различные свойства текста для обработки сложных скриптов.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-106">Analyzes various text properties for complex script processing.</span></span>

## <a name="members"></a><span data-ttu-id="fbaf4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="fbaf4-107">Members</span></span>

<span data-ttu-id="fbaf4-108">Интерфейс **IDWriteTextAnalyzer2** наследует от [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span><span class="sxs-lookup"><span data-stu-id="fbaf4-108">The **IDWriteTextAnalyzer2** interface inherits from [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1).</span></span> <span data-ttu-id="fbaf4-109">**IDWriteTextAnalyzer2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fbaf4-109">**IDWriteTextAnalyzer2** also has these types of members:</span></span>

-   [<span data-ttu-id="fbaf4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="fbaf4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="fbaf4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fbaf4-111">Methods</span></span>

<span data-ttu-id="fbaf4-112">Интерфейс **IDWriteTextAnalyzer2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-112">The **IDWriteTextAnalyzer2** interface has these methods.</span></span>



| <span data-ttu-id="fbaf4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="fbaf4-113">Method</span></span>                                                                                    | <span data-ttu-id="fbaf4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fbaf4-114">Description</span></span>                                                                             |
|:------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="fbaf4-115">**чекктипографикфеатуре**</span><span class="sxs-lookup"><span data-stu-id="fbaf4-115">**CheckTypographicFeature**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-checktypographicfeature)           | <span data-ttu-id="fbaf4-116">Проверяет, доступна ли типографская функция для глифа или набора глифов.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-116">Checks if a typographic feature is available for a glyph or a set of glyphs.</span></span><br/> |
| [<span data-ttu-id="fbaf4-117">**жетглифориентатионтрансформ**</span><span class="sxs-lookup"><span data-stu-id="fbaf4-117">**GetGlyphOrientationTransform**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-getglyphorientationtransform) | <span data-ttu-id="fbaf4-118">Возвращает матрицу преобразования 2 для соответствующего угла для прорисовки выполнения глифа.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-118">Returns 2x3 transform matrix for the respective angle to draw the glyph run.</span></span><br/> |
| [<span data-ttu-id="fbaf4-119">**жеттипографикфеатурес**</span><span class="sxs-lookup"><span data-stu-id="fbaf4-119">**GetTypographicFeatures**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextanalyzer2-gettypographicfeatures)             | <span data-ttu-id="fbaf4-120">Возвращает полный список функций OpenType, доступных для сценария или шрифта.</span><span class="sxs-lookup"><span data-stu-id="fbaf4-120">Returns a complete list of OpenType features available for a script or font.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fbaf4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="fbaf4-121">Requirements</span></span>



| <span data-ttu-id="fbaf4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="fbaf4-122">Requirement</span></span> | <span data-ttu-id="fbaf4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="fbaf4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaf4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fbaf4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fbaf4-125">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="fbaf4-125">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="fbaf4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fbaf4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fbaf4-127">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="fbaf4-127">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="fbaf4-128">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="fbaf4-128">Minimum supported phone</span></span><br/>  | <span data-ttu-id="fbaf4-129">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="fbaf4-129">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="fbaf4-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fbaf4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="fbaf4-131"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf4-131"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="fbaf4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fbaf4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbaf4-133"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbaf4-133"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fbaf4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fbaf4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbaf4-135">**IDWriteTextAnalyzer1**</span><span class="sxs-lookup"><span data-stu-id="fbaf4-135">**IDWriteTextAnalyzer1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)
</dt> </dl>

 

