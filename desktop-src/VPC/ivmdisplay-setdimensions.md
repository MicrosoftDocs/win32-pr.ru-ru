---
title: Метод Ивмдисплай Сетдименсионс (Впккоминтерфацес. h)
description: Задает высоту и ширину дисплея виртуальной машины в пикселях.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Метод Сетдименсионс Virtual PC
- Метод Сетдименсионс Virtual PC, интерфейс Ивмдисплай
- Ивмдисплай интерфейс Virtual PC, метод Сетдименсионс
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672817"
---
# <a name="ivmdisplaysetdimensions-method"></a><span data-ttu-id="13059-106">Метод Ивмдисплай:: Сетдименсионс</span><span class="sxs-lookup"><span data-stu-id="13059-106">IVMDisplay::SetDimensions method</span></span>

<span data-ttu-id="13059-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="13059-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="13059-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="13059-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="13059-109">Задает высоту и ширину дисплея виртуальной машины (ВМ) в пикселях.</span><span class="sxs-lookup"><span data-stu-id="13059-109">Sets the height and width of the virtual machine's (VM's) display, in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="13059-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13059-110">Syntax</span></span>


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a><span data-ttu-id="13059-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="13059-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13059-112">*дисплайпикселвидс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13059-112">*displayPixelWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13059-113">Ширина (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="13059-113">The width, in pixels.</span></span> <span data-ttu-id="13059-114">Значение должно быть между значениями 640 и 2048.</span><span class="sxs-lookup"><span data-stu-id="13059-114">The value must be between the values of 640 and 2048.</span></span> <span data-ttu-id="13059-115">Если значение не делится на 8, оно будет уменьшено до следующего меньшего значения, кратного 8.</span><span class="sxs-lookup"><span data-stu-id="13059-115">If the value is not evenly divisible by 8, then it will be reduced to the next lower multiple of 8.</span></span>

</dd> <dt>

<span data-ttu-id="13059-116">*дисплайпикселхеигхт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13059-116">*displayPixelHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13059-117">Высота (в пикселях).</span><span class="sxs-lookup"><span data-stu-id="13059-117">The height, in pixels.</span></span> <span data-ttu-id="13059-118">Значение должно быть между значениями 480 и 1920.</span><span class="sxs-lookup"><span data-stu-id="13059-118">The value must be between the values of 480 and 1920.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13059-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13059-119">Return value</span></span>

<span data-ttu-id="13059-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="13059-120">This method can return one of these values.</span></span>



| <span data-ttu-id="13059-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="13059-121">Return code/value</span></span>                                                                                                                                                                    | <span data-ttu-id="13059-122">Описание</span><span class="sxs-lookup"><span data-stu-id="13059-122">Description</span></span>                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="13059-123"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="13059-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                          | <span data-ttu-id="13059-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="13059-124">The operation was successful.</span></span><br/>                                                                                                                                                                         |
| <dl> <span data-ttu-id="13059-125"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="13059-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                         | <span data-ttu-id="13059-126">Параметр *дисплайпикселвидс* не делится на 8, или параметр *дисплайпикселвидс* или *дисплайпикселхеигхт* находится за пределами разрешенного минимума (640x480) или максимума 2048x1920).</span><span class="sxs-lookup"><span data-stu-id="13059-126">The *displayPixelWidth* parameter is not evenly divisible by 8 or the *displayPixelWidth* or *displayPixelHeight* parameter is outside of the allowed minimum (640x480) or maximum 2048x1920) values.</span></span><br/> |
| <dl> <span data-ttu-id="13059-127"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="13059-127"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                     | <span data-ttu-id="13059-128">Изменение разрешения не завершилось вовремя.</span><span class="sxs-lookup"><span data-stu-id="13059-128">The resolution change did not finish in a timely manner.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="13059-129"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="13059-129"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>               | <span data-ttu-id="13059-130">Для этой операции должна быть запущена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="13059-130">The virtual machine must be running for this operation.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="13059-131"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="13059-131"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                    | <span data-ttu-id="13059-132">Виртуальная машина является недопустимой или не запущена в данный момент.</span><span class="sxs-lookup"><span data-stu-id="13059-132">The virtual machine is not valid or is not currently running.</span></span><br/>                                                                                                                                         |
| <dl> <span data-ttu-id="13059-133"><dt>**Виртуальная машина \_ \_Нет \_ отображаемых**</dt> <dt>0xA0040850</dt></span><span class="sxs-lookup"><span data-stu-id="13059-133"><dt>**VM\_E\_NO\_DISPLAY**</dt> <dt>0xA0040850</dt></span></span> </dl>                    | <span data-ttu-id="13059-134">Не удалось выбрать допустимое отображение для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="13059-134">Unable to locate a valid display for the VM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="13059-135"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="13059-135"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl> | <span data-ttu-id="13059-136">Версия компонентов интеграции, установленных в операционной системе на виртуальной машине, не поддерживает эту операцию.</span><span class="sxs-lookup"><span data-stu-id="13059-136">The version of the integration components installed in the guest operating system does not support this operation.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="13059-137"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="13059-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                    | <span data-ttu-id="13059-138">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="13059-138">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="13059-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="13059-139">Remarks</span></span>

<span data-ttu-id="13059-140">Минимальный размер дисплея виртуальной машины составляет 640 x 480 пикселей.</span><span class="sxs-lookup"><span data-stu-id="13059-140">The minimum size of the virtual machine's display is 640 x 480 pixels.</span></span> <span data-ttu-id="13059-141">Максимальный размер — 2048 x 1920.</span><span class="sxs-lookup"><span data-stu-id="13059-141">The maximum size is 2048 x 1920.</span></span> <span data-ttu-id="13059-142">При попытке установить размер отображаемого значения за пределами этих ограничений или любой ширины, не кратной 8, будет возвращена ошибка **E \_ INVALIDARG** .</span><span class="sxs-lookup"><span data-stu-id="13059-142">Attempts to set the display size to values outside these limits, or to any width not evenly divisible by 8, will result in an **E\_INVALIDARG** error being returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="13059-143">Требования</span><span class="sxs-lookup"><span data-stu-id="13059-143">Requirements</span></span>



| <span data-ttu-id="13059-144">Требование</span><span class="sxs-lookup"><span data-stu-id="13059-144">Requirement</span></span> | <span data-ttu-id="13059-145">Значение</span><span class="sxs-lookup"><span data-stu-id="13059-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13059-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13059-146">Minimum supported client</span></span><br/> | <span data-ttu-id="13059-147">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="13059-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13059-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13059-148">Minimum supported server</span></span><br/> | <span data-ttu-id="13059-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="13059-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="13059-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="13059-150">End of client support</span></span><br/>    | <span data-ttu-id="13059-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="13059-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="13059-152">Продукт</span><span class="sxs-lookup"><span data-stu-id="13059-152">Product</span></span><br/>                  | <span data-ttu-id="13059-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="13059-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="13059-154">Header</span><span class="sxs-lookup"><span data-stu-id="13059-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="13059-155"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="13059-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="13059-156">IID</span><span class="sxs-lookup"><span data-stu-id="13059-156">IID</span></span><br/>                      | <span data-ttu-id="13059-157">IID \_ ивмдисплай определен как 960895e9-f743-4498-96aa-261f867e7fc5</span><span class="sxs-lookup"><span data-stu-id="13059-157">IID\_IVMDisplay is defined as 960895e9-f743-4498-96aa-261f867e7fc5</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="13059-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13059-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13059-159">**ивмдисплай**</span><span class="sxs-lookup"><span data-stu-id="13059-159">**IVMDisplay**</span></span>](ivmdisplay.md)
</dt> </dl>

 

