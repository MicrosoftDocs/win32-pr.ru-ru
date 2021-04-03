---
title: Метод Ивммаусе Сетбуттон (Впккоминтерфацес. h)
description: Задает текущее состояние (вверх или вниз) указанной кнопки мыши.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Метод Сетбуттон Virtual PC
- Метод Сетбуттон Virtual PC, интерфейс Ивммаусе
- Ивммаусе интерфейс Virtual PC, метод Сетбуттон
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137230"
---
# <a name="ivmmousesetbutton-method"></a><span data-ttu-id="25fbd-106">Метод Ивммаусе:: Сетбуттон</span><span class="sxs-lookup"><span data-stu-id="25fbd-106">IVMMouse::SetButton method</span></span>

<span data-ttu-id="25fbd-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="25fbd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="25fbd-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="25fbd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="25fbd-109">Задает текущее состояние (вверх или вниз) указанной кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="25fbd-109">Sets the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="25fbd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="25fbd-110">Syntax</span></span>


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a><span data-ttu-id="25fbd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="25fbd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25fbd-112">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25fbd-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fbd-113">Индекс кнопки.</span><span class="sxs-lookup"><span data-stu-id="25fbd-113">The button index.</span></span> <span data-ttu-id="25fbd-114">Список значений см. в разделе [**вммаусебуттон**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="25fbd-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="25fbd-115">не *работает* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25fbd-115">*down* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25fbd-116">Новое состояние кнопки.</span><span class="sxs-lookup"><span data-stu-id="25fbd-116">The new button state.</span></span> <span data-ttu-id="25fbd-117">Используйте **значение true** , если состояние кнопки должно быть не ниже, и **false** , если необходимо установить значение up.</span><span class="sxs-lookup"><span data-stu-id="25fbd-117">Use **TRUE** if the button state is to be set to down, and **FALSE** if it is to be set to up.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25fbd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25fbd-118">Return value</span></span>

<span data-ttu-id="25fbd-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="25fbd-119">This method can return one of these values.</span></span>



| <span data-ttu-id="25fbd-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="25fbd-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="25fbd-121">Описание</span><span class="sxs-lookup"><span data-stu-id="25fbd-121">Description</span></span>                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="25fbd-122"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="25fbd-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="25fbd-123">The operation was successful.</span></span><br/>                                                                                                          |
| <dl> <span data-ttu-id="25fbd-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="25fbd-125">Недопустимый параметр *буттониндекс* .</span><span class="sxs-lookup"><span data-stu-id="25fbd-125">The *buttonIndex* parameter is not valid.</span></span><br/>                                                                                              |
| <dl> <span data-ttu-id="25fbd-126"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-126"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="25fbd-127">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="25fbd-127">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="25fbd-128"><dt>**Виртуальная машина \_ Электронная \_ мышь \_ не \_ активна**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-128"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="25fbd-129">Не удалось выполнить операцию, так как устройство мыши не включено или сейчас не активно на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="25fbd-129">The operation could not be completed because the mouse device is not powered up, or it is not currently active in the virtual machine.</span></span><br/> |
| <dl> <span data-ttu-id="25fbd-130"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-130"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="25fbd-131">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="25fbd-131">An unexpected error has occurred.</span></span><br/>                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="25fbd-132">Требования</span><span class="sxs-lookup"><span data-stu-id="25fbd-132">Requirements</span></span>



| <span data-ttu-id="25fbd-133">Требование</span><span class="sxs-lookup"><span data-stu-id="25fbd-133">Requirement</span></span> | <span data-ttu-id="25fbd-134">Значение</span><span class="sxs-lookup"><span data-stu-id="25fbd-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="25fbd-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25fbd-135">Minimum supported client</span></span><br/> | <span data-ttu-id="25fbd-136">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="25fbd-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="25fbd-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25fbd-137">Minimum supported server</span></span><br/> | <span data-ttu-id="25fbd-138">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="25fbd-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="25fbd-139">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="25fbd-139">End of client support</span></span><br/>    | <span data-ttu-id="25fbd-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="25fbd-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="25fbd-141">Продукт</span><span class="sxs-lookup"><span data-stu-id="25fbd-141">Product</span></span><br/>                  | <span data-ttu-id="25fbd-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="25fbd-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="25fbd-143">Header</span><span class="sxs-lookup"><span data-stu-id="25fbd-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="25fbd-144"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="25fbd-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="25fbd-145">IID</span><span class="sxs-lookup"><span data-stu-id="25fbd-145">IID</span></span><br/>                      | <span data-ttu-id="25fbd-146">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="25fbd-146">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="25fbd-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="25fbd-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25fbd-148">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="25fbd-148">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

