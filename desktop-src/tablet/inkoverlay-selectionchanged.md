---
description: Происходит при изменении выделения рукописных данных в элементе управления, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: Событие InkOverlay. SelectionChanged (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703057"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="03d3d-103">Событие InkOverlay. SelectionChanged</span><span class="sxs-lookup"><span data-stu-id="03d3d-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="03d3d-104">Происходит при изменении выделения рукописных данных в элементе управления, например при внесении изменений в пользовательский интерфейс, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="03d3d-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="03d3d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03d3d-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="03d3d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03d3d-106">Parameters</span></span>

<span data-ttu-id="03d3d-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="03d3d-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="03d3d-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="03d3d-108">Return value</span></span>

<span data-ttu-id="03d3d-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="03d3d-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="03d3d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03d3d-110">Remarks</span></span>

<span data-ttu-id="03d3d-111">Данные событий отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="03d3d-111">There are no event data.</span></span>

<span data-ttu-id="03d3d-112">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектиончанжед.</span><span class="sxs-lookup"><span data-stu-id="03d3d-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="03d3d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="03d3d-113">Requirements</span></span>



| <span data-ttu-id="03d3d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="03d3d-114">Requirement</span></span> | <span data-ttu-id="03d3d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="03d3d-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03d3d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="03d3d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="03d3d-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="03d3d-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="03d3d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="03d3d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="03d3d-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="03d3d-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="03d3d-120">Header</span><span class="sxs-lookup"><span data-stu-id="03d3d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="03d3d-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="03d3d-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="03d3d-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="03d3d-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="03d3d-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03d3d-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="03d3d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="03d3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03d3d-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="03d3d-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="03d3d-126">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="03d3d-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




