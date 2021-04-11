---
description: Происходит перед удалением штрихов из свойства рукописного ввода.
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: Событие InkOverlay. Строкесделетинг (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999261"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="ee637-103">Событие InkOverlay. Строкесделетинг</span><span class="sxs-lookup"><span data-stu-id="ee637-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="ee637-104">Происходит перед удалением штрихов из свойства [**рукописного ввода**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="ee637-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee637-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ee637-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="ee637-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ee637-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee637-107">*Штрихи* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ee637-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee637-108">Коллекция [инкстрокес](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) , удаленная при срабатывании события **строкесделетинг** .</span><span class="sxs-lookup"><span data-stu-id="ee637-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee637-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ee637-109">Return value</span></span>

<span data-ttu-id="ee637-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ee637-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee637-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ee637-111">Remarks</span></span>

<span data-ttu-id="ee637-112">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоестрокесделетинг.</span><span class="sxs-lookup"><span data-stu-id="ee637-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee637-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ee637-113">Requirements</span></span>



| <span data-ttu-id="ee637-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ee637-114">Requirement</span></span> | <span data-ttu-id="ee637-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ee637-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee637-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ee637-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ee637-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="ee637-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ee637-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ee637-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ee637-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ee637-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ee637-120">Header</span><span class="sxs-lookup"><span data-stu-id="ee637-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee637-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="ee637-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ee637-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ee637-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ee637-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee637-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ee637-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ee637-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee637-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="ee637-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="ee637-126">[**Свойство рукописного ввода \[ класса InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="ee637-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

