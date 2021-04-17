---
title: Метод Ивмвиртуалмачине Жетконфигуратионвалуе (Впккоминтерфацес. h)
description: Извлекает значение указанного параметра конфигурации для этой виртуальной машины.
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- Метод Жетконфигуратионвалуе Virtual PC
- Метод Жетконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Жетконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415673"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="8256d-106">Метод Ивмвиртуалмачине:: Жетконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="8256d-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="8256d-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="8256d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8256d-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="8256d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8256d-109">Извлекает значение указанного параметра конфигурации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8256d-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="8256d-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8256d-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="8256d-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="8256d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8256d-112">*конфигуратионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8256d-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8256d-113">Ключ, используемый для задания значения конфигурации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="8256d-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="8256d-114">*configurationValue* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8256d-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="8256d-115">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8256d-115">The configuration value.</span></span> <span data-ttu-id="8256d-116">Это значение может быть одним из следующих **вариантов** : **VT \_ Array** \| **VT \_ UI1** (RAW bytes), **VT \_ BSTR** (String), **VT \_ I4** (целое число) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="8256d-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8256d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8256d-117">Return value</span></span>

<span data-ttu-id="8256d-118">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="8256d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="8256d-119">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="8256d-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="8256d-120">Описание</span><span class="sxs-lookup"><span data-stu-id="8256d-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="8256d-121"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8256d-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="8256d-122">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8256d-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="8256d-123"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8256d-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="8256d-124">Параметр *конфигуратионкэй* имеет **значение NULL** или является пустым.</span><span class="sxs-lookup"><span data-stu-id="8256d-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="8256d-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="8256d-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="8256d-126">Параметр *configurationValue* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="8256d-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="8256d-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8256d-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="8256d-128">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="8256d-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="8256d-129"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8256d-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="8256d-130">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="8256d-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="8256d-131"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8256d-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="8256d-132">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="8256d-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="8256d-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8256d-133">Remarks</span></span>

<span data-ttu-id="8256d-134">Этот метод обеспечивает доступ низкого уровня к любому значению конфигурации.</span><span class="sxs-lookup"><span data-stu-id="8256d-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="8256d-135">Его можно использовать для считывания значений конфигурации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="8256d-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="8256d-136">Ключи конфигурации находятся в \* файле ". VMC" виртуальной машины в формате XML.</span><span class="sxs-lookup"><span data-stu-id="8256d-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="8256d-137">Ключи хранятся в виде иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="8256d-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="8256d-138">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="8256d-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="8256d-139">Например, для чтения значения ключа "RAM \_ size", расположенного в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="8256d-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="8256d-140">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8256d-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="8256d-141">Если какой-либо из ключей в требуемом дереве имеет значение атрибута ID, атрибут и его значение внедряются в строку пути *конфигуратионкэй* сразу после связанного с ней ключа конфигурации, используя следующий формат в квадратных скобках: " \[ @id ="*\_ значение идентификатора*" \] ".</span><span class="sxs-lookup"><span data-stu-id="8256d-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="8256d-142">Например, чтобы считать значение абсолютного ключа, расположенного в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="8256d-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="8256d-143">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8256d-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="8256d-144">Требования</span><span class="sxs-lookup"><span data-stu-id="8256d-144">Requirements</span></span>



| <span data-ttu-id="8256d-145">Требование</span><span class="sxs-lookup"><span data-stu-id="8256d-145">Requirement</span></span> | <span data-ttu-id="8256d-146">Значение</span><span class="sxs-lookup"><span data-stu-id="8256d-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8256d-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8256d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="8256d-148">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8256d-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8256d-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8256d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="8256d-150">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8256d-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8256d-151">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8256d-151">End of client support</span></span><br/>    | <span data-ttu-id="8256d-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8256d-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8256d-153">Продукт</span><span class="sxs-lookup"><span data-stu-id="8256d-153">Product</span></span><br/>                  | <span data-ttu-id="8256d-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8256d-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8256d-155">Header</span><span class="sxs-lookup"><span data-stu-id="8256d-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="8256d-156"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="8256d-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8256d-157">IID</span><span class="sxs-lookup"><span data-stu-id="8256d-157">IID</span></span><br/>                      | <span data-ttu-id="8256d-158">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="8256d-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="8256d-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8256d-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8256d-160">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="8256d-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

