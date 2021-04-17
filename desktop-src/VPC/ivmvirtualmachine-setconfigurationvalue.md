---
title: Метод Ивмвиртуалмачине Сетконфигуратионвалуе (Впккоминтерфацес. h)
description: Задает значение указанного параметра конфигурации для виртуальной машины.
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- Метод Сетконфигуратионвалуе Virtual PC
- Метод Сетконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Сетконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691906"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="986c0-106">Метод Ивмвиртуалмачине:: Сетконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="986c0-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="986c0-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="986c0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="986c0-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="986c0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="986c0-109">Задает значение указанного параметра конфигурации для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="986c0-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="986c0-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="986c0-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="986c0-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="986c0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986c0-112">*конфигуратионкэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="986c0-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986c0-113">Ключ, используемый для задания значения конфигурации, хранящегося в файле " \* . VMC".</span><span class="sxs-lookup"><span data-stu-id="986c0-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="986c0-114">Изменения следует вносить в " \* . VMC" только с помощью метода **сетконфигуратионвалуе** .</span><span class="sxs-lookup"><span data-stu-id="986c0-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="986c0-115">Изменение " \* . VMC" с помощью любого другого метода не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="986c0-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="986c0-116">*configurationValue* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="986c0-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="986c0-117">Значение конфигурации.</span><span class="sxs-lookup"><span data-stu-id="986c0-117">The configuration value.</span></span> <span data-ttu-id="986c0-118">Это значение может должно быть одним из следующих типов **вариантов** : **VT \_ Array** \| **VT \_ UI1** (необработанные байты), **VT \_ BSTR** (строка), **VT \_ UI4** (Integer) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="986c0-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986c0-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="986c0-119">Return value</span></span>

<span data-ttu-id="986c0-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="986c0-120">This method can return one of these values.</span></span>



| <span data-ttu-id="986c0-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="986c0-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="986c0-122">Описание</span><span class="sxs-lookup"><span data-stu-id="986c0-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="986c0-123"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="986c0-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="986c0-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="986c0-125"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="986c0-126">Параметр *конфигуратионкэй* имеет **значение NULL** или является пустым, либо параметр *configurationValue* не является допустимым типом Variant.</span><span class="sxs-lookup"><span data-stu-id="986c0-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="986c0-127"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="986c0-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="986c0-128">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="986c0-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="986c0-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="986c0-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="986c0-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="986c0-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="986c0-131">Remarks</span></span>

<span data-ttu-id="986c0-132">Для параметра *конфигуратионкэй* поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="986c0-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="986c0-133">значение *конфигуратионкэй*</span><span class="sxs-lookup"><span data-stu-id="986c0-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="986c0-134">Описание</span><span class="sxs-lookup"><span data-stu-id="986c0-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="986c0-135">Тип данных</span><span class="sxs-lookup"><span data-stu-id="986c0-135">Data type</span></span>            | <span data-ttu-id="986c0-136">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="986c0-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="986c0-137">"оборудование/BIOS/ \_ Синхронизация времени \_ при \_ загрузке"</span><span class="sxs-lookup"><span data-stu-id="986c0-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="986c0-138">значение true, если синхронизация CMOS-памяти виртуальной машины выполняется с часами узла при загрузке; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="986c0-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="986c0-139">логическая</span><span class="sxs-lookup"><span data-stu-id="986c0-139">"boolean"</span></span><br/> | <span data-ttu-id="986c0-140">True</span><span class="sxs-lookup"><span data-stu-id="986c0-140">"true"</span></span><br/> |
| <span data-ttu-id="986c0-141">"интеграция/Microsoft/ \_ время узла \_ Синхронизация/включение" "</span><span class="sxs-lookup"><span data-stu-id="986c0-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="986c0-142">"true", если синхронизация времени узла включена в компонентах интеграции; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="986c0-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="986c0-143">логическая</span><span class="sxs-lookup"><span data-stu-id="986c0-143">"boolean"</span></span><br/> | <span data-ttu-id="986c0-144">True</span><span class="sxs-lookup"><span data-stu-id="986c0-144">"true"</span></span><br/> |
| <span data-ttu-id="986c0-145">"параметры пользовательского интерфейса \_ / \_ Автоматическая \_ Публикация приложений"</span><span class="sxs-lookup"><span data-stu-id="986c0-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="986c0-146">"true", если автоматическая публикация приложений включена в компонентах интеграции; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="986c0-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="986c0-147">Это также называется виртуальными приложениями.</span><span class="sxs-lookup"><span data-stu-id="986c0-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="986c0-148">логическая</span><span class="sxs-lookup"><span data-stu-id="986c0-148">"boolean"</span></span><br/> | <span data-ttu-id="986c0-149">True</span><span class="sxs-lookup"><span data-stu-id="986c0-149">"true"</span></span><br/> |
| <span data-ttu-id="986c0-150">"параметры пользовательского интерфейса \_ /секунды \_ для \_ сохранения"</span><span class="sxs-lookup"><span data-stu-id="986c0-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="986c0-151">Число секунд ожидания перед сохранением виртуальной машины после закрытия всех приложений.</span><span class="sxs-lookup"><span data-stu-id="986c0-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="986c0-152">Однако значения ниже 20 и более 4 294 968 имеют особое значение.</span><span class="sxs-lookup"><span data-stu-id="986c0-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="986c0-153">Дополнительные сведения см. в следующем списке.</span><span class="sxs-lookup"><span data-stu-id="986c0-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="986c0-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="986c0-155">Никогда не сохраняйте виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="986c0-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="986c0-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="986c0-157">Подождите 20 секунд, прежде чем сохранять виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="986c0-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="986c0-158"><dt><span id="214_294_967"></span>21 4 294 967</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="986c0-159">Подождите указанное число секунд, прежде чем сохранять виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="986c0-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="986c0-160"><dt><span id="4_294_9684_294_967_295"></span>4 294 968 4 294 967 295</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="986c0-161">Подождите 4 294 968 секунд перед сохранением виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="986c0-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="986c0-162">цело</span><span class="sxs-lookup"><span data-stu-id="986c0-162">"integer"</span></span><br/> | <span data-ttu-id="986c0-163">300</span><span class="sxs-lookup"><span data-stu-id="986c0-163">300</span></span><br/>    |



 

<span data-ttu-id="986c0-164">Этот метод обеспечивает доступ низкого уровня к любому значению конфигурации.</span><span class="sxs-lookup"><span data-stu-id="986c0-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="986c0-165">Его можно использовать для задания значений конфигурации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="986c0-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="986c0-166">Будьте внимательны при использовании этого метода для задания значений конфигурации системы, так как для значения конфигурации не выполняется проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="986c0-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="986c0-167">Кроме того, некоторые значения конфигурации нельзя изменить, пока виртуальная машина работает.</span><span class="sxs-lookup"><span data-stu-id="986c0-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="986c0-168">Ключи конфигурации находятся в \* файле ". VMC" виртуальной машины в формате XML.</span><span class="sxs-lookup"><span data-stu-id="986c0-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="986c0-169">Ключи хранятся в виде иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="986c0-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="986c0-170">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="986c0-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="986c0-171">Например, чтобы задать значение ключа "ОЗУ \_ size", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="986c0-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="986c0-172">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="986c0-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="986c0-173">Если какой-либо из ключей в требуемом дереве имеет значение атрибута ID, атрибут и его значение внедряются в строку пути *конфигуратионкэй* сразу после связанного с ней ключа конфигурации, используя следующий формат в квадратных скобках: " \[ @id ="*\_ значение идентификатора*" \] ".</span><span class="sxs-lookup"><span data-stu-id="986c0-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="986c0-174">Например, чтобы задать значение ключа «гольф», расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="986c0-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="986c0-175">Строка пути *конфигуратионкэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="986c0-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="986c0-176">Требования</span><span class="sxs-lookup"><span data-stu-id="986c0-176">Requirements</span></span>



| <span data-ttu-id="986c0-177">Требование</span><span class="sxs-lookup"><span data-stu-id="986c0-177">Requirement</span></span> | <span data-ttu-id="986c0-178">Значение</span><span class="sxs-lookup"><span data-stu-id="986c0-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="986c0-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="986c0-179">Minimum supported client</span></span><br/> | <span data-ttu-id="986c0-180">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="986c0-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="986c0-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="986c0-181">Minimum supported server</span></span><br/> | <span data-ttu-id="986c0-182">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="986c0-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="986c0-183">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="986c0-183">End of client support</span></span><br/>    | <span data-ttu-id="986c0-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="986c0-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="986c0-185">Продукт</span><span class="sxs-lookup"><span data-stu-id="986c0-185">Product</span></span><br/>                  | <span data-ttu-id="986c0-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="986c0-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="986c0-187">Header</span><span class="sxs-lookup"><span data-stu-id="986c0-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="986c0-188"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="986c0-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="986c0-189">IID</span><span class="sxs-lookup"><span data-stu-id="986c0-189">IID</span></span><br/>                      | <span data-ttu-id="986c0-190">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="986c0-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="986c0-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="986c0-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986c0-192">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="986c0-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="986c0-193">**Ивмвиртуалпк:: Сетконфигуратионвалуе**</span><span class="sxs-lookup"><span data-stu-id="986c0-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

