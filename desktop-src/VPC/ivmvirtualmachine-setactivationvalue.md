---
title: Метод Ивмвиртуалмачине Сетактиватионвалуе (Впккоминтерфацес. h)
description: Задает значение указанного параметра активации для этой виртуальной машины.
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- Метод Сетактиватионвалуе Virtual PC
- Метод Сетактиватионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Сетактиватионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492225"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="2dafa-106">Метод Ивмвиртуалмачине:: Сетактиватионвалуе</span><span class="sxs-lookup"><span data-stu-id="2dafa-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="2dafa-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2dafa-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="2dafa-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="2dafa-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="2dafa-109">Задает значение указанного параметра активации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2dafa-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dafa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2dafa-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="2dafa-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="2dafa-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dafa-112">*активатионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dafa-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dafa-113">Ключ, используемый для обнаружения значения активации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="2dafa-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="2dafa-114">*активатионвалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2dafa-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dafa-115">Значение активации.</span><span class="sxs-lookup"><span data-stu-id="2dafa-115">The activation value.</span></span> <span data-ttu-id="2dafa-116">Это значение может быть одним из следующих **вариантов** : **VT \_ Array** \| **VT \_ UI1** (необработанные байты) **, VT \_ BSTR** (String), **VT \_ UI4** (целое число) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="2dafa-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dafa-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2dafa-117">Return value</span></span>

<span data-ttu-id="2dafa-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="2dafa-118">This method can return one of these values.</span></span>



| <span data-ttu-id="2dafa-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="2dafa-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="2dafa-120">Описание</span><span class="sxs-lookup"><span data-stu-id="2dafa-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2dafa-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="2dafa-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2dafa-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="2dafa-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="2dafa-124">Параметр *активатионкэй* имеет **значение NULL** или является пустым, либо параметр *активатионвалуе* не является допустимым типом Variant.</span><span class="sxs-lookup"><span data-stu-id="2dafa-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="2dafa-125"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="2dafa-126">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="2dafa-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="2dafa-127"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="2dafa-128">В конфигурации отсутствует действительная активация.</span><span class="sxs-lookup"><span data-stu-id="2dafa-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="2dafa-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="2dafa-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2dafa-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="2dafa-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2dafa-131">Remarks</span></span>

<span data-ttu-id="2dafa-132">Этот метод обеспечивает доступ низкого уровня к любому значению активации.</span><span class="sxs-lookup"><span data-stu-id="2dafa-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="2dafa-133">Его можно использовать для задания значений активации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="2dafa-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="2dafa-134">Будьте внимательны при использовании этого метода для задания значений активации системы, так как для значения активации не выполняется проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="2dafa-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="2dafa-135">Кроме того, некоторые значения активации нельзя изменить, пока виртуальная машина работает.</span><span class="sxs-lookup"><span data-stu-id="2dafa-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="2dafa-136">При запуске виртуальной машины выполняется копия ее значений конфигурации, которая становится набором значений активации.</span><span class="sxs-lookup"><span data-stu-id="2dafa-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="2dafa-137">Значения активации сохраняются до тех пор, пока виртуальная машина не будет выключена или перезапущена.</span><span class="sxs-lookup"><span data-stu-id="2dafa-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="2dafa-138">Обратите внимание, что Windows Virtual PC может использовать конфигурацию только для хранения значений для определенных ключей, то есть значение активации не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="2dafa-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="2dafa-139">Для изменения любых значений активации необходимо запустить сеанс виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2dafa-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="2dafa-140">Ключи активации хранятся внутри иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="2dafa-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="2dafa-141">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="2dafa-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="2dafa-142">Например, чтобы задать значение ключа "действие по умолчанию \_ ", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="2dafa-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="2dafa-143">Строка пути *активатионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2dafa-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="2dafa-144">Требования</span><span class="sxs-lookup"><span data-stu-id="2dafa-144">Requirements</span></span>



| <span data-ttu-id="2dafa-145">Требование</span><span class="sxs-lookup"><span data-stu-id="2dafa-145">Requirement</span></span> | <span data-ttu-id="2dafa-146">Значение</span><span class="sxs-lookup"><span data-stu-id="2dafa-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dafa-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2dafa-147">Minimum supported client</span></span><br/> | <span data-ttu-id="2dafa-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2dafa-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2dafa-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2dafa-149">Minimum supported server</span></span><br/> | <span data-ttu-id="2dafa-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="2dafa-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="2dafa-151">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="2dafa-151">End of client support</span></span><br/>    | <span data-ttu-id="2dafa-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="2dafa-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="2dafa-153">Продукт</span><span class="sxs-lookup"><span data-stu-id="2dafa-153">Product</span></span><br/>                  | <span data-ttu-id="2dafa-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="2dafa-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="2dafa-155">Header</span><span class="sxs-lookup"><span data-stu-id="2dafa-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dafa-156"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="2dafa-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="2dafa-157">IID</span><span class="sxs-lookup"><span data-stu-id="2dafa-157">IID</span></span><br/>                      | <span data-ttu-id="2dafa-158">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="2dafa-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="2dafa-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2dafa-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dafa-160">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="2dafa-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

