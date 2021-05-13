---
description: Вызывается при отмене регистрации окна оболочки.
title: Дшеллвиндовсевентс. Виндовревокед, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843185"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="a0af7-103">Дшеллвиндовсевентс. Виндовревокед, метод</span><span class="sxs-lookup"><span data-stu-id="a0af7-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="a0af7-104">Вызывается при отмене регистрации окна оболочки.</span><span class="sxs-lookup"><span data-stu-id="a0af7-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0af7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0af7-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="a0af7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0af7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0af7-107">*лкукие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a0af7-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0af7-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="a0af7-108">Type: **Integer**</span></span>

<span data-ttu-id="a0af7-109">Файл cookie, определяющий отозванное окно.</span><span class="sxs-lookup"><span data-stu-id="a0af7-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0af7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a0af7-110">Return value</span></span>

<span data-ttu-id="a0af7-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a0af7-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0af7-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="a0af7-112">Remarks</span></span>

<span data-ttu-id="a0af7-113">При регистрации в окне оболочки ему предоставляется файл cookie.</span><span class="sxs-lookup"><span data-stu-id="a0af7-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="a0af7-114">Дополнительные сведения см. в разделе [**Регистрация**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="a0af7-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="a0af7-115">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="a0af7-115">Requirements</span></span>



| <span data-ttu-id="a0af7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a0af7-116">Requirement</span></span> | <span data-ttu-id="a0af7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a0af7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0af7-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="a0af7-118">Product</span></span><br/> | <span data-ttu-id="a0af7-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="a0af7-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="a0af7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a0af7-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="a0af7-121"><dt>Shdocvw.dll (версия 5.00.2014.0216 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="a0af7-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0af7-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a0af7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0af7-123">**дшеллвиндовсевентс**</span><span class="sxs-lookup"><span data-stu-id="a0af7-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="a0af7-124">**виндоврегистеред**</span><span class="sxs-lookup"><span data-stu-id="a0af7-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="a0af7-125">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="a0af7-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




