---
description: Возвращает ожидающую операцию физического присутствия доверенного платформенного модуля. Используйте метод Сетфисикалпресенцерекуест для запроса операции.
ms.assetid: c50378ae-b465-4c82-beb9-8ecb7939dae2
title: Метод Жетфисикалпресенцерекуест класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceRequest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8d631aabfc1e2df15aa4182b8332091fe503f539
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684061"
---
# <a name="getphysicalpresencerequest-method-of-the-win32_tpm-class"></a><span data-ttu-id="9da37-104">Метод Жетфисикалпресенцерекуест \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="9da37-104">GetPhysicalPresenceRequest method of the Win32\_Tpm class</span></span>

<span data-ttu-id="9da37-105">Метод **жетфисикалпресенцерекуест** класса [**\_ TPM Win32**](win32-tpm.md) возвращает ожидающую операцию физического присутствия доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-105">The **GetPhysicalPresenceRequest** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the pending TPM physical presence operation.</span></span> <span data-ttu-id="9da37-106">Используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) для запроса операции.</span><span class="sxs-lookup"><span data-stu-id="9da37-106">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9da37-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9da37-107">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceRequest(
  [out] uint32 Request
);
```



## <a name="parameters"></a><span data-ttu-id="9da37-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9da37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9da37-109">*Запрос* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9da37-109">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9da37-110">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9da37-110">Type: **uint32**</span></span>

<span data-ttu-id="9da37-111">Значение, указывающее отложенную операцию физического присутствия TPM.</span><span class="sxs-lookup"><span data-stu-id="9da37-111">A value that specifies the pending TPM physical presence operation.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9da37-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9da37-112">Value</span></span></th>
<th><span data-ttu-id="9da37-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9da37-113">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-114"><dt>0,0</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-114"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-115">Нет запроса.</span><span class="sxs-lookup"><span data-stu-id="9da37-115">No request.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-117">Включите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-117">Enable the TPM.</span></span><br/> <span data-ttu-id="9da37-118">Эта операция обращена к операции 2.</span><span class="sxs-lookup"><span data-stu-id="9da37-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="9da37-119">Дополнительные сведения см. в разделе связанные методы, не затрагивающие физическое присутствие:</span><span class="sxs-lookup"><span data-stu-id="9da37-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="9da37-120"><a href="enable-win32-tpm.md"><strong>Включить</strong></a></span><span class="sxs-lookup"><span data-stu-id="9da37-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="9da37-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="9da37-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-123">Отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-123">Disable the TPM.</span></span><br/> <span data-ttu-id="9da37-124">Эта операция обращена к операции 1.</span><span class="sxs-lookup"><span data-stu-id="9da37-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="9da37-125">Дополнительные сведения см. в этом связанном методе, который не участвует в физическом присутствии: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9da37-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-126"><dt>3-5</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-127">Активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-127">Activate the TPM.</span></span><br/> <span data-ttu-id="9da37-128">Эта операция обращена к операции 4.</span><span class="sxs-lookup"><span data-stu-id="9da37-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-129"><dt>четырех</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-130">Отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="9da37-131">Эта операция обращена к операции 3.</span><span class="sxs-lookup"><span data-stu-id="9da37-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-132"><dt>5.0</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-133">Очистите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-133">Clear the TPM.</span></span><br/> <span data-ttu-id="9da37-134">Эта операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="9da37-134">This operation cannot be reversed.</span></span><br/> <span data-ttu-id="9da37-135">Дополнительные сведения см. в этом связанном методе, который не участвует в физическом присутствии: <a href="clear-win32-tpm.md"><strong>clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9da37-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-136"><dt>1-6</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-137">Включите и активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-137">Enable and activate the TPM.</span></span> <br/> <span data-ttu-id="9da37-138">Эта операция обращена к операции 7.</span><span class="sxs-lookup"><span data-stu-id="9da37-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-140">Деактивируйте и отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="9da37-141">Эта операция отменена операцией 6.</span><span class="sxs-lookup"><span data-stu-id="9da37-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-143">Разрешить установку владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-143">Allow the installation of a TPM owner.</span></span> <br/> <span data-ttu-id="9da37-144">Эта операция обращена к операции 9.</span><span class="sxs-lookup"><span data-stu-id="9da37-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-145"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-146">Запрещает установку владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="9da37-147">Эта операция обращена к операции 8.</span><span class="sxs-lookup"><span data-stu-id="9da37-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-148"><dt>штук</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-149">Включение, активация и разрешение установки владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="9da37-150">Эта операция обращена к операции 11.</span><span class="sxs-lookup"><span data-stu-id="9da37-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-151"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-152">Отключение, отключение и предотвращение установки владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="9da37-153">Эта операция обращена к операции 10.</span><span class="sxs-lookup"><span data-stu-id="9da37-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="9da37-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-155">Отложенная физическая Пресенцеуновнедфиелдупграде</span><span class="sxs-lookup"><span data-stu-id="9da37-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="9da37-156">Параметр физического присутствия обновлен.</span><span class="sxs-lookup"><span data-stu-id="9da37-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="9da37-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-158"><dt>открыт</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-159">Очистите, включите и активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="9da37-160">Эта операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="9da37-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="9da37-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="9da37-163">Задает назначение, которое должно быть физическим присутствием для задания доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="9da37-164">Эта операция обращена к операции 16.</span><span class="sxs-lookup"><span data-stu-id="9da37-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="9da37-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-166"><dt>глубин</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="9da37-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="9da37-168">Задает назначение, которое не обязательно должно быть физическим присутствием для задания доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="9da37-169">Эта операция обращена к операции 15.</span><span class="sxs-lookup"><span data-stu-id="9da37-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="9da37-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-171"><dt>широкоэкранны</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="9da37-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="9da37-173">Задает назначение, которое должно быть физическим присутствием для очистки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="9da37-174">Эта операция обращена к операции 18.</span><span class="sxs-lookup"><span data-stu-id="9da37-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="9da37-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-176"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="9da37-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="9da37-178">Задает назначение, которое не должно быть физическим присутствием для очистки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="9da37-179">Эта операция обращена к операции 17.</span><span class="sxs-lookup"><span data-stu-id="9da37-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="9da37-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-181"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="9da37-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="9da37-183">Задает назначение, которое должно быть физическим присутствием для поддержки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="9da37-184">Эта операция обращена к операции 20.</span><span class="sxs-lookup"><span data-stu-id="9da37-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="9da37-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="9da37-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="9da37-188">Задает назначение, которое должно быть физическим присутствием для поддержки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="9da37-189">Эта операция обращена к операции 19.</span><span class="sxs-lookup"><span data-stu-id="9da37-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="9da37-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="9da37-191"><dt>открыт</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-192">Включить + активировать + очистить</span><span class="sxs-lookup"><span data-stu-id="9da37-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="9da37-193">Включение, активация и очистка доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="9da37-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="9da37-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="9da37-195"><dt>максималь</dt> </span><span class="sxs-lookup"><span data-stu-id="9da37-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="9da37-196">Включить + активировать + очистить + включить + активировать</span><span class="sxs-lookup"><span data-stu-id="9da37-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="9da37-197">Включите, активируйте и очистите доверенный платформенный модуль, а затем включите и повторно активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="9da37-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="9da37-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="9da37-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9da37-199">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9da37-199">Return value</span></span>

<span data-ttu-id="9da37-200">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9da37-200">Type: **uint32**</span></span>

<span data-ttu-id="9da37-201">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="9da37-201">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="9da37-202">В следующей таблице перечислены общие коды возврата.</span><span class="sxs-lookup"><span data-stu-id="9da37-202">The following table lists the common return codes.</span></span>



| <span data-ttu-id="9da37-203">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="9da37-203">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="9da37-204">Описание</span><span class="sxs-lookup"><span data-stu-id="9da37-204">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9da37-205"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="9da37-205"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="9da37-206">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="9da37-206">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="9da37-207"><dt>**Доверенный платформенный модуль \_ E \_ PPI \_ ACPI \_ сбой**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="9da37-207"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="9da37-208">Произошла ошибка оборудования.</span><span class="sxs-lookup"><span data-stu-id="9da37-208">A hardware failure occurred.</span></span> <span data-ttu-id="9da37-209">Для получения дополнительных сведений обратитесь к изготовителю компьютера.</span><span class="sxs-lookup"><span data-stu-id="9da37-209">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9da37-210">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9da37-210">Remarks</span></span>

<span data-ttu-id="9da37-211">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9da37-211">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9da37-212">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="9da37-212">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="9da37-213">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9da37-213">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9da37-214">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="9da37-214">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9da37-215">Требования</span><span class="sxs-lookup"><span data-stu-id="9da37-215">Requirements</span></span>



| <span data-ttu-id="9da37-216">Требование</span><span class="sxs-lookup"><span data-stu-id="9da37-216">Requirement</span></span> | <span data-ttu-id="9da37-217">Значение</span><span class="sxs-lookup"><span data-stu-id="9da37-217">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9da37-218">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9da37-218">Minimum supported client</span></span><br/> | <span data-ttu-id="9da37-219">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9da37-219">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="9da37-220">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9da37-220">Minimum supported server</span></span><br/> | <span data-ttu-id="9da37-221">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9da37-221">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9da37-222">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9da37-222">Namespace</span></span><br/>                | <span data-ttu-id="9da37-223">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="9da37-223">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="9da37-224">MOF</span><span class="sxs-lookup"><span data-stu-id="9da37-224">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9da37-225"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9da37-225"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="9da37-226">DLL</span><span class="sxs-lookup"><span data-stu-id="9da37-226">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9da37-227"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="9da37-227"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9da37-228">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9da37-228">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9da37-229">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="9da37-229">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9da37-230">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="9da37-230">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9da37-231">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="9da37-231">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9da37-232">**Включить**</span><span class="sxs-lookup"><span data-stu-id="9da37-232">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9da37-233">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="9da37-233">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="9da37-234">**сетфисикалпресенцерекуест**</span><span class="sxs-lookup"><span data-stu-id="9da37-234">**SetPhysicalPresenceRequest**</span></span>](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
