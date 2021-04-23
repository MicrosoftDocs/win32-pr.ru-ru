---
description: Метод Enable \_ класса TPM Win32 указывает, включено ли устройство. Это значение можно изменить с помощью методов Enable и Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Включенный метод класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682548"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="effa5-104">Включенный метод \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="effa5-104">IsEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="effa5-105">Метод **Enable** класса [**\_ TPM Win32**](win32-tpm.md) указывает, включено ли устройство.</span><span class="sxs-lookup"><span data-stu-id="effa5-105">The **IsEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is enabled.</span></span> <span data-ttu-id="effa5-106">Это значение можно изменить с помощью методов [**Enable**](enable-win32-tpm.md) и [**Disable**](disable-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="effa5-106">This value can be changed by the [**Enable**](enable-win32-tpm.md) and [**Disable**](disable-win32-tpm.md) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="effa5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="effa5-107">Syntax</span></span>


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="effa5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="effa5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effa5-109">*Включено* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="effa5-109">*IsEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="effa5-110">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="effa5-110">Type: **boolean**</span></span>

<span data-ttu-id="effa5-111">Если задано **значение true**, устройство включено.</span><span class="sxs-lookup"><span data-stu-id="effa5-111">If **true**, the device is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="effa5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="effa5-112">Return value</span></span>

<span data-ttu-id="effa5-113">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="effa5-113">Type: **uint32**</span></span>

<span data-ttu-id="effa5-114">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="effa5-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="effa5-115">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="effa5-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="effa5-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="effa5-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="effa5-117">Описание</span><span class="sxs-lookup"><span data-stu-id="effa5-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="effa5-118"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="effa5-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="effa5-119">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="effa5-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="effa5-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="effa5-120">Remarks</span></span>

<span data-ttu-id="effa5-121">В соответствии со спецификацией организация TCG (TCG) v 1.2 доступны только следующие команды, если устройство находится в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="effa5-121">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="effa5-122">\_КОНТИНУЕСЕЛФТЕСТ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-122">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="effa5-123">\_ДСАП TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-123">TPM\_DSAP</span></span>
-   <span data-ttu-id="effa5-124">\_ФЛУШСПЕЦИФИК TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-124">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="effa5-125">\_Поддержка TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-125">TPM\_GetCapability</span></span>
-   <span data-ttu-id="effa5-126">\_ЖЕТТЕСТРЕСУЛТ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-126">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="effa5-127">\_Инициализация TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-127">TPM\_Init</span></span>
-   <span data-ttu-id="effa5-128">\_ОИАП TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-128">TPM\_OIAP</span></span>
-   <span data-ttu-id="effa5-129">\_ОСАП TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-129">TPM\_OSAP</span></span>
-   <span data-ttu-id="effa5-130">\_ОВНЕРСЕТДИСАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-130">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="effa5-131">\_ \_ Сброс параметров PCR модуля</span><span class="sxs-lookup"><span data-stu-id="effa5-131">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="effa5-132">\_ФИСИКАЛДИСАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-132">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="effa5-133">\_ФИСИКАЛЕНАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-133">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="effa5-134">\_ФИСИКАЛСЕТДЕАКТИВАТЕД TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-134">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="effa5-135">\_Сброс TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-135">TPM\_Reset</span></span>
-   <span data-ttu-id="effa5-136">Модуль \_ SaveState TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-136">TPM\_SaveState</span></span>
-   <span data-ttu-id="effa5-137">\_СЕЛФТЕСТФУЛЛ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-137">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="effa5-138">\_СЕТКАПАБИЛИТИ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-138">TPM\_SetCapability</span></span>
-   <span data-ttu-id="effa5-139">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-139">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="effa5-140">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-140">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="effa5-141">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-141">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="effa5-142">\_Запуск TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-142">TPM\_Startup</span></span>
-   <span data-ttu-id="effa5-143">\_ТАКЕОВНЕРШИП TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-143">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="effa5-144">\_Маркер завершения \_ TPM</span><span class="sxs-lookup"><span data-stu-id="effa5-144">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="effa5-145">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="effa5-145">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="effa5-146">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="effa5-146">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="effa5-147">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="effa5-147">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="effa5-148">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="effa5-148">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="effa5-149">Требования</span><span class="sxs-lookup"><span data-stu-id="effa5-149">Requirements</span></span>



| <span data-ttu-id="effa5-150">Требование</span><span class="sxs-lookup"><span data-stu-id="effa5-150">Requirement</span></span> | <span data-ttu-id="effa5-151">Значение</span><span class="sxs-lookup"><span data-stu-id="effa5-151">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="effa5-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="effa5-152">Minimum supported client</span></span><br/> | <span data-ttu-id="effa5-153">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="effa5-153">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="effa5-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="effa5-154">Minimum supported server</span></span><br/> | <span data-ttu-id="effa5-155">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="effa5-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="effa5-156">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="effa5-156">Namespace</span></span><br/>                | <span data-ttu-id="effa5-157">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="effa5-157">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="effa5-158">MOF</span><span class="sxs-lookup"><span data-stu-id="effa5-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="effa5-159"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="effa5-159"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="effa5-160">DLL</span><span class="sxs-lookup"><span data-stu-id="effa5-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="effa5-161"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="effa5-161"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="effa5-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="effa5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effa5-163">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="effa5-163">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="effa5-164">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="effa5-164">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="effa5-165">**Включить**</span><span class="sxs-lookup"><span data-stu-id="effa5-165">**Enable**</span></span>](enable-win32-tpm.md)
</dt> </dl>

 

 
