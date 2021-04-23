---
description: Если доверенный платформенный модуль (TPM) (TPM) доступен, этот метод обеспечивает защиту ключа шифрования тома, расширенного внешним ключом.
ms.assetid: 58bc2de7-645f-4049-949c-975062f8c8ce
title: Метод Протекткэйвистпмандстартупкэй класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndStartupKey
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 06ab2b9474b3564a567374490d9aeb70448338be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662291"
---
# <a name="protectkeywithtpmandstartupkey-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="0ab8f-103">Метод Протекткэйвистпмандстартупкэй \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="0ab8f-103">ProtectKeyWithTPMAndStartupKey method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="0ab8f-104">Метод **протекткэйвистпмандстартупкэй** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью аппаратного обеспечения безопасности доверенный платформенный модуль (TPM) (доверенного платформенного модуля) на компьютере (при его наличии), дополненного внешним ключом, который должен быть представлен для компьютера при запуске.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-104">The **ProtectKeyWithTPMAndStartupKey** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by an external key that must be presented to the computer at startup.</span></span>

<span data-ttu-id="0ab8f-105">Обе проверки TPM и вход USB-устройства памяти, содержащие внешний ключ, необходимы для доступа к ключу шифрования тома и разблокировки содержимого тома.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-105">Both validation by the TPM and input of a USB memory device that contains the external key are necessary to access the volume's encryption key and unlock the volume contents.</span></span> <span data-ttu-id="0ab8f-106">Используйте метод [**савикстерналкэйтофиле**](saveexternalkeytofile-win32-encryptablevolume.md) , чтобы сохранить этот внешний ключ в файл на USB-устройстве для использования в качестве ключа запуска.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-106">Use the [**SaveExternalKeyToFile**](saveexternalkeytofile-win32-encryptablevolume.md) method to save this external key to a file on a USB memory device for usage as a startup key.</span></span>

<span data-ttu-id="0ab8f-107">Этот метод применим только к тому, который содержит текущую операционную систему.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-107">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="0ab8f-108">Для тома создается предохранитель ключа с типом "TPM и ключ запуска", если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-108">A key protector of type "TPM And Startup Key" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ab8f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ab8f-109">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndStartupKey(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in, optional] uint8  ExternalKey[],
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="0ab8f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ab8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ab8f-111">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-111">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab8f-112">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-112">Type: **string**</span></span>

<span data-ttu-id="0ab8f-113">Назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-113">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="0ab8f-114">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-114">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8f-115">*Платформвалидатионпрофиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-115">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab8f-116">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-116">Type: **uint8\[\]**</span></span>

<span data-ttu-id="0ab8f-117">Массив целых чисел, указывающий, как оборудование безопасности доверенный платформенный модуль (TPM) компьютера (TPM) защищает ключ шифрования тома диска.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-117">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the encryption key of the disk volume.</span></span>

<span data-ttu-id="0ab8f-118">Профиль проверки платформы состоит из набора индексов реестра конфигурации платформы (PCR) в диапазоне от 0 до 23 включительно.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-118">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="0ab8f-119">Значения Repeat в параметре не учитываются.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-119">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="0ab8f-120">Каждый индекс PCR связан со службами, которые выполняются при запуске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-120">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="0ab8f-121">При каждом запуске компьютера доверенный платформенный модуль проверит, не изменились ли службы, указанные в профиле проверки платформы.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-121">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="0ab8f-122">Если какая-либо из этих служб изменилась, когда шифрование диска BitLocker (BDE) остается включенной, доверенный платформенный модуль не будет освобождать ключ шифрования для разблокировки тома диска, и компьютер будет переведен в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-122">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="0ab8f-123">Если этот параметр задан, а соответствующий параметр групповая политика включен, он должен соответствовать параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-123">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="0ab8f-124">Если этот параметр не указан, используется значение по умолчанию, равное 0, 2, 4, 5, 8, 9, 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-124">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="0ab8f-125">Профиль проверки платформы по умолчанию защищает ключ шифрования от изменений в следующих элементах:</span><span class="sxs-lookup"><span data-stu-id="0ab8f-125">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="0ab8f-126">Основной корень доверия измерения (КРТМ)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-126">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="0ab8f-127">BIOS</span><span class="sxs-lookup"><span data-stu-id="0ab8f-127">BIOS</span></span>
-   <span data-ttu-id="0ab8f-128">Расширения платформы (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-128">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="0ab8f-129">Код варианта ПЗУ (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-129">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="0ab8f-130">Код основной загрузочной записи (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-130">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="0ab8f-131">Таблица разделов основной загрузочной записи (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-131">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="0ab8f-132">Загрузочный сектор NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-132">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="0ab8f-133">Загрузочный блок NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-133">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="0ab8f-134">Диспетчер загрузки (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-134">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="0ab8f-135">Контроль доступа BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-135">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="0ab8f-136">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-136">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="0ab8f-137">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-137">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="0ab8f-138">Компьютеры на основе Единый интерфейс EFI (UEFI) по умолчанию не используют PCR 5.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-138">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="0ab8f-139">Изменение профиля по умолчанию влияет на безопасность и управляемость компьютера.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-139">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="0ab8f-140">Чувствительность BitLocker к изменениям платформы (вредоносных или полномочных) увеличивается или уменьшается в зависимости от включения или исключения, соответственно, для PCRs.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-140">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="0ab8f-141">Чтобы включить защиту BitLocker, профиль проверки платформы должен включать PCR 11.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-141">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="0ab8f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab8f-142">Value</span></span>                                                                         | <span data-ttu-id="0ab8f-143">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab8f-143">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ab8f-144"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-144"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-145">Корневой корень доверия измерений (КРТМ), BIOS и расширений платформы</span><span class="sxs-lookup"><span data-stu-id="0ab8f-145">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="0ab8f-146"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-146"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-147">Конфигурация и данные платформы и материнской платы</span><span class="sxs-lookup"><span data-stu-id="0ab8f-147">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="0ab8f-148"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-148"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-149">Код варианта ПЗУ</span><span class="sxs-lookup"><span data-stu-id="0ab8f-149">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="0ab8f-150"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-150"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-151">Конфигурация и данные с поддержкой ПЗУ</span><span class="sxs-lookup"><span data-stu-id="0ab8f-151">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="0ab8f-152"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-152"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-153">Код основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-153">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="0ab8f-154"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-154"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-155">Таблица разделов основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="0ab8f-155">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="0ab8f-156"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-156"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-157">События смены состояния и пробуждения</span><span class="sxs-lookup"><span data-stu-id="0ab8f-157">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="0ab8f-158"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-158"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-159">Manufacturer-Specific компьютера</span><span class="sxs-lookup"><span data-stu-id="0ab8f-159">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="0ab8f-160"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-160"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-161">Загрузочный сектор NTFS</span><span class="sxs-lookup"><span data-stu-id="0ab8f-161">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0ab8f-162"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-162"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="0ab8f-163">Загрузочный блок NTFS</span><span class="sxs-lookup"><span data-stu-id="0ab8f-163">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="0ab8f-164"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-164"><dt>10</dt></span></span> </dl> | <span data-ttu-id="0ab8f-165">Диспетчер загрузки</span><span class="sxs-lookup"><span data-stu-id="0ab8f-165">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="0ab8f-166"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-166"><dt>11</dt></span></span> </dl> | <span data-ttu-id="0ab8f-167">Контроль доступа BitLocker</span><span class="sxs-lookup"><span data-stu-id="0ab8f-167">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="0ab8f-168"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-168"><dt>12</dt></span></span> </dl> | <span data-ttu-id="0ab8f-169">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-169">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="0ab8f-170"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-170"><dt>13</dt></span></span> </dl> | <span data-ttu-id="0ab8f-171">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-171">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="0ab8f-172"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-172"><dt>14</dt></span></span> </dl> | <span data-ttu-id="0ab8f-173">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-173">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="0ab8f-174"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-174"><dt>15</dt></span></span> </dl> | <span data-ttu-id="0ab8f-175">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-175">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="0ab8f-176"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-176"><dt>16</dt></span></span> </dl> | <span data-ttu-id="0ab8f-177">Используется для отладки</span><span class="sxs-lookup"><span data-stu-id="0ab8f-177">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="0ab8f-178"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-178"><dt>17</dt></span></span> </dl> | <span data-ttu-id="0ab8f-179">Динамический КРТМ</span><span class="sxs-lookup"><span data-stu-id="0ab8f-179">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="0ab8f-180"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-180"><dt>18</dt></span></span> </dl> | <span data-ttu-id="0ab8f-181">Определенная платформа</span><span class="sxs-lookup"><span data-stu-id="0ab8f-181">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="0ab8f-182"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-182"><dt>19</dt></span></span> </dl> | <span data-ttu-id="0ab8f-183">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-183">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ab8f-184"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-184"><dt>20</dt></span></span> </dl> | <span data-ttu-id="0ab8f-185">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-185">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ab8f-186"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-186"><dt>21</dt></span></span> </dl> | <span data-ttu-id="0ab8f-187">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-187">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ab8f-188"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-188"><dt>22</dt></span></span> </dl> | <span data-ttu-id="0ab8f-189">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="0ab8f-189">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ab8f-190"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-190"><dt>23</dt></span></span> </dl> | <span data-ttu-id="0ab8f-191">Поддержка приложений</span><span class="sxs-lookup"><span data-stu-id="0ab8f-191">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="0ab8f-192">*Екстерналкэй* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-192">*ExternalKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab8f-193">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-193">Type: **uint8\[\]**</span></span>

<span data-ttu-id="0ab8f-194">Массив байтов, указывающий 256-разрядный внешний ключ, используемый для разблокировки тома при запуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-194">An array of bytes that specifies the 256-bit external key used to unlock the volume when the computer starts.</span></span>

<span data-ttu-id="0ab8f-195">Если внешний ключ не указан, он создается случайным образом.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-195">If no external key is specified, one is randomly generated.</span></span> <span data-ttu-id="0ab8f-196">Используйте метод [**жеткэйпротекторекстерналкэй**](getkeyprotectorexternalkey-win32-encryptablevolume.md) для получения созданного случайным образом ключа.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-196">Use the [**GetKeyProtectorExternalKey**](getkeyprotectorexternalkey-win32-encryptablevolume.md) method to obtain the randomly generated key.</span></span>

</dd> <dt>

<span data-ttu-id="0ab8f-197">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-197">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ab8f-198">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-198">Type: **string**</span></span>

<span data-ttu-id="0ab8f-199">Строка, которая представляет собой уникальный идентификатор, связанный с созданным предохранителем ключа, который можно использовать для управления предохранителем ключа.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-199">A string that is the unique identifier associated with the created key protector that can be used to manage the key protector.</span></span>

<span data-ttu-id="0ab8f-200">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-200">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ab8f-201">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ab8f-201">Return value</span></span>

<span data-ttu-id="0ab8f-202">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-202">Type: **uint32**</span></span>

<span data-ttu-id="0ab8f-203">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-203">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="0ab8f-204">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="0ab8f-204">Return code/value</span></span>                                                                                                                                                                         | <span data-ttu-id="0ab8f-205">Описание</span><span class="sxs-lookup"><span data-stu-id="0ab8f-205">Description</span></span>                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ab8f-206"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-206"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                         | <span data-ttu-id="0ab8f-207">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-207">The method was successful.</span></span><br/>                                                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="0ab8f-208"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-208"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>        | <span data-ttu-id="0ab8f-209">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-209">The volume is locked.</span></span><br/>                                                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="0ab8f-210"><dt>**TBS \_ \_Служба E \_ не \_ работает**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-210"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl> | <span data-ttu-id="0ab8f-211">На этом компьютере не найден совместимый доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-211">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="0ab8f-212"><dt>**ФВЕ \_ E \_ внешний \_ том**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-212"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>       | <span data-ttu-id="0ab8f-213">Доверенный платформенный модуль не может защитить ключ шифрования тома, так как этот том не содержит текущую операционную систему.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-213">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                                                                                                               |
| <dl> <span data-ttu-id="0ab8f-214"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-214"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                 | <span data-ttu-id="0ab8f-215">Параметр *платформвалидатионпрофиле* предоставляется, но его значения не находятся в известном диапазоне или не соответствуют текущему параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-215">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> <span data-ttu-id="0ab8f-216">Параметр *екстерналкэй* предоставляется, но не является массивом размера 32.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-216">The *ExternalKey* parameter is provided but is not an array of size 32.</span></span><br/> |
| <dl> <span data-ttu-id="0ab8f-217"><dt>**ФВЕ \_ E \_ загрузочная \_ кддвд**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-217"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>       | <span data-ttu-id="0ab8f-218">На этом компьютере находится загрузочный компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-218">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="0ab8f-219">Удалите компакт-диск или диск DVD и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-219">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="0ab8f-220"><dt>**ФВЕ \_ Средство \_ защиты E \_ существует**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>     | <span data-ttu-id="0ab8f-221">Предохранитель ключа этого типа уже существует.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-221">A key protector of this type already exists.</span></span><br/>                                                                                                                                                                                                                |



 

## <a name="security-considerations"></a><span data-ttu-id="0ab8f-222">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="0ab8f-222">Security Considerations</span></span>

<span data-ttu-id="0ab8f-223">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-223">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="0ab8f-224">Для дополнительной защиты от изменений кода раннего запуска используйте профиль PCRs 0, 2, 4, 5, 8, 9, 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-224">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="0ab8f-225">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-225">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="0ab8f-226">Изменение профиля по умолчанию влияет на безопасность или удобство использования компьютера.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-226">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ab8f-227">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ab8f-227">Remarks</span></span>

<span data-ttu-id="0ab8f-228">В любой момент времени может существовать не более одного предохранителя ключа типа "TPM и ключ запуска" для тома.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-228">At most one key protector of type "TPM And Startup Key" can exist for a volume at any time.</span></span> <span data-ttu-id="0ab8f-229">Если вы хотите изменить отображаемое имя или профиль проверки платформы, используемый существующим предохранителем ключа "TPM и ключ запуска", необходимо сначала удалить существующий предохранитель ключа, а затем вызвать **протекткэйвистпмандстартупкэй** , чтобы создать новый.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-229">If you want to change the display name or the platform validation profile used by an existing "TPM plus Startup Key" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndStartupKey** to create a new one.</span></span> <span data-ttu-id="0ab8f-230">Необходимо указать дополнительные предохранители ключа, чтобы разблокировать том в сценариях восстановления, где невозможно получить доступ к ключу шифрования тома. Например, если доверенный платформенный модуль не может успешно проверить профиль проверки платформы или если USB-память, содержащая внешний ключ, потеряна.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-230">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when USB memory that contains the external key is lost.</span></span>

<span data-ttu-id="0ab8f-231">Используйте [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) или [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , чтобы создать один или несколько предохранителей ключа для восстановления тома, заблокированного иным образом.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-231">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="0ab8f-232">Хотя возможно наличие предохранителя ключа типа "TPM" и другого типа "TPM и ключ запуска", наличие типа предохранителя ключа "TPM" отрицательно влияет на влияние других предохранителей ключей на основе TPM.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-232">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And Startup Key", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="0ab8f-233">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ab8f-233">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ab8f-234">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-234">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0ab8f-235">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0ab8f-235">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ab8f-236">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0ab8f-236">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ab8f-237">Требования</span><span class="sxs-lookup"><span data-stu-id="0ab8f-237">Requirements</span></span>



| <span data-ttu-id="0ab8f-238">Требование</span><span class="sxs-lookup"><span data-stu-id="0ab8f-238">Requirement</span></span> | <span data-ttu-id="0ab8f-239">Значение</span><span class="sxs-lookup"><span data-stu-id="0ab8f-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ab8f-240">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ab8f-240">Minimum supported client</span></span><br/> | <span data-ttu-id="0ab8f-241">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-241">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0ab8f-242">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ab8f-242">Minimum supported server</span></span><br/> | <span data-ttu-id="0ab8f-243">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0ab8f-243">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0ab8f-244">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ab8f-244">Namespace</span></span><br/>                | <span data-ttu-id="0ab8f-245">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="0ab8f-245">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="0ab8f-246">MOF</span><span class="sxs-lookup"><span data-stu-id="0ab8f-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ab8f-247"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ab8f-247"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ab8f-248">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ab8f-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ab8f-249">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-249">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="0ab8f-250">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="0ab8f-250">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
