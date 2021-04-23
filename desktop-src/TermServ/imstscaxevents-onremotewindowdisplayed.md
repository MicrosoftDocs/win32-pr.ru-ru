---
title: Имстскаксевентс Онремотевиндовдисплайед, метод
description: Вызывается при отображении окна RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онремотевиндовдисплайед
- Службы удаленных рабочих столов метода Онремотевиндовдисплайед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онремотевиндовдисплайед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415756"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="04aa2-106">Метод Имстскаксевентс:: Онремотевиндовдисплайед</span><span class="sxs-lookup"><span data-stu-id="04aa2-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="04aa2-107">Вызывается при отображении окна RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="04aa2-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="04aa2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04aa2-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="04aa2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="04aa2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04aa2-110">*вбдисплайед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04aa2-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04aa2-111">Тип: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="04aa2-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="04aa2-112">Указывает, отображается ли окно RemoteApp или скрыто.</span><span class="sxs-lookup"><span data-stu-id="04aa2-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="04aa2-113">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04aa2-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04aa2-114">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="04aa2-114">Type: **HWND**</span></span>

<span data-ttu-id="04aa2-115">Отображаемый маркер окна.</span><span class="sxs-lookup"><span data-stu-id="04aa2-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="04aa2-116">*виндоваттрибуте* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="04aa2-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04aa2-117">Тип: **[ **ремотевиндовдисплайедаттрибуте**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="04aa2-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="04aa2-118">Значение перечисления [**ремотевиндовдисплайедаттрибуте**](remotewindowdisplayedattribute.md) , которое указывает дополнительные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="04aa2-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04aa2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04aa2-119">Return value</span></span>

<span data-ttu-id="04aa2-120">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="04aa2-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="04aa2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="04aa2-121">Requirements</span></span>



| <span data-ttu-id="04aa2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="04aa2-122">Requirement</span></span> | <span data-ttu-id="04aa2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="04aa2-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04aa2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04aa2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="04aa2-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="04aa2-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="04aa2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04aa2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="04aa2-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04aa2-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="04aa2-128">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="04aa2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="04aa2-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04aa2-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="04aa2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="04aa2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04aa2-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04aa2-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04aa2-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="04aa2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04aa2-133">**ремотевиндовдисплайедаттрибуте**</span><span class="sxs-lookup"><span data-stu-id="04aa2-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="04aa2-134">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="04aa2-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





