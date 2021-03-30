---
description: Указывает, требуется ли подтверждение от физически присутствующего пользователя для данной операции физического присутствия.
ms.assetid: 1CE558B7-EB6F-42CB-B52B-2A0101E90BD5
title: 'Метод Win32_Tpm:: Жетфисикалпресенцеконфирматионстатус'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceConfirmationStatus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 61dc2798973a82cfc75c803f2bf8307c8a43b3c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998882"
---
# <a name="win32_tpmgetphysicalpresenceconfirmationstatus-method"></a><span data-ttu-id="c16b1-103">\_Метод Win32 TPM:: жетфисикалпресенцеконфирматионстатус</span><span class="sxs-lookup"><span data-stu-id="c16b1-103">Win32\_Tpm::GetPhysicalPresenceConfirmationStatus method</span></span>

<span data-ttu-id="c16b1-104">Указывает, требуется ли подтверждение от физически присутствующего пользователя для данной операции физического присутствия.</span><span class="sxs-lookup"><span data-stu-id="c16b1-104">Indicates if confirmation from a physically present user is required for a given physical presence operation.</span></span>

<span data-ttu-id="c16b1-105">Этот метод доступен только локальным администраторам.</span><span class="sxs-lookup"><span data-stu-id="c16b1-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="c16b1-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c16b1-106">Syntax</span></span>


```C++
uint32 GetPhysicalPresenceConfirmationStatus(
  [in]  uint32 Operation,
  [out] uint32 ConfirmationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="c16b1-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c16b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c16b1-108">*Операция* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c16b1-108">*Operation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c16b1-109">Целочисленное значение, указывающее запрошенную операцию TPM, для которой требуется физическое присутствие.</span><span class="sxs-lookup"><span data-stu-id="c16b1-109">An integer value that specifies the requested TPM operation that requires physical presence.</span></span> <span data-ttu-id="c16b1-110">Также поддерживаются команды, относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="c16b1-110">Vendor specific commands are supported as well.</span></span>

<span data-ttu-id="c16b1-111">Параметр *операции* может состоять из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c16b1-111">The *Operation* parameter may consist of the following values.</span></span>



| <span data-ttu-id="c16b1-112">Значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-112">Value</span></span>                                                                                                                               | <span data-ttu-id="c16b1-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-113">Meaning</span></span>                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c16b1-114"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-114"><dt>1</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-115">Включить</span><span class="sxs-lookup"><span data-stu-id="c16b1-115">Enable</span></span><br/>                                        |
| <dl> <span data-ttu-id="c16b1-116"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-116"><dt>2</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-117">Отключить</span><span class="sxs-lookup"><span data-stu-id="c16b1-117">Disable</span></span><br/>                                       |
| <dl> <span data-ttu-id="c16b1-118"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-118"><dt>3</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-119">Активировать</span><span class="sxs-lookup"><span data-stu-id="c16b1-119">Activate</span></span><br/>                                      |
| <dl> <span data-ttu-id="c16b1-120"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-120"><dt>4</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-121">Отключение</span><span class="sxs-lookup"><span data-stu-id="c16b1-121">Deactivate</span></span><br/>                                    |
| <dl> <span data-ttu-id="c16b1-122"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-122"><dt>5</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-123">Clear</span><span class="sxs-lookup"><span data-stu-id="c16b1-123">Clear</span></span><br/>                                         |
| <dl> <span data-ttu-id="c16b1-124"><dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-124"><dt>6</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-125">Включить + активировать</span><span class="sxs-lookup"><span data-stu-id="c16b1-125">Enable + Activate</span></span><br/>                             |
| <dl> <span data-ttu-id="c16b1-126"><dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-126"><dt>7</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-127">Деактивировать и отключить</span><span class="sxs-lookup"><span data-stu-id="c16b1-127">Deactivate + Disable</span></span><br/>                          |
| <dl> <span data-ttu-id="c16b1-128"><dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-128"><dt>8</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-129">Сетовнеринсталл \_ true</span><span class="sxs-lookup"><span data-stu-id="c16b1-129">SetOwnerInstall\_True</span></span><br/>                         |
| <dl> <span data-ttu-id="c16b1-130"><dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-130"><dt>9</dt></span></span> </dl>                                                        | <span data-ttu-id="c16b1-131">Сетовнеринсталл \_ false</span><span class="sxs-lookup"><span data-stu-id="c16b1-131">SetOwnerInstall\_False</span></span><br/>                        |
| <dl> <span data-ttu-id="c16b1-132"><dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-132"><dt>10</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-133">Включить + активировать + Сетовнеринсталл \_ true</span><span class="sxs-lookup"><span data-stu-id="c16b1-133">Enable + Activate + SetOwnerInstall\_True</span></span><br/>     |
| <dl> <span data-ttu-id="c16b1-134"><dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-134"><dt>11</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-135">Сетовнеринсталл \_ false + деактивация + отключить</span><span class="sxs-lookup"><span data-stu-id="c16b1-135">SetOwnerInstall\_False + Deactivate + Disable</span></span><br/> |
| <dl> <span data-ttu-id="c16b1-136"><dt></dt><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-136"><dt></dt> <dt>12</dt></span></span> </dl> | <span data-ttu-id="c16b1-137">Отложенная физическая Пресенцеуновнедфиелдупграде</span><span class="sxs-lookup"><span data-stu-id="c16b1-137">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> |
| <dl> <span data-ttu-id="c16b1-138"><dt></dt><dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-138"><dt></dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="c16b1-139">Clear + включить + активировать</span><span class="sxs-lookup"><span data-stu-id="c16b1-139">Clear + Enable + Activate</span></span><br/>                     |
| <dl> <span data-ttu-id="c16b1-140"><dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-140"><dt>15</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-141">Сетноппипровисион \_ false</span><span class="sxs-lookup"><span data-stu-id="c16b1-141">SetNoPPIProvision\_False</span></span><br/>                      |
| <dl> <span data-ttu-id="c16b1-142"><dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-142"><dt>16</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-143">Сетноппипровисион \_ true</span><span class="sxs-lookup"><span data-stu-id="c16b1-143">SetNoPPIProvision\_True</span></span><br/>                       |
| <dl> <span data-ttu-id="c16b1-144"><dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-144"><dt>17</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-145">Сетноппиклеар \_ false</span><span class="sxs-lookup"><span data-stu-id="c16b1-145">SetNoPPIClear\_False</span></span><br/>                          |
| <dl> <span data-ttu-id="c16b1-146"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-146"><dt>18</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-147">Сетноппиклеар \_ true</span><span class="sxs-lookup"><span data-stu-id="c16b1-147">SetNoPPIClear\_True</span></span><br/>                           |
| <dl> <span data-ttu-id="c16b1-148"><dt>стр</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-148"><dt>19</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-149">Сетноппимаинтенанце \_ false</span><span class="sxs-lookup"><span data-stu-id="c16b1-149">SetNoPPIMaintenance\_False</span></span><br/>                    |
| <dl> <span data-ttu-id="c16b1-150"><dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-150"><dt>20</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-151">Сетноппимаинтенанце \_ true</span><span class="sxs-lookup"><span data-stu-id="c16b1-151">SetNoPPIMaintenance\_True</span></span><br/>                     |
| <dl> <span data-ttu-id="c16b1-152"><dt>открыт</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-152"><dt>21</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-153">Включить + активировать + очистить</span><span class="sxs-lookup"><span data-stu-id="c16b1-153">Enable + Activate + Clear</span></span><br/>                     |
| <dl> <span data-ttu-id="c16b1-154"><dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-154"><dt>22</dt></span></span> </dl>                                                       | <span data-ttu-id="c16b1-155">Включить + активировать + очистить + включить + активировать</span><span class="sxs-lookup"><span data-stu-id="c16b1-155">Enable + Activate + Clear + Enable + Activate</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c16b1-156">*Конфирматионстатус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c16b1-156">*ConfirmationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c16b1-157">Возвращает состояние подтверждения для команды физического присутствия.</span><span class="sxs-lookup"><span data-stu-id="c16b1-157">Returns the confirmation status for physical presence command.</span></span>

<span data-ttu-id="c16b1-158">Параметр *конфирматионстатус* может состоять из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c16b1-158">The *ConfirmationStatus* parameter may consist of the following values.</span></span>



| <span data-ttu-id="c16b1-159">Значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-159">Value</span></span>                                                                        | <span data-ttu-id="c16b1-160">Значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-160">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c16b1-161"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-161"><dt>0</dt></span></span> </dl> | <span data-ttu-id="c16b1-162">Не реализовано</span><span class="sxs-lookup"><span data-stu-id="c16b1-162">Not implemented</span></span><br/>                                             |
| <dl> <span data-ttu-id="c16b1-163"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-163"><dt>1</dt></span></span> </dl> | <span data-ttu-id="c16b1-164">Только BIOS.</span><span class="sxs-lookup"><span data-stu-id="c16b1-164">BIOS only.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="c16b1-165"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-165"><dt>2</dt></span></span> </dl> | <span data-ttu-id="c16b1-166">Заблокировано для операционной системы в конфигурации BIOS.</span><span class="sxs-lookup"><span data-stu-id="c16b1-166">Blocked for the operating system by the BIOS configuration.</span></span><br/> |
| <dl> <span data-ttu-id="c16b1-167"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-167"><dt>3</dt></span></span> </dl> | <span data-ttu-id="c16b1-168">Разрешенные и физически существующие пользователи должны быть обязательными.</span><span class="sxs-lookup"><span data-stu-id="c16b1-168">Allowed and physically present user required.</span></span><br/>               |
| <dl> <span data-ttu-id="c16b1-169"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-169"><dt>4</dt></span></span> </dl> | <span data-ttu-id="c16b1-170">Разрешенные и физически существующие пользователи не требуются</span><span class="sxs-lookup"><span data-stu-id="c16b1-170">Allowed and physically present user not required</span></span><br/>            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c16b1-171">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-171">Return value</span></span>

<span data-ttu-id="c16b1-172">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к [базовым службам TPM](../tbs/tbs-return-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c16b1-172">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="c16b1-173">Ниже приведены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="c16b1-173">Common return codes are listed below.</span></span>



| <span data-ttu-id="c16b1-174">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-174">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="c16b1-175">Описание</span><span class="sxs-lookup"><span data-stu-id="c16b1-175">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="c16b1-176"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-176"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="c16b1-177">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="c16b1-177">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c16b1-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c16b1-178">Remarks</span></span>

<span data-ttu-id="c16b1-179">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="c16b1-179">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="c16b1-180">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="c16b1-180">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="c16b1-181">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="c16b1-181">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="c16b1-182">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="c16b1-182">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c16b1-183">Требования</span><span class="sxs-lookup"><span data-stu-id="c16b1-183">Requirements</span></span>



| <span data-ttu-id="c16b1-184">Требование</span><span class="sxs-lookup"><span data-stu-id="c16b1-184">Requirement</span></span> | <span data-ttu-id="c16b1-185">Значение</span><span class="sxs-lookup"><span data-stu-id="c16b1-185">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="c16b1-186">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c16b1-186">Minimum supported client</span></span><br/> | <span data-ttu-id="c16b1-187">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="c16b1-187">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c16b1-188">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c16b1-188">Minimum supported server</span></span><br/> | <span data-ttu-id="c16b1-189">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="c16b1-189">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="c16b1-190">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c16b1-190">Namespace</span></span><br/>                | <span data-ttu-id="c16b1-191">\\\\.\\ корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="c16b1-191">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="c16b1-192">MOF</span><span class="sxs-lookup"><span data-stu-id="c16b1-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c16b1-193"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-193"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="c16b1-194">DLL</span><span class="sxs-lookup"><span data-stu-id="c16b1-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c16b1-195"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="c16b1-195"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c16b1-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c16b1-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c16b1-197">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="c16b1-197">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
