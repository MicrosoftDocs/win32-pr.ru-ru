---
description: Происходит до завершения перерисовки объекта InkOverlay или InkPicture.
ms.assetid: abfd37fb-2d2b-4d60-96a1-08f68b73417b
title: Событие InkOverlay. Painting (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fc056667f88c0631e84a76767fc97f90ca05a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546562"
---
# <a name="inkoverlaypainting-event"></a><span data-ttu-id="9a7bf-103">Событие InkOverlay. Paint</span><span class="sxs-lookup"><span data-stu-id="9a7bf-103">InkOverlay.Painting event</span></span>

<span data-ttu-id="9a7bf-104">Происходит до завершения перерисовки объекта [**InkOverlay**](inkoverlay-class.md) или [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="9a7bf-104">Occurs before the [**InkOverlay**](inkoverlay-class.md) object or [InkPicture](inkpicture-control-reference.md) has completed redrawing itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7bf-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a7bf-105">Syntax</span></span>


```C++
void Painting(
  [in]      long          hDC,
  [in]      IInkRectangle *Rect,
  [in, out] VARIANT_BOOL  *Allow
);
```



## <a name="parameters"></a><span data-ttu-id="9a7bf-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9a7bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a7bf-107">*HDC* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a7bf-107">*hDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7bf-108">Контекст устройства, на котором будет происходить рисование.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-108">The device context on which painting will occur.</span></span>

</dd> <dt>

<span data-ttu-id="9a7bf-109">*Rect* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9a7bf-109">*Rect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7bf-110">Прямоугольник, который необходимо перерисовать.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-110">The rectangle that is to be repainted.</span></span>

</dd> <dt>

<span data-ttu-id="9a7bf-111">*Разрешить* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9a7bf-111">*Allow* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a7bf-112">Будет ли происходить перерисовка.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-112">Whether the repaint will occur.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a7bf-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9a7bf-113">Return value</span></span>

<span data-ttu-id="9a7bf-114">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a7bf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9a7bf-115">Remarks</span></span>

<span data-ttu-id="9a7bf-116">Этот метод события определен в \_ \_ интерфейсах диспетчеризации иинковерлайевентс и иинкпиктуривентс (DISP) с идентификатором DISPID \_ иоепаинтинг.</span><span class="sxs-lookup"><span data-stu-id="9a7bf-116">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEPainting.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7bf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9a7bf-117">Requirements</span></span>



| <span data-ttu-id="9a7bf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9a7bf-118">Requirement</span></span> | <span data-ttu-id="9a7bf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9a7bf-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7bf-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9a7bf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7bf-121">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9a7bf-121">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="9a7bf-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9a7bf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7bf-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9a7bf-123">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="9a7bf-124">Header</span><span class="sxs-lookup"><span data-stu-id="9a7bf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7bf-125"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9a7bf-125"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9a7bf-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9a7bf-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a7bf-127"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7bf-127"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="9a7bf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a7bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7bf-129">**Класс InkOverlay**</span><span class="sxs-lookup"><span data-stu-id="9a7bf-129">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> </dl>

 

 




