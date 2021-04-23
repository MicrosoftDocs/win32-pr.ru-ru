---
description: Если доверенный платформенный модуль (TPM) (TPM) доступен, этот метод обеспечивает защиту ключа шифрования тома.
ms.assetid: 79bee9ca-c86a-482b-a06f-1cfb887e7fae
title: Метод Протекткэйвистпм класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPM
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 0369e44d96a4f1dcacf33dbf1b1da6ad6d37eed2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663914"
---
# <a name="protectkeywithtpm-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="16294-103">Метод Протекткэйвистпм \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="16294-103">ProtectKeyWithTPM method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="16294-104">Метод **протекткэйвистпм** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью оборудования безопасности доверенный платформенный модуль (TPM) (доверенного платформенного модуля) на компьютере, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="16294-104">The **ProtectKeyWithTPM** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available.</span></span>

<span data-ttu-id="16294-105">Для тома создается предохранитель ключа типа "TPM", если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="16294-105">A key protector of type "TPM" is created for the volume, if one does not already exist.</span></span>

<span data-ttu-id="16294-106">Этот метод применим только к тому, который содержит текущую операционную систему, и если предохранитель ключа еще не существует на томе.</span><span class="sxs-lookup"><span data-stu-id="16294-106">This method is only applicable for the volume that contains the currently running operating system, and if a key protector does not already exist on the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="16294-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16294-107">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPM(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="16294-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="16294-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16294-109">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="16294-109">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16294-110">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="16294-110">Type: **string**</span></span>

<span data-ttu-id="16294-111">Строка, указывающая назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="16294-111">A string that specifies a user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="16294-112">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="16294-112">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="16294-113">*Платформвалидатионпрофиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="16294-113">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="16294-114">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="16294-114">Type: **uint8\[\]**</span></span>

<span data-ttu-id="16294-115">Массив целых чисел, указывающий, как оборудование безопасности доверенный платформенный модуль (TPM) компьютера (TPM) защищает ключ шифрования тома диска.</span><span class="sxs-lookup"><span data-stu-id="16294-115">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="16294-116">Профиль проверки платформы состоит из набора индексов реестра конфигурации платформы (PCR) в диапазоне от 0 до 23 включительно.</span><span class="sxs-lookup"><span data-stu-id="16294-116">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="16294-117">Значения Repeat в параметре не учитываются.</span><span class="sxs-lookup"><span data-stu-id="16294-117">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="16294-118">Каждый индекс PCR связан со службами, которые выполняются при запуске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="16294-118">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="16294-119">При каждом запуске компьютера доверенный платформенный модуль проверит, не изменились ли службы, указанные в профиле проверки платформы.</span><span class="sxs-lookup"><span data-stu-id="16294-119">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="16294-120">Если какая-либо из этих служб изменилась, когда шифрование диска BitLocker (BDE) остается включенной, доверенный платформенный модуль не будет освобождать ключ шифрования для разблокировки тома диска, и компьютер будет переведен в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="16294-120">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="16294-121">Если этот параметр задан, а соответствующий параметр групповая политика включен, он должен соответствовать параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="16294-121">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="16294-122">Если этот параметр не указан, используется значение по умолчанию, равное 0, 2, 4, 5, 8, 9, 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="16294-122">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="16294-123">Профиль проверки платформы по умолчанию защищает ключ шифрования от изменений в основном корне доверия измерений (КРТМ). BIOS и расширения платформы (PCR 0), код варианта ПЗУ (PCR 2), код основной загрузочной записи (PCR 4), таблица разделов основной загрузочной записи (PCR 5), загрузочный сектор NTFS (PCR 8), загрузочный код NTFS (PCR 9), диспетчер загрузки (PCR 10). и шифрование диска BitLocker управления доступом (PCR 11).</span><span class="sxs-lookup"><span data-stu-id="16294-123">The default platform validation profile secures the encryption key against changes to the Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions (PCR 0), Option ROM Code (PCR 2), the Master Boot Record (MBR) Code (PCR 4), the Master Boot Record (MBR) Partition Table (PCR 5), the NTFS Boot Sector (PCR 8), the NTFS Boot Code (PCR 9), the Boot Manager (PCR 10), and the BitLocker Drive Encryption Access Control (PCR 11).</span></span> <span data-ttu-id="16294-124">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16294-124">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="16294-125">Компьютеры на основе Единый интерфейс EFI (UEFI) по умолчанию не используют PCR 5.</span><span class="sxs-lookup"><span data-stu-id="16294-125">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span> <span data-ttu-id="16294-126">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="16294-126">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="16294-127">Изменение профиля по умолчанию влияет на безопасность и управляемость компьютера.</span><span class="sxs-lookup"><span data-stu-id="16294-127">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="16294-128">Чувствительность BitLocker к изменениям платформы (вредоносных или полномочных) увеличивается или уменьшается в зависимости от включения или исключения, соответственно, для PCRs.</span><span class="sxs-lookup"><span data-stu-id="16294-128">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="16294-129">Чтобы включить защиту BitLocker, профиль проверки платформы должен включать PCR 11.</span><span class="sxs-lookup"><span data-stu-id="16294-129">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="16294-130">Значение</span><span class="sxs-lookup"><span data-stu-id="16294-130">Value</span></span>                                                                         | <span data-ttu-id="16294-131">Значение</span><span class="sxs-lookup"><span data-stu-id="16294-131">Meaning</span></span>                                                                             |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16294-132"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="16294-132"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="16294-133">Корневой корень доверия измерений (КРТМ), BIOS и расширений платформы.</span><span class="sxs-lookup"><span data-stu-id="16294-133">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions.</span></span><br/> |
| <dl> <span data-ttu-id="16294-134"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="16294-134"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="16294-135">Конфигурация и данные платформы и материнской платы</span><span class="sxs-lookup"><span data-stu-id="16294-135">Platform and Motherboard Configuration and Data</span></span><br/>                          |
| <dl> <span data-ttu-id="16294-136"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="16294-136"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="16294-137">Код варианта ПЗУ</span><span class="sxs-lookup"><span data-stu-id="16294-137">Option ROM Code</span></span><br/>                                                          |
| <dl> <span data-ttu-id="16294-138"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="16294-138"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="16294-139">Конфигурация и данные с поддержкой ПЗУ</span><span class="sxs-lookup"><span data-stu-id="16294-139">Option ROM Configuration and Data</span></span><br/>                                        |
| <dl> <span data-ttu-id="16294-140"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="16294-140"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="16294-141">Код основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="16294-141">Master Boot Record (MBR) Code</span></span><br/>                                            |
| <dl> <span data-ttu-id="16294-142"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="16294-142"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="16294-143">Таблица разделов основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="16294-143">Master Boot Record (MBR) Partition Table</span></span><br/>                                 |
| <dl> <span data-ttu-id="16294-144"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="16294-144"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="16294-145">События смены состояния и пробуждения</span><span class="sxs-lookup"><span data-stu-id="16294-145">State Transition and Wake Events</span></span><br/>                                         |
| <dl> <span data-ttu-id="16294-146"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="16294-146"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="16294-147">Manufacturer-Specific компьютера</span><span class="sxs-lookup"><span data-stu-id="16294-147">Computer Manufacturer-Specific</span></span><br/>                                           |
| <dl> <span data-ttu-id="16294-148"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="16294-148"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="16294-149">Загрузочный сектор NTFS</span><span class="sxs-lookup"><span data-stu-id="16294-149">NTFS Boot Sector</span></span><br/>                                                         |
| <dl> <span data-ttu-id="16294-150"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="16294-150"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="16294-151">Загрузочный код NTFS</span><span class="sxs-lookup"><span data-stu-id="16294-151">NTFS Boot Code</span></span><br/>                                                           |
| <dl> <span data-ttu-id="16294-152"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="16294-152"><dt>10</dt></span></span> </dl> | <span data-ttu-id="16294-153">Диспетчер загрузки</span><span class="sxs-lookup"><span data-stu-id="16294-153">Boot Manager</span></span><br/>                                                             |
| <dl> <span data-ttu-id="16294-154"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="16294-154"><dt>11</dt></span></span> </dl> | <span data-ttu-id="16294-155">шифрование диска BitLocker контроля доступа</span><span class="sxs-lookup"><span data-stu-id="16294-155">BitLocker Drive Encryption Access Control</span></span><br/>                                |
| <dl> <span data-ttu-id="16294-156"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="16294-156"><dt>12</dt></span></span> </dl> | <span data-ttu-id="16294-157">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-157">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="16294-158"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="16294-158"><dt>13</dt></span></span> </dl> | <span data-ttu-id="16294-159">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-159">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="16294-160"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="16294-160"><dt>14</dt></span></span> </dl> | <span data-ttu-id="16294-161">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-161">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="16294-162"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="16294-162"><dt>15</dt></span></span> </dl> | <span data-ttu-id="16294-163">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-163">Defined for use by the static operating system</span></span><br/>                           |
| <dl> <span data-ttu-id="16294-164"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="16294-164"><dt>16</dt></span></span> </dl> | <span data-ttu-id="16294-165">Используется для отладки</span><span class="sxs-lookup"><span data-stu-id="16294-165">Used for debugging</span></span><br/>                                                       |
| <dl> <span data-ttu-id="16294-166"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="16294-166"><dt>17</dt></span></span> </dl> | <span data-ttu-id="16294-167">Динамический КРТМ</span><span class="sxs-lookup"><span data-stu-id="16294-167">Dynamic CRTM</span></span><br/>                                                             |
| <dl> <span data-ttu-id="16294-168"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="16294-168"><dt>18</dt></span></span> </dl> | <span data-ttu-id="16294-169">Определенная платформа</span><span class="sxs-lookup"><span data-stu-id="16294-169">Platform defined</span></span><br/>                                                         |
| <dl> <span data-ttu-id="16294-170"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="16294-170"><dt>19</dt></span></span> </dl> | <span data-ttu-id="16294-171">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-171">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="16294-172"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="16294-172"><dt>20</dt></span></span> </dl> | <span data-ttu-id="16294-173">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-173">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="16294-174"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="16294-174"><dt>21</dt></span></span> </dl> | <span data-ttu-id="16294-175">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-175">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="16294-176"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="16294-176"><dt>22</dt></span></span> </dl> | <span data-ttu-id="16294-177">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="16294-177">Used by trusted operating system</span></span><br/>                                         |
| <dl> <span data-ttu-id="16294-178"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="16294-178"><dt>23</dt></span></span> </dl> | <span data-ttu-id="16294-179">Поддержка приложений</span><span class="sxs-lookup"><span data-stu-id="16294-179">Application support</span></span><br/>                                                      |



 

</dd> <dt>

<span data-ttu-id="16294-180">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="16294-180">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="16294-181">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="16294-181">Type: **string**</span></span>

<span data-ttu-id="16294-182">Строка, однозначно определяющая созданный предохранитель, который может использоваться для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="16294-182">A string that uniquely identifies the created protector and which can be used to manage the key protector.</span></span>

<span data-ttu-id="16294-183">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="16294-183">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16294-184">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16294-184">Return value</span></span>

<span data-ttu-id="16294-185">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="16294-185">Type: **uint32**</span></span>

<span data-ttu-id="16294-186">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="16294-186">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="16294-187">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="16294-187">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="16294-188">Описание</span><span class="sxs-lookup"><span data-stu-id="16294-188">Description</span></span>                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16294-189"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-189"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="16294-190">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="16294-190">The method was successful.</span></span><br/>                                                                                                                                              |
| <dl> <span data-ttu-id="16294-191"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-191"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="16294-192">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="16294-192">The volume is locked.</span></span><br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="16294-193"><dt>**TBS \_ \_Служба E \_ не \_ работает**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-193"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="16294-194">На этом компьютере не найден совместимый доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="16294-194">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="16294-195"><dt>**ФВЕ \_ E \_ внешний \_ том**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-195"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="16294-196">Доверенный платформенный модуль не может защитить ключ шифрования тома, так как этот том не содержит текущую операционную систему.</span><span class="sxs-lookup"><span data-stu-id="16294-196">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                           |
| <dl> <span data-ttu-id="16294-197"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-197"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="16294-198">Параметр *платформвалидатионпрофиле* предоставляется, но его значения не находятся в известном диапазоне или не соответствуют текущему параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="16294-198">The *PlatformValidationProfile* parameter is provided but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="16294-199"><dt>**ФВЕ \_ Средство \_ защиты E \_ существует**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="16294-199"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="16294-200">Предохранитель ключа этого типа уже существует.</span><span class="sxs-lookup"><span data-stu-id="16294-200">A key protector of this type already exists.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="16294-201">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="16294-201">Security Considerations</span></span>

<span data-ttu-id="16294-202">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16294-202">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="16294-203">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="16294-203">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="16294-204">Изменение профиля по умолчанию влияет на безопасность или удобство использования компьютера.</span><span class="sxs-lookup"><span data-stu-id="16294-204">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="16294-205">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16294-205">Remarks</span></span>

<span data-ttu-id="16294-206">В любой момент времени может существовать не более одного предохранителя ключа типа "TPM" для тома.</span><span class="sxs-lookup"><span data-stu-id="16294-206">At most one key protector of type "TPM" can exist for a volume at any time.</span></span> <span data-ttu-id="16294-207">Если вы хотите изменить отображаемое имя или профиль проверки платформы, используемый существующим предохранителем ключа "TPM", необходимо сначала удалить существующий предохранитель ключа, а затем вызвать **протекткэйвистпм** , чтобы создать новый.</span><span class="sxs-lookup"><span data-stu-id="16294-207">If you want to change the display name or the platform validation profile used by an existing "TPM" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPM** to create a new one.</span></span>

<span data-ttu-id="16294-208">Для индексов PCR от 0 до 5 текущие измерения в регистрах используются для защиты ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="16294-208">For PCR indices 0 through 5, the current measurements in the registers are used to protect the encryption key.</span></span> <span data-ttu-id="16294-209">Для значений PCR 8 – 11 используются измерения, которые должны существовать в следующем цикле запуска.</span><span class="sxs-lookup"><span data-stu-id="16294-209">For PCR values 8 through 11, the measurements used are the ones expected to exist on the next start cycle.</span></span>

<span data-ttu-id="16294-210">Необходимо указать дополнительные предохранители ключа, чтобы разблокировать том в сценариях восстановления, где невозможно получить доступ к ключу шифрования тома. Например, если доверенный платформенный модуль не может успешно проверить профиль проверки платформы.</span><span class="sxs-lookup"><span data-stu-id="16294-210">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile.</span></span> <span data-ttu-id="16294-211">Используйте [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) или [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , чтобы создать один или несколько предохранителей ключа для восстановления тома, заблокированного иным образом.</span><span class="sxs-lookup"><span data-stu-id="16294-211">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="16294-212">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="16294-212">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="16294-213">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="16294-213">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="16294-214">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="16294-214">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="16294-215">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="16294-215">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="16294-216">Требования</span><span class="sxs-lookup"><span data-stu-id="16294-216">Requirements</span></span>



| <span data-ttu-id="16294-217">Требование</span><span class="sxs-lookup"><span data-stu-id="16294-217">Requirement</span></span> | <span data-ttu-id="16294-218">Значение</span><span class="sxs-lookup"><span data-stu-id="16294-218">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16294-219">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16294-219">Minimum supported client</span></span><br/> | <span data-ttu-id="16294-220">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="16294-220">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="16294-221">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16294-221">Minimum supported server</span></span><br/> | <span data-ttu-id="16294-222">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="16294-222">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="16294-223">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="16294-223">Namespace</span></span><br/>                | <span data-ttu-id="16294-224">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="16294-224">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="16294-225">MOF</span><span class="sxs-lookup"><span data-stu-id="16294-225">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16294-226"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="16294-226"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16294-227">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16294-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16294-228">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="16294-228">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="16294-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="16294-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
