---
title: Метод Ивмхарддискконнектион Сетбуслокатион (Впккоминтерфацес. h)
description: Задает расположение шины, к которой подключен этот жесткий диск.
ms.assetid: 0aa303ae-d8bf-4d38-94ab-bdbb4e744c7b
keywords:
- Метод Сетбуслокатион Virtual PC
- Метод Сетбуслокатион Virtual PC, интерфейс Ивмхарддискконнектион
- Ивмхарддискконнектион интерфейс Virtual PC, метод Сетбуслокатион
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.SetBusLocation
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61de0f595bc06d497e7f5913da9173ccb3bf1ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340335"
---
# <a name="ivmharddiskconnectionsetbuslocation-method"></a><span data-ttu-id="1c2a3-106">Метод Ивмхарддискконнектион:: Сетбуслокатион</span><span class="sxs-lookup"><span data-stu-id="1c2a3-106">IVMHardDiskConnection::SetBusLocation method</span></span>

<span data-ttu-id="1c2a3-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1c2a3-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1c2a3-109">Задает расположение шины, к которой подключен этот жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-109">Sets the bus location to which this hard disk is attached.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c2a3-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c2a3-110">Syntax</span></span>


```C++
HRESULT SetBusLocation(
  [in] long vmBusNumber,
  [in] long vmDeviceNumber
);
```



## <a name="parameters"></a><span data-ttu-id="1c2a3-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c2a3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c2a3-112">*вмбуснумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-112">*vmBusNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2a3-113">Номер шины, которая будет использоваться.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-113">The bus number to be used.</span></span>

</dd> <dt>

<span data-ttu-id="1c2a3-114">*вмдевиценумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-114">*vmDeviceNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c2a3-115">Номер используемого устройства.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-115">The device number to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c2a3-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c2a3-116">Return value</span></span>

<span data-ttu-id="1c2a3-117">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-117">This method can return one of these values.</span></span>



| <span data-ttu-id="1c2a3-118">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="1c2a3-118">Return code/value</span></span>                                                                                                                                                               | <span data-ttu-id="1c2a3-119">Описание</span><span class="sxs-lookup"><span data-stu-id="1c2a3-119">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c2a3-120"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                     | <span data-ttu-id="1c2a3-121">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-121">The operation was successful.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="1c2a3-122"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                    | <span data-ttu-id="1c2a3-123">Указано недопустимое расположение шины.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-123">The bus location specified is not valid.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="1c2a3-124"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl>    | <span data-ttu-id="1c2a3-125">Не удалось задать расположение шины, так как виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-125">The bus location could not be set because the virtual machine is in a running or saved state.</span></span><br/>    |
| <dl> <span data-ttu-id="1c2a3-126"><dt>**Виртуальная машина \_ \_Шина диска \_ E \_ \_ с \_ помощью**</dt> <dt>0xA00400503</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-126"><dt>**VM\_E\_DRIVE\_BUS\_LOC\_IN\_USE**</dt> <dt>0xA00400503</dt></span></span> </dl> | <span data-ttu-id="1c2a3-127">Не удалось установить расположение шины, так как в данный момент другое устройство подключено к этому расположению.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-127">The bus location could not be set because another device is currently attached to this location.</span></span><br/> |
| <dl> <span data-ttu-id="1c2a3-128"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-128"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>            | <span data-ttu-id="1c2a3-129">Текущий диск является недопустимым.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-129">The current drive is not valid.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="1c2a3-130"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-130"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>               | <span data-ttu-id="1c2a3-131">Недопустимая Текущая виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-131">The current virtual machine is not valid.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="1c2a3-132"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-132"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>               | <span data-ttu-id="1c2a3-133">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="1c2a3-133">An unexpected error has occurred.</span></span><br/>                                                                |



 

## <a name="requirements"></a><span data-ttu-id="1c2a3-134">Требования</span><span class="sxs-lookup"><span data-stu-id="1c2a3-134">Requirements</span></span>



| <span data-ttu-id="1c2a3-135">Требование</span><span class="sxs-lookup"><span data-stu-id="1c2a3-135">Requirement</span></span> | <span data-ttu-id="1c2a3-136">Значение</span><span class="sxs-lookup"><span data-stu-id="1c2a3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c2a3-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c2a3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1c2a3-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="1c2a3-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1c2a3-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c2a3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1c2a3-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1c2a3-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1c2a3-141">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1c2a3-141">End of client support</span></span><br/>    | <span data-ttu-id="1c2a3-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1c2a3-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1c2a3-143">Продукт</span><span class="sxs-lookup"><span data-stu-id="1c2a3-143">Product</span></span><br/>                  | <span data-ttu-id="1c2a3-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1c2a3-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1c2a3-145">Header</span><span class="sxs-lookup"><span data-stu-id="1c2a3-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c2a3-146"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c2a3-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1c2a3-147">IID</span><span class="sxs-lookup"><span data-stu-id="1c2a3-147">IID</span></span><br/>                      | <span data-ttu-id="1c2a3-148">IID \_ ивмхарддискконнектион определен как aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span><span class="sxs-lookup"><span data-stu-id="1c2a3-148">IID\_IVMHardDiskconnection is defined as aefa36a5-463a-46ae-9e6c-a1fb4e12e671</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="1c2a3-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c2a3-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c2a3-150">**ивмхарддискконнектион**</span><span class="sxs-lookup"><span data-stu-id="1c2a3-150">**IVMHardDiskConnection**</span></span>](ivmharddiskconnection.md)
</dt> </dl>

 

