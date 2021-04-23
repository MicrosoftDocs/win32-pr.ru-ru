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
ms.openlocfilehash: b036bdde2916c2fa037d1b6e286a2096d9e1d8bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987602"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="04a9f-103">Дшеллвиндовсевентс. Виндовревокед, метод</span><span class="sxs-lookup"><span data-stu-id="04a9f-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="04a9f-104">Вызывается при отмене регистрации окна оболочки.</span><span class="sxs-lookup"><span data-stu-id="04a9f-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="04a9f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04a9f-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="04a9f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04a9f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04a9f-107">*лкукие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04a9f-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04a9f-108">Тип: **Integer**</span><span class="sxs-lookup"><span data-stu-id="04a9f-108">Type: **Integer**</span></span>

<span data-ttu-id="04a9f-109">Файл cookie, определяющий отозванное окно.</span><span class="sxs-lookup"><span data-stu-id="04a9f-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04a9f-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04a9f-110">Return value</span></span>

<span data-ttu-id="04a9f-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04a9f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04a9f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="04a9f-112">Remarks</span></span>

<span data-ttu-id="04a9f-113">При регистрации в окне оболочки ему предоставляется файл cookie.</span><span class="sxs-lookup"><span data-stu-id="04a9f-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="04a9f-114">Дополнительные сведения см. в разделе [**Регистрация**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span><span class="sxs-lookup"><span data-stu-id="04a9f-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="04a9f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="04a9f-115">Requirements</span></span>



| <span data-ttu-id="04a9f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="04a9f-116">Requirement</span></span> | <span data-ttu-id="04a9f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="04a9f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04a9f-118">Продукт</span><span class="sxs-lookup"><span data-stu-id="04a9f-118">Product</span></span><br/> | <span data-ttu-id="04a9f-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="04a9f-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="04a9f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="04a9f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="04a9f-121"><dt>Shdocvw.dll (версия 5.00.2014.0216 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="04a9f-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04a9f-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04a9f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04a9f-123">**дшеллвиндовсевентс**</span><span class="sxs-lookup"><span data-stu-id="04a9f-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="04a9f-124">**виндоврегистеред**</span><span class="sxs-lookup"><span data-stu-id="04a9f-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="04a9f-125">**Revoke**</span><span class="sxs-lookup"><span data-stu-id="04a9f-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




