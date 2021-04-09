---
description: Происходит перед удалением объектов Иинкстрокедисп из свойства Ink.
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: Событие InkPicture. Строкесделетинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081246"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="07ebc-103">Событие InkPicture. Строкесделетинг</span><span class="sxs-lookup"><span data-stu-id="07ebc-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="07ebc-104">Происходит перед удалением объектов [**иинкстрокедисп**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) из свойства [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="07ebc-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="07ebc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07ebc-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="07ebc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="07ebc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07ebc-107">*Штрихи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="07ebc-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07ebc-108">Коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , удаленная при срабатывании события **строкесделетинг** .</span><span class="sxs-lookup"><span data-stu-id="07ebc-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07ebc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="07ebc-109">Return value</span></span>

<span data-ttu-id="07ebc-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="07ebc-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07ebc-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07ebc-111">Remarks</span></span>

<span data-ttu-id="07ebc-112">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоестрокесделетинг.</span><span class="sxs-lookup"><span data-stu-id="07ebc-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="07ebc-113">Требования</span><span class="sxs-lookup"><span data-stu-id="07ebc-113">Requirements</span></span>



| <span data-ttu-id="07ebc-114">Требование</span><span class="sxs-lookup"><span data-stu-id="07ebc-114">Requirement</span></span> | <span data-ttu-id="07ebc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="07ebc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07ebc-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07ebc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07ebc-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="07ebc-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="07ebc-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07ebc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07ebc-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07ebc-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="07ebc-120">Header</span><span class="sxs-lookup"><span data-stu-id="07ebc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07ebc-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="07ebc-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="07ebc-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="07ebc-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="07ebc-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07ebc-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="07ebc-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07ebc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07ebc-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="07ebc-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

