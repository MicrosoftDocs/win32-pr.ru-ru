---
title: Метод Ивмвиртуалмачине Ремовехарддискконнектион (Впккоминтерфацес. h)
description: Удаляет указанное подключение жесткого диска из виртуальной машины.
ms.assetid: d31f2442-aae4-4987-9188-fd32778604a1
keywords:
- Метод Ремовехарддискконнектион Virtual PC
- Метод Ремовехарддискконнектион Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Ремовехарддискконнектион
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveHardDiskConnection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62a9bbf8b3aac0dd35c8390343c20a1b67b59101
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415617"
---
# <a name="ivmvirtualmachineremoveharddiskconnection-method"></a><span data-ttu-id="c6c5a-106">Метод Ивмвиртуалмачине:: Ремовехарддискконнектион</span><span class="sxs-lookup"><span data-stu-id="c6c5a-106">IVMVirtualMachine::RemoveHardDiskConnection method</span></span>

<span data-ttu-id="c6c5a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c6c5a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c6c5a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c6c5a-109">Удаляет указанное подключение жесткого диска из виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-109">Removes the specified hard disk connection from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6c5a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c6c5a-110">Syntax</span></span>


```C++
HRESULT RemoveHardDiskConnection(
  [in] IVMHardDiskConnection *hardDiskConnection
);
```



## <a name="parameters"></a><span data-ttu-id="c6c5a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6c5a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6c5a-112">*харддискконнектион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c6c5a-112">*hardDiskConnection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6c5a-113">Объект [**ивмхарддискконнектион**](ivmharddiskconnection.md) , представляющий удаляемое подключение к жесткому диску.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-113">An [**IVMHardDiskConnection**](ivmharddiskconnection.md) object that represents the hard disk connection to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6c5a-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6c5a-114">Return value</span></span>

<span data-ttu-id="c6c5a-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-115">This method can return one of these values.</span></span>



| <span data-ttu-id="c6c5a-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c6c5a-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="c6c5a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c6c5a-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6c5a-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="c6c5a-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="c6c5a-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c6c5a-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="c6c5a-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="c6c5a-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="c6c5a-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="c6c5a-124"><dt>**Виртуальная машина \_ \_Виртуальная машина \_ с установленным \_ или \_ сохраненным**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="c6c5a-125">Виртуальная машина находится в работающем или сохраненном состоянии.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="c6c5a-126"><dt>**Виртуальная машина \_ \_Диск E \_ Недопустимый**</dt> <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="c6c5a-127">Указанный диск не подключен к этому расположению шины.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="c6c5a-128"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="c6c5a-129">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="c6c5a-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c6c5a-130">Remarks</span></span>

<span data-ttu-id="c6c5a-131">Удалить существующее подключение к жесткому диску можно только из остановленной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c6c5a-131">You can only remove an existing hard disk connection from a stopped virtual machine.</span></span> <span data-ttu-id="c6c5a-132">Список соединений, подключенных к виртуальной машине в настоящее время, можно получить, перечисляя свойство [**харддискконнектионс**](ivmvirtualmachine-harddiskconnections.md) .</span><span class="sxs-lookup"><span data-stu-id="c6c5a-132">A list of connections currently attached to the virtual machine is obtained by enumerating the [**HardDiskConnections**](ivmvirtualmachine-harddiskconnections.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6c5a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="c6c5a-133">Requirements</span></span>



| <span data-ttu-id="c6c5a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="c6c5a-134">Requirement</span></span> | <span data-ttu-id="c6c5a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="c6c5a-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6c5a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c6c5a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="c6c5a-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c6c5a-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c6c5a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c6c5a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="c6c5a-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c6c5a-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c6c5a-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c6c5a-140">End of client support</span></span><br/>    | <span data-ttu-id="c6c5a-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c6c5a-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c6c5a-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="c6c5a-142">Product</span></span><br/>                  | <span data-ttu-id="c6c5a-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c6c5a-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c6c5a-144">Header</span><span class="sxs-lookup"><span data-stu-id="c6c5a-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6c5a-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6c5a-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c6c5a-146">IID</span><span class="sxs-lookup"><span data-stu-id="c6c5a-146">IID</span></span><br/>                      | <span data-ttu-id="c6c5a-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c6c5a-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c6c5a-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c6c5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6c5a-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="c6c5a-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

