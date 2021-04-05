---
title: Имстскаксевентс Онмаусеинпутмодечанжед, метод
description: Вызывается при изменении режима ввода с помощью мыши.
ms.assetid: d0554c59-967d-4181-98cd-9e88dde32752
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Онмаусеинпутмодечанжед
- Службы удаленных рабочих столов метода Онмаусеинпутмодечанжед, интерфейс Имстскаксевентс
- Службы удаленных рабочих столов интерфейса Имстскаксевентс, метод Онмаусеинпутмодечанжед
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnMouseInputModeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dbfef19aa79ba634a13d92b8d11866b8016e893
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136326"
---
# <a name="imstscaxeventsonmouseinputmodechanged-method"></a><span data-ttu-id="4f101-106">Метод Имстскаксевентс:: Онмаусеинпутмодечанжед</span><span class="sxs-lookup"><span data-stu-id="4f101-106">IMsTscAxEvents::OnMouseInputModeChanged method</span></span>

<span data-ttu-id="4f101-107">Вызывается при изменении режима ввода с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="4f101-107">Called when the mouse input mode has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f101-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f101-108">Syntax</span></span>


```C++
void OnMouseInputModeChanged(
  [in] VARIANT_BOOL fMouseModeRelative
);
```



## <a name="parameters"></a><span data-ttu-id="4f101-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f101-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f101-110">*фмаусемодерелативе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f101-110">*fMouseModeRelative* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f101-111">Указывает, находится ли указатель мыши в относительном режиме.</span><span class="sxs-lookup"><span data-stu-id="4f101-111">Indicates whether the mouse is in relative mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f101-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f101-112">Return value</span></span>

<span data-ttu-id="4f101-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4f101-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f101-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f101-114">Remarks</span></span>

<span data-ttu-id="4f101-115">Реализуйте этот метод в приемнике событий, чтобы получить уведомление о том, что режим ввода мыши изменился.</span><span class="sxs-lookup"><span data-stu-id="4f101-115">Implement this method in your event sink to receive notification that the mouse input mode has changed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f101-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4f101-116">Requirements</span></span>



| <span data-ttu-id="4f101-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4f101-117">Requirement</span></span> | <span data-ttu-id="4f101-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4f101-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f101-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f101-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4f101-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f101-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4f101-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f101-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4f101-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f101-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4f101-123">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="4f101-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="4f101-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f101-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f101-125">DLL</span><span class="sxs-lookup"><span data-stu-id="4f101-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f101-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f101-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f101-127">IID</span><span class="sxs-lookup"><span data-stu-id="4f101-127">IID</span></span><br/>                      | <span data-ttu-id="4f101-128">Имстскаксевентс определяется как 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="4f101-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4f101-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f101-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f101-130">**имстскаксевентс**</span><span class="sxs-lookup"><span data-stu-id="4f101-130">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





