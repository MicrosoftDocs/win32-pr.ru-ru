---
title: EDITBOX. Жетлинеиндекс
description: Метод Жетлинеиндекс извлекает индекс символа первого символа в строке с указанным индексом строки.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- Жетлинеиндекс Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699274"
---
# <a name="editboxgetlineindex"></a><span data-ttu-id="11598-104">EDITBOX. Жетлинеиндекс</span><span class="sxs-lookup"><span data-stu-id="11598-104">EDITBOX.getLineIndex</span></span>

<span data-ttu-id="11598-105">Метод **жетлинеиндекс** извлекает индекс символа первого символа в строке с указанным индексом строки.</span><span class="sxs-lookup"><span data-stu-id="11598-105">The **getLineIndex** method retrieves the character index of the first character on the line with the specified line index.</span></span>

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a><span data-ttu-id="11598-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="11598-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11598-107"><span id="index"></span><span id="INDEX"></span>*номер*</span><span class="sxs-lookup"><span data-stu-id="11598-107"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="11598-108">**Число** (**Long**), содержащее индекс строки, индекс которой необходимо получить.</span><span class="sxs-lookup"><span data-stu-id="11598-108">**Number** (**long**) containing the index of the line whose character index is to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11598-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11598-109">Return Value</span></span>

<span data-ttu-id="11598-110">Этот метод возвращает **число** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="11598-110">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="11598-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11598-111">Remarks</span></span>

<span data-ttu-id="11598-112">Если указанный индекс строки равен 1, то используется строка, содержащая точку вставки.</span><span class="sxs-lookup"><span data-stu-id="11598-112">If the specified line index is  1, the line containing the insertion point is used.</span></span>

<span data-ttu-id="11598-113">Этот метод может быть вызван только после того, как элемент управления станет видимым.</span><span class="sxs-lookup"><span data-stu-id="11598-113">This method can only be called after the control becomes visible.</span></span>

## <a name="requirements"></a><span data-ttu-id="11598-114">Требования</span><span class="sxs-lookup"><span data-stu-id="11598-114">Requirements</span></span>



| <span data-ttu-id="11598-115">Требование</span><span class="sxs-lookup"><span data-stu-id="11598-115">Requirement</span></span> | <span data-ttu-id="11598-116">Значение</span><span class="sxs-lookup"><span data-stu-id="11598-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="11598-117">Версия</span><span class="sxs-lookup"><span data-stu-id="11598-117">Version</span></span><br/> | <span data-ttu-id="11598-118">Проигрыватель Windows Media для Windows XP или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="11598-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11598-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11598-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11598-120">**EDITBOX, элемент**</span><span class="sxs-lookup"><span data-stu-id="11598-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="11598-121">**EDITBOX. в строке**</span><span class="sxs-lookup"><span data-stu-id="11598-121">**EDITBOX.getLine**</span></span>](editbox-getline.md)
</dt> <dt>

[<span data-ttu-id="11598-122">**EDITBOX. Жетлинефромчар**</span><span class="sxs-lookup"><span data-stu-id="11598-122">**EDITBOX.getLineFromChar**</span></span>](editbox-getlinefromchar.md)
</dt> </dl>

 

 





