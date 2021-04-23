---
title: Метод Ивмвиртуалмачине Ремовеконфигуратионвалуе (Впккоминтерфацес. h)
description: Удаляет значение указанного параметра конфигурации для этой виртуальной машины.
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- Метод Ремовеконфигуратионвалуе Virtual PC
- Метод Ремовеконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Ремовеконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491877"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="837fd-106">Метод Ивмвиртуалмачине:: Ремовеконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="837fd-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="837fd-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="837fd-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="837fd-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="837fd-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="837fd-109">Удаляет значение указанного параметра конфигурации для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="837fd-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="837fd-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="837fd-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="837fd-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="837fd-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="837fd-112">*конфигуратионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="837fd-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="837fd-113">Ключ, используемый для задания значения конфигурации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="837fd-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="837fd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="837fd-114">Return value</span></span>

<span data-ttu-id="837fd-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="837fd-115">This method can return one of these values.</span></span>



| <span data-ttu-id="837fd-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="837fd-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="837fd-117">Описание</span><span class="sxs-lookup"><span data-stu-id="837fd-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="837fd-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="837fd-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="837fd-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="837fd-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="837fd-120"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="837fd-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="837fd-121">Параметр имеет **значение NULL** или является пустым.</span><span class="sxs-lookup"><span data-stu-id="837fd-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="837fd-122"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="837fd-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="837fd-123">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="837fd-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="837fd-124"><dt>**Виртуальная машина \_ E \_ преф \_ не \_ Найдено**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="837fd-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="837fd-125">Предпочтение не найдено.</span><span class="sxs-lookup"><span data-stu-id="837fd-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="837fd-126"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="837fd-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="837fd-127">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="837fd-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="837fd-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="837fd-128">Remarks</span></span>

<span data-ttu-id="837fd-129">Этот метод обеспечивает доступ низкого уровня к любому значению конфигурации.</span><span class="sxs-lookup"><span data-stu-id="837fd-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="837fd-130">Его можно использовать для удаления значений конфигурации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="837fd-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="837fd-131">Будьте внимательны при использовании этого метода для удаления значений конфигурации системы, так как некоторые значения не могут быть изменены во время работы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="837fd-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="837fd-132">Ключи конфигурации находятся в \* файле ". VMC" виртуальной машины в формате XML.</span><span class="sxs-lookup"><span data-stu-id="837fd-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="837fd-133">Ключи хранятся в виде иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="837fd-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="837fd-134">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="837fd-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="837fd-135">Например, чтобы удалить значение ключа "ОЗУ \_ size", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="837fd-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="837fd-136">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="837fd-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="837fd-137">Если какой-либо из ключей в требуемом дереве имеет значение атрибута ID, атрибут и его значение внедряются в строку пути *конфигуратионкэй* сразу после связанного с ней ключа конфигурации, используя следующий формат в квадратных скобках: " \[ @id ="*\_ значение идентификатора*" \] ".</span><span class="sxs-lookup"><span data-stu-id="837fd-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="837fd-138">Например, чтобы удалить значение абсолютного ключа, расположенного в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="837fd-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="837fd-139">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="837fd-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="837fd-140">Требования</span><span class="sxs-lookup"><span data-stu-id="837fd-140">Requirements</span></span>



| <span data-ttu-id="837fd-141">Требование</span><span class="sxs-lookup"><span data-stu-id="837fd-141">Requirement</span></span> | <span data-ttu-id="837fd-142">Значение</span><span class="sxs-lookup"><span data-stu-id="837fd-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="837fd-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="837fd-143">Minimum supported client</span></span><br/> | <span data-ttu-id="837fd-144">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="837fd-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="837fd-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="837fd-145">Minimum supported server</span></span><br/> | <span data-ttu-id="837fd-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="837fd-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="837fd-147">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="837fd-147">End of client support</span></span><br/>    | <span data-ttu-id="837fd-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="837fd-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="837fd-149">Продукт</span><span class="sxs-lookup"><span data-stu-id="837fd-149">Product</span></span><br/>                  | <span data-ttu-id="837fd-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="837fd-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="837fd-151">Header</span><span class="sxs-lookup"><span data-stu-id="837fd-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="837fd-152"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="837fd-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="837fd-153">IID</span><span class="sxs-lookup"><span data-stu-id="837fd-153">IID</span></span><br/>                      | <span data-ttu-id="837fd-154">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="837fd-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="837fd-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="837fd-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837fd-156">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="837fd-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

