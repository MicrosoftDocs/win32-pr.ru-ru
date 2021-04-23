---
title: Метод Ивмвиртуалмачине Ремовеактиватионвалуе (Впккоминтерфацес. h)
description: Удаляет значение указанного параметра активации для этой виртуальной машины.
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- Метод Ремовеактиватионвалуе Virtual PC
- Метод Ремовеактиватионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Ремовеактиватионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071717"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="35ebf-106">Метод Ивмвиртуалмачине:: Ремовеактиватионвалуе</span><span class="sxs-lookup"><span data-stu-id="35ebf-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="35ebf-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="35ebf-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35ebf-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="35ebf-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35ebf-109">Удаляет значение указанного параметра активации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35ebf-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ebf-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="35ebf-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="35ebf-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="35ebf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ebf-112">*активатионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="35ebf-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ebf-113">Ключ, используемый для обнаружения значения активации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="35ebf-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ebf-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="35ebf-114">Return value</span></span>

<span data-ttu-id="35ebf-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="35ebf-115">This method can return one of these values.</span></span>



| <span data-ttu-id="35ebf-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="35ebf-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="35ebf-117">Описание</span><span class="sxs-lookup"><span data-stu-id="35ebf-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35ebf-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="35ebf-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35ebf-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="35ebf-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="35ebf-121">Параметр имеет **значение NULL** или является пустым.</span><span class="sxs-lookup"><span data-stu-id="35ebf-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="35ebf-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="35ebf-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="35ebf-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="35ebf-124"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="35ebf-125">Предпочтение не найдено, или эта конфигурация не имеет допустимой активации.</span><span class="sxs-lookup"><span data-stu-id="35ebf-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="35ebf-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="35ebf-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="35ebf-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="35ebf-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="35ebf-128">Remarks</span></span>

<span data-ttu-id="35ebf-129">Этот метод обеспечивает доступ низкого уровня к любому значению активации.</span><span class="sxs-lookup"><span data-stu-id="35ebf-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="35ebf-130">Его можно использовать для удаления значений активации для определяемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="35ebf-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="35ebf-131">Будьте внимательны при использовании этого метода для удаления значений активации системы, так как некоторые значения не могут быть изменены во время работы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35ebf-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="35ebf-132">При запуске виртуальной машины выполняется копия ее значений конфигурации, которая становится набором значений активации.</span><span class="sxs-lookup"><span data-stu-id="35ebf-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="35ebf-133">Значения активации сохраняются до тех пор, пока виртуальная машина не будет выключена или перезапущена.</span><span class="sxs-lookup"><span data-stu-id="35ebf-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="35ebf-134">Обратите внимание, что Windows Virtual PC может использовать конфигурацию только для хранения значений для определенных ключей, то есть значение активации не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="35ebf-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="35ebf-135">Для изменения любых значений активации необходимо запустить сеанс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35ebf-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="35ebf-136">Ключи активации хранятся внутри иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="35ebf-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="35ebf-137">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="35ebf-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="35ebf-138">Например, чтобы удалить значение ключа "действие по умолчанию \_ ", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="35ebf-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="35ebf-139">Строка пути *активатионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="35ebf-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="35ebf-140">Требования</span><span class="sxs-lookup"><span data-stu-id="35ebf-140">Requirements</span></span>



| <span data-ttu-id="35ebf-141">Требование</span><span class="sxs-lookup"><span data-stu-id="35ebf-141">Requirement</span></span> | <span data-ttu-id="35ebf-142">Значение</span><span class="sxs-lookup"><span data-stu-id="35ebf-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ebf-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="35ebf-143">Minimum supported client</span></span><br/> | <span data-ttu-id="35ebf-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="35ebf-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35ebf-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="35ebf-145">Minimum supported server</span></span><br/> | <span data-ttu-id="35ebf-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="35ebf-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35ebf-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="35ebf-147">End of client support</span></span><br/>    | <span data-ttu-id="35ebf-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35ebf-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35ebf-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="35ebf-149">Product</span></span><br/>                  | <span data-ttu-id="35ebf-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35ebf-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35ebf-151">Header</span><span class="sxs-lookup"><span data-stu-id="35ebf-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ebf-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="35ebf-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35ebf-153">IID</span><span class="sxs-lookup"><span data-stu-id="35ebf-153">IID</span></span><br/>                      | <span data-ttu-id="35ebf-154">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="35ebf-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="35ebf-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="35ebf-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ebf-156">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="35ebf-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

