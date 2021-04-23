---
description: Происходит при наличии системного события.
ms.assetid: 3d9e98f0-b11e-4a65-a544-9e1998a80d5f
title: 'Метод Итаблетевентсинк:: Системевент'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletEventSink.SystemEvent
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 71b5882fd9e19df43581e00cce55c2af5faa432b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647487"
---
# <a name="itableteventsinksystemevent-method"></a><span data-ttu-id="27565-103">Метод Итаблетевентсинк:: Системевент</span><span class="sxs-lookup"><span data-stu-id="27565-103">ITabletEventSink::SystemEvent method</span></span>

<span data-ttu-id="27565-104">Происходит при наличии системного события.</span><span class="sxs-lookup"><span data-stu-id="27565-104">Occurs when a system event is available.</span></span>

## <a name="syntax"></a><span data-ttu-id="27565-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="27565-105">Syntax</span></span>


```C++
HRESULT SystemEvent(
  [in] TABLET_CONTEXT_ID tcid,
  [in] CURSOR_ID         cid,
  [in] SYSTEM_EVENT      event,
  [in] SYSTEM_EVENT_DATA eventdata
);
```



## <a name="parameters"></a><span data-ttu-id="27565-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="27565-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27565-107">*тЦид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27565-107">*tcid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27565-108">Идентификатор планшета.</span><span class="sxs-lookup"><span data-stu-id="27565-108">The identifier of the tablet.</span></span>

</dd> <dt>

<span data-ttu-id="27565-109">*CID* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="27565-109">*cid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27565-110">Идентификатор пера.</span><span class="sxs-lookup"><span data-stu-id="27565-110">The identifier of the stylus.</span></span>

</dd> <dt>

<span data-ttu-id="27565-111">*событие* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27565-111">*event* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27565-112">Код системного события.</span><span class="sxs-lookup"><span data-stu-id="27565-112">The system event code.</span></span>

</dd> <dt>

<span data-ttu-id="27565-113">*EVENTDATA* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="27565-113">*eventdata* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27565-114">Данные системных событий.</span><span class="sxs-lookup"><span data-stu-id="27565-114">The system event data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27565-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="27565-115">Return value</span></span>

<span data-ttu-id="27565-116">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="27565-116">This method can return one of these values.</span></span>



| <span data-ttu-id="27565-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="27565-117">Return code</span></span>                                                                            | <span data-ttu-id="27565-118">Описание</span><span class="sxs-lookup"><span data-stu-id="27565-118">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="27565-119"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="27565-119"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="27565-120">Успешно.</span><span class="sxs-lookup"><span data-stu-id="27565-120">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="27565-121"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="27565-121"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="27565-122">Произошла неизвестная ошибка.</span><span class="sxs-lookup"><span data-stu-id="27565-122">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="27565-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27565-123">Remarks</span></span>

<span data-ttu-id="27565-124">Следующий список содержит допустимые значения для параметра события.</span><span class="sxs-lookup"><span data-stu-id="27565-124">The following list contains the valid values for the event parameter.</span></span>

-   <span data-ttu-id="27565-125">\_касание SE</span><span class="sxs-lookup"><span data-stu-id="27565-125">SE\_TAP</span></span>
-   <span data-ttu-id="27565-126">SE \_ Двойное \_ касание</span><span class="sxs-lookup"><span data-stu-id="27565-126">SE\_DBL\_TAP</span></span>
-   <span data-ttu-id="27565-127">SE, \_ правое \_ касание</span><span class="sxs-lookup"><span data-stu-id="27565-127">SE\_RIGHT\_TAP</span></span>
-   <span data-ttu-id="27565-128">SE, \_ перетаскивание</span><span class="sxs-lookup"><span data-stu-id="27565-128">SE\_DRAG</span></span>
-   <span data-ttu-id="27565-129">SE \_ , \_ перетаскивание</span><span class="sxs-lookup"><span data-stu-id="27565-129">SE\_RIGHT\_DRAG</span></span>
-   <span data-ttu-id="27565-130">SE, \_ удержание \_ Ввод</span><span class="sxs-lookup"><span data-stu-id="27565-130">SE\_HOLD\_ENTER</span></span>
-   <span data-ttu-id="27565-131">SE, \_ удержание \_ оставить</span><span class="sxs-lookup"><span data-stu-id="27565-131">SE\_HOLD\_LEAVE</span></span>
-   <span data-ttu-id="27565-132">SE. \_ Ввод с наведением \_</span><span class="sxs-lookup"><span data-stu-id="27565-132">SE\_HOVER\_ENTER</span></span>
-   <span data-ttu-id="27565-133">SE \_ навести на \_ выход</span><span class="sxs-lookup"><span data-stu-id="27565-133">SE\_HOVER\_LEAVE</span></span>
-   <span data-ttu-id="27565-134">\_средний щелчок по центру SE \_</span><span class="sxs-lookup"><span data-stu-id="27565-134">SE\_MIDDLE\_CLICK</span></span>
-   <span data-ttu-id="27565-135">\_ключ SE</span><span class="sxs-lookup"><span data-stu-id="27565-135">SE\_KEY</span></span>
-   <span data-ttu-id="27565-136">\_ключ модификатора \_ SE</span><span class="sxs-lookup"><span data-stu-id="27565-136">SE\_MODIFIER\_KEY</span></span>
-   <span data-ttu-id="27565-137">\_режим ЖЕСТОВ \_ SE</span><span class="sxs-lookup"><span data-stu-id="27565-137">SE\_GESTURE\_MODE</span></span>
-   <span data-ttu-id="27565-138">\_курсор SE</span><span class="sxs-lookup"><span data-stu-id="27565-138">SE\_CURSOR</span></span>

## <a name="requirements"></a><span data-ttu-id="27565-139">Требования</span><span class="sxs-lookup"><span data-stu-id="27565-139">Requirements</span></span>



| <span data-ttu-id="27565-140">Требование</span><span class="sxs-lookup"><span data-stu-id="27565-140">Requirement</span></span> | <span data-ttu-id="27565-141">Значение</span><span class="sxs-lookup"><span data-stu-id="27565-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="27565-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27565-142">Minimum supported client</span></span><br/> | <span data-ttu-id="27565-143">Только классические приложения Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="27565-143">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="27565-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27565-144">Minimum supported server</span></span><br/> | <span data-ttu-id="27565-145">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="27565-145">None supported</span></span><br/>                                                              |
| <span data-ttu-id="27565-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="27565-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="27565-147"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="27565-147"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27565-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27565-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27565-149">**Интерфейс Итаблетевентсинк**</span><span class="sxs-lookup"><span data-stu-id="27565-149">**ITabletEventSink Interface**</span></span>](itableteventsink.md)
</dt> </dl>

 

 




