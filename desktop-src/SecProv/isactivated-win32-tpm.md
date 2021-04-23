---
description: Метод Activate \_ класса TPM Win32 указывает, активировано ли устройство.
ms.assetid: 862c386c-c5b5-44d2-89a5-3735b99bf8bc
title: Метод активации класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsActivated
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6482163a27f211b4f4ce24284a8339f2b7254f3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265903"
---
# <a name="isactivated-method-of-the-win32_tpm-class"></a><span data-ttu-id="bd888-103">Метод активации \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="bd888-103">IsActivated method of the Win32\_Tpm class</span></span>

<span data-ttu-id="bd888-104">Метод **Activate** класса [**\_ TPM Win32**](win32-tpm.md) указывает, активировано ли устройство.</span><span class="sxs-lookup"><span data-stu-id="bd888-104">The **IsActivated** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device is activated.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd888-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bd888-105">Syntax</span></span>


```mof
uint32 IsActivated(
  [out] boolean IsActivated
);
```



## <a name="parameters"></a><span data-ttu-id="bd888-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bd888-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd888-107">*Активируется* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bd888-107">*IsActivated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd888-108">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="bd888-108">Type: **boolean**</span></span>

<span data-ttu-id="bd888-109">Если задано **значение true**, устройство активируется.</span><span class="sxs-lookup"><span data-stu-id="bd888-109">If **true**, the device is activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd888-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bd888-110">Return value</span></span>

<span data-ttu-id="bd888-111">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd888-111">Type: **uint32**</span></span>

<span data-ttu-id="bd888-112">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="bd888-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="bd888-113">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="bd888-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="bd888-114">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="bd888-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="bd888-115">Описание</span><span class="sxs-lookup"><span data-stu-id="bd888-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="bd888-116"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="bd888-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="bd888-117">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="bd888-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bd888-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bd888-118">Remarks</span></span>

<span data-ttu-id="bd888-119">Деактивация аналогична отключенной, но возможны изменения в рабочем состоянии.</span><span class="sxs-lookup"><span data-stu-id="bd888-119">Deactivation is similar to disabled, but operational state changes are possible.</span></span> <span data-ttu-id="bd888-120">В соответствии со спецификацией организация TCG (TCG) v 1.2 доступны только следующие команды, если устройство находится в отключенном состоянии.</span><span class="sxs-lookup"><span data-stu-id="bd888-120">According to the Trusted Computing Group (TCG) v1.2 specification only the following commands are available when the device is in a deactivated state.</span></span>

-   <span data-ttu-id="bd888-121">\_КОНТИНУЕСЕЛФТЕСТ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-121">TPM\_ContinueSelfTest</span></span>
-   <span data-ttu-id="bd888-122">\_ДСАП TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-122">TPM\_DSAP</span></span>
-   <span data-ttu-id="bd888-123">\_ФЛУШСПЕЦИФИК TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-123">TPM\_FlushSpecific</span></span>
-   <span data-ttu-id="bd888-124">\_Поддержка TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-124">TPM\_GetCapability</span></span>
-   <span data-ttu-id="bd888-125">\_ЖЕТТЕСТРЕСУЛТ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-125">TPM\_GetTestResult</span></span>
-   <span data-ttu-id="bd888-126">\_Инициализация TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-126">TPM\_Init</span></span>
-   <span data-ttu-id="bd888-127">\_ОИАП TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-127">TPM\_OIAP</span></span>
-   <span data-ttu-id="bd888-128">\_ОСАП TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-128">TPM\_OSAP</span></span>
-   <span data-ttu-id="bd888-129">\_ОВНЕРСЕТДИСАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-129">TPM\_OwnerSetDisable</span></span>
-   <span data-ttu-id="bd888-130">\_ \_ Сброс параметров PCR модуля</span><span class="sxs-lookup"><span data-stu-id="bd888-130">TPM\_PCR\_Reset</span></span>
-   <span data-ttu-id="bd888-131">\_ФИСИКАЛДИСАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-131">TPM\_PhysicalDisable</span></span>
-   <span data-ttu-id="bd888-132">\_ФИСИКАЛЕНАБЛЕ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-132">TPM\_PhysicalEnable</span></span>
-   <span data-ttu-id="bd888-133">\_ФИСИКАЛСЕТДЕАКТИВАТЕД TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-133">TPM\_PhysicalSetDeactivated</span></span>
-   <span data-ttu-id="bd888-134">\_Сброс TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-134">TPM\_Reset</span></span>
-   <span data-ttu-id="bd888-135">Модуль \_ SaveState TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-135">TPM\_SaveState</span></span>
-   <span data-ttu-id="bd888-136">\_СЕЛФТЕСТФУЛЛ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-136">TPM\_SelfTestFull</span></span>
-   <span data-ttu-id="bd888-137">\_СЕТКАПАБИЛИТИ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-137">TPM\_SetCapability</span></span>
-   <span data-ttu-id="bd888-138">\_SHA1COMPLETE TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-138">TPM\_SHA1Complete</span></span>
-   <span data-ttu-id="bd888-139">\_SHA1START TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-139">TPM\_SHA1Start</span></span>
-   <span data-ttu-id="bd888-140">\_SHA1UPDATE TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-140">TPM\_SHA1Update</span></span>
-   <span data-ttu-id="bd888-141">\_Запуск TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-141">TPM\_Startup</span></span>
-   <span data-ttu-id="bd888-142">\_ТАКЕОВНЕРШИП TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-142">TPM\_TakeOwnership</span></span>
-   <span data-ttu-id="bd888-143">\_Маркер завершения \_ TPM</span><span class="sxs-lookup"><span data-stu-id="bd888-143">TPM\_Terminate\_Handle</span></span>

<span data-ttu-id="bd888-144">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="bd888-144">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="bd888-145">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="bd888-145">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="bd888-146">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="bd888-146">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="bd888-147">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="bd888-147">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bd888-148">Требования</span><span class="sxs-lookup"><span data-stu-id="bd888-148">Requirements</span></span>



| <span data-ttu-id="bd888-149">Требование</span><span class="sxs-lookup"><span data-stu-id="bd888-149">Requirement</span></span> | <span data-ttu-id="bd888-150">Значение</span><span class="sxs-lookup"><span data-stu-id="bd888-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd888-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd888-151">Minimum supported client</span></span><br/> | <span data-ttu-id="bd888-152">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd888-152">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bd888-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd888-153">Minimum supported server</span></span><br/> | <span data-ttu-id="bd888-154">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd888-154">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="bd888-155">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="bd888-155">Namespace</span></span><br/>                | <span data-ttu-id="bd888-156">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="bd888-156">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="bd888-157">MOF</span><span class="sxs-lookup"><span data-stu-id="bd888-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd888-158"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd888-158"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd888-159">DLL</span><span class="sxs-lookup"><span data-stu-id="bd888-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd888-160"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="bd888-160"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd888-161">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd888-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd888-162">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="bd888-162">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
