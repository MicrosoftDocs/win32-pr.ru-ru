---
description: Извлекает профиль проверки платформы для данного предохранителя ключа соответствующего типа.
ms.assetid: 45fa6ba7-169c-4753-8586-0029a7650acc
title: Метод Жеткэйпротекторплатформвалидатионпрофиле класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetKeyProtectorPlatformValidationProfile
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: b9b951d3ce9eab52687730831f7052942fcbec93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684060"
---
# <a name="getkeyprotectorplatformvalidationprofile-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="4f7bc-103">Метод Жеткэйпротекторплатформвалидатионпрофиле \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="4f7bc-103">GetKeyProtectorPlatformValidationProfile method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="4f7bc-104">Метод **жеткэйпротекторплатформвалидатионпрофиле** извлекает профиль проверки платформы для данного предохранителя ключа соответствующего типа.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-104">The **GetKeyProtectorPlatformValidationProfile** method retrieves the platform validation profile for a given key protector of the appropriate type.</span></span>

<span data-ttu-id="4f7bc-105">Идентификатор предохранителя ключа должен ссылаться на предохранитель ключа типа "TPM", "TPM и ПИН-код", "TPM, ПИН-код и ключ запуска", "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="4f7bc-105">The key protector identifier must refer to a key protector of type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span>

## <a name="syntax"></a><span data-ttu-id="4f7bc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f7bc-106">Syntax</span></span>


```mof
uint32 GetKeyProtectorPlatformValidationProfile(
  [in]  string VolumeKeyProtectorID,
  [out] uint8  PlatformValidationProfile[]
);
```



## <a name="parameters"></a><span data-ttu-id="4f7bc-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f7bc-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f7bc-108">*Волумекэйпротекторид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4f7bc-108">*VolumeKeyProtectorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f7bc-109">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4f7bc-109">Type: **string**</span></span>

<span data-ttu-id="4f7bc-110">Уникальный строковый идентификатор, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-110">A unique string identifier used to manage an encrypted volume key protector.</span></span>

</dd> <dt>

<span data-ttu-id="4f7bc-111">*Платформвалидатионпрофиле* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4f7bc-111">*PlatformValidationProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f7bc-112">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="4f7bc-112">Type: **uint8\[\]**</span></span>

<span data-ttu-id="4f7bc-113">Массив целых чисел, указывающий, доверенный платформенный модуль (TPM) как оборудование безопасности (TPM) компьютера защищает ключ шифрования тома диска.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-113">An array of integers that specifies how the Trusted Platform Module (TPM) Security Hardware of the computer secures the encryption key of the disk volume.</span></span>



| <span data-ttu-id="4f7bc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="4f7bc-114">Value</span></span>                                                                         | <span data-ttu-id="4f7bc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4f7bc-115">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f7bc-116"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-116"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-117">Корневой корень доверия измерений (КРТМ), BIOS и расширений платформы</span><span class="sxs-lookup"><span data-stu-id="4f7bc-117">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="4f7bc-118"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-118"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-119">Конфигурация и данные платформы и материнской платы</span><span class="sxs-lookup"><span data-stu-id="4f7bc-119">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="4f7bc-120"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-120"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-121">Код варианта ПЗУ</span><span class="sxs-lookup"><span data-stu-id="4f7bc-121">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4f7bc-122"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-122"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-123">Конфигурация и данные с поддержкой ПЗУ</span><span class="sxs-lookup"><span data-stu-id="4f7bc-123">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="4f7bc-124"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-124"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-125">Код основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="4f7bc-125">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="4f7bc-126"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-126"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-127">Таблица разделов основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="4f7bc-127">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="4f7bc-128"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-128"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-129">События смены состояния и пробуждения</span><span class="sxs-lookup"><span data-stu-id="4f7bc-129">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="4f7bc-130"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-130"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-131">Manufacturer-Specific компьютера</span><span class="sxs-lookup"><span data-stu-id="4f7bc-131">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="4f7bc-132"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-132"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-133">Загрузочный сектор NTFS</span><span class="sxs-lookup"><span data-stu-id="4f7bc-133">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4f7bc-134"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-134"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="4f7bc-135">Загрузочный блок NTFS</span><span class="sxs-lookup"><span data-stu-id="4f7bc-135">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="4f7bc-136"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-136"><dt>10</dt></span></span> </dl> | <span data-ttu-id="4f7bc-137">Диспетчер загрузки</span><span class="sxs-lookup"><span data-stu-id="4f7bc-137">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4f7bc-138"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-138"><dt>11</dt></span></span> </dl> | <span data-ttu-id="4f7bc-139">Контроль доступа BitLocker</span><span class="sxs-lookup"><span data-stu-id="4f7bc-139">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="4f7bc-140"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-140"><dt>12</dt></span></span> </dl> | <span data-ttu-id="4f7bc-141">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-141">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4f7bc-142"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-142"><dt>13</dt></span></span> </dl> | <span data-ttu-id="4f7bc-143">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-143">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4f7bc-144"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-144"><dt>14</dt></span></span> </dl> | <span data-ttu-id="4f7bc-145">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-145">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4f7bc-146"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-146"><dt>15</dt></span></span> </dl> | <span data-ttu-id="4f7bc-147">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-147">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="4f7bc-148"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-148"><dt>16</dt></span></span> </dl> | <span data-ttu-id="4f7bc-149">Используется для отладки</span><span class="sxs-lookup"><span data-stu-id="4f7bc-149">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="4f7bc-150"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-150"><dt>17</dt></span></span> </dl> | <span data-ttu-id="4f7bc-151">Динамический КРТМ</span><span class="sxs-lookup"><span data-stu-id="4f7bc-151">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="4f7bc-152"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-152"><dt>18</dt></span></span> </dl> | <span data-ttu-id="4f7bc-153">Определенная платформа</span><span class="sxs-lookup"><span data-stu-id="4f7bc-153">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="4f7bc-154"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-154"><dt>19</dt></span></span> </dl> | <span data-ttu-id="4f7bc-155">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-155">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f7bc-156"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-156"><dt>20</dt></span></span> </dl> | <span data-ttu-id="4f7bc-157">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-157">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f7bc-158"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-158"><dt>21</dt></span></span> </dl> | <span data-ttu-id="4f7bc-159">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-159">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f7bc-160"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-160"><dt>22</dt></span></span> </dl> | <span data-ttu-id="4f7bc-161">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="4f7bc-161">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="4f7bc-162"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-162"><dt>23</dt></span></span> </dl> | <span data-ttu-id="4f7bc-163">Поддержка приложений</span><span class="sxs-lookup"><span data-stu-id="4f7bc-163">Application support</span></span><br/>                                                     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f7bc-164">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4f7bc-164">Return value</span></span>

<span data-ttu-id="4f7bc-165">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4f7bc-165">Type: **uint32**</span></span>

<span data-ttu-id="4f7bc-166">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-166">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="4f7bc-167">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="4f7bc-167">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="4f7bc-168">Описание</span><span class="sxs-lookup"><span data-stu-id="4f7bc-168">Description</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4f7bc-169"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-169"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="4f7bc-170">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-170">The method was successful.</span></span><br/>                                                                                                                                        |
| <dl> <span data-ttu-id="4f7bc-171"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-171"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>          | <span data-ttu-id="4f7bc-172">Параметр *волумекэйпротекторид* не ссылается на предохранитель ключа типа "TPM", "TPM и ПИН-код", "TPM и ключ запуска", "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="4f7bc-172">The *VolumeKeyProtectorID* parameter does not refer to a key protector of the type "TPM", "TPM And PIN", "TPM And PIN And Startup Key", or "TPM And Startup Key".</span></span><br/> |
| <dl> <span data-ttu-id="4f7bc-173"><dt>**ФВЕ \_ E \_ не \_ активировано**</dt> <dt>2150694920 (0x80310008)</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-173"><dt>**FVE\_E\_NOT\_ACTIVATED**</dt> <dt>2150694920 (0x80310008)</dt></span></span> </dl> | <span data-ttu-id="4f7bc-174">Средство BitLocker не включено в томе.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-174">BitLocker is not enabled on the volume.</span></span> <span data-ttu-id="4f7bc-175">Добавьте предохранитель ключа, чтобы включить BitLocker.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-175">Add a key protector to enable BitLocker.</span></span><br/>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="4f7bc-176">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4f7bc-176">Remarks</span></span>

<span data-ttu-id="4f7bc-177">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="4f7bc-177">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4f7bc-178">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-178">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="4f7bc-179">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="4f7bc-179">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4f7bc-180">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="4f7bc-180">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4f7bc-181">Требования</span><span class="sxs-lookup"><span data-stu-id="4f7bc-181">Requirements</span></span>



| <span data-ttu-id="4f7bc-182">Требование</span><span class="sxs-lookup"><span data-stu-id="4f7bc-182">Requirement</span></span> | <span data-ttu-id="4f7bc-183">Значение</span><span class="sxs-lookup"><span data-stu-id="4f7bc-183">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7bc-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4f7bc-184">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7bc-185">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="4f7bc-185">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="4f7bc-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4f7bc-186">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7bc-187">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4f7bc-187">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4f7bc-188">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4f7bc-188">Namespace</span></span><br/>                | <span data-ttu-id="4f7bc-189">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="4f7bc-189">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="4f7bc-190">MOF</span><span class="sxs-lookup"><span data-stu-id="4f7bc-190">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f7bc-191"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f7bc-191"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f7bc-192">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4f7bc-192">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7bc-193">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="4f7bc-193">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
