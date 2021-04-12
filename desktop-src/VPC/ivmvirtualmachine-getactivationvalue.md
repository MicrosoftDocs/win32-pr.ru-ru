---
title: Метод Ивмвиртуалмачине Жетактиватионвалуе (Впккоминтерфацес. h)
description: Извлекает значение указанного параметра активации для этой виртуальной машины.
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- Метод Жетактиватионвалуе Virtual PC
- Метод Жетактиватионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Жетактиватионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340315"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="d1398-106">Метод Ивмвиртуалмачине:: Жетактиватионвалуе</span><span class="sxs-lookup"><span data-stu-id="d1398-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="d1398-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="d1398-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="d1398-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="d1398-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="d1398-109">Извлекает значение указанного параметра активации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d1398-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1398-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1398-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="d1398-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1398-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1398-112">*активатионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d1398-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1398-113">Ключ, используемый для обнаружения значения активации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="d1398-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="d1398-114">*активатионвалуе* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="d1398-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="d1398-115">Значение активации.</span><span class="sxs-lookup"><span data-stu-id="d1398-115">The activation value.</span></span> <span data-ttu-id="d1398-116">Это значение может быть одним из следующих **вариантов** : **VT \_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ I4** (целое число) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="d1398-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1398-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d1398-117">Return value</span></span>

<span data-ttu-id="d1398-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="d1398-118">This method can return one of these values.</span></span>



| <span data-ttu-id="d1398-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="d1398-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="d1398-120">Описание</span><span class="sxs-lookup"><span data-stu-id="d1398-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d1398-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d1398-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="d1398-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="d1398-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="d1398-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="d1398-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="d1398-124">Параметр *активатионкэй* имеет **значение NULL** или является пустым.</span><span class="sxs-lookup"><span data-stu-id="d1398-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="d1398-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="d1398-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="d1398-126">Параметр *активатионвалуе* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="d1398-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="d1398-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="d1398-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="d1398-128">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="d1398-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="d1398-129"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="d1398-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="d1398-130">Предпочтение не найдено, или эта конфигурация не имеет допустимой активации.</span><span class="sxs-lookup"><span data-stu-id="d1398-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="d1398-131"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="d1398-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="d1398-132">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="d1398-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="d1398-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1398-133">Remarks</span></span>

<span data-ttu-id="d1398-134">Этот метод обеспечивает доступ низкого уровня к любому значению активации.</span><span class="sxs-lookup"><span data-stu-id="d1398-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="d1398-135">Его можно использовать для задания значений активации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="d1398-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="d1398-136">При запуске виртуальной машины выполняется копия ее значений конфигурации, которая становится набором значений активации.</span><span class="sxs-lookup"><span data-stu-id="d1398-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="d1398-137">Значения активации сохраняются до тех пор, пока виртуальная машина не будет выключена или перезапущена.</span><span class="sxs-lookup"><span data-stu-id="d1398-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="d1398-138">Обратите внимание, что Windows Virtual PC может использовать конфигурацию только для хранения значений для определенных ключей, то есть значение активации не может использоваться.</span><span class="sxs-lookup"><span data-stu-id="d1398-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="d1398-139">Ключи активации хранятся внутри иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="d1398-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="d1398-140">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="d1398-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="d1398-141">Например, чтобы прочитать значение ключа "действие по умолчанию \_ ", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="d1398-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="d1398-142">Строка пути *активатионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d1398-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="d1398-143">Требования</span><span class="sxs-lookup"><span data-stu-id="d1398-143">Requirements</span></span>



| <span data-ttu-id="d1398-144">Требование</span><span class="sxs-lookup"><span data-stu-id="d1398-144">Requirement</span></span> | <span data-ttu-id="d1398-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d1398-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1398-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1398-146">Minimum supported client</span></span><br/> | <span data-ttu-id="d1398-147">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="d1398-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d1398-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1398-148">Minimum supported server</span></span><br/> | <span data-ttu-id="d1398-149">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d1398-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="d1398-150">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="d1398-150">End of client support</span></span><br/>    | <span data-ttu-id="d1398-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d1398-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="d1398-152">Продукт</span><span class="sxs-lookup"><span data-stu-id="d1398-152">Product</span></span><br/>                  | <span data-ttu-id="d1398-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="d1398-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="d1398-154">Header</span><span class="sxs-lookup"><span data-stu-id="d1398-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1398-155"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1398-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="d1398-156">IID</span><span class="sxs-lookup"><span data-stu-id="d1398-156">IID</span></span><br/>                      | <span data-ttu-id="d1398-157">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="d1398-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="d1398-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1398-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1398-159">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="d1398-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

