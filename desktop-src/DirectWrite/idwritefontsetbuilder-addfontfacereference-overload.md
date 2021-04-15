---
title: Методы Идвритефонтсетбуилдер Аддфонтфацереференце (Дврите \_ 3. h)
description: Добавляет ссылку на шрифт в создаваемый набор.
ms.assetid: 2543720f-1b5a-ca1d-9e24-3fcd61a4de37
keywords:
- Методы Аддфонтфацереференце Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3c20ca2832bfce3696a98c22730580442f621469
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689028"
---
# <a name="idwritefontsetbuilderaddfontfacereference-methods"></a><span data-ttu-id="3fbf2-104">Методы Идвритефонтсетбуилдер:: Аддфонтфацереференце</span><span class="sxs-lookup"><span data-stu-id="3fbf2-104">IDWriteFontSetBuilder::AddFontFaceReference methods</span></span>

<span data-ttu-id="3fbf2-105">Добавляет ссылку на шрифт в создаваемый набор.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-105">Adds a reference to a font to the set being built.</span></span>

### <a name="overload-list"></a><span data-ttu-id="3fbf2-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="3fbf2-106">Overload list</span></span>



| <span data-ttu-id="3fbf2-107">Метод</span><span class="sxs-lookup"><span data-stu-id="3fbf2-107">Method</span></span>                                                                                                                                           | <span data-ttu-id="3fbf2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="3fbf2-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbf2-109">[**Аддфонтфацереференце (Идвритефонтфацереференце \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span><span class="sxs-lookup"><span data-stu-id="3fbf2-109">[**AddFontFaceReference(IDWriteFontFaceReference\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference))</span></span>                                         | <span data-ttu-id="3fbf2-110">Добавляет ссылку на шрифт в создаваемый набор.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-110">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="3fbf2-111">Необходимые метаданные будут автоматически извлечены из шрифта при вызове Креатефонтсет.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-111">The necessary metadata will automatically be extracted from the font upon calling CreateFontSet.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="3fbf2-112">[**Аддфонтфацереференце (Идвритефонтфацереференце \* , свойство const \_ дврите \_ Font \* , UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span><span class="sxs-lookup"><span data-stu-id="3fbf2-112">[**AddFontFaceReference(IDWriteFontFaceReference\*, const DWRITE\_FONT\_PROPERTY\*, UINT32)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference_dwrite_font_propertyconst_uint32))</span></span> | <span data-ttu-id="3fbf2-113">Добавляет ссылку на шрифт в создаваемый набор.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-113">Adds a reference to a font to the set being built.</span></span> <span data-ttu-id="3fbf2-114">Вызывающий объект предоставляет достаточно информации для поиска, избегая необходимости открывать потенциально нелокальный шрифт.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-114">The caller supplies enough information to search on, avoiding the need to open the potentially non-local font.</span></span> <span data-ttu-id="3fbf2-115">Все свойства, не предоставляемые вызывающим объектом, будут отсутствовать, и эти свойства будут недоступны в качестве фильтров в Жетматчингфонтс.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-115">Any properties not supplied by the caller will be missing, and those properties will not be available as filters in GetMatchingFonts.</span></span> <span data-ttu-id="3fbf2-116">GetPropertyValues для отсутствующих свойств вернет пустой список строк.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-116">GetPropertyValues for missing properties will return an empty string list.</span></span> <span data-ttu-id="3fbf2-117">Передаваемые свойства обычно должны соответствовать фактическому содержимому шрифта, но они не должны быть.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-117">The properties passed should generally be consistent with the actual font contents, but they need not be.</span></span> <span data-ttu-id="3fbf2-118">Например, можно создать псевдоним для шрифта, используя другое имя или уникальный идентификатор, или задать пользовательские теги, отсутствующие в фактическом шрифте.</span><span class="sxs-lookup"><span data-stu-id="3fbf2-118">You could, for example, alias a font using a different name or unique identifier, or you could set custom tags not present in the actual font.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3fbf2-119">Требования</span><span class="sxs-lookup"><span data-stu-id="3fbf2-119">Requirements</span></span>



| <span data-ttu-id="3fbf2-120">Требование</span><span class="sxs-lookup"><span data-stu-id="3fbf2-120">Requirement</span></span> | <span data-ttu-id="3fbf2-121">Значение</span><span class="sxs-lookup"><span data-stu-id="3fbf2-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fbf2-122">Header</span><span class="sxs-lookup"><span data-stu-id="3fbf2-122">Header</span></span><br/> | <dl> <span data-ttu-id="3fbf2-123"><dt>Дврите \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fbf2-123"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fbf2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3fbf2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fbf2-125">**идвритефонтсетбуилдер**</span><span class="sxs-lookup"><span data-stu-id="3fbf2-125">**IDWriteFontSetBuilder**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
</dt> </dl>

<span data-ttu-id="3fbf2-126">�</span><span class="sxs-lookup"><span data-stu-id="3fbf2-126">�</span></span>

<span data-ttu-id="3fbf2-127">�</span><span class="sxs-lookup"><span data-stu-id="3fbf2-127">�</span></span>
