---
title: Метод Ивмдвддриве Сетбуслокатион (Впккоминтерфацес. h)
description: Подключает DVD-дисковод к указанному расположению шины на виртуальной машине.
ms.assetid: 765274b8-91bc-475a-ac4d-994b2425a421
keywords:
- Метод Сетбуслокатион Virtual PC
- Метод Сетбуслокатион Virtual PC, интерфейс Ивмдвддриве
- Ивмдвддриве интерфейс Virtual PC, метод Сетбуслокатион
topic_type:
- apiref
api_name:
- IVMDVDDrive.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db6091493a56c020f57300e65328fee0eb65a69e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672673"
---
# <a name="ivmdvddrivesetbuslocation-method"></a><span data-ttu-id="d528b-106">Метод Ивмдвддриве:: Сетбуслокатион</span><span class="sxs-lookup"><span data-stu-id="d528b-106">IVMDVDDrive::SetBusLocation method</span></span>

<span data-ttu-id="d528b-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d528b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d528b-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d528b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d528b-109">Подключает DVD-дисковод к указанному расположению шины на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="d528b-109">Attaches the DVD drive to the specified bus location in the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d528b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d528b-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long busNumber,
  [in] long deviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="d528b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d528b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d528b-112">*буснумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d528b-112">*busNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d528b-113">Номер шины, к которой должен быть подключен диск.</span><span class="sxs-lookup"><span data-stu-id="d528b-113">The bus number to which this drive is to be attached.</span></span> <span data-ttu-id="d528b-114">Например, на шине IDE это число указывает, следует ли использовать номер основной или дополнительной шины.</span><span class="sxs-lookup"><span data-stu-id="d528b-114">For example, on an IDE bus, this number would represent whether to use the primary or secondary bus number.</span></span>

</dd> <dt>

<span data-ttu-id="d528b-115">*девиценумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d528b-115">*deviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d528b-116">Номер устройства, к которому будет присоединен этот диск.</span><span class="sxs-lookup"><span data-stu-id="d528b-116">The device number to which this drive is to be attached.</span></span> <span data-ttu-id="d528b-117">Например, на шине IDE это число будет представлять необходимость использования основного или дополнительного расположения устройства.</span><span class="sxs-lookup"><span data-stu-id="d528b-117">For example, on an IDE bus, this number would represent whether to use the primary or secondary device location.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d528b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d528b-118">Return value</span></span>

<span data-ttu-id="d528b-119">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d528b-119">This method can return one of these values.</span></span>



| <span data-ttu-id="d528b-120">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d528b-120">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="d528b-121">Описание</span><span class="sxs-lookup"><span data-stu-id="d528b-121">Description</span></span>                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d528b-122"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="d528b-123">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d528b-123">The operation was successful.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="d528b-124"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                 | <span data-ttu-id="d528b-125">Указано недопустимое расположение шины.</span><span class="sxs-lookup"><span data-stu-id="d528b-125">The bus location specified is not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="d528b-126"><dt>**Д \_ Сбой**</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-126"><dt>**E\_FAIL**</dt> <dt>0x80004005</dt></span></span> </dl>                       | <span data-ttu-id="d528b-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d528b-127">An unexpected error has occurred.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="d528b-128"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-128"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="d528b-129">Невозможно задать расположение шины, пока виртуальная машина работает или находится в сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="d528b-129">The bus location cannot be set while the virtual machine is running or in a saved state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d528b-130"><dt>**\_ \_ \_ \_ используемая шина виртуальной машины \_ E**</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-130"><dt>**VM\_E\_BUS\_LOC\_IN\_USE**</dt></span></span> </dl>                                                                      | <span data-ttu-id="d528b-131">Другое устройство уже подключено к указанному расположению шины.</span><span class="sxs-lookup"><span data-stu-id="d528b-131">Another device is already attached to the specified bus location.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="d528b-132"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-132"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="d528b-133">Не удалось инициализировать текущий диск.</span><span class="sxs-lookup"><span data-stu-id="d528b-133">The current drive could not be initialized.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="d528b-134"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d528b-134"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="d528b-135">Не удалось записать изменения в файл настроек, так как не удалось определить виртуальную машину для этого диска.</span><span class="sxs-lookup"><span data-stu-id="d528b-135">The changes could not be written to the preferences file because the virtual machine for this drive could not be determined.</span></span><br/> |
| <dl> <span data-ttu-id="d528b-136"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="d528b-137">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d528b-137">An unexpected error has occurred.</span></span><br/>                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="d528b-138">Требования</span><span class="sxs-lookup"><span data-stu-id="d528b-138">Requirements</span></span>



| <span data-ttu-id="d528b-139">Требование</span><span class="sxs-lookup"><span data-stu-id="d528b-139">Requirement</span></span> | <span data-ttu-id="d528b-140">Значение</span><span class="sxs-lookup"><span data-stu-id="d528b-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d528b-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d528b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d528b-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d528b-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d528b-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d528b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d528b-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d528b-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d528b-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d528b-145">End of client support</span></span><br/>    | <span data-ttu-id="d528b-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d528b-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d528b-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="d528b-147">Product</span></span><br/>                  | <span data-ttu-id="d528b-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d528b-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d528b-149">Header</span><span class="sxs-lookup"><span data-stu-id="d528b-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="d528b-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d528b-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d528b-151">IID</span><span class="sxs-lookup"><span data-stu-id="d528b-151">IID</span></span><br/>                      | <span data-ttu-id="d528b-152">IID \_ ивмдвддриве определен как b96328f6-6732-437d-a00d-ffa47e43971c</span><span class="sxs-lookup"><span data-stu-id="d528b-152">IID\_IVMDVDDrive is defined as b96328f6-6732-437d-a00d-ffa47e43971c</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="d528b-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d528b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d528b-154">**ивмдвддриве**</span><span class="sxs-lookup"><span data-stu-id="d528b-154">**IVMDVDDrive**</span></span>](ivmdvddrive.md)
</dt> </dl>

 

