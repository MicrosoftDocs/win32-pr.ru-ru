---
title: Список воспроизведения. sortColumn
description: Метод sortColumn сортирует данные в указанном столбце.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Проигрыватель Windows Media Player. sortColumn
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718169"
---
# <a name="playlistsortcolumn"></a><span data-ttu-id="6df7b-104">Список воспроизведения. sortColumn</span><span class="sxs-lookup"><span data-stu-id="6df7b-104">PLAYLIST.sortColumn</span></span>

<span data-ttu-id="6df7b-105">Метод **sortColumn** сортирует данные в указанном столбце.</span><span class="sxs-lookup"><span data-stu-id="6df7b-105">The **sortColumn** method sorts the data in the specified column.</span></span>

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a><span data-ttu-id="6df7b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6df7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6df7b-107"><span id="column"></span><span id="COLUMN"></span>*рубрик*</span><span class="sxs-lookup"><span data-stu-id="6df7b-107"><span id="column"></span><span id="COLUMN"></span>*column*</span></span>
</dt> <dd>

<span data-ttu-id="6df7b-108">**Число** (**Long**), указывающее индекс столбца для сортировки.</span><span class="sxs-lookup"><span data-stu-id="6df7b-108">**Number** (**long**) indicating the index of the column to sort.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6df7b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6df7b-109">Return Value</span></span>

<span data-ttu-id="6df7b-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="6df7b-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6df7b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6df7b-111">Remarks</span></span>

<span data-ttu-id="6df7b-112">Этот метод сортирует указанный столбец так же, как кнопки заголовка столбца в элементе **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="6df7b-112">This method sorts the specified column in the same way as the column header buttons in the **PLAYLIST** element.</span></span> <span data-ttu-id="6df7b-113">Если столбец еще не отсортирован, он сортируется в алфавитно-цифровом порядке.</span><span class="sxs-lookup"><span data-stu-id="6df7b-113">If the column has not yet been sorted, it is sorted in alphanumeric order.</span></span> <span data-ttu-id="6df7b-114">Если сортировка выполнена, ее порядок изменяется на обратный.</span><span class="sxs-lookup"><span data-stu-id="6df7b-114">If it has been sorted, its order is reversed.</span></span>

<span data-ttu-id="6df7b-115">Чтобы этот метод работал, атрибуту **алловколумнсортинг** должно быть присвоено значение true.</span><span class="sxs-lookup"><span data-stu-id="6df7b-115">For this method to work, the **allowColumnSorting** attribute must be set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="6df7b-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6df7b-116">Requirements</span></span>



| <span data-ttu-id="6df7b-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6df7b-117">Requirement</span></span> | <span data-ttu-id="6df7b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6df7b-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6df7b-119">Версия</span><span class="sxs-lookup"><span data-stu-id="6df7b-119">Version</span></span><br/> | <span data-ttu-id="6df7b-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="6df7b-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6df7b-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6df7b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6df7b-122">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="6df7b-122">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="6df7b-123">**Список воспроизведения. Алловколумнсортинг**</span><span class="sxs-lookup"><span data-stu-id="6df7b-123">**PLAYLIST.allowColumnSorting**</span></span>](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





