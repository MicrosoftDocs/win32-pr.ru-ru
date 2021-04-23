---
description: Если доверенный платформенный модуль (TPM) (доверенный платформенный модуль) доступен, этот метод обеспечивает защиту ключа шифрования тома, расширенного с помощью указанного пользователем личного идентификационного номера.
ms.assetid: 8c4c434a-dd60-491a-a983-b3fa78c91c0d
title: Метод Протекткэйвистпмандпин класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.ProtectKeyWithTPMAndPIN
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: e5a0a7a253723bec84df7a86fa94ab182bd192dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897046"
---
# <a name="protectkeywithtpmandpin-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="415d6-103">Метод Протекткэйвистпмандпин \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="415d6-103">ProtectKeyWithTPMAndPIN method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="415d6-104">Метод **протекткэйвистпмандпин** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) защищает ключ шифрования тома с помощью аппаратного обеспечения безопасности доверенный платформенный модуль (TPM) (доверенного платформенного модуля) на компьютере (при его наличии), дополненного пользовательским идентификационным номером (ПИН-кодом), который должен быть предоставлен компьютеру при запуске.</span><span class="sxs-lookup"><span data-stu-id="415d6-104">The **ProtectKeyWithTPMAndPIN** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class secures the volume's encryption key by using the Trusted Platform Module (TPM) Security Hardware on the computer, if available, enhanced by a user-specified personal identification number (PIN) that must be provided to the computer at startup.</span></span>

<span data-ttu-id="415d6-105">Для доступа к ключу шифрования тома и разблокировки содержимого тома необходимы обе проверки, предоставляемые TPM и входные данные личной строки идентификации.</span><span class="sxs-lookup"><span data-stu-id="415d6-105">Both validation by the TPM and input of the personal identification string are necessary to access the volume's encryption key and unlock volume contents.</span></span>

<span data-ttu-id="415d6-106">Этот метод применим только к тому, который содержит текущую операционную систему.</span><span class="sxs-lookup"><span data-stu-id="415d6-106">This method is only applicable for the volume that contains the currently running operating system.</span></span>

<span data-ttu-id="415d6-107">Для тома создается предохранитель ключа типа "TPM и ПИН-код", если он еще не существует.</span><span class="sxs-lookup"><span data-stu-id="415d6-107">A key protector of type "TPM And PIN" is created for the volume, if one does not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="415d6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="415d6-108">Syntax</span></span>


```mof
uint32 ProtectKeyWithTPMAndPIN(
  [in, optional] string FriendlyName,
  [in, optional] uint8  PlatformValidationProfile[],
  [in]           string PIN,
  [out]          string VolumeKeyProtectorID
);
```



## <a name="parameters"></a><span data-ttu-id="415d6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="415d6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415d6-110">*FriendlyName* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="415d6-110">*FriendlyName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="415d6-111">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="415d6-111">Type: **string**</span></span>

<span data-ttu-id="415d6-112">Назначенный пользователем строковый идентификатор для предохранителя ключа.</span><span class="sxs-lookup"><span data-stu-id="415d6-112">A user-assigned string identifier for this key protector.</span></span> <span data-ttu-id="415d6-113">Если этот параметр не указан, используется пустое значение.</span><span class="sxs-lookup"><span data-stu-id="415d6-113">If this parameter is not specified, a blank value is used.</span></span>

</dd> <dt>

<span data-ttu-id="415d6-114">*Платформвалидатионпрофиле* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="415d6-114">*PlatformValidationProfile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="415d6-115">Тип: **Uint8 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="415d6-115">Type: **uint8\[\]**</span></span>

<span data-ttu-id="415d6-116">Массив целых чисел, указывающий, как оборудование безопасности доверенный платформенный модуль (TPM) компьютера (TPM) защищает ключ шифрования тома диска.</span><span class="sxs-lookup"><span data-stu-id="415d6-116">An array of integers that specifies how the computer's Trusted Platform Module (TPM) Security Hardware secures the disk volume's encryption key.</span></span>

<span data-ttu-id="415d6-117">Профиль проверки платформы состоит из набора индексов реестра конфигурации платформы (PCR) в диапазоне от 0 до 23 включительно.</span><span class="sxs-lookup"><span data-stu-id="415d6-117">A platform validation profile consists of a set of Platform Configuration Register (PCR) indices ranging from 0 to 23, inclusive.</span></span> <span data-ttu-id="415d6-118">Значения Repeat в параметре не учитываются.</span><span class="sxs-lookup"><span data-stu-id="415d6-118">Repeat values in the parameter are ignored.</span></span> <span data-ttu-id="415d6-119">Каждый индекс PCR связан со службами, которые выполняются при запуске операционной системы.</span><span class="sxs-lookup"><span data-stu-id="415d6-119">Each PCR index is associated with services that run when the operating system starts.</span></span> <span data-ttu-id="415d6-120">При каждом запуске компьютера доверенный платформенный модуль проверит, не изменились ли службы, указанные в профиле проверки платформы.</span><span class="sxs-lookup"><span data-stu-id="415d6-120">Each time the computer starts, the TPM will check that the services you specified in the platform validation profile have not changed.</span></span> <span data-ttu-id="415d6-121">Если какая-либо из этих служб изменилась, когда шифрование диска BitLocker (BDE) остается включенной, доверенный платформенный модуль не будет освобождать ключ шифрования для разблокировки тома диска, и компьютер будет переведен в режим восстановления.</span><span class="sxs-lookup"><span data-stu-id="415d6-121">If any of these services change while BitLocker Drive Encryption (BDE) protection remains on, the TPM will not release the encryption key to unlock the disk volume, and the computer will enter into recovery mode.</span></span>

<span data-ttu-id="415d6-122">Если этот параметр задан, а соответствующий параметр групповая политика включен, он должен соответствовать параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="415d6-122">If this parameter is specified while the corresponding Group Policy setting has been enabled, it must match the Group Policy setting.</span></span>

<span data-ttu-id="415d6-123">Если этот параметр не указан, используется значение по умолчанию, равное 0, 2, 4, 5, 8, 9, 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="415d6-123">If this parameter is not specified, the default of 0, 2, 4, 5, 8, 9, 10, and 11 is used.</span></span> <span data-ttu-id="415d6-124">Профиль проверки платформы по умолчанию защищает ключ шифрования от изменений в следующих элементах:</span><span class="sxs-lookup"><span data-stu-id="415d6-124">The default platform validation profile secures the encryption key against changes to the following elements:</span></span>

-   <span data-ttu-id="415d6-125">Основной корень доверия измерения (КРТМ)</span><span class="sxs-lookup"><span data-stu-id="415d6-125">Core Root of Trust of Measurement (CRTM)</span></span>
-   <span data-ttu-id="415d6-126">BIOS</span><span class="sxs-lookup"><span data-stu-id="415d6-126">BIOS</span></span>
-   <span data-ttu-id="415d6-127">Расширения платформы (PCR 0)</span><span class="sxs-lookup"><span data-stu-id="415d6-127">Platform Extensions (PCR 0)</span></span>
-   <span data-ttu-id="415d6-128">Код варианта ПЗУ (PCR 2)</span><span class="sxs-lookup"><span data-stu-id="415d6-128">Option ROM Code (PCR 2)</span></span>
-   <span data-ttu-id="415d6-129">Код основной загрузочной записи (PCR 4)</span><span class="sxs-lookup"><span data-stu-id="415d6-129">Master Boot Record (MBR) Code (PCR 4)</span></span>
-   <span data-ttu-id="415d6-130">Таблица разделов основной загрузочной записи (PCR 5)</span><span class="sxs-lookup"><span data-stu-id="415d6-130">Master Boot Record (MBR) Partition Table (PCR 5)</span></span>
-   <span data-ttu-id="415d6-131">Загрузочный сектор NTFS (PCR 8)</span><span class="sxs-lookup"><span data-stu-id="415d6-131">NTFS Boot Sector (PCR 8)</span></span>
-   <span data-ttu-id="415d6-132">Загрузочный блок NTFS (PCR 9)</span><span class="sxs-lookup"><span data-stu-id="415d6-132">NTFS Boot Block (PCR 9)</span></span>
-   <span data-ttu-id="415d6-133">Диспетчер загрузки (PCR 10)</span><span class="sxs-lookup"><span data-stu-id="415d6-133">Boot Manager (PCR 10)</span></span>
-   <span data-ttu-id="415d6-134">Контроль доступа BitLocker (PCR 11)</span><span class="sxs-lookup"><span data-stu-id="415d6-134">BitLocker Access Control (PCR 11)</span></span>

<span data-ttu-id="415d6-135">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="415d6-135">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="415d6-136">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="415d6-136">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span> <span data-ttu-id="415d6-137">Компьютеры на основе Единый интерфейс EFI (UEFI) по умолчанию не используют PCR 5.</span><span class="sxs-lookup"><span data-stu-id="415d6-137">Unified Extensible Firmware Interface (UEFI)–based computers do not use PCR 5 by default.</span></span>

<span data-ttu-id="415d6-138">Изменение профиля по умолчанию влияет на безопасность и управляемость компьютера.</span><span class="sxs-lookup"><span data-stu-id="415d6-138">Changing from the default profile affects the security and manageability of your computer.</span></span> <span data-ttu-id="415d6-139">Чувствительность BitLocker к изменениям платформы (вредоносных или полномочных) увеличивается или уменьшается в зависимости от включения или исключения, соответственно, для PCRs.</span><span class="sxs-lookup"><span data-stu-id="415d6-139">The sensitivity of BitLocker to platform modifications (malicious or authorized) is increased or decreased depending upon the inclusion or exclusion, respectively, of the PCRs.</span></span> <span data-ttu-id="415d6-140">Чтобы включить защиту BitLocker, профиль проверки платформы должен включать PCR 11.</span><span class="sxs-lookup"><span data-stu-id="415d6-140">For BitLocker protection to be enabled, the platform validation profile must include PCR 11.</span></span>



| <span data-ttu-id="415d6-141">Значение</span><span class="sxs-lookup"><span data-stu-id="415d6-141">Value</span></span>                                                                         | <span data-ttu-id="415d6-142">Значение</span><span class="sxs-lookup"><span data-stu-id="415d6-142">Meaning</span></span>                                                                            |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="415d6-143"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-143"><dt>0</dt></span></span> </dl>  | <span data-ttu-id="415d6-144">Корневой корень доверия измерений (КРТМ), BIOS и расширений платформы</span><span class="sxs-lookup"><span data-stu-id="415d6-144">Core Root of Trust of Measurement (CRTM), BIOS, and Platform Extensions</span></span><br/> |
| <dl> <span data-ttu-id="415d6-145"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-145"><dt>1</dt></span></span> </dl>  | <span data-ttu-id="415d6-146">Конфигурация и данные платформы и материнской платы</span><span class="sxs-lookup"><span data-stu-id="415d6-146">Platform and Motherboard Configuration and Data</span></span><br/>                         |
| <dl> <span data-ttu-id="415d6-147"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-147"><dt>2</dt></span></span> </dl>  | <span data-ttu-id="415d6-148">Код варианта ПЗУ</span><span class="sxs-lookup"><span data-stu-id="415d6-148">Option ROM Code</span></span><br/>                                                         |
| <dl> <span data-ttu-id="415d6-149"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-149"><dt>3</dt></span></span> </dl>  | <span data-ttu-id="415d6-150">Конфигурация и данные с поддержкой ПЗУ</span><span class="sxs-lookup"><span data-stu-id="415d6-150">Option ROM Configuration and Data</span></span><br/>                                       |
| <dl> <span data-ttu-id="415d6-151"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-151"><dt>4</dt></span></span> </dl>  | <span data-ttu-id="415d6-152">Код основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="415d6-152">Master Boot Record (MBR) Code</span></span><br/>                                           |
| <dl> <span data-ttu-id="415d6-153"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-153"><dt>5</dt></span></span> </dl>  | <span data-ttu-id="415d6-154">Таблица разделов основной загрузочной записи (MBR)</span><span class="sxs-lookup"><span data-stu-id="415d6-154">Master Boot Record (MBR) Partition Table</span></span><br/>                                |
| <dl> <span data-ttu-id="415d6-155"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-155"><dt>6</dt></span></span> </dl>  | <span data-ttu-id="415d6-156">События смены состояния и пробуждения</span><span class="sxs-lookup"><span data-stu-id="415d6-156">State Transition and Wake Events</span></span><br/>                                        |
| <dl> <span data-ttu-id="415d6-157"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-157"><dt>7</dt></span></span> </dl>  | <span data-ttu-id="415d6-158">Manufacturer-Specific компьютера</span><span class="sxs-lookup"><span data-stu-id="415d6-158">Computer Manufacturer-Specific</span></span><br/>                                          |
| <dl> <span data-ttu-id="415d6-159"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-159"><dt>8</dt></span></span> </dl>  | <span data-ttu-id="415d6-160">Загрузочный сектор NTFS</span><span class="sxs-lookup"><span data-stu-id="415d6-160">NTFS Boot Sector</span></span><br/>                                                        |
| <dl> <span data-ttu-id="415d6-161"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-161"><dt>9</dt></span></span> </dl>  | <span data-ttu-id="415d6-162">Загрузочный блок NTFS</span><span class="sxs-lookup"><span data-stu-id="415d6-162">NTFS Boot Block</span></span><br/>                                                         |
| <dl> <span data-ttu-id="415d6-163"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-163"><dt>10</dt></span></span> </dl> | <span data-ttu-id="415d6-164">Диспетчер загрузки</span><span class="sxs-lookup"><span data-stu-id="415d6-164">Boot Manager</span></span><br/>                                                            |
| <dl> <span data-ttu-id="415d6-165"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-165"><dt>11</dt></span></span> </dl> | <span data-ttu-id="415d6-166">Контроль доступа BitLocker</span><span class="sxs-lookup"><span data-stu-id="415d6-166">BitLocker Access Control</span></span><br/>                                                |
| <dl> <span data-ttu-id="415d6-167"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-167"><dt>12</dt></span></span> </dl> | <span data-ttu-id="415d6-168">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-168">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="415d6-169"><dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-169"><dt>13</dt></span></span> </dl> | <span data-ttu-id="415d6-170">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-170">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="415d6-171"><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-171"><dt>14</dt></span></span> </dl> | <span data-ttu-id="415d6-172">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-172">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="415d6-173"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-173"><dt>15</dt></span></span> </dl> | <span data-ttu-id="415d6-174">Определено для использования статической операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-174">Defined for use by the static operating system</span></span><br/>                          |
| <dl> <span data-ttu-id="415d6-175"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-175"><dt>16</dt></span></span> </dl> | <span data-ttu-id="415d6-176">Используется для отладки</span><span class="sxs-lookup"><span data-stu-id="415d6-176">Used for debugging</span></span><br/>                                                      |
| <dl> <span data-ttu-id="415d6-177"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-177"><dt>17</dt></span></span> </dl> | <span data-ttu-id="415d6-178">Динамический КРТМ</span><span class="sxs-lookup"><span data-stu-id="415d6-178">Dynamic CRTM</span></span><br/>                                                            |
| <dl> <span data-ttu-id="415d6-179"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-179"><dt>18</dt></span></span> </dl> | <span data-ttu-id="415d6-180">Определенная платформа</span><span class="sxs-lookup"><span data-stu-id="415d6-180">Platform defined</span></span><br/>                                                        |
| <dl> <span data-ttu-id="415d6-181"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-181"><dt>19</dt></span></span> </dl> | <span data-ttu-id="415d6-182">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-182">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="415d6-183"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-183"><dt>20</dt></span></span> </dl> | <span data-ttu-id="415d6-184">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-184">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="415d6-185"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-185"><dt>21</dt></span></span> </dl> | <span data-ttu-id="415d6-186">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-186">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="415d6-187"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-187"><dt>22</dt></span></span> </dl> | <span data-ttu-id="415d6-188">Используется доверенной операционной системой</span><span class="sxs-lookup"><span data-stu-id="415d6-188">Used by a trusted operating system</span></span><br/>                                      |
| <dl> <span data-ttu-id="415d6-189"><dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-189"><dt>23</dt></span></span> </dl> | <span data-ttu-id="415d6-190">Поддержка приложений</span><span class="sxs-lookup"><span data-stu-id="415d6-190">Application support</span></span><br/>                                                     |



 

</dd> <dt>

<span data-ttu-id="415d6-191">*Закрепить* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="415d6-191">*PIN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="415d6-192">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="415d6-192">Type: **string**</span></span>

<span data-ttu-id="415d6-193">Указанная пользователем личная строка идентификации.</span><span class="sxs-lookup"><span data-stu-id="415d6-193">A user-specified personal identification string.</span></span> <span data-ttu-id="415d6-194">Эта строка должна содержать от 6 до 20 цифр или, если включена групповая политика "разрешить Расширенные ПИН-коды для запуска", от 6 до 20 букв, символов, пробелов или чисел.</span><span class="sxs-lookup"><span data-stu-id="415d6-194">This string must consist of a sequence of 6 to 20 digits or, if the "Allow enhanced PINs for startup" group policy is enabled, 6 to 20 letters, symbols, spaces, or numbers.</span></span>

</dd> <dt>

<span data-ttu-id="415d6-195">*Волумекэйпротекторид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="415d6-195">*VolumeKeyProtectorID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415d6-196">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="415d6-196">Type: **string**</span></span>

<span data-ttu-id="415d6-197">Обновленный уникальный идентификатор строки, используемый для управления предохранителем ключа зашифрованного тома.</span><span class="sxs-lookup"><span data-stu-id="415d6-197">The updated unique string identifier used to manage an encrypted volume key protector.</span></span>

<span data-ttu-id="415d6-198">Если диск поддерживает аппаратное шифрование, а BitLocker не использует нестандартное владение, для строки идентификатора задается значение "BitLocker", а предохранитель ключа записывается в метаданные диапазона.</span><span class="sxs-lookup"><span data-stu-id="415d6-198">If the drive supports hardware encryption and BitLocker has not taken band ownership, the ID string is set to "BitLocker" and the key protector is written to per band metadata.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="415d6-199">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="415d6-199">Return value</span></span>

<span data-ttu-id="415d6-200">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="415d6-200">Type: **uint32**</span></span>

<span data-ttu-id="415d6-201">При сбое этот метод возвращает один из следующих кодов или другой код ошибки.</span><span class="sxs-lookup"><span data-stu-id="415d6-201">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="415d6-202">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="415d6-202">Return code/value</span></span>                                                                                                                                                                                | <span data-ttu-id="415d6-203">Описание</span><span class="sxs-lookup"><span data-stu-id="415d6-203">Description</span></span>                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="415d6-204"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-204"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                                | <span data-ttu-id="415d6-205">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="415d6-205">The method was successful.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="415d6-206"><dt>**Д \_ INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-206"><dt>**E\_INVALIDARG**</dt> <dt>2147942487 (0x80070057)</dt></span></span> </dl>                        | <span data-ttu-id="415d6-207">Параметр *платформвалидатионпрофиле* предоставляется, но его значения не находятся в известном диапазоне или не соответствуют текущему параметру групповая политика.</span><span class="sxs-lookup"><span data-stu-id="415d6-207">The *PlatformValidationProfile* parameter is provided, but its values are not within the known range, or it does not match the Group Policy setting currently in effect.</span></span><br/> |
| <dl> <span data-ttu-id="415d6-208"><dt>**ФВЕ \_ E \_ загрузочная \_ кддвд**</dt> <dt>2150694960 (0x80310030)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-208"><dt>**FVE\_E\_BOOTABLE\_CDDVD**</dt> <dt>2150694960 (0x80310030)</dt></span></span> </dl>              | <span data-ttu-id="415d6-209">На этом компьютере находится загрузочный компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="415d6-209">A bootable CD/DVD is found in this computer.</span></span> <span data-ttu-id="415d6-210">Удалите компакт-диск или диск DVD и перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="415d6-210">Remove the CD/DVD and restart the computer.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="415d6-211"><dt>**ФВЕ \_ E \_ внешний \_ том**</dt> <dt>2150694947 (0x80310023)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-211"><dt>**FVE\_E\_FOREIGN\_VOLUME**</dt> <dt>2150694947 (0x80310023)</dt></span></span> </dl>              | <span data-ttu-id="415d6-212">Доверенный платформенный модуль не может защитить ключ шифрования тома, так как этот том не содержит текущую операционную систему.</span><span class="sxs-lookup"><span data-stu-id="415d6-212">The TPM cannot secure the volume's encryption key because the volume does not contain the currently running operating system.</span></span><br/>                                            |
| <dl> <span data-ttu-id="415d6-213"><dt>**ФВЕ \_ E \_ Недопустимый \_ ПИН-код \_**</dt> <dt>2150695066 (0x8031009A)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-213"><dt>**FVE\_E\_INVALID\_PIN\_CHARS**</dt> <dt>2150695066 (0x8031009A)</dt></span></span> </dl>          | <span data-ttu-id="415d6-214">Параметр *невпин* содержит недопустимые символы.</span><span class="sxs-lookup"><span data-stu-id="415d6-214">The *NewPIN* parameter contains characters that are not valid.</span></span> <span data-ttu-id="415d6-215">При отключении групповая политика "разрешить Расширенные ПИН-коды для запуска" поддерживаются только цифры.</span><span class="sxs-lookup"><span data-stu-id="415d6-215">When the "Allow enhanced PINs for startup" Group Policy is disabled, only numbers are supported.</span></span><br/>          |
| <dl> <span data-ttu-id="415d6-216"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-216"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl>               | <span data-ttu-id="415d6-217">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="415d6-217">The volume is locked.</span></span><br/>                                                                                                                                                    |
| <dl> <span data-ttu-id="415d6-218"><dt>**ФВЕ \_ E \_ Policy \_ Недопустимая \_ \_ длина ПИН-кода**</dt> <dt>2150695016 (0x80310068)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-218"><dt>**FVE\_E\_POLICY\_INVALID\_PIN\_LENGTH**</dt> <dt>2150695016 (0x80310068)</dt></span></span> </dl> | <span data-ttu-id="415d6-219">Предоставленный параметр *невпин* имеет длину более 20 символов, короче 6 символов, или короче минимальной длины, указанной групповая политика.</span><span class="sxs-lookup"><span data-stu-id="415d6-219">The *NewPIN* parameter supplied is either longer than 20 characters, shorter than 6 characters, or shorter than the minimum length specified by Group Policy.</span></span><br/>            |
| <dl> <span data-ttu-id="415d6-220"><dt>**ФВЕ \_ Средство \_ защиты E \_ существует**</dt> <dt>2150694961 (0x80310031)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-220"><dt>**FVE\_E\_PROTECTOR\_EXISTS**</dt> <dt>2150694961 (0x80310031)</dt></span></span> </dl>            | <span data-ttu-id="415d6-221">Предохранитель ключа этого типа уже существует.</span><span class="sxs-lookup"><span data-stu-id="415d6-221">A key protector of this type already exists.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="415d6-222"><dt>**TBS \_ \_Служба E \_ не \_ работает**</dt> <dt>2150121480 (0x80284008)</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-222"><dt>**TBS\_E\_SERVICE\_NOT\_RUNNING**</dt> <dt>2150121480 (0x80284008)</dt></span></span> </dl>        | <span data-ttu-id="415d6-223">На этом компьютере не найден совместимый доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="415d6-223">No compatible TPM is found on this computer.</span></span><br/>                                                                                                                             |



 

## <a name="security-considerations"></a><span data-ttu-id="415d6-224">Соображения безопасности</span><span class="sxs-lookup"><span data-stu-id="415d6-224">Security Considerations</span></span>

<span data-ttu-id="415d6-225">Для обеспечения безопасности компьютера рекомендуется использовать профиль по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="415d6-225">For the security of your computer, we recommend the default profile.</span></span> <span data-ttu-id="415d6-226">Для дополнительной защиты от изменений кода раннего запуска используйте профиль PCRs 0, 2, 4, 5, 8, 9, 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="415d6-226">For additional protection against early startup code changes, use a profile of PCRs 0, 2, 4, 5, 8, 9, 10, and 11.</span></span> <span data-ttu-id="415d6-227">Для дополнительной защиты от изменений в конфигурации с ранним запуском используйте профиль PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span><span class="sxs-lookup"><span data-stu-id="415d6-227">For additional protection against early startup configuration changes, use a profile of PCRs 0, 1, 2, 3, 4, 5, 8, 9, 10, 11.</span></span>

<span data-ttu-id="415d6-228">Изменение профиля по умолчанию влияет на безопасность или удобство использования компьютера.</span><span class="sxs-lookup"><span data-stu-id="415d6-228">Changing from the default profile affects the security or usability of your computer.</span></span>

## <a name="remarks"></a><span data-ttu-id="415d6-229">Комментарии</span><span class="sxs-lookup"><span data-stu-id="415d6-229">Remarks</span></span>

<span data-ttu-id="415d6-230">В любой момент времени может существовать не более одного предохранителя ключа типа "TPM и ПИН-код" для тома.</span><span class="sxs-lookup"><span data-stu-id="415d6-230">At most one key protector of type "TPM And PIN" can exist for a volume at any time.</span></span> <span data-ttu-id="415d6-231">Если вы хотите изменить отображаемое имя или профиль проверки платформы, используемый существующим предохранителем ключа "TPM и ПИН-код", необходимо сначала удалить существующий предохранитель ключа, а затем вызвать **протекткэйвистпмандпин** , чтобы создать новый.</span><span class="sxs-lookup"><span data-stu-id="415d6-231">If you want to change the display name or the platform validation profile used by an existing "TPM And PIN" key protector, you must first remove the existing key protector and then call **ProtectKeyWithTPMAndPIN** to create a new one.</span></span>

<span data-ttu-id="415d6-232">Необходимо указать дополнительные предохранители ключа, чтобы разблокировать том в сценариях восстановления, где невозможно получить доступ к ключу шифрования тома. Например, если доверенный платформенный модуль не может успешно проверить профиль проверки платформы или при потере ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="415d6-232">Additional key protectors should be specified to unlock the volume in recovery scenarios where access to the volume's encryption key cannot be obtained; for example, when the TPM cannot successfully validate against the platform validation profile or when the PIN is lost.</span></span>

<span data-ttu-id="415d6-233">Используйте [**протекткэйвисекстерналкэй**](protectkeywithexternalkey-win32-encryptablevolume.md) или [**протекткэйвиснумерикалпассворд**](protectkeywithnumericalpassword-win32-encryptablevolume.md) , чтобы создать один или несколько предохранителей ключа для восстановления тома, заблокированного иным образом.</span><span class="sxs-lookup"><span data-stu-id="415d6-233">Use [**ProtectKeyWithExternalKey**](protectkeywithexternalkey-win32-encryptablevolume.md) or [**ProtectKeyWithNumericalPassword**](protectkeywithnumericalpassword-win32-encryptablevolume.md) to create one or more key protectors for recovering an otherwise locked volume.</span></span>

<span data-ttu-id="415d6-234">Хотя возможно наличие предохранителя ключа типа "TPM" и другого типа "TPM и ПИН", наличие типа предохранителя ключа "TPM" негативно влияет на влияние других предохранителей ключей на основе доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="415d6-234">While it is possible to have both a key protector of the type "TPM" and another of the type "TPM And PIN", the presence of the "TPM" key protector type negates the effects of other TPM-based key protectors.</span></span>

<span data-ttu-id="415d6-235">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="415d6-235">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="415d6-236">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="415d6-236">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="415d6-237">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="415d6-237">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="415d6-238">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="415d6-238">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="415d6-239">Требования</span><span class="sxs-lookup"><span data-stu-id="415d6-239">Requirements</span></span>



| <span data-ttu-id="415d6-240">Требование</span><span class="sxs-lookup"><span data-stu-id="415d6-240">Requirement</span></span> | <span data-ttu-id="415d6-241">Значение</span><span class="sxs-lookup"><span data-stu-id="415d6-241">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415d6-242">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="415d6-242">Minimum supported client</span></span><br/> | <span data-ttu-id="415d6-243">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="415d6-243">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="415d6-244">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="415d6-244">Minimum supported server</span></span><br/> | <span data-ttu-id="415d6-245">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="415d6-245">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="415d6-246">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="415d6-246">Namespace</span></span><br/>                | <span data-ttu-id="415d6-247">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="415d6-247">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="415d6-248">MOF</span><span class="sxs-lookup"><span data-stu-id="415d6-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="415d6-249"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="415d6-249"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415d6-250">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="415d6-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415d6-251">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="415d6-251">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> <dt>

[<span data-ttu-id="415d6-252">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="415d6-252">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
