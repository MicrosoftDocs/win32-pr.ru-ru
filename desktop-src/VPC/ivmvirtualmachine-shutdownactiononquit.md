---
title: Свойство Шутдовнактиононкуит Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Действие, выполняемое на этой виртуальной машине, если оно выполняется при выходе Windows Virtual PC.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Шутдовнактиононкуит свойство Virtual PC
- Шутдовнактиононкуит свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Шутдовнактиононкуит
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492222"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a><span data-ttu-id="d041e-106">Свойство Ивмвиртуалмачине:: Шутдовнактиононкуит</span><span class="sxs-lookup"><span data-stu-id="d041e-106">IVMVirtualMachine::ShutdownActionOnQuit property</span></span>

<span data-ttu-id="d041e-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d041e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d041e-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d041e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d041e-109">Извлекает и задает действие, выполняемое на этой виртуальной машине, если оно выполняется при выходе Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d041e-109">Retrieves and sets the action to be performed on this virtual machine (VM) if it is running when Windows Virtual PC is quit.</span></span>

<span data-ttu-id="d041e-110">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="d041e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d041e-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d041e-111">Syntax</span></span>


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a><span data-ttu-id="d041e-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d041e-112">Property value</span></span>

<span data-ttu-id="d041e-113">Указывает, как завершить работу этой виртуальной машины, если она работает при выходе Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d041e-113">Specifies how to shut down this VM if it is running when Windows Virtual PC is quit.</span></span> <span data-ttu-id="d041e-114">Список значений см. в разделе [**вмшутдовнактион**](vmshutdownaction.md).</span><span class="sxs-lookup"><span data-stu-id="d041e-114">For a list of values, see [**VMShutdownAction**](vmshutdownaction.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d041e-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="d041e-115">Error codes</span></span>



| <span data-ttu-id="d041e-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="d041e-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="d041e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d041e-117">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d041e-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d041e-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="d041e-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d041e-119">The operation was successful.</span></span><br/>                                       |
| <dl> <span data-ttu-id="d041e-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d041e-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="d041e-121">Параметр имеет **значение NULL** или не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="d041e-121">The parameter is **NULL** or not a valid value.</span></span><br/>                     |
| <dl> <span data-ttu-id="d041e-122"><dt>Д \_ ACCESSDENIED</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="d041e-122"><dt>E\_ACCESSDENIED</dt> <dt>0x80070005</dt></span></span> </dl>    | <span data-ttu-id="d041e-123">У текущего пользователя недостаточно прав доступа к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="d041e-123">The current user has insufficient access to the configuration file.</span></span><br/> |
| <dl> <span data-ttu-id="d041e-124"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d041e-124"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="d041e-125">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="d041e-125">The configuration is unknown.</span></span><br/>                                       |
| <dl> <span data-ttu-id="d041e-126"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d041e-126"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="d041e-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d041e-127">An unexpected error has occurred.</span></span><br/>                                   |



## <a name="remarks"></a><span data-ttu-id="d041e-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d041e-128">Remarks</span></span>

<span data-ttu-id="d041e-129">По умолчанию работающие виртуальные машины сохраняются при выходе Windows Virtual PC.</span><span class="sxs-lookup"><span data-stu-id="d041e-129">By default, running VMs are saved when Windows Virtual PC is quit.</span></span> <span data-ttu-id="d041e-130">Действие завершения работы **вмшутдовнактион \_ Save** (0) сохранит состояние виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d041e-130">The shutdown action **vmShutdownAction\_Save** (0) will save the VM's state.</span></span> <span data-ttu-id="d041e-131">Действие **вмшутдовнактион \_ турнофф** (1) отключит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d041e-131">The **vmShutdownAction\_TurnOff** (1) action will turn off the VM.</span></span> <span data-ttu-id="d041e-132">Действие **\_ Завершение работы вмшутдовнактион** (2) приведет к завершению работы операционной системы на виртуальной машине, если компоненты интеграции доступны и в противном случае сохранит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d041e-132">The **vmShutdownAction\_Shutdown** (2) action will shut down the guest operating system if the integration components are available and will save the VM otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d041e-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d041e-133">Requirements</span></span>



| <span data-ttu-id="d041e-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d041e-134">Requirement</span></span> | <span data-ttu-id="d041e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d041e-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d041e-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d041e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d041e-137">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d041e-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d041e-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d041e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d041e-139">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d041e-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d041e-140">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d041e-140">End of client support</span></span><br/>    | <span data-ttu-id="d041e-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d041e-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d041e-142">Продукт</span><span class="sxs-lookup"><span data-stu-id="d041e-142">Product</span></span><br/>                  | <span data-ttu-id="d041e-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d041e-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d041e-144">Header</span><span class="sxs-lookup"><span data-stu-id="d041e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="d041e-145"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d041e-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d041e-146">IID</span><span class="sxs-lookup"><span data-stu-id="d041e-146">IID</span></span><br/>                      | <span data-ttu-id="d041e-147">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d041e-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d041e-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d041e-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d041e-149">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="d041e-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="d041e-150">**вмшутдовнактион**</span><span class="sxs-lookup"><span data-stu-id="d041e-150">**VMShutdownAction**</span></span>](vmshutdownaction.md)
</dt> </dl>

 

