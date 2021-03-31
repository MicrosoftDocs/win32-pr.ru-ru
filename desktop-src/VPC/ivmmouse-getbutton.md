---
title: Метод Ивммаусе-Button (Впккоминтерфацес. h)
description: Извлекает текущее состояние указанной кнопки мыши.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Метод кнопки Virtual PC
- Метод "Кнопка" Virtual PC, интерфейс Ивммаусе
- Интерфейс Ивммаусе Virtual PC, метод "Кнопка"
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73929a1fc9dfaa3942ed49f8a449343a594eec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803743"
---
# <a name="ivmmousegetbutton-method"></a><span data-ttu-id="2d6ac-106">Метод Ивммаусе:: "Button"</span><span class="sxs-lookup"><span data-stu-id="2d6ac-106">IVMMouse::GetButton method</span></span>

<span data-ttu-id="2d6ac-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2d6ac-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2d6ac-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2d6ac-109">Извлекает текущее состояние (вверх или вниз) указанной кнопки мыши.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-109">Retrieves the current state (up or down) of the specified mouse button.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d6ac-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2d6ac-110">Syntax</span></span>


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a><span data-ttu-id="2d6ac-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2d6ac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d6ac-112">*буттониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2d6ac-112">*buttonIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6ac-113">Индекс кнопки, состояние которой запрашивается.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-113">The index of the button whose state is being requested.</span></span> <span data-ttu-id="2d6ac-114">Список значений см. в разделе [**вммаусебуттон**](vmmousebutton.md).</span><span class="sxs-lookup"><span data-stu-id="2d6ac-114">For a list of values, see [**VMMouseButton**](vmmousebutton.md).</span></span>

</dd> <dt>

<span data-ttu-id="2d6ac-115">*раскрывающийся список* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2d6ac-115">*isDown* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2d6ac-116">Состояние указанной кнопки.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-116">The state of the indicated button.</span></span> <span data-ttu-id="2d6ac-117">**Значение true** , если кнопка в настоящее время отключена в виртуальной машине; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="2d6ac-117">**TRUE** if the button is currently down in the virtual machine, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d6ac-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2d6ac-118">Return value</span></span>

<span data-ttu-id="2d6ac-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-119">This method can return one of these values.</span></span>



| <span data-ttu-id="2d6ac-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2d6ac-120">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="2d6ac-121">Описание</span><span class="sxs-lookup"><span data-stu-id="2d6ac-121">Description</span></span>                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2d6ac-122"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                              | <span data-ttu-id="2d6ac-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="2d6ac-124"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2d6ac-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                | <span data-ttu-id="2d6ac-125">Параметр " *Down* " имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-125">The *isDown* parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="2d6ac-126"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>             | <span data-ttu-id="2d6ac-127">Недопустимый параметр *буттониндекс* .</span><span class="sxs-lookup"><span data-stu-id="2d6ac-127">The *buttonIndex* parameter is not valid.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2d6ac-128"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-128"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>   | <span data-ttu-id="2d6ac-129">Виртуальная машина, к которой подключено это устройство с мышью, в данный момент не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-129">The virtual machine to which this mouse device is attached is not currently running.</span></span><br/> |
| <dl> <span data-ttu-id="2d6ac-130"><dt>**Виртуальная машина \_ Электронная \_ мышь \_ не \_ активна**</dt> <dt>0xA0040800</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-130"><dt>**VM\_E\_MOUSE\_NOT\_ACTIVE**</dt> <dt>0xA0040800</dt></span></span> </dl> | <span data-ttu-id="2d6ac-131">Устройство мыши не включено.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-131">The mouse device has not been powered up.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2d6ac-132"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>        | <span data-ttu-id="2d6ac-133">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2d6ac-133">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="2d6ac-134">Требования</span><span class="sxs-lookup"><span data-stu-id="2d6ac-134">Requirements</span></span>



| <span data-ttu-id="2d6ac-135">Требование</span><span class="sxs-lookup"><span data-stu-id="2d6ac-135">Requirement</span></span> | <span data-ttu-id="2d6ac-136">Значение</span><span class="sxs-lookup"><span data-stu-id="2d6ac-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d6ac-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2d6ac-137">Minimum supported client</span></span><br/> | <span data-ttu-id="2d6ac-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2d6ac-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2d6ac-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2d6ac-139">Minimum supported server</span></span><br/> | <span data-ttu-id="2d6ac-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2d6ac-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2d6ac-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2d6ac-141">End of client support</span></span><br/>    | <span data-ttu-id="2d6ac-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2d6ac-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2d6ac-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="2d6ac-143">Product</span></span><br/>                  | <span data-ttu-id="2d6ac-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2d6ac-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2d6ac-145">Header</span><span class="sxs-lookup"><span data-stu-id="2d6ac-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d6ac-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d6ac-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2d6ac-147">IID</span><span class="sxs-lookup"><span data-stu-id="2d6ac-147">IID</span></span><br/>                      | <span data-ttu-id="2d6ac-148">IID \_ ивммаусе определен как ac903f6d-6346-4f29-8875-5d511a13895e</span><span class="sxs-lookup"><span data-stu-id="2d6ac-148">IID\_IVMmouse is defined as ac903f6d-6346-4f29-8875-5d511a13895e</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="2d6ac-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2d6ac-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d6ac-150">**ивммаусе**</span><span class="sxs-lookup"><span data-stu-id="2d6ac-150">**IVMMouse**</span></span>](ivmmouse.md)
</dt> </dl>

 

