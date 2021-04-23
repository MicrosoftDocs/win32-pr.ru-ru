---
description: Экспортирует сведения, которые могут помочь в восстановлении зашифрованных данных, если диск сильно поврежден и не существует файлов резервных копий данных.
ms.assetid: 3d376a02-3392-433e-b842-24c73074610c
title: Метод Жеткэйпаккаже класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyPackage
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: d1b2348a90b6b3cd01685c740fdfa67ad5a2d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684064"
---
# <a name="getkeypackage-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="3999b-103">Метод Жеткэйпаккаже \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="3999b-103">GetKeyPackage method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="3999b-104">Метод **жеткэйпаккаже** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) экспортирует сведения, которые могут помочь в восстановлении зашифрованных данных, если диск сильно поврежден и не существует файлов резервных копий данных.</span><span class="sxs-lookup"><span data-stu-id="3999b-104">The **GetKeyPackage** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class exports information that may help salvage encrypted data when the drive is severely damaged and no data backup files exist.</span></span>

<span data-ttu-id="3999b-105">Экспортированные данные состоят из ключа шифрования тома, защищенного предохранителем ключа типа "числовой пароль" или "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="3999b-105">The exported information consists of the volume's encryption key secured by a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="3999b-106">Чтобы использовать этот пакет, необходимо также сохранить соответствующий числовой пароль или внешний ключ.</span><span class="sxs-lookup"><span data-stu-id="3999b-106">To make use of this package, you must also save the corresponding numerical password or external key.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3999b-107">Если вы решили экспортировать пакет ключей, убедитесь, что эти сведения хранятся в надежном месте.</span><span class="sxs-lookup"><span data-stu-id="3999b-107">If you choose to export a key package, make certain to keep this information in a well-protected location.</span></span> <span data-ttu-id="3999b-108">Не выполняйте эти сведения вместе с компьютером.</span><span class="sxs-lookup"><span data-stu-id="3999b-108">Do not carry this information with your computer.</span></span> <span data-ttu-id="3999b-109">Если этот пакет ключей потерян или украден, необходимо будет расшифровать том и повторно зашифровать его с помощью нового ключа.</span><span class="sxs-lookup"><span data-stu-id="3999b-109">If this key package is lost or stolen, you will need to decrypt the volume and reencrypt it by using a new key.</span></span>

 

<span data-ttu-id="3999b-110">В случае сбоя диска существует средство восстановления BitLocker, помогающее в восстановлении доступных данных.</span><span class="sxs-lookup"><span data-stu-id="3999b-110">In the event of a drive failure, the BitLocker Repair Tool exists to help salvage available data.</span></span> <span data-ttu-id="3999b-111">Дополнительные сведения о том, как это средство может использовать пакет ключей, см. в разделе [Использование средства восстановления BitLocker для восстановления данных из зашифрованного тома в Windows Vista](https://support.microsoft.com/kb/928201).</span><span class="sxs-lookup"><span data-stu-id="3999b-111">For more information about how this tool can use the key package, see [How to use the BitLocker Repair Tool to help recover data from an encrypted volume in Windows Vista](https://support.microsoft.com/kb/928201).</span></span>

## <a name="syntax"></a><span data-ttu-id="3999b-112">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3999b-112">Syntax</span></span>


```mof
uint32 GetKeyPackage(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  KeyPackage[]
);
```



## <a name="parameters"></a><span data-ttu-id="3999b-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="3999b-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3999b-114">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3999b-114">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3999b-115">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="3999b-115">Type: **string**</span></span>

<span data-ttu-id="3999b-116">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="3999b-116">A unique string identifier used to manage an encrypted volume key protector.</span></span> <span data-ttu-id="3999b-117">Для экспорта пакета ключей необходимо использовать предохранитель ключа типа "числовой пароль" или "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="3999b-117">To export a key package, you must use a key protector of type "Numerical Password" or "External Key".</span></span>

</dd> <dt>

<span data-ttu-id="3999b-118">*\[ Кэйпаккаже \]* \[исходящий трафик\]</span><span class="sxs-lookup"><span data-stu-id="3999b-118">*KeyPackage\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3999b-119">Тип: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="3999b-119">Type: **uint8**</span></span>

<span data-ttu-id="3999b-120">Байтовый поток, содержащий ключ шифрования для тома, защищенный с помощью указанного предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="3999b-120">A byte stream that contains the encryption key for a volume, secured by the specified key protector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3999b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3999b-121">Return value</span></span>

<span data-ttu-id="3999b-122">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3999b-122">Type: **uint32**</span></span>

<span data-ttu-id="3999b-123">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="3999b-123">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="3999b-124">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="3999b-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="3999b-125">Описание</span><span class="sxs-lookup"><span data-stu-id="3999b-125">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3999b-126"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-126"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                            | <span data-ttu-id="3999b-127">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="3999b-127">The method was successful.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="3999b-128"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-128"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>           | <span data-ttu-id="3999b-129">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="3999b-129">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="3999b-130"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-130"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl>           | <span data-ttu-id="3999b-131">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="3999b-131">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="3999b-132">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="3999b-132">Add a key protector to enable BitLocker.</span></span> <br/>                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="3999b-133"><dt>**ФВЕ \_ \_ \_ Не \_ найден предохранитель "E**</dt> <dt>" 2150694963 (0x80310033)</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-133"><dt>**FVE\_E\_PROTECTOR\_NOT\_FOUND**</dt> <dt>2150694963 (0x80310033)</dt></span></span> </dl>    | <span data-ttu-id="3999b-134">Указанный предохранитель ключа не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="3999b-134">The provided key protector does not exist on the volume.</span></span><br/>                                                                                                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="3999b-135"><dt>**ФВЕ \_ \_Недопустимый \_ \_ тип предохранителя**</dt> <dt>2150694970 (0x8031003A)</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-135"><dt>**FVE\_E\_INVALID\_PROTECTOR\_TYPE**</dt> <dt>2150694970 (0x8031003A)</dt></span></span> </dl> | <span data-ttu-id="3999b-136">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "числовой пароль" или "внешний ключ".</span><span class="sxs-lookup"><span data-stu-id="3999b-136">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "Numerical Password" or "External Key".</span></span> <span data-ttu-id="3999b-137">Используйте метод [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) или [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) для создания предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="3999b-137">Use either the [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) or [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) method to create a key protector of the appropriate type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3999b-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3999b-138">Remarks</span></span>

<span data-ttu-id="3999b-139">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="3999b-139">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3999b-140">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="3999b-140">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="3999b-141">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="3999b-141">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3999b-142">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="3999b-142">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3999b-143">Требования</span><span class="sxs-lookup"><span data-stu-id="3999b-143">Requirements</span></span>



| <span data-ttu-id="3999b-144">Требование</span><span class="sxs-lookup"><span data-stu-id="3999b-144">Requirement</span></span> | <span data-ttu-id="3999b-145">Значение</span><span class="sxs-lookup"><span data-stu-id="3999b-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3999b-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3999b-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3999b-147">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="3999b-147">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3999b-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3999b-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3999b-149">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3999b-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3999b-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3999b-150">Namespace</span></span><br/>                | <span data-ttu-id="3999b-151">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="3999b-151">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="3999b-152">MOF</span><span class="sxs-lookup"><span data-stu-id="3999b-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3999b-153"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3999b-153"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3999b-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3999b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3999b-155">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="3999b-155">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
