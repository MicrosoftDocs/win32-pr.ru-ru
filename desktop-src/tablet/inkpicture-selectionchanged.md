---
description: Происходит при изменении выделения рукописных данных в элементе управления InkPicture, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: Событие InkPicture. SelectionChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656687"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="79094-103">Событие InkPicture. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="79094-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="79094-104">Происходит при изменении выделения рукописных данных в элементе управления [InkPicture](inkpicture-control-reference.md) , например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="79094-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="79094-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79094-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="79094-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="79094-106">Parameters</span></span>

<span data-ttu-id="79094-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="79094-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79094-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79094-108">Return value</span></span>

<span data-ttu-id="79094-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="79094-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79094-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79094-110">Remarks</span></span>

<span data-ttu-id="79094-111">Дополнительные сведения об этом событии см. в описании события [**SelectionChanged**](inkoverlay-selectionchanged.md) объекта [**InkOverlay**](inkoverlay-class.md) , имеющего те же функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="79094-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="79094-112">Требования</span><span class="sxs-lookup"><span data-stu-id="79094-112">Requirements</span></span>



| <span data-ttu-id="79094-113">Требование</span><span class="sxs-lookup"><span data-stu-id="79094-113">Requirement</span></span> | <span data-ttu-id="79094-114">Значение</span><span class="sxs-lookup"><span data-stu-id="79094-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79094-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79094-115">Minimum supported client</span></span><br/> | <span data-ttu-id="79094-116">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="79094-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="79094-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79094-117">Minimum supported server</span></span><br/> | <span data-ttu-id="79094-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79094-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="79094-119">Header</span><span class="sxs-lookup"><span data-stu-id="79094-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="79094-120"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="79094-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="79094-121">Библиотека</span><span class="sxs-lookup"><span data-stu-id="79094-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="79094-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79094-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="79094-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79094-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79094-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="79094-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="79094-125">[**\[Элемент управления InkPicture свойства Selection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="79094-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




