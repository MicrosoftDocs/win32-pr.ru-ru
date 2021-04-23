---
description: Происходит перед перерисовкой элемента управления InkPicture.
ms.assetid: 97d017ce-fdab-49e5-9ea6-0bcc5d7b14fb
title: Событие InkPicture. Painting (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc76bbf3079d61c84ac14d1b22690d645a7cce4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265067"
---
# <a name="inkpicturepainting-event"></a><span data-ttu-id="92dcc-103">Событие InkPicture. Paint</span><span class="sxs-lookup"><span data-stu-id="92dcc-103">InkPicture.Painting event</span></span>

<span data-ttu-id="92dcc-104">Происходит перед перерисовкой элемента управления [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="92dcc-104">Occurs before the [InkPicture](inkpicture-control-reference.md) control redraws itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="92dcc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92dcc-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="92dcc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92dcc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92dcc-107">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92dcc-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92dcc-108">Контекст устройства, на котором будет происходить рисование.</span><span class="sxs-lookup"><span data-stu-id="92dcc-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="92dcc-109">*Rect* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="92dcc-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92dcc-110">Прямоугольник рукописного ввода, который необходимо перерисовать.</span><span class="sxs-lookup"><span data-stu-id="92dcc-110">The ink rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="92dcc-111">*Разрешить* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="92dcc-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="92dcc-112">Будет ли происходить перерисовка.</span><span class="sxs-lookup"><span data-stu-id="92dcc-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92dcc-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92dcc-113">Return value</span></span>

<span data-ttu-id="92dcc-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="92dcc-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92dcc-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92dcc-115">Remarks</span></span>

<span data-ttu-id="92dcc-116">Этот метод события определен в интерфейсах диспетчеризации **\_ иинковерлайевентс** и **\_ ИИНКПИКТУРИВЕНТС** (DISP) с идентификатором DISPID \_ иоепаинтинг.</span><span class="sxs-lookup"><span data-stu-id="92dcc-116">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="92dcc-117">Требования</span><span class="sxs-lookup"><span data-stu-id="92dcc-117">Requirements</span></span>



| <span data-ttu-id="92dcc-118">Требование</span><span class="sxs-lookup"><span data-stu-id="92dcc-118">Requirement</span></span> | <span data-ttu-id="92dcc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="92dcc-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92dcc-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92dcc-120">Minimum supported client</span></span><br/> | <span data-ttu-id="92dcc-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="92dcc-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92dcc-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92dcc-122">Minimum supported server</span></span><br/> | <span data-ttu-id="92dcc-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="92dcc-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="92dcc-124">Header</span><span class="sxs-lookup"><span data-stu-id="92dcc-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="92dcc-125"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="92dcc-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92dcc-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="92dcc-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="92dcc-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92dcc-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="92dcc-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92dcc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92dcc-129">InkPicture</span><span class="sxs-lookup"><span data-stu-id="92dcc-129">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




