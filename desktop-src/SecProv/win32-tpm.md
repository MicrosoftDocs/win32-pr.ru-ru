---
description: Представляет доверенный платформенный модуль (TPM) (доверенный платформенный модуль), микросхема безопасности оборудования, которая предоставляет корень доверия для компьютерной системы.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Класс Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664215"
---
# <a name="win32_tpm-class"></a><span data-ttu-id="77509-103">\_Класс TPM Win32</span><span class="sxs-lookup"><span data-stu-id="77509-103">Win32\_Tpm class</span></span>

<span data-ttu-id="77509-104">Класс **\_ TPM Win32** представляет доверенный платформенный модуль (TPM) (доверенный платформенный модуль), микросхема безопасности оборудования, которая предоставляет корень доверия для компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="77509-104">The **Win32\_Tpm** class represents the Trusted Platform Module (TPM), a hardware security chip that provides a root of trust for a computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="77509-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="77509-105">Syntax</span></span>

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a><span data-ttu-id="77509-106">Члены</span><span class="sxs-lookup"><span data-stu-id="77509-106">Members</span></span>

<span data-ttu-id="77509-107">Класс **\_ TPM Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="77509-107">The **Win32\_Tpm** class has these types of members:</span></span>

-   [<span data-ttu-id="77509-108">Методы</span><span class="sxs-lookup"><span data-stu-id="77509-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="77509-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="77509-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77509-110">Методы</span><span class="sxs-lookup"><span data-stu-id="77509-110">Methods</span></span>

<span data-ttu-id="77509-111">Класс **\_ TPM Win32** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="77509-111">The **Win32\_Tpm** class has these methods.</span></span>



| <span data-ttu-id="77509-112">Метод</span><span class="sxs-lookup"><span data-stu-id="77509-112">Method</span></span>                                                                                   | <span data-ttu-id="77509-113">Описание</span><span class="sxs-lookup"><span data-stu-id="77509-113">Description</span></span>                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="77509-114">**аддблоккедкомманд**</span><span class="sxs-lookup"><span data-stu-id="77509-114">**AddBlockedCommand**</span></span>](addblockedcommand-win32-tpm.md)                                 | <span data-ttu-id="77509-115">Добавляет команду доверенного платформенного модуля в локальный список команд, заблокированных в Windows.</span><span class="sxs-lookup"><span data-stu-id="77509-115">Adds a TPM command to the local list of commands blocked on Windows.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="77509-116">**чанжеовнераус**</span><span class="sxs-lookup"><span data-stu-id="77509-116">**ChangeOwnerAuth**</span></span>](changeownerauth-win32-tpm.md)                                     | <span data-ttu-id="77509-117">Изменяет значение авторизации владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-117">Changes the TPM owner authorization value.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="77509-118">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="77509-118">**Clear**</span></span>](clear-win32-tpm.md)                                                         | <span data-ttu-id="77509-119">Сбрасывает доверенный платформенный модуль до заводских состояний по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="77509-119">Resets the TPM to its factory-default state.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="77509-120">**конверттувнераус**</span><span class="sxs-lookup"><span data-stu-id="77509-120">**ConvertToOwnerAuth**</span></span>](converttoownerauth-win32-tpm.md)                               | <span data-ttu-id="77509-121">Преобразует предоставленную пользователем парольную фразу в значение авторизации владельца в 20 байт, которое может использоваться для взаимодействия с доверенным платформенным модулем.</span><span class="sxs-lookup"><span data-stu-id="77509-121">Converts a user-provided passphrase to a 20-byte owner authorization value that can be used to interact with the TPM.</span></span><br/>                                                            |
| [<span data-ttu-id="77509-122">**креатиндорсементкэйпаир**</span><span class="sxs-lookup"><span data-stu-id="77509-122">**CreateEndorsementKeyPair**</span></span>](createendorsementkeypair-win32-tpm.md)                   | <span data-ttu-id="77509-123">Создает 2048-разрядную пару ключей подтверждения в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="77509-123">Creates a 2048-bit endorsement key pair on the TPM.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="77509-124">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="77509-124">**Disable**</span></span>](disable-win32-tpm.md)                                                     | <span data-ttu-id="77509-125">Позволяет владельцу доверенного платформенного модуля отключить доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-125">Allows the TPM owner to disable the TPM.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="77509-126">**Включить**</span><span class="sxs-lookup"><span data-stu-id="77509-126">**Enable**</span></span>](enable-win32-tpm.md)                                                       | <span data-ttu-id="77509-127">Позволяет владельцу доверенного платформенного модуля включить доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-127">Allows the TPM owner to enable the TPM.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="77509-128">**жетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="77509-128">**GetPhysicalPresenceRequest**</span></span>](getphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="77509-129">Возвращает и возвращает ожидаемую операцию физического присутствия доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-129">Gets and returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="77509-130">Используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) для запроса операции.</span><span class="sxs-lookup"><span data-stu-id="77509-130">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span><br/> |
| [<span data-ttu-id="77509-131">**жетфисикалпресенцереспонсе**</span><span class="sxs-lookup"><span data-stu-id="77509-131">**GetPhysicalPresenceResponse**</span></span>](getphysicalpresenceresponse-win32-tpm.md)             | <span data-ttu-id="77509-132">Возвращает и возвращает результаты выполнения операции физического присутствия доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-132">Gets and returns the results from a TPM physical presence operation that was performed.</span></span><br/>                                                                                          |
| [<span data-ttu-id="77509-133">**жетфисикалпресенцетранситион**</span><span class="sxs-lookup"><span data-stu-id="77509-133">**GetPhysicalPresenceTransition**</span></span>](getphysicalpresencetransition-win32-tpm.md)         | <span data-ttu-id="77509-134">Указывает действие пользователя, необходимое для выполнения операции физического присутствия TPM.</span><span class="sxs-lookup"><span data-stu-id="77509-134">Indicates the user action that is needed to perform a TPM physical presence operation.</span></span><br/>                                                                                           |
| [<span data-ttu-id="77509-135">**Активируется**</span><span class="sxs-lookup"><span data-stu-id="77509-135">**IsActivated**</span></span>](isactivated-win32-tpm.md)                                             | <span data-ttu-id="77509-136">Указывает, активирован ли доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-136">Indicates whether the TPM is activated.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="77509-137">**искоммандблоккед**</span><span class="sxs-lookup"><span data-stu-id="77509-137">**IsCommandBlocked**</span></span>](iscommandblocked-win32-tpm.md)                                   | <span data-ttu-id="77509-138">Указывает, может ли команда доверенного платформенного модуля запускаться в этой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="77509-138">Indicates whether the TPM command can run on this operating system.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="77509-139">**искоммандпресент**</span><span class="sxs-lookup"><span data-stu-id="77509-139">**IsCommandPresent**</span></span>](iscommandpresent-win32-tpm.md)                                   | <span data-ttu-id="77509-140">Указывает, поддерживается ли команда TPM этим компьютером.</span><span class="sxs-lookup"><span data-stu-id="77509-140">Indicates whether a TPM command is supported by this computer.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="77509-141">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="77509-141">**IsEnabled**</span></span>](isenabled-win32-tpm.md)                                                 | <span data-ttu-id="77509-142">Указывает, включен ли доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-142">Indicates whether the TPM is enabled.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="77509-143">**исендорсементкэйпаирпресент**</span><span class="sxs-lookup"><span data-stu-id="77509-143">**IsEndorsementKeyPairPresent**</span></span>](isendorsementkeypairpresent-win32-tpm.md)             | <span data-ttu-id="77509-144">Указывает, имеет ли TPM пару ключей подтверждения.</span><span class="sxs-lookup"><span data-stu-id="77509-144">Indicates whether the TPM has an endorsement key pair.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="77509-145">**Владелец**</span><span class="sxs-lookup"><span data-stu-id="77509-145">**IsOwned**</span></span>](isowned-win32-tpm.md)                                                     | <span data-ttu-id="77509-146">Указывает, имеет ли TPM владелец.</span><span class="sxs-lookup"><span data-stu-id="77509-146">Indicates whether the TPM has an owner.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="77509-147">**исовнерклеардисаблед**</span><span class="sxs-lookup"><span data-stu-id="77509-147">**IsOwnerClearDisabled**</span></span>](isownercleardisabled-win32-tpm.md)                           | <span data-ttu-id="77509-148">Указывает, может ли владелец доверенного платформенного модуля очищать доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-148">Indicates whether the TPM owner can clear the TPM.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="77509-149">**исовнершипалловед**</span><span class="sxs-lookup"><span data-stu-id="77509-149">**IsOwnershipAllowed**</span></span>](isownershipallowed-win32-tpm.md)                               | <span data-ttu-id="77509-150">Указывает, можно ли установить владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-150">Indicates whether a TPM owner can be installed.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="77509-151">**исфисикалклеардисаблед**</span><span class="sxs-lookup"><span data-stu-id="77509-151">**IsPhysicalClearDisabled**</span></span>](isphysicalcleardisabled-win32-tpm.md)                     | <span data-ttu-id="77509-152">Указывает, может ли операция физического присутствия доверенного платформенного модуля очистить доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-152">Indicates whether a TPM physical presence operation can clear the TPM.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="77509-153">**исфисикалпресенцехардваринаблед**</span><span class="sxs-lookup"><span data-stu-id="77509-153">**IsPhysicalPresenceHardwareEnabled**</span></span>](isphysicalpresencehardwareenabled-win32-tpm.md) | <span data-ttu-id="77509-154">Указывает, поддерживает ли этот компьютер выделенный аппаратный путь для сигнала физического присутствия.</span><span class="sxs-lookup"><span data-stu-id="77509-154">Indicates whether this computer supports a dedicated hardware path to signal physical presence.</span></span><br/>                                                                                  |
| [<span data-ttu-id="77509-155">**иссркаускомпатибле**</span><span class="sxs-lookup"><span data-stu-id="77509-155">**IsSrkAuthCompatible**</span></span>](issrkauthcompatible-win32-tpm.md)                             | <span data-ttu-id="77509-156">Указывает, совместима ли авторизация корневого ключа хранилища (SRK) с Windows.</span><span class="sxs-lookup"><span data-stu-id="77509-156">Indicates whether the Storage Root Key (SRK) authorization is compatible with Windows.</span></span><br/>                                                                                           |
| [<span data-ttu-id="77509-157">**ремовеблоккедкомманд**</span><span class="sxs-lookup"><span data-stu-id="77509-157">**RemoveBlockedCommand**</span></span>](removeblockedcommand-win32-tpm.md)                           | <span data-ttu-id="77509-158">Удаляет команду доверенного платформенного модуля из локального списка команд, заблокированных Windows.</span><span class="sxs-lookup"><span data-stu-id="77509-158">Removes a TPM command from the local list of commands blocked by Windows.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="77509-159">**ресетауслоккаут**</span><span class="sxs-lookup"><span data-stu-id="77509-159">**ResetAuthLockOut**</span></span>](resetauthlockout-win32-tpm.md)                                   | <span data-ttu-id="77509-160">Сбрасывает период ожидания или другой механизм, реализуемый производителями TPM для защиты от атак из словарей в доверенном платформенном модуле.</span><span class="sxs-lookup"><span data-stu-id="77509-160">Resets the time-out period or other mechanism that TPM manufacturers implement to protect against dictionary attacks on the TPM.</span></span><br/>                                                 |
| [<span data-ttu-id="77509-161">**ресетсркаус**</span><span class="sxs-lookup"><span data-stu-id="77509-161">**ResetSrkAuth**</span></span>](resetsrkauth-win32-tpm.md)                                           | <span data-ttu-id="77509-162">Сбрасывает значение авторизации корневого ключа хранилища (SRK) для совместимости с Windows.</span><span class="sxs-lookup"><span data-stu-id="77509-162">Resets the Storage Root Key (SRK) authorization value to be compatible with Windows.</span></span><br/>                                                                                             |
| [<span data-ttu-id="77509-163">**SelfTest**</span><span class="sxs-lookup"><span data-stu-id="77509-163">**SelfTest**</span></span>](selftest-win32-tpm.md)                                                   | <span data-ttu-id="77509-164">Выполняет самотестирование TPM и возвращает результат.</span><span class="sxs-lookup"><span data-stu-id="77509-164">Performs a self-test of the TPM and returns the result.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="77509-165">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="77509-165">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)               | <span data-ttu-id="77509-166">Запрашивает выполнение операции физического присутствия TPM.</span><span class="sxs-lookup"><span data-stu-id="77509-166">Requests a TPM physical presence operation to run.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="77509-167">**TakeOwnership**</span><span class="sxs-lookup"><span data-stu-id="77509-167">**TakeOwnership**</span></span>](takeownership-win32-tpm.md)                                         | <span data-ttu-id="77509-168">Устанавливает владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-168">Installs an owner for the TPM.</span></span><br/>                                                                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="77509-169">Свойства</span><span class="sxs-lookup"><span data-stu-id="77509-169">Properties</span></span>

<span data-ttu-id="77509-170">Класс **\_ TPM Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="77509-170">The **Win32\_Tpm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="77509-171">**\_Инитиалвалуе**</span><span class="sxs-lookup"><span data-stu-id="77509-171">**IsActivated\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77509-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77509-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-174">Указывает, активирован ли доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-174">Indicates whether the TPM is activated.</span></span>

<span data-ttu-id="77509-175">**значение true** , если устройство активировано (то есть если **\_ инитиалвалуе** имеет значение true); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="77509-175">**true** if the device is activated (that is, if **IsActivated\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="77509-176">Это значение сохраняется при создании экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="77509-176">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="77509-177">Доверенный платформенный модуль может изменять состояние между созданием экземпляра и при проверке этого значения.</span><span class="sxs-lookup"><span data-stu-id="77509-177">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="77509-178">Чтобы проверить, активирован ли доверенный платформенный модуль в режиме реального времени, используйте метод [**Activate**](isactivated-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="77509-178">To check whether the TPM is activated in real time, use the [**IsActivated**](isactivated-win32-tpm.md) method.</span></span>

<span data-ttu-id="77509-179">**Windows Server 2008 и Windows Vista:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="77509-179">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="77509-180">**Включенный \_ инитиалвалуе**</span><span class="sxs-lookup"><span data-stu-id="77509-180">**IsEnabled\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-181">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77509-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77509-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-182">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-183">Указывает, включен ли доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="77509-183">Indicates whether the TPM is enabled.</span></span>

<span data-ttu-id="77509-184">**значение true** , если устройство включено (то есть если параметр **\_ инитиалвалуе** имеет значение true); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="77509-184">**true** if the device is enabled (that is, if **IsEnabled\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="77509-185">Это значение сохраняется при создании экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="77509-185">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="77509-186">Доверенный платформенный модуль может изменять состояние между созданием экземпляра и при проверке этого значения.</span><span class="sxs-lookup"><span data-stu-id="77509-186">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="77509-187">Чтобы проверить, включен ли доверенный платформенный модуль в режиме реального времени, используйте метод, [**включенный**](isenabled-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="77509-187">To check whether the TPM is enabled in real time, use the [**IsEnabled**](isenabled-win32-tpm.md) method.</span></span>

<span data-ttu-id="77509-188">**Windows Server 2008 и Windows Vista:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="77509-188">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="77509-189">**Владелец \_ инитиалвалуе**</span><span class="sxs-lookup"><span data-stu-id="77509-189">**IsOwned\_InitialValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-190">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="77509-190">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="77509-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-192">Указывает, имеет ли TPM владелец.</span><span class="sxs-lookup"><span data-stu-id="77509-192">Indicates whether the TPM has an owner.</span></span>

<span data-ttu-id="77509-193">**значение true** , если у устройства есть владелец (то есть если **\_ инитиалвалуе** имеет значение true); в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="77509-193">**true** if the device has an owner (that is, if **IsOwned\_InitialValue** is true); otherwise, **false**.</span></span>

<span data-ttu-id="77509-194">Это значение сохраняется при создании экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="77509-194">This value is stored when the class is instantiated.</span></span> <span data-ttu-id="77509-195">Доверенный платформенный модуль может изменять состояние между созданием экземпляра и при проверке этого значения.</span><span class="sxs-lookup"><span data-stu-id="77509-195">It is possible for the TPM to change state between the instantiation and when you check this value.</span></span> <span data-ttu-id="77509-196">Чтобы проверить, владеет ли TPM в режиме реального времени, используйте метод, [**принадлежащий**](isowned-win32-tpm.md) .</span><span class="sxs-lookup"><span data-stu-id="77509-196">To check whether the TPM is owned in real time, use the [**IsOwned**](isowned-win32-tpm.md) method.</span></span>

<span data-ttu-id="77509-197">**Windows Server 2008 и Windows Vista:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="77509-197">**Windows Server 2008 and Windows Vista:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="77509-198">**мануфактурерид**</span><span class="sxs-lookup"><span data-stu-id="77509-198">**ManufacturerId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-199">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="77509-199">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="77509-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-201">Идентифицирующие сведения, которые уникально называет изготовителя TPM.</span><span class="sxs-lookup"><span data-stu-id="77509-201">The identifying information that uniquely names the TPM manufacturer.</span></span>

<span data-ttu-id="77509-202">Если данные недоступны, возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="77509-202">When the data is unavailable, zero is returned.</span></span>

<span data-ttu-id="77509-203">Это целое значение может быть преобразовано в строковое значение путем интерпретации каждого байта как символа ASCII.</span><span class="sxs-lookup"><span data-stu-id="77509-203">This integer value can be translated to a string value by interpreting each byte as an ASCII character.</span></span> <span data-ttu-id="77509-204">Например, целочисленное значение 1414548736 можно разделить на следующие 4 байта: 0x54, 0x50, 0x4D и 0x00.</span><span class="sxs-lookup"><span data-stu-id="77509-204">For example, an integer value of 1414548736 can be divided into these 4 bytes: 0x54, 0x50, 0x4D, and 0x00.</span></span> <span data-ttu-id="77509-205">Предполагая, что строка интерпретируется слева направо, это целочисленное значение преобразуется в строковое значение "TPM".</span><span class="sxs-lookup"><span data-stu-id="77509-205">Assuming the string is interpreted from left to right, this integer value translated to a string value of "TPM".</span></span>

</dd> <dt>

<span data-ttu-id="77509-206">**мануфактурерверсион**</span><span class="sxs-lookup"><span data-stu-id="77509-206">**ManufacturerVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-207">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77509-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77509-208">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-209">Версия TPM, указанная производителем.</span><span class="sxs-lookup"><span data-stu-id="77509-209">The version of the TPM, as specified by the manufacturer.</span></span>

<span data-ttu-id="77509-210">Если данные недоступны, возвращается значение «не поддерживается».</span><span class="sxs-lookup"><span data-stu-id="77509-210">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="77509-211">**мануфактурерверсионинфо**</span><span class="sxs-lookup"><span data-stu-id="77509-211">**ManufacturerVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-212">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77509-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77509-213">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-214">Другие сведения о версии для TPM, зависящие от производителя.</span><span class="sxs-lookup"><span data-stu-id="77509-214">Other manufacturer-specific version information for the TPM.</span></span>

<span data-ttu-id="77509-215">Если данные недоступны, возвращается значение «не поддерживается».</span><span class="sxs-lookup"><span data-stu-id="77509-215">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="77509-216">**фисикалпресенцеверсионинфо**</span><span class="sxs-lookup"><span data-stu-id="77509-216">**PhysicalPresenceVersionInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-217">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77509-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77509-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-219">Версия интерфейса физического присутствия — механизм связи, используемый для выполнения операций с устройством, требующих физического присутствия, которые поддерживает компьютер.</span><span class="sxs-lookup"><span data-stu-id="77509-219">The version of the Physical Presence Interface, a communication mechanism used to run device operations that require physical presence, that the computer supports.</span></span>

<span data-ttu-id="77509-220">Этот интерфейс должен быть доступен для выполнения операций физического присутствия доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="77509-220">This interface must be available to run TPM physical presence operations.</span></span> <span data-ttu-id="77509-221">Методы **\_ TPM Win32** [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md), [**жетфисикалпресенцерекуест**](getphysicalpresencerequest-win32-tpm.md), [**жетфисикалпресенцетранситион**](getphysicalpresencetransition-win32-tpm.md)и [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) предоставляют возможности интерфейса физического присутствия.</span><span class="sxs-lookup"><span data-stu-id="77509-221">The **Win32\_Tpm** methods [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md), and [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) expose the capabilities of the Physical Presence Interface.</span></span>

<span data-ttu-id="77509-222">Если данные недоступны, возвращается значение «не поддерживается».</span><span class="sxs-lookup"><span data-stu-id="77509-222">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> <dt>

<span data-ttu-id="77509-223">**спекверсион**</span><span class="sxs-lookup"><span data-stu-id="77509-223">**SpecVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="77509-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="77509-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="77509-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="77509-225">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="77509-226">Версия спецификации организация TCG (TCG), которую поддерживает TPM.</span><span class="sxs-lookup"><span data-stu-id="77509-226">The version of the Trusted Computing Group (TCG) specification that the TPM supports.</span></span> <span data-ttu-id="77509-227">Это значение включает в себя основную и дополнительную версию спецификации TCG, уровень редакции спецификации и уровень редакции ошибок.</span><span class="sxs-lookup"><span data-stu-id="77509-227">This value includes the major and minor TCG specification version, the specification revision level, and the errata revision level.</span></span> <span data-ttu-id="77509-228">Все значения указаны в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="77509-228">All values are in hexadecimal.</span></span> <span data-ttu-id="77509-229">Например, информация о версии "1,2, 2, 0" указывает на то, что устройство было применено к спецификации TCG версии 1,2, версии 2 и без ошибок.</span><span class="sxs-lookup"><span data-stu-id="77509-229">For example, a version information of "1.2, 2, 0" indicates that the device was implemented to TCG specification version 1.2, revision level 2, and with no errata.</span></span>

<span data-ttu-id="77509-230">Если данные недоступны, возвращается значение «не поддерживается».</span><span class="sxs-lookup"><span data-stu-id="77509-230">When the data is unavailable, "Not Supported" is returned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77509-231">Комментарии</span><span class="sxs-lookup"><span data-stu-id="77509-231">Remarks</span></span>

<span data-ttu-id="77509-232">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="77509-232">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="77509-233">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="77509-233">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="77509-234">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="77509-234">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="77509-235">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="77509-235">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77509-236">Требования</span><span class="sxs-lookup"><span data-stu-id="77509-236">Requirements</span></span>



| <span data-ttu-id="77509-237">Требование</span><span class="sxs-lookup"><span data-stu-id="77509-237">Requirement</span></span> | <span data-ttu-id="77509-238">Значение</span><span class="sxs-lookup"><span data-stu-id="77509-238">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="77509-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77509-239">Minimum supported client</span></span><br/> | <span data-ttu-id="77509-240">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77509-240">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="77509-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77509-241">Minimum supported server</span></span><br/> | <span data-ttu-id="77509-242">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="77509-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="77509-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="77509-243">Namespace</span></span><br/>                | <span data-ttu-id="77509-244">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="77509-244">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="77509-245">MOF</span><span class="sxs-lookup"><span data-stu-id="77509-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="77509-246"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="77509-246"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="77509-247">DLL</span><span class="sxs-lookup"><span data-stu-id="77509-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77509-248"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="77509-248"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



 

 
