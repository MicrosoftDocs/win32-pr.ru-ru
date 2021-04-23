---
title: EDITBOX. Реплацеселектион
description: Метод Реплацеселектион заменяет текущее выделение на указанный текст.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Реплацеселектион Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694727"
---
# <a name="editboxreplaceselection"></a><span data-ttu-id="b77b7-104">EDITBOX. Реплацеселектион</span><span class="sxs-lookup"><span data-stu-id="b77b7-104">EDITBOX.replaceSelection</span></span>

<span data-ttu-id="b77b7-105">Метод **реплацеселектион** заменяет текущее выделение на указанный текст.</span><span class="sxs-lookup"><span data-stu-id="b77b7-105">The **replaceSelection** method replaces the current selection with the specified text.</span></span>

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a><span data-ttu-id="b77b7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b77b7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b77b7-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span><span class="sxs-lookup"><span data-stu-id="b77b7-107"><span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*</span></span>
</dt> <dd>

<span data-ttu-id="b77b7-108">**Строка** , содержащая текст для замены выделенного текста.</span><span class="sxs-lookup"><span data-stu-id="b77b7-108">**String** containing the text to replace the selected text.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b77b7-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b77b7-109">Return Value</span></span>

<span data-ttu-id="b77b7-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b77b7-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b77b7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b77b7-111">Remarks</span></span>

<span data-ttu-id="b77b7-112">Если текст не выбран, замещающий текст вставляется в текущую позицию курсора.</span><span class="sxs-lookup"><span data-stu-id="b77b7-112">If there is no text selected, the replacement text is inserted at the current location of the insertion point.</span></span>

<span data-ttu-id="b77b7-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="b77b7-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="b77b7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b77b7-114">Requirements</span></span>



| <span data-ttu-id="b77b7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b77b7-115">Requirement</span></span> | <span data-ttu-id="b77b7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b77b7-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="b77b7-117">Версия</span><span class="sxs-lookup"><span data-stu-id="b77b7-117">Version</span></span><br/> | <span data-ttu-id="b77b7-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b77b7-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b77b7-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b77b7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b77b7-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="b77b7-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="b77b7-121">**EDITBOX. Жетселектионенд**</span><span class="sxs-lookup"><span data-stu-id="b77b7-121">**EDITBOX.getSelectionEnd**</span></span>](editbox-getselectionend.md)
</dt> <dt>

[<span data-ttu-id="b77b7-122">**EDITBOX. Жетселектионстарт**</span><span class="sxs-lookup"><span data-stu-id="b77b7-122">**EDITBOX.getSelectionStart**</span></span>](editbox-getselectionstart.md)
</dt> <dt>

[<span data-ttu-id="b77b7-123">**EDITBOX. Сетселектион**</span><span class="sxs-lookup"><span data-stu-id="b77b7-123">**EDITBOX.setSelection**</span></span>](editbox-setselection.md)
</dt> </dl>

 

 





