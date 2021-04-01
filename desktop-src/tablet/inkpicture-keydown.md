---
description: Происходит при нажатии клавиши и в расположении вниз, пока элемент управления InkPicture находится в фокусе.
ms.assetid: d83823ea-d863-4eb7-8f6b-fa7a3396e64b
title: Событие InkPicture. KeyDown (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5d6bd3555aeec98ac28555c1674dfef32ecc53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081590"
---
# <a name="inkpicturekeydown-event"></a><span data-ttu-id="dcef8-103">Событие InkPicture. KeyDown</span><span class="sxs-lookup"><span data-stu-id="dcef8-103">InkPicture.KeyDown event</span></span>

<span data-ttu-id="dcef8-104">Происходит при нажатии клавиши и в расположении вниз, пока элемент управления [InkPicture](inkpicture-control-reference.md) находится в фокусе.</span><span class="sxs-lookup"><span data-stu-id="dcef8-104">Occurs when a key is pressed and in the down position while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcef8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dcef8-105">Syntax</span></span>


```C++
void KeyDown(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="dcef8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcef8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcef8-107">*KeyCode* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dcef8-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcef8-108">Значение ASCII для нажатого клавиши.</span><span class="sxs-lookup"><span data-stu-id="dcef8-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="dcef8-109">*SHIFT* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="dcef8-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dcef8-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="dcef8-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcef8-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcef8-111">Return value</span></span>

<span data-ttu-id="dcef8-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dcef8-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcef8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcef8-113">Remarks</span></span>

<span data-ttu-id="dcef8-114">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="dcef8-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="dcef8-115">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйдовн.</span><span class="sxs-lookup"><span data-stu-id="dcef8-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyDown.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcef8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="dcef8-116">Requirements</span></span>



| <span data-ttu-id="dcef8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="dcef8-117">Requirement</span></span> | <span data-ttu-id="dcef8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dcef8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcef8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcef8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcef8-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="dcef8-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="dcef8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcef8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcef8-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="dcef8-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="dcef8-123">Header</span><span class="sxs-lookup"><span data-stu-id="dcef8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="dcef8-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="dcef8-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="dcef8-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="dcef8-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="dcef8-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcef8-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="dcef8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcef8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcef8-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="dcef8-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

