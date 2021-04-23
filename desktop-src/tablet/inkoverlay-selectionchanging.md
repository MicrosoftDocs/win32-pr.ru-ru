---
description: Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при выборе свойства Selection.
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: Событие InkOverlay. Селектиончангинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693466"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="bed0c-103">Событие InkOverlay. Селектиончангинг</span><span class="sxs-lookup"><span data-stu-id="bed0c-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="bed0c-104">Происходит при изменении выделения рукописных данных в элементе управления, например при выполнении изменений в пользовательском интерфейсе, процедурах вырезания и вставки или при [**выборе свойства Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) .</span><span class="sxs-lookup"><span data-stu-id="bed0c-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="bed0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bed0c-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="bed0c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bed0c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bed0c-107">*Невселектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bed0c-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bed0c-108">Новая коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , которая выбрана.</span><span class="sxs-lookup"><span data-stu-id="bed0c-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bed0c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bed0c-109">Return value</span></span>

<span data-ttu-id="bed0c-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bed0c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bed0c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bed0c-111">Remarks</span></span>

<span data-ttu-id="bed0c-112">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоеселектиончангинг.</span><span class="sxs-lookup"><span data-stu-id="bed0c-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="bed0c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bed0c-113">Requirements</span></span>



| <span data-ttu-id="bed0c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="bed0c-114">Requirement</span></span> | <span data-ttu-id="bed0c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="bed0c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bed0c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bed0c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bed0c-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="bed0c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bed0c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bed0c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bed0c-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="bed0c-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="bed0c-120">Header</span><span class="sxs-lookup"><span data-stu-id="bed0c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bed0c-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="bed0c-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="bed0c-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bed0c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="bed0c-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bed0c-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="bed0c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bed0c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bed0c-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="bed0c-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="bed0c-126">**Свойство Selection**</span><span class="sxs-lookup"><span data-stu-id="bed0c-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

