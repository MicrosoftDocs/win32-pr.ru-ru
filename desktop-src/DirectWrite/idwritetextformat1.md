---
title: Интерфейс IDWriteTextFormat1
description: Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах. | Интерфейс IDWriteTextFormat1
ms.assetid: 15295A17-E542-4071-AE38-02014A1235D5
keywords:
- Непосредственная запись интерфейса IDWriteTextFormat1
- Непосредственная запись интерфейса IDWriteTextFormat1, описание
topic_type:
- apiref
api_name:
- IDWriteTextFormat1
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796c5f845b5ed0d0522039865f2acb023fc2ab0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105664864"
---
# <a name="idwritetextformat1-interface"></a><span data-ttu-id="55580-106">Интерфейс IDWriteTextFormat1</span><span class="sxs-lookup"><span data-stu-id="55580-106">IDWriteTextFormat1 interface</span></span>

<span data-ttu-id="55580-107">Описывает свойства шрифта и абзаца, используемые для форматирования текста, а также сведения о языковых стандартах.</span><span class="sxs-lookup"><span data-stu-id="55580-107">Describes the font and paragraph properties used to format text, and it describes locale information.</span></span> <span data-ttu-id="55580-108">Этот интерфейс имеет все те же методы, что и [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) , и добавляет возможность применения явной ориентации.</span><span class="sxs-lookup"><span data-stu-id="55580-108">This interface has all the same methods as [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) and adds the ability for you to apply an explicit orientation.</span></span>

## <a name="members"></a><span data-ttu-id="55580-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="55580-109">Members</span></span>

<span data-ttu-id="55580-110">Интерфейс **IDWriteTextFormat1** наследует от [**идвритетекстформат**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span><span class="sxs-lookup"><span data-stu-id="55580-110">The **IDWriteTextFormat1** interface inherits from [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat).</span></span> <span data-ttu-id="55580-111">**IDWriteTextFormat1** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55580-111">**IDWriteTextFormat1** also has these types of members:</span></span>

-   [<span data-ttu-id="55580-112">Методы</span><span class="sxs-lookup"><span data-stu-id="55580-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55580-113">Методы</span><span class="sxs-lookup"><span data-stu-id="55580-113">Methods</span></span>

<span data-ttu-id="55580-114">Интерфейс **IDWriteTextFormat1** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="55580-114">The **IDWriteTextFormat1** interface has these methods.</span></span>



| <span data-ttu-id="55580-115">Метод</span><span class="sxs-lookup"><span data-stu-id="55580-115">Method</span></span>                                                                                | <span data-ttu-id="55580-116">Описание</span><span class="sxs-lookup"><span data-stu-id="55580-116">Description</span></span>                                                                                                             |
|:--------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55580-117">**жетфонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="55580-117">**GetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getfontfallback)                         | <span data-ttu-id="55580-118">Возвращает текущий откат.</span><span class="sxs-lookup"><span data-stu-id="55580-118">Gets the current fallback.</span></span> <span data-ttu-id="55580-119">Если после создания макета ни один из них не был задан, он будет иметь значение nullptr.</span><span class="sxs-lookup"><span data-stu-id="55580-119">If none was ever set since creating the layout, it will be nullptr.</span></span><br/>               |
| [<span data-ttu-id="55580-120">**жетластлиневраппинг**</span><span class="sxs-lookup"><span data-stu-id="55580-120">**GetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getlastlinewrapping)                 | <span data-ttu-id="55580-121">Возвращает режим переноса для последней строки.</span><span class="sxs-lookup"><span data-stu-id="55580-121">Gets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="55580-122">**жетоптикалалигнмент**</span><span class="sxs-lookup"><span data-stu-id="55580-122">**GetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getopticalalignment)                 | <span data-ttu-id="55580-123">Возвращает выравнивание оптического поля для текстового формата.</span><span class="sxs-lookup"><span data-stu-id="55580-123">Gets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="55580-124">**жетвертикалглифориентатион**</span><span class="sxs-lookup"><span data-stu-id="55580-124">**GetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-getverticalglyphorientation) | <span data-ttu-id="55580-125">Получение предпочтительной ориентации глифов при использовании направления чтения по вертикали.</span><span class="sxs-lookup"><span data-stu-id="55580-125">Get the preferred orientation of glyphs when using a vertical reading direction.</span></span><br/>                             |
| [<span data-ttu-id="55580-126">**сетфонтфаллбакк**</span><span class="sxs-lookup"><span data-stu-id="55580-126">**SetFontFallback**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setfontfallback)                         | <span data-ttu-id="55580-127">Применяет к макету пользовательский откат шрифта.</span><span class="sxs-lookup"><span data-stu-id="55580-127">Applies the custom font fallback onto the layout.</span></span> <span data-ttu-id="55580-128">Если параметр не задан, используется список резервных системных систем по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="55580-128">If none is set, it uses the default system fallback list.</span></span> <br/> |
| [<span data-ttu-id="55580-129">**сетластлиневраппинг**</span><span class="sxs-lookup"><span data-stu-id="55580-129">**SetLastLineWrapping**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setlastlinewrapping)                   | <span data-ttu-id="55580-130">Задает режим переноса для последней строки.</span><span class="sxs-lookup"><span data-stu-id="55580-130">Sets the wrapping mode of the last line.</span></span><br/>                                                                     |
| [<span data-ttu-id="55580-131">**сетоптикалалигнмент**</span><span class="sxs-lookup"><span data-stu-id="55580-131">**SetOpticalAlignment**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setopticalalignment)                 | <span data-ttu-id="55580-132">Задает для текстового формата выравнивание в виде оптического поля.</span><span class="sxs-lookup"><span data-stu-id="55580-132">Sets the optical margin alignment for the text format.</span></span><br/>                                                       |
| [<span data-ttu-id="55580-133">**сетвертикалглифориентатион**</span><span class="sxs-lookup"><span data-stu-id="55580-133">**SetVerticalGlyphOrientation**</span></span>](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritetextformat1-setverticalglyphorientation) | <span data-ttu-id="55580-134">Задает ориентацию текстового формата.</span><span class="sxs-lookup"><span data-stu-id="55580-134">Sets the orientation of a text format.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="55580-135">Требования</span><span class="sxs-lookup"><span data-stu-id="55580-135">Requirements</span></span>



| <span data-ttu-id="55580-136">Требование</span><span class="sxs-lookup"><span data-stu-id="55580-136">Requirement</span></span> | <span data-ttu-id="55580-137">Значение</span><span class="sxs-lookup"><span data-stu-id="55580-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55580-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55580-138">Minimum supported client</span></span><br/> | <span data-ttu-id="55580-139">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="55580-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="55580-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55580-140">Minimum supported server</span></span><br/> | <span data-ttu-id="55580-141">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="55580-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="55580-142">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="55580-142">Minimum supported phone</span></span><br/>  | <span data-ttu-id="55580-143">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]</span><span class="sxs-lookup"><span data-stu-id="55580-143">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="55580-144">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55580-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="55580-145"><dt>Дврите. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55580-145"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="55580-146">DLL</span><span class="sxs-lookup"><span data-stu-id="55580-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55580-147"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55580-147"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="55580-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55580-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55580-149">**идвритетекстформат**</span><span class="sxs-lookup"><span data-stu-id="55580-149">**IDWriteTextFormat**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat)
</dt> </dl>

 

