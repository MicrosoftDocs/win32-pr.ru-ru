---
description: Происходит при освобождении ключа, когда элемент управления InkPicture имеет фокус.
ms.assetid: e22633b5-40fe-4b94-a660-684c4f5c96f3
title: Событие InkPicture. KeyUp (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2390b6cbb7b91ab8e447df912e591ea37248e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712363"
---
# <a name="inkpicturekeyup-event"></a><span data-ttu-id="921ae-103">Событие InkPicture. KeyUp</span><span class="sxs-lookup"><span data-stu-id="921ae-103">InkPicture.KeyUp event</span></span>

<span data-ttu-id="921ae-104">Происходит при освобождении ключа, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="921ae-104">Occurs when a key is released while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="921ae-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="921ae-105">Syntax</span></span>


```C++
void KeyUp(
  [in, out] short *KeyCode,
  [in, out] short *Shift
);
```



## <a name="parameters"></a><span data-ttu-id="921ae-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="921ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="921ae-107">*KeyCode* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="921ae-107">*KeyCode* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="921ae-108">Значение ASCII для нажатого клавиши.</span><span class="sxs-lookup"><span data-stu-id="921ae-108">The ASCII value of the key that is being pressed.</span></span>

</dd> <dt>

<span data-ttu-id="921ae-109">*SHIFT* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="921ae-109">*Shift* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="921ae-110">Состояние клавиши SHIFT.</span><span class="sxs-lookup"><span data-stu-id="921ae-110">The state of the SHIFT key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="921ae-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="921ae-111">Return value</span></span>

<span data-ttu-id="921ae-112">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="921ae-112">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="921ae-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="921ae-113">Remarks</span></span>

<span data-ttu-id="921ae-114">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="921ae-114">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="921ae-115">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйуп.</span><span class="sxs-lookup"><span data-stu-id="921ae-115">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyUp.</span></span>

## <a name="requirements"></a><span data-ttu-id="921ae-116">Требования</span><span class="sxs-lookup"><span data-stu-id="921ae-116">Requirements</span></span>



| <span data-ttu-id="921ae-117">Требование</span><span class="sxs-lookup"><span data-stu-id="921ae-117">Requirement</span></span> | <span data-ttu-id="921ae-118">Значение</span><span class="sxs-lookup"><span data-stu-id="921ae-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="921ae-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="921ae-119">Minimum supported client</span></span><br/> | <span data-ttu-id="921ae-120">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="921ae-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="921ae-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="921ae-121">Minimum supported server</span></span><br/> | <span data-ttu-id="921ae-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="921ae-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="921ae-123">Header</span><span class="sxs-lookup"><span data-stu-id="921ae-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="921ae-124"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="921ae-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="921ae-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="921ae-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="921ae-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="921ae-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="921ae-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="921ae-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="921ae-128">InkPicture</span><span class="sxs-lookup"><span data-stu-id="921ae-128">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

