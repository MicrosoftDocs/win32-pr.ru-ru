---
title: Методы Идвритефонтсет GetPropertyValues (Дврите \_ 3. h)
description: Возвращает значения свойств для набора шрифтов.
ms.assetid: 3c3fd5b7-88dd-d434-0b62-f365b407c379
keywords:
- Методы GetPropertyValues Direct Write
topic_type:
- apiref
api_location:
- dwrite_3.h
api_type:
- HeaderDef
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3d135a63be987a4999d898c8e9c7d84251c8ece3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668534"
---
# <a name="idwritefontsetgetpropertyvalues-methods"></a><span data-ttu-id="1e637-104">Методы Идвритефонтсет:: GetPropertyValues</span><span class="sxs-lookup"><span data-stu-id="1e637-104">IDWriteFontSet::GetPropertyValues methods</span></span>

<span data-ttu-id="1e637-105">Возвращает значения свойств для набора шрифтов.</span><span class="sxs-lookup"><span data-stu-id="1e637-105">Returns property values for the font set.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1e637-106">Список перегрузок</span><span class="sxs-lookup"><span data-stu-id="1e637-106">Overload list</span></span>



| <span data-ttu-id="1e637-107">Метод</span><span class="sxs-lookup"><span data-stu-id="1e637-107">Method</span></span>                                                                                                                                   | <span data-ttu-id="1e637-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1e637-108">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e637-109">[**GetPropertyValues ( \_ \_ идентификатор свойства шрифта Дврите \_ , идвритестринглист \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="1e637-109">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span>                       | <span data-ttu-id="1e637-110">Возвращает все уникальные значения свойств в наборе, которые можно использовать для таких целей, как отображение списка семейств или пометки в облаке.</span><span class="sxs-lookup"><span data-stu-id="1e637-110">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="1e637-111">Все значения возвращаются независимо от языка, включая все локализованные имена.</span><span class="sxs-lookup"><span data-stu-id="1e637-111">All values are returned regardless of language, including all localized names.</span></span> <br/>                                                                                       |
| <span data-ttu-id="1e637-112">[**GetPropertyValues ( \_ \_ идентификатор свойства шрифта дврите \_ , const WCHAR \* , идвритестринглист \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="1e637-112">[**GetPropertyValues(DWRITE\_FONT\_PROPERTY\_ID, const WCHAR\*, IDWriteStringList\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_wcharconst_idwritestringlist))</span></span>        | <span data-ttu-id="1e637-113">Возвращает все уникальные значения свойств в наборе, которые можно использовать для таких целей, как отображение списка семейств или пометки в облаке.</span><span class="sxs-lookup"><span data-stu-id="1e637-113">Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud.</span></span> <span data-ttu-id="1e637-114">Значения возвращаются в порядке приоритета в соответствии со списком языков, так что если шрифт содержит более одного локализованного имени, будет возвращено предпочтительное из них.</span><span class="sxs-lookup"><span data-stu-id="1e637-114">Values are returned in priority order according to the language list, such that if a font contains more than one localized name, the preferred one will be returned.</span></span> <br/> |
| <span data-ttu-id="1e637-115">[**GetPropertyValues (UINT32, \_ \_ идентификатор свойства шрифта ДВРИТЕ \_ , bool \* , идврителокализедстрингс \* \* )**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span><span class="sxs-lookup"><span data-stu-id="1e637-115">[**GetPropertyValues(UINT32, DWRITE\_FONT\_PROPERTY\_ID, BOOL\*, IDWriteLocalizedStrings\*\*)**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset-getpropertyvalues(dwrite_font_property_id_idwritestringlist))</span></span> | <span data-ttu-id="1e637-116">Возвращает значения свойств определенного индекса элемента шрифта.</span><span class="sxs-lookup"><span data-stu-id="1e637-116">Returns the property values of a specific font item index.</span></span><br/>                                                                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="1e637-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1e637-117">Requirements</span></span>



| <span data-ttu-id="1e637-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1e637-118">Requirement</span></span> | <span data-ttu-id="1e637-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1e637-119">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e637-120">Header</span><span class="sxs-lookup"><span data-stu-id="1e637-120">Header</span></span><br/> | <dl> <span data-ttu-id="1e637-121"><dt>Дврите \_ 3. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e637-121"><dt>Dwrite\_3.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e637-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1e637-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e637-123">**идвритефонтсет**</span><span class="sxs-lookup"><span data-stu-id="1e637-123">**IDWriteFontSet**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
</dt> </dl>

<span data-ttu-id="1e637-124">�</span><span class="sxs-lookup"><span data-stu-id="1e637-124">�</span></span>

<span data-ttu-id="1e637-125">�</span><span class="sxs-lookup"><span data-stu-id="1e637-125">�</span></span>
