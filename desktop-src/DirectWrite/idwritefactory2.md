---
title: Интерфейс IDWriteFactory2
description: Интерфейс корневой фабрики для всех объектов DirectWrite.
ms.assetid: 1D3EEC28-EAB3-4FA2-98E9-7A8FDAF6E6FE
keywords:
- Непосредственная запись интерфейса IDWriteFactory1
- Непосредственная запись интерфейса IDWriteFactory1, описание
topic_type:
- apiref
api_name:
- IDWriteFactory1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7d5ba0f8d480981ab6ebea6dcdbd955b7b967e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681954"
---
# <a name="idwritefactory2-interface"></a><span data-ttu-id="d810e-105">Интерфейс IDWriteFactory2</span><span class="sxs-lookup"><span data-stu-id="d810e-105">IDWriteFactory2 interface</span></span>

<span data-ttu-id="d810e-106">Интерфейс корневой фабрики для всех объектов [DirectWrite](direct-write-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d810e-106">The root factory interface for all [DirectWrite](direct-write-portal.md) objects.</span></span>

## <a name="members"></a><span data-ttu-id="d810e-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="d810e-107">Members</span></span>

<span data-ttu-id="d810e-108">Интерфейс **IDWriteFactory1** наследует от [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span><span class="sxs-lookup"><span data-stu-id="d810e-108">The **IDWriteFactory1** interface inherits from [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1).</span></span> <span data-ttu-id="d810e-109">**IDWriteFactory2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d810e-109">**IDWriteFactory2** also has these types of members:</span></span>

-   [<span data-ttu-id="d810e-110">Методы</span><span class="sxs-lookup"><span data-stu-id="d810e-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="d810e-111">Методы</span><span class="sxs-lookup"><span data-stu-id="d810e-111">Methods</span></span>

<span data-ttu-id="d810e-112">Интерфейс **IDWriteFactory1** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="d810e-112">The **IDWriteFactory1** interface has these methods.</span></span>



| <span data-ttu-id="d810e-113">Метод</span><span class="sxs-lookup"><span data-stu-id="d810e-113">Method</span></span>                                                                             | <span data-ttu-id="d810e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d810e-114">Description</span></span>                                                                                                |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d810e-115">**креатекустомрендерингпарамс**</span><span class="sxs-lookup"><span data-stu-id="d810e-115">**CreateCustomRenderingParams**</span></span>](idwritefactory2-createcustomrenderingparams.md) | <span data-ttu-id="d810e-116">Создает объект параметров отрисовки с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="d810e-116">Creates a rendering parameters object with the specified properties.</span></span><br/>                            |
| [<span data-ttu-id="d810e-117">**креатефонтфаллбаккбуилдер**</span><span class="sxs-lookup"><span data-stu-id="d810e-117">**CreateFontFallbackBuilder**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-createfontfallbackbuilder)     | <span data-ttu-id="d810e-118">Создает объект построителя шрифтов.</span><span class="sxs-lookup"><span data-stu-id="d810e-118">Creates a font fallback builder object.</span></span><br/>                                                         |
| [<span data-ttu-id="d810e-119">**креатеглифрунаналисис**</span><span class="sxs-lookup"><span data-stu-id="d810e-119">**CreateGlyphRunAnalysis**</span></span>](idwritefactory2-createglyphrunanalysis.md)           | <span data-ttu-id="d810e-120">Создает объект анализа выполнения глифа, который инкапсулирует сведения, используемые для визуализации выполнения глифа.</span><span class="sxs-lookup"><span data-stu-id="d810e-120">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span><br/> |
| [<span data-ttu-id="d810e-121">**жетсистемфонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="d810e-121">**GetSystemFontFallback**</span></span>](idwritefactory2-getsystemfontfallback.md)             | <span data-ttu-id="d810e-122">Создает резервный объект шрифта из списка резервных шрифтов системы.</span><span class="sxs-lookup"><span data-stu-id="d810e-122">Creates a font fallback object from the system font fallback list.</span></span><br/>                              |
| [<span data-ttu-id="d810e-123">**транслатеколорглифрун**</span><span class="sxs-lookup"><span data-stu-id="d810e-123">**TranslateColorGlyphRun**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)           | <span data-ttu-id="d810e-124">Этот метод вызывается для выполнения глифа, чтобы перевести его в несколько цветовых глифов.</span><span class="sxs-lookup"><span data-stu-id="d810e-124">This method is called on a glyph run to translate it in to multiple color glyph runs.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="d810e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="d810e-125">Requirements</span></span>



| <span data-ttu-id="d810e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="d810e-126">Requirement</span></span> | <span data-ttu-id="d810e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="d810e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d810e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d810e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d810e-129">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="d810e-129">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d810e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d810e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d810e-131">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="d810e-131">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d810e-132">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="d810e-132">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d810e-133">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="d810e-133">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d810e-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d810e-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="d810e-135"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d810e-135"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d810e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d810e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d810e-137"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d810e-137"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d810e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d810e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d810e-139">**IDWriteFactory1**</span><span class="sxs-lookup"><span data-stu-id="d810e-139">**IDWriteFactory1**</span></span>](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)
</dt> <dt>

[<span data-ttu-id="d810e-140">**идвритефактори**</span><span class="sxs-lookup"><span data-stu-id="d810e-140">**IDWriteFactory**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefactory)
</dt> </dl>

 

