---
description: Вызывается, когда окно регистрируется как окно оболочки.
title: Дшеллвиндовсевентс. Виндоврегистеред, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987590"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="61f5f-103">Дшеллвиндовсевентс. Виндоврегистеред, метод</span><span class="sxs-lookup"><span data-stu-id="61f5f-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="61f5f-104">Вызывается, когда окно регистрируется как окно оболочки.</span><span class="sxs-lookup"><span data-stu-id="61f5f-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f5f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61f5f-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="61f5f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="61f5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61f5f-107">*лкукие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="61f5f-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61f5f-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="61f5f-108">Type: **Integer**</span></span>

<span data-ttu-id="61f5f-109">Файл cookie, определяющий зарегистрированное окно.</span><span class="sxs-lookup"><span data-stu-id="61f5f-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61f5f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="61f5f-110">Return value</span></span>

<span data-ttu-id="61f5f-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="61f5f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61f5f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="61f5f-112">Remarks</span></span>

<span data-ttu-id="61f5f-113">При регистрации в окне оболочки ему предоставляется файл cookie.</span><span class="sxs-lookup"><span data-stu-id="61f5f-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="61f5f-114">Дополнительные сведения см. в разделе [**Регистрация**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="61f5f-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="61f5f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="61f5f-115">Requirements</span></span>



| <span data-ttu-id="61f5f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="61f5f-116">Requirement</span></span> | <span data-ttu-id="61f5f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="61f5f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61f5f-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="61f5f-118">Product</span></span><br/> | <span data-ttu-id="61f5f-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="61f5f-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="61f5f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="61f5f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="61f5f-121"><dt>Shdocvw.dll (версия 5.00.2014.0216 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="61f5f-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61f5f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61f5f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61f5f-123">**дшеллвиндовсевентс**</span><span class="sxs-lookup"><span data-stu-id="61f5f-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="61f5f-124">**виндовревокед**</span><span class="sxs-lookup"><span data-stu-id="61f5f-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="61f5f-125">**Регистрация**</span><span class="sxs-lookup"><span data-stu-id="61f5f-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="61f5f-126">**регистерпендинг**</span><span class="sxs-lookup"><span data-stu-id="61f5f-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




