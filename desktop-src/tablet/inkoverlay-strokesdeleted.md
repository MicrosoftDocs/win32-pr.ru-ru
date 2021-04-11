---
description: Происходит после удаления штрихов из свойства рукописного ввода.
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: Событие InkOverlay. Строкесделетед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264891"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="084e9-103">Событие InkOverlay. Строкесделетед</span><span class="sxs-lookup"><span data-stu-id="084e9-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="084e9-104">Происходит после удаления штрихов из свойства [**рукописного ввода**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) .</span><span class="sxs-lookup"><span data-stu-id="084e9-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="084e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="084e9-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="084e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="084e9-106">Parameters</span></span>

<span data-ttu-id="084e9-107">У этого события нет параметров.</span><span class="sxs-lookup"><span data-stu-id="084e9-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="084e9-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="084e9-108">Return value</span></span>

<span data-ttu-id="084e9-109">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="084e9-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="084e9-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="084e9-110">Remarks</span></span>

<span data-ttu-id="084e9-111">Данные событий отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="084e9-111">There is no event data.</span></span>

<span data-ttu-id="084e9-112">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоестрокесделетед.</span><span class="sxs-lookup"><span data-stu-id="084e9-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="084e9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="084e9-113">Requirements</span></span>



| <span data-ttu-id="084e9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="084e9-114">Requirement</span></span> | <span data-ttu-id="084e9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="084e9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="084e9-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="084e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="084e9-117">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="084e9-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="084e9-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="084e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="084e9-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="084e9-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="084e9-120">Header</span><span class="sxs-lookup"><span data-stu-id="084e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="084e9-121"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="084e9-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="084e9-122">Библиотека</span><span class="sxs-lookup"><span data-stu-id="084e9-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="084e9-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="084e9-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="084e9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="084e9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="084e9-125">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="084e9-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="084e9-126">[**Свойство рукописного ввода \[ класса InkCollector/InkOverLay\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="084e9-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




