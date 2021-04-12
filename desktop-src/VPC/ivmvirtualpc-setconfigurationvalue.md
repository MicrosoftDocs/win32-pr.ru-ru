---
title: Метод Ивмвиртуалпк Сетконфигуратионвалуе (Впккоминтерфацес. h)
description: Задает значение указанного параметра конфигурации.
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- Метод Сетконфигуратионвалуе Virtual PC
- Метод Сетконфигуратионвалуе Virtual PC, интерфейс Ивмвиртуалпк
- Ивмвиртуалпк интерфейс Virtual PC, метод Сетконфигуратионвалуе
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534853"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="b1a64-106">Метод Ивмвиртуалпк:: Сетконфигуратионвалуе</span><span class="sxs-lookup"><span data-stu-id="b1a64-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="b1a64-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b1a64-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b1a64-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b1a64-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b1a64-109">Задает значение указанного параметра конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b1a64-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a64-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1a64-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="b1a64-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1a64-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a64-112">*преференцекэй* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1a64-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a64-113">Ключ, используемый для задания предпочтения, который хранится в файле конфигурации для каждого пользователя (Options.xml в "% LocalAppData% \\ Microsoft \\ Windows Virtual PC").</span><span class="sxs-lookup"><span data-stu-id="b1a64-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1a64-114">Необходимо внести изменения в Options.xml только с помощью метода **сетконфигуратионвалуе** .</span><span class="sxs-lookup"><span data-stu-id="b1a64-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="b1a64-115">Изменение Options.xml с помощью любого другого метода не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b1a64-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="b1a64-116">*преференцевалуе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b1a64-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a64-117">Значение предпочтения.</span><span class="sxs-lookup"><span data-stu-id="b1a64-117">The preference value.</span></span> <span data-ttu-id="b1a64-118">Это значение может быть одним из следующих **вариантов** : **VT \_ Array** \| **VT \_ UI1** (необработанные байты) **, VT \_ BSTR** (String), **VT \_ UI4** (целое число) или **VT \_ bool** (Boolean).</span><span class="sxs-lookup"><span data-stu-id="b1a64-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a64-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1a64-119">Return value</span></span>

<span data-ttu-id="b1a64-120">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="b1a64-120">This method can return one of these values.</span></span>



| <span data-ttu-id="b1a64-121">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="b1a64-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="b1a64-122">Описание</span><span class="sxs-lookup"><span data-stu-id="b1a64-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1a64-123"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="b1a64-124">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b1a64-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="b1a64-125"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b1a64-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="b1a64-126">Параметр *преференцекэй* или *Преференцевалуе* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="b1a64-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="b1a64-127"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="b1a64-128">Параметр *преференцекэй* недопустим или является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="b1a64-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="b1a64-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="b1a64-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1a64-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="b1a64-131"><dt>**Д \_ ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="b1a64-132">У текущего пользователя недостаточно прав доступа к файлу конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b1a64-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="b1a64-133"><dt>**Виртуальная машина \_ E \_ аппаратная \_ виртуализация \_ отключена**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="b1a64-134">Процессор не поддерживает расширения виртуализации с аппаратным ускорением (ЗАКОНЧИТЕ).</span><span class="sxs-lookup"><span data-stu-id="b1a64-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1a64-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1a64-135">Remarks</span></span>

<span data-ttu-id="b1a64-136">Для параметра *преференцекэй* поддерживаются следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b1a64-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="b1a64-137">значение *преференцекэй*</span><span class="sxs-lookup"><span data-stu-id="b1a64-137">*preferenceKey* value</span></span>      | <span data-ttu-id="b1a64-138">Описание</span><span class="sxs-lookup"><span data-stu-id="b1a64-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="b1a64-139">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b1a64-139">Data type</span></span>            | <span data-ttu-id="b1a64-140">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b1a64-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="b1a64-141">" \_ время ожидания простоя"</span><span class="sxs-lookup"><span data-stu-id="b1a64-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="b1a64-142">Количество секунд, в течение которых vpc.exe должно ожидать выхода, если нет активных виртуальных машин или приложений, использующих [интерфейсы ВИРТУАЛЬНЫХ ПК Windows](virtual-pc-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b1a64-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="b1a64-143">цело</span><span class="sxs-lookup"><span data-stu-id="b1a64-143">"integer"</span></span><br/> | <span data-ttu-id="b1a64-144">пределах</span><span class="sxs-lookup"><span data-stu-id="b1a64-144">"30"</span></span><br/> |



 

<span data-ttu-id="b1a64-145">Этот метод обеспечивает доступ низкого уровня к любому значению конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b1a64-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="b1a64-146">Его можно использовать для задания значений конфигурации для определяемых пользователем ключей.</span><span class="sxs-lookup"><span data-stu-id="b1a64-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="b1a64-147">Будьте внимательны при использовании этого метода для задания значений конфигурации системы, так как для значения конфигурации не выполняется проверка ошибок.</span><span class="sxs-lookup"><span data-stu-id="b1a64-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="b1a64-148">Кроме того, некоторые значения конфигурации нельзя изменить во время работы виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1a64-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="b1a64-149">Ключи конфигурации находятся в файле "Options.xml" виртуальной машины в формате XML.</span><span class="sxs-lookup"><span data-stu-id="b1a64-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="b1a64-150">Ключи хранятся в виде иерархической структуры аналогично разделам реестра в Windows.</span><span class="sxs-lookup"><span data-stu-id="b1a64-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="b1a64-151">Чтобы указать конкретный подраздел, создается «путь к ключу», который задает различные ключи в формате с разделителями-отметками.</span><span class="sxs-lookup"><span data-stu-id="b1a64-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="b1a64-152">Например, чтобы задать значение ключа "время ожидания простоя \_ ", расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="b1a64-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="b1a64-153">Строка пути *преференцекэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b1a64-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="b1a64-154">Если какой-либо из ключей в требуемом дереве имеет значение атрибута ID, атрибут и его значение внедряются в строку пути *преференцекэй* сразу после связанного с ней ключа конфигурации, используя следующий формат в квадратных скобках: " \[ @id ="*\_ значение идентификатора*" \] ".</span><span class="sxs-lookup"><span data-stu-id="b1a64-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="b1a64-155">Например, чтобы задать значение ключа «гольф», расположенное в следующем дереве ключей:</span><span class="sxs-lookup"><span data-stu-id="b1a64-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="b1a64-156">Строка пути *преференцекэй* будет указана следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b1a64-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="b1a64-157">Требования</span><span class="sxs-lookup"><span data-stu-id="b1a64-157">Requirements</span></span>



| <span data-ttu-id="b1a64-158">Требование</span><span class="sxs-lookup"><span data-stu-id="b1a64-158">Requirement</span></span> | <span data-ttu-id="b1a64-159">Значение</span><span class="sxs-lookup"><span data-stu-id="b1a64-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a64-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1a64-160">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a64-161">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b1a64-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b1a64-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1a64-162">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a64-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b1a64-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b1a64-164">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b1a64-164">End of client support</span></span><br/>    | <span data-ttu-id="b1a64-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b1a64-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b1a64-166">Продукт</span><span class="sxs-lookup"><span data-stu-id="b1a64-166">Product</span></span><br/>                  | <span data-ttu-id="b1a64-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b1a64-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b1a64-168">Header</span><span class="sxs-lookup"><span data-stu-id="b1a64-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a64-169"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a64-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b1a64-170">IID</span><span class="sxs-lookup"><span data-stu-id="b1a64-170">IID</span></span><br/>                      | <span data-ttu-id="b1a64-171">IID \_ ивмвиртуалпк определен как 236ba0d9-a24a-4292-A132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b1a64-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b1a64-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1a64-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a64-173">**ивмвиртуалпк**</span><span class="sxs-lookup"><span data-stu-id="b1a64-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="b1a64-174">**Ивмвиртуалмачине:: Сетконфигуратионвалуе**</span><span class="sxs-lookup"><span data-stu-id="b1a64-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

