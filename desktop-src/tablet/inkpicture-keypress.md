---
description: Происходит при нажатии клавиши, когда элемент управления InkPicture имеет фокус.
ms.assetid: adb61eff-a92c-40b0-940c-02e14cd34e5f
title: Событие InkPicture. KeyPress (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f9ef48a0e117d6a3d4c29a9ca69aba3bf6e054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991231"
---
# <a name="inkpicturekeypress-event"></a><span data-ttu-id="b21a9-103">Событие InkPicture. KeyPress</span><span class="sxs-lookup"><span data-stu-id="b21a9-103">InkPicture.KeyPress event</span></span>

<span data-ttu-id="b21a9-104">Происходит при нажатии клавиши, когда элемент управления [InkPicture](inkpicture-control-reference.md) имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="b21a9-104">Occurs when a key is pressed while the [InkPicture](inkpicture-control-reference.md) control has focus.</span></span>

## <a name="syntax"></a><span data-ttu-id="b21a9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b21a9-105">Syntax</span></span>


```C++
void KeyPress(
  [in, out] short *KeyAscii
);
```



## <a name="parameters"></a><span data-ttu-id="b21a9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b21a9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b21a9-107">*КэйасЦии* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="b21a9-107">*KeyAscii* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b21a9-108">Значение ASCII для нажатого клавиши.</span><span class="sxs-lookup"><span data-stu-id="b21a9-108">The ASCII value of the key that is being pressed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b21a9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b21a9-109">Return value</span></span>

<span data-ttu-id="b21a9-110">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b21a9-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b21a9-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b21a9-111">Remarks</span></span>

<span data-ttu-id="b21a9-112">Этот метод события определен в интерфейсе **\_ иинкпиктуривентс** .</span><span class="sxs-lookup"><span data-stu-id="b21a9-112">This event method is defined in the **\_IInkPictureEvents** interface.</span></span> <span data-ttu-id="b21a9-113">Интерфейс **\_ иинкпиктуривентс** реализует интерфейс [**IDISPATCH**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с идентификатором DISPID \_ ипекэйпресс.</span><span class="sxs-lookup"><span data-stu-id="b21a9-113">The **\_IInkPictureEvents** interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_IPEKeyPress.</span></span>

## <a name="requirements"></a><span data-ttu-id="b21a9-114">Требования</span><span class="sxs-lookup"><span data-stu-id="b21a9-114">Requirements</span></span>



| <span data-ttu-id="b21a9-115">Требование</span><span class="sxs-lookup"><span data-stu-id="b21a9-115">Requirement</span></span> | <span data-ttu-id="b21a9-116">Значение</span><span class="sxs-lookup"><span data-stu-id="b21a9-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b21a9-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b21a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b21a9-118">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="b21a9-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b21a9-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b21a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b21a9-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b21a9-120">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="b21a9-121">Header</span><span class="sxs-lookup"><span data-stu-id="b21a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b21a9-122"><dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="b21a9-122"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="b21a9-123">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b21a9-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b21a9-124"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b21a9-124"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="b21a9-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b21a9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b21a9-126">InkPicture</span><span class="sxs-lookup"><span data-stu-id="b21a9-126">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

