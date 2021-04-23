---
description: Указывает, доступны ли для тома предохранители.
ms.assetid: 92a959ea-27ec-4d38-a955-846bfd7b3a60
title: Метод Искэйпротектораваилабле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.IsKeyProtectorAvailable
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: a80f731bf77a39d1e16c7dfe9cca4884b80eec49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262991"
---
# <a name="iskeyprotectoravailable-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="66391-103">Метод Искэйпротектораваилабле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="66391-103">IsKeyProtectorAvailable method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="66391-104">Метод **искэйпротектораваилабле** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает, доступны ли для тома предохранители.</span><span class="sxs-lookup"><span data-stu-id="66391-104">The **IsKeyProtectorAvailable** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates whether protectors are available for the volume.</span></span>

<span data-ttu-id="66391-105">Если указан тип предохранителя, то метод указывает, доступны ли для тома средства защиты указанного типа.</span><span class="sxs-lookup"><span data-stu-id="66391-105">If a protector type is provided, then the method indicates whether protectors of the specified type are available for the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="66391-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="66391-106">Syntax</span></span>


```mof
uint32 IsKeyProtectorAvailable(
  [in, optional] uint32  KeyProtectorType,
  [out]          boolean IsKeyProtectorAvailable
);
```



## <a name="parameters"></a><span data-ttu-id="66391-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="66391-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66391-108">*Кэйпротектортипе* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="66391-108">*KeyProtectorType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="66391-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66391-109">Type: **uint32**</span></span>

<span data-ttu-id="66391-110">Целое число без знака, указывающее тип запрашиваемого предохранителя ключа тома.</span><span class="sxs-lookup"><span data-stu-id="66391-110">An unsigned integer that indicates the type of volume key protector queried.</span></span>

<span data-ttu-id="66391-111">Если этот параметр не указан, запрашиваются все доступные предохранители ключа тома.</span><span class="sxs-lookup"><span data-stu-id="66391-111">If this parameter is not specified, all available key protectors of the volume are queried.</span></span>



| <span data-ttu-id="66391-112">Значение</span><span class="sxs-lookup"><span data-stu-id="66391-112">Value</span></span>                                                                         | <span data-ttu-id="66391-113">Значение</span><span class="sxs-lookup"><span data-stu-id="66391-113">Meaning</span></span>                                                          |
|-------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="66391-114"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66391-114"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="66391-115">Все типы.</span><span class="sxs-lookup"><span data-stu-id="66391-115">All types.</span></span><br/> <span data-ttu-id="66391-116">Все предохранители ключа запрашиваются.</span><span class="sxs-lookup"><span data-stu-id="66391-116">All key protectors are queried.</span></span><br/> |
| <dl> <span data-ttu-id="66391-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="66391-117"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="66391-118">Доверенный платформенный модуль (TPM) (доверенный платформенный модуль).</span><span class="sxs-lookup"><span data-stu-id="66391-118">Trusted Platform Module (TPM).</span></span><br/>                        |
| <dl> <span data-ttu-id="66391-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="66391-119"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="66391-120">Внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="66391-120">External key.</span></span><br/>                                         |
| <dl> <span data-ttu-id="66391-121"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="66391-121"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="66391-122">Числовой пароль.</span><span class="sxs-lookup"><span data-stu-id="66391-122">Numerical password.</span></span><br/>                                   |
| <dl> <span data-ttu-id="66391-123"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="66391-123"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="66391-124">TPM и ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="66391-124">TPM And PIN.</span></span><br/>                                          |
| <dl> <span data-ttu-id="66391-125"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="66391-125"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="66391-126">TPM и ключ запуска.</span><span class="sxs-lookup"><span data-stu-id="66391-126">TPM And Startup Key.</span></span><br/>                                  |
| <dl> <span data-ttu-id="66391-127"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="66391-127"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="66391-128">TPM, ПИН-код и ключ запуска.</span><span class="sxs-lookup"><span data-stu-id="66391-128">TPM And PIN And Startup Key.</span></span><br/>                          |
| <dl> <span data-ttu-id="66391-129"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="66391-129"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="66391-130">Открытый ключ.</span><span class="sxs-lookup"><span data-stu-id="66391-130">Public Key.</span></span><br/>                                           |
| <dl> <span data-ttu-id="66391-131"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="66391-131"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="66391-132">Кодов.</span><span class="sxs-lookup"><span data-stu-id="66391-132">Passphrase.</span></span><br/>                                           |
| <dl> <span data-ttu-id="66391-133"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="66391-133"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="66391-134">Сертификат TPM</span><span class="sxs-lookup"><span data-stu-id="66391-134">TPM Certificate</span></span><br/>                                       |
| <dl> <span data-ttu-id="66391-135"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="66391-135"><dt>10</dt></span></span> </dl> | <span data-ttu-id="66391-136">Идентификатор безопасности (SID)</span><span class="sxs-lookup"><span data-stu-id="66391-136">Security Identifier (SID)</span></span><br/>                             |



 

</dd> <dt>

<span data-ttu-id="66391-137">*Искэйпротектораваилабле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="66391-137">*IsKeyProtectorAvailable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66391-138">Тип: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="66391-138">Type: **boolean**</span></span>

<span data-ttu-id="66391-139">Логическое значение, указывающее, существует ли на томе предохранитель ключа тома указанного типа.</span><span class="sxs-lookup"><span data-stu-id="66391-139">A Boolean value that indicates whether a volume key protector of the specified type exists on the volume.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66391-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="66391-140">Return value</span></span>

<span data-ttu-id="66391-141">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="66391-141">Type: **uint32**</span></span>

<span data-ttu-id="66391-142">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="66391-142">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="66391-143">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="66391-143">Return code/value</span></span>                                                                                                                                                         | <span data-ttu-id="66391-144">Описание</span><span class="sxs-lookup"><span data-stu-id="66391-144">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66391-145"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="66391-145"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                         | <span data-ttu-id="66391-146">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="66391-146">The method was successful.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="66391-147"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="66391-147"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl> | <span data-ttu-id="66391-148">Параметр *кэйпротектортипе* указан, но не ссылается на допустимый тип предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="66391-148">The *KeyProtectorType* parameter is specified but does not refer to a valid key protector type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66391-149">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66391-149">Remarks</span></span>

<span data-ttu-id="66391-150">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="66391-150">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="66391-151">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="66391-151">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="66391-152">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="66391-152">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="66391-153">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="66391-153">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66391-154">Требования</span><span class="sxs-lookup"><span data-stu-id="66391-154">Requirements</span></span>



| <span data-ttu-id="66391-155">Требование</span><span class="sxs-lookup"><span data-stu-id="66391-155">Requirement</span></span> | <span data-ttu-id="66391-156">Значение</span><span class="sxs-lookup"><span data-stu-id="66391-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66391-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66391-157">Minimum supported client</span></span><br/> | <span data-ttu-id="66391-158">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="66391-158">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="66391-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66391-159">Minimum supported server</span></span><br/> | <span data-ttu-id="66391-160">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="66391-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66391-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="66391-161">Namespace</span></span><br/>                | <span data-ttu-id="66391-162">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="66391-162">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="66391-163">MOF</span><span class="sxs-lookup"><span data-stu-id="66391-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="66391-164"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="66391-164"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66391-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66391-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66391-166">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="66391-166">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
