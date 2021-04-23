---
description: Указывает действие пользователя, необходимое для выполнения операции физического присутствия доверенный платформенный модуль (TPM) (TPM). Используйте метод Сетфисикалпресенцерекуест для запроса операции.
ms.assetid: abbd9702-c3a7-468a-bc83-2b7739d0b7bf
title: Метод Жетфисикалпресенцетранситион класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceTransition
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 4e6a3ab2295cc26cd439465b569f594dd1e0580a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684058"
---
# <a name="getphysicalpresencetransition-method-of-the-win32_tpm-class"></a><span data-ttu-id="7bbfc-104">Метод Жетфисикалпресенцетранситион \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="7bbfc-104">GetPhysicalPresenceTransition method of the Win32\_Tpm class</span></span>

<span data-ttu-id="7bbfc-105">Метод **жетфисикалпресенцетранситион** класса [**\_ TPM Win32**](win32-tpm.md) указывает действие пользователя, необходимое для выполнения операции физического присутствия доверенный платформенный модуль (TPM) (TPM).</span><span class="sxs-lookup"><span data-stu-id="7bbfc-105">The **GetPhysicalPresenceTransition** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates the user action that is needed to perform the Trusted Platform Module (TPM) physical presence operation.</span></span> <span data-ttu-id="7bbfc-106">Используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) для запроса операции.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span> <span data-ttu-id="7bbfc-107">Необходимое действие пользователя устанавливается для компьютера во время изготовления.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-107">The required user action is set for your computer at the time of manufacture.</span></span> <span data-ttu-id="7bbfc-108">Обычно требуется перезагрузка компьютера.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-108">Usually a computer restart is needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbfc-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bbfc-109">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceTransition(
  [out] uint32 Transition
);
```



## <a name="parameters"></a><span data-ttu-id="7bbfc-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bbfc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbfc-111">*Переход* \[ на заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-111">*Transition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbfc-112">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbfc-112">Type: **uint32**</span></span>

<span data-ttu-id="7bbfc-113">Целочисленное значение, указывающее переход, необходимый для выполнения операции физического присутствия TPM.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-113">An integer value that specifies the transition needed to perform a TPM physical presence operation.</span></span>



| <span data-ttu-id="7bbfc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7bbfc-114">Value</span></span>                                                                        | <span data-ttu-id="7bbfc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7bbfc-115">Meaning</span></span>                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bbfc-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-116"><dt>0</dt></span></span> </dl> | <span data-ttu-id="7bbfc-117">Для выполнения операции физического присутствия доверенного платформенного модуля никаких действий пользователя не требуется.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-117">No user action is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                                                                                                              |
| <dl> <span data-ttu-id="7bbfc-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-118"><dt>1</dt></span></span> </dl> | <span data-ttu-id="7bbfc-119">Чтобы выполнить операцию физического присутствия TPM, пользователь должен завершить работу компьютера, а затем снова включить его с помощью кнопки питания.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-119">To perform a TPM physical presence operation, the user must shutdown the computer and then turn it back on by using the power button.</span></span> <span data-ttu-id="7bbfc-120">Пользователь должен быть физически представлен на компьютере, чтобы принять или отклонить изменение при появлении запроса BIOS.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-120">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/> |
| <dl> <span data-ttu-id="7bbfc-121"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-121"><dt>2</dt></span></span> </dl> | <span data-ttu-id="7bbfc-122">Чтобы выполнить операцию физического присутствия TPM, пользователь должен перезагрузить компьютер, используя горячую перезагрузку.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-122">To perform a TPM physical presence operation, the user must restart the computer by using a warm reboot.</span></span> <span data-ttu-id="7bbfc-123">Пользователь должен быть физически представлен на компьютере, чтобы принять или отклонить изменение при появлении запроса BIOS.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-123">The user must be physically present at the computer to accept or reject the change when prompted by the BIOS.</span></span><br/>                              |
| <dl> <span data-ttu-id="7bbfc-124"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-124"><dt>3</dt></span></span> </dl> | <span data-ttu-id="7bbfc-125">Требуемое действие пользователя неизвестно.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-125">The required user action is unknown.</span></span><br/>                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bbfc-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bbfc-126">Return value</span></span>

<span data-ttu-id="7bbfc-127">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7bbfc-127">Type: **uint32**</span></span>

<span data-ttu-id="7bbfc-128">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-128">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="7bbfc-129">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-129">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="7bbfc-130">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="7bbfc-130">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="7bbfc-131">Описание</span><span class="sxs-lookup"><span data-stu-id="7bbfc-131">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bbfc-132"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-132"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="7bbfc-133">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-133">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="7bbfc-134"><dt>**Доверенный платформенный модуль \_ E \_ PPI \_ ACPI \_ сбой**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-134"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="7bbfc-135">Произошла ошибка оборудования.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-135">A hardware failure occurred.</span></span> <span data-ttu-id="7bbfc-136">Для получения дополнительных сведений обратитесь к изготовителю компьютера.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-136">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7bbfc-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7bbfc-137">Remarks</span></span>

<span data-ttu-id="7bbfc-138">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="7bbfc-138">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="7bbfc-139">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-139">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="7bbfc-140">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="7bbfc-140">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="7bbfc-141">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="7bbfc-141">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbfc-142">Требования</span><span class="sxs-lookup"><span data-stu-id="7bbfc-142">Requirements</span></span>



| <span data-ttu-id="7bbfc-143">Требование</span><span class="sxs-lookup"><span data-stu-id="7bbfc-143">Requirement</span></span> | <span data-ttu-id="7bbfc-144">Значение</span><span class="sxs-lookup"><span data-stu-id="7bbfc-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbfc-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7bbfc-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbfc-146">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-146">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7bbfc-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7bbfc-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbfc-148">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7bbfc-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7bbfc-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7bbfc-149">Namespace</span></span><br/>                | <span data-ttu-id="7bbfc-150">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="7bbfc-150">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="7bbfc-151">MOF</span><span class="sxs-lookup"><span data-stu-id="7bbfc-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bbfc-152"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-152"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bbfc-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbfc-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbfc-154"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="7bbfc-154"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bbfc-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7bbfc-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bbfc-156">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="7bbfc-156">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="7bbfc-157">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="7bbfc-157">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
