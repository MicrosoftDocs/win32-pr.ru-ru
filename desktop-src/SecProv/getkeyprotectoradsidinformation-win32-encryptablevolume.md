---
description: Возвращает идентификатор безопасности и флаги, используемые для защиты ключа.
ms.assetid: 5EF97F44-78FF-4FBF-9142-F2DD0A849057
title: Метод Жеткэйпротекторадсидинформатион класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorCertificate
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 57e72488a9e53f49383d179b0bcb1a8b9ff1f706
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/26/2021
ms.locfileid: "105689539"
---
# <a name="getkeyprotectoradsidinformation-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="e4e6c-103">Метод Жеткэйпротекторадсидинформатион \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="e4e6c-103">GetKeyProtectorAdSidInformation method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="e4e6c-104">Метод **жеткэйпротекторадсидинформатион** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) извлекает идентификатор безопасности и флаги, используемые для защиты ключа.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-104">The **GetKeyProtectorAdSidInformation** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the security identifier and flags used to protect a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4e6c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e4e6c-105">Syntax</span></span>


```mof
uint32 GetKeyProtectorCertificate(
  [in]  string VolumeKeyProtectorID,
  [out] string SidString,
  [out] uint32 Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e4e6c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e4e6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4e6c-107">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e4e6c-107">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6c-108">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="e4e6c-108">Type: **string**</span></span>

<span data-ttu-id="e4e6c-109">Идентификатор строки, который может использоваться для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-109">A string identifier that can be used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="e4e6c-110">*Сидстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4e6c-110">*SidString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6c-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="e4e6c-111">Type: **string**</span></span>

<span data-ttu-id="e4e6c-112">Строка, содержащая идентификатор безопасности (SID).</span><span class="sxs-lookup"><span data-stu-id="e4e6c-112">A string that contains the security identifier (SID).</span></span>

</dd> <dt>

<span data-ttu-id="e4e6c-113">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e4e6c-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e4e6c-114">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4e6c-114">Type: **uint32**</span></span>

<span data-ttu-id="e4e6c-115">Флаги, изменяющие поведение функции.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-115">Flags that change the function behavior.</span></span> <span data-ttu-id="e4e6c-116">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-116">This can be one of the following values.</span></span>



| <span data-ttu-id="e4e6c-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e6c-117">Value</span></span>                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="e4e6c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e6c-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FVE_DPAPI_NG_FLAG_NONE"></span><span id="fve_dpapi_ng_flag_none"></span><dl> <span data-ttu-id="e4e6c-119"><dt>**ФВЕ \_ DPAPI \_ NG \_ флаг \_ None**</dt> <dt>Символ 0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6c-119"><dt>**FVE\_DPAPI\_NG\_FLAG\_NONE**</dt> <dt>0x0000</dt></span></span> </dl>                                                                   | <span data-ttu-id="e4e6c-120">Не влияет.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-120">No effect.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="FVE_DPAPI_NG_FLAG_UNLOCK_AS_SERVICE_ACCOUNT"></span><span id="fve_dpapi_ng_flag_unlock_as_service_account"></span><dl> <span data-ttu-id="e4e6c-121"><dt>**ФВЕ \_ DPAPI \_ NG \_ флаг \_ разблокировки \_ в качестве \_ \_ учетной записи службы**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6c-121"><dt>**FVE\_DPAPI\_NG\_FLAG\_UNLOCK\_AS\_SERVICE\_ACCOUNT**</dt> <dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="e4e6c-122">Указывает, что предохранитель на основе идентификатора безопасности был защищен учетной записью службы.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-122">Specifies that the SID-based protector was protected to a service account.</span></span> <span data-ttu-id="e4e6c-123">Если этот флаг указан, вызывающий объект должен убедиться, что он работает как соответствующая учетная запись службы перед вызовом [**унлокквисадсид**](unlockwithadsid-win32-encryptablevolume.md) (например, временное удаление олицетворения).</span><span class="sxs-lookup"><span data-stu-id="e4e6c-123">If this flag is specified, the caller should ensure that it is running as the appropriate service account before calling [**UnlockWithAdSid**](unlockwithadsid-win32-encryptablevolume.md) (by temporarily dropping impersonation, for example).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4e6c-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e4e6c-124">Return value</span></span>

<span data-ttu-id="e4e6c-125">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e4e6c-125">Type: **uint32**</span></span>

<span data-ttu-id="e4e6c-126">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-126">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="e4e6c-127">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e4e6c-127">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="e4e6c-128">Описание</span><span class="sxs-lookup"><span data-stu-id="e4e6c-128">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="e4e6c-129"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6c-129"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="e4e6c-130">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-130">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e4e6c-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4e6c-131">Remarks</span></span>

<span data-ttu-id="e4e6c-132">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="e4e6c-132">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="e4e6c-133">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-133">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="e4e6c-134">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="e4e6c-134">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="e4e6c-135">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="e4e6c-135">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4e6c-136">Требования</span><span class="sxs-lookup"><span data-stu-id="e4e6c-136">Requirements</span></span>



| <span data-ttu-id="e4e6c-137">Требование</span><span class="sxs-lookup"><span data-stu-id="e4e6c-137">Requirement</span></span> | <span data-ttu-id="e4e6c-138">Значение</span><span class="sxs-lookup"><span data-stu-id="e4e6c-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4e6c-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4e6c-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e4e6c-140">Windows 8 Корпоративная, \[ только классические приложения Windows 8 Pro\]</span><span class="sxs-lookup"><span data-stu-id="e4e6c-140">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e4e6c-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4e6c-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e4e6c-142">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e4e6c-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e4e6c-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e4e6c-143">Namespace</span></span><br/>                | <span data-ttu-id="e4e6c-144">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="e4e6c-144">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="e4e6c-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e4e6c-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4e6c-146"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4e6c-146"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4e6c-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e4e6c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4e6c-148">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="e4e6c-148">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
