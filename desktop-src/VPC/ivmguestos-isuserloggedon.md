---
title: Метод Ивмгуестос Исусерлогжедон (Впккоминтерфацес. h)
description: Определяет, имеется ли запрошенный сеанс.
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- Метод Исусерлогжедон Virtual PC
- Метод Исусерлогжедон Virtual PC, интерфейс Ивмгуестос
- Ивмгуестос интерфейс Virtual PC, метод Исусерлогжедон
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691776"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="2f74f-106">Метод Ивмгуестос:: Исусерлогжедон</span><span class="sxs-lookup"><span data-stu-id="2f74f-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="2f74f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f74f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2f74f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2f74f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2f74f-109">Определяет, имеется ли запрошенный сеанс.</span><span class="sxs-lookup"><span data-stu-id="2f74f-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f74f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2f74f-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="2f74f-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2f74f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f74f-112">*инраилсессион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2f74f-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f74f-113">Задайте значение 0 для сеанса шины или 1 для сеанса RDP.</span><span class="sxs-lookup"><span data-stu-id="2f74f-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="2f74f-114">*аутсессионпресент* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="2f74f-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="2f74f-115">Задайте значение **\_ true** , если сеанс имеется, и **вариант \_ false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2f74f-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f74f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2f74f-116">Return value</span></span>

<span data-ttu-id="2f74f-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2f74f-117">This method can return one of these values.</span></span>



| <span data-ttu-id="2f74f-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2f74f-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="2f74f-119">Описание</span><span class="sxs-lookup"><span data-stu-id="2f74f-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f74f-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="2f74f-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2f74f-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2f74f-122"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="2f74f-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="2f74f-123">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f74f-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2f74f-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="2f74f-125">Параметр *аутсессионпресент* недопустим или имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="2f74f-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="2f74f-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="2f74f-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2f74f-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="2f74f-128"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (Error \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="2f74f-129">Недостаточно памяти для выполнения этого запроса.</span><span class="sxs-lookup"><span data-stu-id="2f74f-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="2f74f-130"><dt>**Виртуальная машина \_ \_Истекло время \_ ожидания**</dt> <dt>0xA0040202</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="2f74f-131">Операция не завершилась своевременно.</span><span class="sxs-lookup"><span data-stu-id="2f74f-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="2f74f-132"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="2f74f-133">Для этой операции должна быть запущена виртуальная машина (ВМ).</span><span class="sxs-lookup"><span data-stu-id="2f74f-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="2f74f-134"><dt>**Виртуальная машина \_ Добавление компонента "E" \_ \_ \_ не \_**</dt> доступно <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="2f74f-135">Компонент интеграции компонентов не установлен на этой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2f74f-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="2f74f-136"><dt>**Виртуальная машина \_ 0xA00400507 \_ Виртуальная машина \_ приостановлена**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="2f74f-137">Виртуальная машина приостановлена.</span><span class="sxs-lookup"><span data-stu-id="2f74f-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="2f74f-138">Требования</span><span class="sxs-lookup"><span data-stu-id="2f74f-138">Requirements</span></span>



| <span data-ttu-id="2f74f-139">Требование</span><span class="sxs-lookup"><span data-stu-id="2f74f-139">Requirement</span></span> | <span data-ttu-id="2f74f-140">Значение</span><span class="sxs-lookup"><span data-stu-id="2f74f-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f74f-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2f74f-141">Minimum supported client</span></span><br/> | <span data-ttu-id="2f74f-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2f74f-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f74f-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2f74f-143">Minimum supported server</span></span><br/> | <span data-ttu-id="2f74f-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2f74f-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2f74f-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2f74f-145">End of client support</span></span><br/>    | <span data-ttu-id="2f74f-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2f74f-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2f74f-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="2f74f-147">Product</span></span><br/>                  | <span data-ttu-id="2f74f-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2f74f-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2f74f-149">Header</span><span class="sxs-lookup"><span data-stu-id="2f74f-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f74f-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f74f-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2f74f-151">IID</span><span class="sxs-lookup"><span data-stu-id="2f74f-151">IID</span></span><br/>                      | <span data-ttu-id="2f74f-152">IID \_ ивмгуестос определен как 99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="2f74f-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="2f74f-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2f74f-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f74f-154">**ивмгуестос**</span><span class="sxs-lookup"><span data-stu-id="2f74f-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

