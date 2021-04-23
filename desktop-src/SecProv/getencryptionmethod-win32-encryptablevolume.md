---
description: Указывает алгоритм шифрования и размер ключа, используемые в томе.
ms.assetid: 89df3dfc-4789-4d3c-b267-d8e26758e754
title: Метод Жетенкриптионмесод класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetEncryptionMethod
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 16fb9b00976b652bcc9643ab5ec4912029898424
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684074"
---
# <a name="getencryptionmethod-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="ef1e9-103">Метод Жетенкриптионмесод \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="ef1e9-103">GetEncryptionMethod method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="ef1e9-104">Метод **жетенкриптионмесод** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) указывает алгоритм шифрования и размер ключа, используемые в томе.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-104">The **GetEncryptionMethod** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class indicates the encryption algorithm and key size used on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1e9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ef1e9-105">Syntax</span></span>


```mof
uint32 GetEncryptionMethod(
  [out] uint32 EncryptionMethod,
  [out] string SelfEncryptionDriveEncryptionMethod
);
```



## <a name="parameters"></a><span data-ttu-id="ef1e9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ef1e9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1e9-107">*Енкриптионмесод* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef1e9-107">*EncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1e9-108">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1e9-108">Type: **uint32**</span></span>

<span data-ttu-id="ef1e9-109">Целое число без знака, указывающее алгоритм шифрования и размер ключа, используемые в томе.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-109">An unsigned integer that specifies the encryption algorithm and key size used on the volume.</span></span>



| <span data-ttu-id="ef1e9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1e9-110">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="ef1e9-111">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1e9-111">Meaning</span></span>                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="None"></span><span id="none"></span><span id="NONE"></span><dl> <span data-ttu-id="ef1e9-112"><dt>**Нет**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-112"><dt>**None**</dt> <dt>0</dt></span></span> </dl>                                | <span data-ttu-id="ef1e9-113">Том не зашифрован.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-113">The volume is not encrypted.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="AES_128_WITH_DIFFUSER"></span><span id="aes_128_with_diffuser"></span><dl> <span data-ttu-id="ef1e9-114"><dt>**AES \_ 128 \_ с \_ диффузором**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-114"><dt>**AES\_128\_WITH\_DIFFUSER**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="ef1e9-115">Том полностью или частично зашифрован с помощью алгоритма AES (AES), дополненного уровнем диффузора, с использованием ключа AES размером 128 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-115">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 128 bits.</span></span> <span data-ttu-id="ef1e9-116">Этот метод больше не доступен на устройствах, работающих Windows 8.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-116">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_256_WITH_DIFFUSER"></span><span id="aes_256_with_diffuser"></span><dl> <span data-ttu-id="ef1e9-117"><dt>**AES \_ 256 \_ с \_ диффузором**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-117"><dt>**AES\_256\_WITH\_DIFFUSER**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="ef1e9-118">Том полностью или частично зашифрован с помощью алгоритма AES (AES), дополненного уровнем диффузора, с использованием ключа AES размером 256 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-118">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm enhanced with a diffuser layer, using an AES key size of 256 bits.</span></span> <span data-ttu-id="ef1e9-119">Этот метод больше не доступен на устройствах, работающих Windows 8.1 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-119">This method is no longer available on devices running Windows 8.1 or higher.</span></span><br/> |
| <span id="AES_128"></span><span id="aes_128"></span><dl> <span data-ttu-id="ef1e9-120"><dt>**AES \_ 128**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-120"><dt>**AES\_128**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="ef1e9-121">Том полностью или частично зашифрован с помощью алгоритма AES (AES) с использованием ключа AES размером 128 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-121">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 128 bits.</span></span><br/>                                                                                                             |
| <span id="AES_256"></span><span id="aes_256"></span><dl> <span data-ttu-id="ef1e9-122"><dt>**AES \_ 256**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-122"><dt>**AES\_256**</dt> <dt>4</dt></span></span> </dl>                                             | <span data-ttu-id="ef1e9-123">Том полностью или частично зашифрован с помощью алгоритма AES (AES) с использованием ключа AES размером 256 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-123">The volume has been fully or partially encrypted with the Advanced Encryption Standard (AES) algorithm, using an AES key size of 256 bits.</span></span><br/>                                                                                                             |
| <span id="HARDWARE_ENCRYPTION"></span><span id="hardware_encryption"></span><dl> <span data-ttu-id="ef1e9-124"><dt>**Оборудование \_ Шифрование**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-124"><dt>**HARDWARE\_ENCRYPTION**</dt> <dt>5</dt></span></span> </dl>         | <span data-ttu-id="ef1e9-125">Том полностью или частично зашифрован с использованием аппаратных возможностей диска.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-125">The volume has been fully or partially encrypted by using the hardware capabilities of the drive.</span></span><br/>                                                                                                                                                      |
| <span id="XTS_AES_128"></span><span id="xts_aes_128"></span><dl> <span data-ttu-id="ef1e9-126"><dt>**XTS \_ AES \_ 128**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-126"><dt>**XTS\_AES\_128**</dt> <dt>6</dt></span></span> </dl>                                | <span data-ttu-id="ef1e9-127">Том полностью или частично зашифрован с помощью XTS с использованием AES (AES) и размером ключа AES 128 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-127">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 128 bits.</span></span> <span data-ttu-id="ef1e9-128">Этот метод доступен только на устройствах под управлением Windows 10 версии 1511 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-128">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <span id="XTS_AES_256"></span><span id="xts_aes_256"></span><dl> <span data-ttu-id="ef1e9-129"><dt>**XTS \_ AES \_ 256**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-129"><dt>**XTS\_AES\_256**</dt> <dt>7</dt></span></span> </dl>                                | <span data-ttu-id="ef1e9-130">Том полностью или частично зашифрован с помощью XTS с использованием AES (AES) и размером ключа AES 256 бит.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-130">The volume has been fully or partially encrypted with XTS using the Advanced Encryption Standard (AES), and an AES key size of 256 bits.</span></span> <span data-ttu-id="ef1e9-131">Этот метод доступен только на устройствах под управлением Windows 10 версии 1511 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-131">This method is only available on devices running Windows 10, version 1511 or higher.</span></span><br/>                          |
| <dl> <span data-ttu-id="ef1e9-132"><dt>(UInt32) — 1</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-132"><dt>(uint32)–1</dt></span></span> </dl>                                                                                                                                                          | <span data-ttu-id="ef1e9-133">UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="ef1e9-133">UNKNOWN</span></span><br/> <span data-ttu-id="ef1e9-134">Том полностью или частично зашифрован с неизвестным алгоритмом и размером ключа.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-134">The volume has been fully or partially encrypted with an unknown algorithm and key size.</span></span><br/>                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="ef1e9-135">*Селфенкриптиондривинкриптионмесод* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ef1e9-135">*SelfEncryptionDriveEncryptionMethod* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1e9-136">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ef1e9-136">Type: **string**</span></span>

<span data-ttu-id="ef1e9-137">Алгоритм шифрования настраивается на диске с самошифрованием.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-137">The encryption algorithm is configured on the self-encrypting drive.</span></span> <span data-ttu-id="ef1e9-138">Строка со значением NULL означает, что BitLocker использует программное шифрование или не сообщается о методе шифрования.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-138">A null string means that either BitLocker is using software encryption or no encryption method is reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1e9-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ef1e9-139">Return value</span></span>

<span data-ttu-id="ef1e9-140">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ef1e9-140">Type: **uint32**</span></span>

<span data-ttu-id="ef1e9-141">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-141">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="ef1e9-142">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="ef1e9-142">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="ef1e9-143">Описание</span><span class="sxs-lookup"><span data-stu-id="ef1e9-143">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="ef1e9-144"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-144"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="ef1e9-145">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-145">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ef1e9-146">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef1e9-146">Remarks</span></span>

<span data-ttu-id="ef1e9-147">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ef1e9-147">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ef1e9-148">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-148">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="ef1e9-149">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ef1e9-149">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ef1e9-150">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="ef1e9-150">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1e9-151">Требования</span><span class="sxs-lookup"><span data-stu-id="ef1e9-151">Requirements</span></span>



| <span data-ttu-id="ef1e9-152">Требование</span><span class="sxs-lookup"><span data-stu-id="ef1e9-152">Requirement</span></span> | <span data-ttu-id="ef1e9-153">Значение</span><span class="sxs-lookup"><span data-stu-id="ef1e9-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1e9-154">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef1e9-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1e9-155">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="ef1e9-155">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ef1e9-156">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef1e9-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1e9-157">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ef1e9-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ef1e9-158">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef1e9-158">Namespace</span></span><br/>                | <span data-ttu-id="ef1e9-159">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="ef1e9-159">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="ef1e9-160">MOF</span><span class="sxs-lookup"><span data-stu-id="ef1e9-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ef1e9-161"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ef1e9-161"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef1e9-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ef1e9-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef1e9-163">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="ef1e9-163">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
