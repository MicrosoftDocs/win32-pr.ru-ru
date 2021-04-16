---
description: Содержит сведения о состоянии аппаратного теста полностью расшифрованного тома операционной системы.
ms.assetid: d76bc266-3718-443e-94f9-dcaa0ec53151
title: Метод Жесардваретестстатус класса Win32_EncryptableVolume
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetHardwareTestStatus
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: 26d1984a79edef5f00f7687260fda7b211153863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684067"
---
# <a name="gethardwareteststatus-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="624b6-103">Метод Жесардваретестстатус \_ класса Win32 енкриптаблеволуме</span><span class="sxs-lookup"><span data-stu-id="624b6-103">GetHardwareTestStatus method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="624b6-104">Метод **жесардваретестстатус** класса [**Win32 \_ енкриптаблеволуме**](win32-encryptablevolume.md) предоставляет сведения о состоянии аппаратного теста полностью расшифрованного тома операционной системы.</span><span class="sxs-lookup"><span data-stu-id="624b6-104">The **GetHardwareTestStatus** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class provides status information about a hardware test of a fully decrypted operating system volume.</span></span>

<span data-ttu-id="624b6-105">Используйте этот метод, чтобы определить, ожидает ли тест оборудования, а также успешное или неуспешное выполнение теста оборудования, завершенного на последнем перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="624b6-105">Use this method to show whether a hardware test is pending, as well as the success or failure of a hardware test that completed on the last computer restart.</span></span> <span data-ttu-id="624b6-106">Чтобы запросить тест оборудования, используйте метод [**енкриптафтерхардваретест**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="624b6-106">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="624b6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="624b6-107">Syntax</span></span>


```mof
uint32 GetHardwareTestStatus(
  [out] uint32 TestStatus,
  [out] uint32 TestError
);
```



## <a name="parameters"></a><span data-ttu-id="624b6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="624b6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="624b6-109">*TestStatus* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="624b6-109">*TestStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="624b6-110">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="624b6-110">Type: **uint32**</span></span>

<span data-ttu-id="624b6-111">Указывает, ожидает ли тест оборудования, а также успешное завершение аппаратного теста, завершенного на последнем перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="624b6-111">Specifies whether a hardware test is pending, as well as the success of failure of a hardware test that completed on the last computer restart.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="624b6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-112">Value</span></span></th>
<th><span data-ttu-id="624b6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="NotFailed_and_NonePending"></span><span id="notfailed_and_nonepending"></span><span id="NOTFAILED_AND_NONEPENDING"></span><dl> <span data-ttu-id="624b6-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span><span class="sxs-lookup"><span data-stu-id="624b6-114"><dt><strong>NotFailed_and_NonePending</strong></dt> <dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="624b6-115">Если тест был запрошен, то тест был успешно выполнен на последнем перезапуске компьютера и теперь выполняется шифрование тома.</span><span class="sxs-lookup"><span data-stu-id="624b6-115">If a test was requested, the test has succeeded on the last computer restart and volume encryption is now in progress.</span></span> <span data-ttu-id="624b6-116">Сведения о состоянии шифрования см. в описании метода <a href="getconversionstatus-win32-encryptablevolume.md"><strong>жетконверсионстатус</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="624b6-116">For the encryption status, see the <a href="getconversionstatus-win32-encryptablevolume.md"><strong>GetConversionStatus</strong></a> method.</span></span> <span data-ttu-id="624b6-117">В противном случае тест не выполнялся при последнем перезапуске компьютера, а ожидание отсутствует.</span><span class="sxs-lookup"><span data-stu-id="624b6-117">Otherwise, no test ran on the last computer restart and none is pending.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="Failed"></span><span id="failed"></span><span id="FAILED"></span><dl> <span data-ttu-id="624b6-118"><dt><strong>Сбой</strong></dt> <dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="624b6-118"><dt><strong>Failed</strong></dt> <dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="624b6-119">Шифрование тома не запущено.</span><span class="sxs-lookup"><span data-stu-id="624b6-119">Volume encryption did not start.</span></span> <span data-ttu-id="624b6-120">Все предохранители ключа удалены.</span><span class="sxs-lookup"><span data-stu-id="624b6-120">All key protectors were removed.</span></span><br/> <span data-ttu-id="624b6-121">Чтобы разрешить неудачный тест:</span><span class="sxs-lookup"><span data-stu-id="624b6-121">To resolve a failed test:</span></span><br/>
<ul>
<li><span data-ttu-id="624b6-122">Просмотрите сведения в параметре <em>тестеррор</em> .</span><span class="sxs-lookup"><span data-stu-id="624b6-122">Consult the information in the <em>TestError</em> parameter.</span></span></li>
<li><span data-ttu-id="624b6-123">Добавьте предохранители ключа и снова используйте метод <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>енкриптафтерхардваретест</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="624b6-123">Add key protectors and use the <a href="encryptafterhardwaretest-win32-encryptablevolume.md"><strong>EncryptAfterHardwareTest</strong></a> method again.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="Pending"></span><span id="pending"></span><span id="PENDING"></span><dl> <span data-ttu-id="624b6-124"><dt><strong>Ожидание</strong></dt> <dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="624b6-124"><dt><strong>Pending</strong></dt> <dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="624b6-125">Тест был запрошен и будет выполнен при следующем перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="624b6-125">A test has been requested and will run on the next computer restart.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="624b6-126">*Тестеррор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="624b6-126">*TestError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="624b6-127">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="624b6-127">Type: **uint32**</span></span>

<span data-ttu-id="624b6-128">Указывает ошибку из последней завершенной проверки оборудования.</span><span class="sxs-lookup"><span data-stu-id="624b6-128">Specifies the error from the last completed hardware test.</span></span>



| <span data-ttu-id="624b6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-129">Value</span></span>                                                                                               | <span data-ttu-id="624b6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-130">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="624b6-131"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-131"><dt>0</dt></span></span> </dl>                        | <span data-ttu-id="624b6-132">Ошибок не было, или проверка оборудования не выполнялась при последнем перезапуске компьютера.</span><span class="sxs-lookup"><span data-stu-id="624b6-132">No errors occurred or no hardware test ran on the last computer restart.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="624b6-133"><dt> 2150694972 (0x8031003C)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-133"><dt> 2150694972 (0x8031003C)</dt></span></span> </dl> | <span data-ttu-id="624b6-134">файл ключа ФВЕ \_ E \_ \_ не \_ найден</span><span class="sxs-lookup"><span data-stu-id="624b6-134">FVE\_E\_KEYFILE\_NOT\_FOUND</span></span><br/> <span data-ttu-id="624b6-135">Не найден флэш-накопитель USB с внешним файлом ключа.</span><span class="sxs-lookup"><span data-stu-id="624b6-135">A USB flash drive with an external key file was not found.</span></span> <span data-ttu-id="624b6-136">Если эта ошибка не исчезнет, компьютер не сможет считывать USB-накопители при перезагрузке.</span><span class="sxs-lookup"><span data-stu-id="624b6-136">If this failure persists, the computer cannot read USB drives during restart.</span></span> <span data-ttu-id="624b6-137">Возможно, вы не сможете использовать внешние ключи для разблокировки тома операционной системы во время перезапуска.</span><span class="sxs-lookup"><span data-stu-id="624b6-137">You may not be able to use external keys to unlock the operating system volume during restart.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="624b6-138"><dt> 2150694973 (0x8031003D)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-138"><dt> 2150694973 (0x8031003D)</dt></span></span> </dl> | <span data-ttu-id="624b6-139">Недопустимый файл keyfile ФВЕ \_ E \_ \_</span><span class="sxs-lookup"><span data-stu-id="624b6-139">FVE\_E\_KEYFILE\_INVALID</span></span><br/> <span data-ttu-id="624b6-140">Внешний файл ключа на флэш-накопителе USB поврежден.</span><span class="sxs-lookup"><span data-stu-id="624b6-140">The external key file on the USB flash drive was corrupt.</span></span> <span data-ttu-id="624b6-141">Попробуйте использовать другое устройство флэш-памяти USB для хранения внешнего файла ключа.</span><span class="sxs-lookup"><span data-stu-id="624b6-141">Try a different USB flash drive to store the external key file.</span></span><br/>                                                                                                                                                                                 |
| <dl> <span data-ttu-id="624b6-142"><dt> 2150694975 (0x8031003F)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-142"><dt> 2150694975 (0x8031003F)</dt></span></span> </dl> | <span data-ttu-id="624b6-143">ФВЕ \_ E \_ TPM \_ отключен</span><span class="sxs-lookup"><span data-stu-id="624b6-143">FVE\_E\_TPM\_DISABLED</span></span><br/> <span data-ttu-id="624b6-144">Доверенный платформенный модуль либо отключен, либо деактивирован, либо отключены и деактивированы.</span><span class="sxs-lookup"><span data-stu-id="624b6-144">The TPM is either disabled or deactivated or both disabled and deactivated.</span></span> <span data-ttu-id="624b6-145">Чтобы включить доверенный платформенный модуль, используйте поставщик WMI [**\_ TPM Win32**](win32-tpm.md) или запустите оснастку управления TPM (TPM. msc).</span><span class="sxs-lookup"><span data-stu-id="624b6-145">To turn on the TPM, use the [**Win32\_Tpm**](win32-tpm.md) WMI provider or run the TPM management snap-in (Tpm.msc).</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="624b6-146"><dt> 2150694977 (0x80310041)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-146"><dt> 2150694977 (0x80310041)</dt></span></span> </dl> | <span data-ttu-id="624b6-147">ФВЕ \_ E \_ TPM \_ Недопустимый \_ PCR</span><span class="sxs-lookup"><span data-stu-id="624b6-147">FVE\_E\_TPM\_INVALID\_PCR</span></span><br/> <span data-ttu-id="624b6-148">Доверенный платформенный модуль обнаружил изменение в службах перезапуска операционной системы в текущем профиле проверки платформы.</span><span class="sxs-lookup"><span data-stu-id="624b6-148">The TPM detected a change in operating system restart services within the current platform validation profile.</span></span> <span data-ttu-id="624b6-149">Удалите с компьютера любой загрузочный компакт-диск или DVD-диск.</span><span class="sxs-lookup"><span data-stu-id="624b6-149">Remove any startup CD or DVD from the computer.</span></span> <span data-ttu-id="624b6-150">В случае повторения этой ошибки убедитесь, что установлены последние обновления встроенного по и BIOS, и что TPM работает правильно.</span><span class="sxs-lookup"><span data-stu-id="624b6-150">If this failure persists, check that the latest firmware and BIOS upgrades are installed, and that the TPM is otherwise working properly.</span></span><br/> |
| <dl> <span data-ttu-id="624b6-151"><dt>2150694979 (0x80310043)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-151"><dt>2150694979 (0x80310043)</dt></span></span> </dl>  | <span data-ttu-id="624b6-152">\_ \_ Недопустимый ПИН-код ФВЕ E \_</span><span class="sxs-lookup"><span data-stu-id="624b6-152">FVE\_E\_PIN\_INVALID</span></span><br/> <span data-ttu-id="624b6-153">Указан неправильный ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="624b6-153">The provided PIN was incorrect.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="624b6-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="624b6-154">Return value</span></span>

<span data-ttu-id="624b6-155">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="624b6-155">Type: **uint32**</span></span>

<span data-ttu-id="624b6-156">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="624b6-156">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="624b6-157">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="624b6-157">Return code/value</span></span>                                                                                                                                                                  | <span data-ttu-id="624b6-158">Описание</span><span class="sxs-lookup"><span data-stu-id="624b6-158">Description</span></span>                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="624b6-159"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-159"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                  | <span data-ttu-id="624b6-160">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="624b6-160">The method succeeded.</span></span><br/> |
| <dl> <span data-ttu-id="624b6-161"><dt>**ФВЕ \_ E с \_ заблокированным \_ томом**</dt> <dt>2150694912 (0x80310000)</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-161"><dt>**FVE\_E\_LOCKED\_VOLUME**</dt> <dt>2150694912 (0x80310000)</dt></span></span> </dl> | <span data-ttu-id="624b6-162">Том заблокирован.</span><span class="sxs-lookup"><span data-stu-id="624b6-162">The volume is locked.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="624b6-163">Комментарии</span><span class="sxs-lookup"><span data-stu-id="624b6-163">Remarks</span></span>

<span data-ttu-id="624b6-164">Чтобы запросить тест оборудования, используйте метод [**енкриптафтерхардваретест**](encryptafterhardwaretest-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="624b6-164">To request a hardware test, use the [**EncryptAfterHardwareTest**](encryptafterhardwaretest-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="624b6-165">Чтобы запустить тест оборудования, если его состояние — Ожидание, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="624b6-165">To run a hardware test when its status is pending, follow these steps:</span></span>

1.  <span data-ttu-id="624b6-166">Вставьте в компьютер флэш-накопитель USB, содержащий внешний файл ключа.</span><span class="sxs-lookup"><span data-stu-id="624b6-166">Insert into the computer a USB flash drive that contains an external key file.</span></span> <span data-ttu-id="624b6-167">Этот шаг применяется только в том случае, если том имеет предохранитель ключа типа "внешний ключ" или "TPM и ключ запуска".</span><span class="sxs-lookup"><span data-stu-id="624b6-167">This step applies only if the volume has a key protector of type "External Key" or "TPM And Startup Key".</span></span>
2.  <span data-ttu-id="624b6-168">Перезагрузите компьютер.</span><span class="sxs-lookup"><span data-stu-id="624b6-168">Restart the computer.</span></span> <span data-ttu-id="624b6-169">При перезагрузке компьютера проверка оборудования выполняется автоматически.</span><span class="sxs-lookup"><span data-stu-id="624b6-169">On computer restart, the hardware test runs automatically.</span></span>

<span data-ttu-id="624b6-170">Чтобы отменить проверку оборудования, используйте метод [**Encrypt**](encrypt-win32-encryptablevolume.md) .</span><span class="sxs-lookup"><span data-stu-id="624b6-170">To cancel the hardware test, use the [**Encrypt**](encrypt-win32-encryptablevolume.md) method.</span></span>

<span data-ttu-id="624b6-171">Успешный тест определяет следующее:</span><span class="sxs-lookup"><span data-stu-id="624b6-171">A successful test determines that:</span></span>

-   <span data-ttu-id="624b6-172">Доверенный платформенный модуль может разблокировать том, если существует предохранитель ключа, связанный с TPM.</span><span class="sxs-lookup"><span data-stu-id="624b6-172">The TPM can unlock the volume if a TPM-related key protector exists.</span></span>
-   <span data-ttu-id="624b6-173">Компьютер может прочитать флэш-накопитель USB, содержащий внешний файл ключа, во время запуска, если том может быть разблокирован внешним ключом (включая ключ запуска).</span><span class="sxs-lookup"><span data-stu-id="624b6-173">The computer can read a USB flash drive that contains an external key file during startup if the volume can be unlocked by an external key (including a startup key).</span></span>

<span data-ttu-id="624b6-174">Результаты тестирования оборудования будут недоступны после каких-либо изменений в преобразовании или после перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="624b6-174">Hardware test results will not be available after any changes in conversion or after the next computer restart.</span></span> <span data-ttu-id="624b6-175">Проверьте журнал системных событий на наличие сведений о тестах оборудования, которые ранее выполнялись на компьютере.</span><span class="sxs-lookup"><span data-stu-id="624b6-175">Check the System event log for the information about any hardware tests that previously ran on the computer.</span></span>

<span data-ttu-id="624b6-176">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="624b6-176">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="624b6-177">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="624b6-177">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="624b6-178">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="624b6-178">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="624b6-179">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="624b6-179">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="624b6-180">Требования</span><span class="sxs-lookup"><span data-stu-id="624b6-180">Requirements</span></span>



| <span data-ttu-id="624b6-181">Требование</span><span class="sxs-lookup"><span data-stu-id="624b6-181">Requirement</span></span> | <span data-ttu-id="624b6-182">Значение</span><span class="sxs-lookup"><span data-stu-id="624b6-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="624b6-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="624b6-183">Minimum supported client</span></span><br/> | <span data-ttu-id="624b6-184">Windows Vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]</span><span class="sxs-lookup"><span data-stu-id="624b6-184">Windows Vista Enterprise, Windows Vista Ultimate \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="624b6-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="624b6-185">Minimum supported server</span></span><br/> | <span data-ttu-id="624b6-186">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="624b6-186">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="624b6-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="624b6-187">Namespace</span></span><br/>                | <span data-ttu-id="624b6-188">Корневой \\ CIMV2 \\ безопасности \\ микрософтволуминкриптион</span><span class="sxs-lookup"><span data-stu-id="624b6-188">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="624b6-189">MOF</span><span class="sxs-lookup"><span data-stu-id="624b6-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="624b6-190"><dt>Win32 \_ енкриптаблеволуме. mof</dt></span><span class="sxs-lookup"><span data-stu-id="624b6-190"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="624b6-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="624b6-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="624b6-192">**\_Енкриптаблеволуме Win32**</span><span class="sxs-lookup"><span data-stu-id="624b6-192">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 
