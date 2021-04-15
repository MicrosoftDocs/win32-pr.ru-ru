---
description: Возвращает результаты выполнения операции физического присутствия доверенного платформенного модуля.
ms.assetid: 28d76149-3905-45db-a41e-32fac1603582
title: Метод Жетфисикалпресенцереспонсе класса Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetPhysicalPresenceResponse
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 47dfad1491b398b035e40867d10d2d3e46327dd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682553"
---
# <a name="getphysicalpresenceresponse-method-of-the-win32_tpm-class"></a><span data-ttu-id="284d2-103">Метод Жетфисикалпресенцереспонсе \_ класса TPM Win32</span><span class="sxs-lookup"><span data-stu-id="284d2-103">GetPhysicalPresenceResponse method of the Win32\_Tpm class</span></span>

<span data-ttu-id="284d2-104">Метод **жетфисикалпресенцереспонсе** класса [**\_ TPM Win32**](win32-tpm.md) возвращает результаты выполнения операции физического присутствия доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-104">The **GetPhysicalPresenceResponse** method of the [**Win32\_Tpm**](win32-tpm.md) class returns the results from a TPM physical presence operation that was performed.</span></span> <span data-ttu-id="284d2-105">Используйте метод [**сетфисикалпресенцерекуест**](setphysicalpresencerequest-win32-tpm.md) для запроса операции.</span><span class="sxs-lookup"><span data-stu-id="284d2-105">Use the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method to request an operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="284d2-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="284d2-106">Syntax</span></span>


```mof
uint32 GetPhysicalPresenceResponse(
  [out] uint32 Request,
  [out] uint32 Response
);
```



## <a name="parameters"></a><span data-ttu-id="284d2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="284d2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="284d2-108">*Запрос* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="284d2-108">*Request* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="284d2-109">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284d2-109">Type: **uint32**</span></span>

<span data-ttu-id="284d2-110">Целочисленное значение, указывающее операцию физического присутствия доверенного платформенного модуля, которая была выполнена.</span><span class="sxs-lookup"><span data-stu-id="284d2-110">An integer value that specifies the TPM physical presence operation that was performed.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="284d2-111">Значение</span><span class="sxs-lookup"><span data-stu-id="284d2-111">Value</span></span></th>
<th><span data-ttu-id="284d2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="284d2-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-113"><dt>0,0</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-113"><dt>0</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-114">Нет запроса.</span><span class="sxs-lookup"><span data-stu-id="284d2-114">No request.</span></span><br/> <span data-ttu-id="284d2-115">Операция физического присутствия не выполнялась.</span><span class="sxs-lookup"><span data-stu-id="284d2-115">No physical presence operation was performed.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-116"><dt>1</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-116"><dt>1</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-117">Включите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-117">Enable the TPM.</span></span><br/> <span data-ttu-id="284d2-118">Эта операция обращена к операции 2.</span><span class="sxs-lookup"><span data-stu-id="284d2-118">This operation is reversed by operation 2.</span></span> <br/> <span data-ttu-id="284d2-119">Дополнительные сведения см. в разделе связанные методы, не затрагивающие физическое присутствие:</span><span class="sxs-lookup"><span data-stu-id="284d2-119">For more information, see these related methods that do not involve physical presence:</span></span>
<ul>
<li><span data-ttu-id="284d2-120"><a href="enable-win32-tpm.md"><strong>Включить</strong></a></span><span class="sxs-lookup"><span data-stu-id="284d2-120"><a href="enable-win32-tpm.md"><strong>Enable</strong></a></span></span></li>
<li><span data-ttu-id="284d2-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="284d2-121"><a href="isenabled-win32-tpm.md"><strong>IsEnabled</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-122"><dt>2</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-122"><dt>2</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-123">Отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-123">Disable the TPM.</span></span><br/> <span data-ttu-id="284d2-124">Эта операция обращена к операции 1.</span><span class="sxs-lookup"><span data-stu-id="284d2-124">This operation is reversed by operation 1.</span></span> <br/> <span data-ttu-id="284d2-125">Дополнительные сведения см. в этом связанном методе, который не участвует в физическом присутствии: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="284d2-125">For more information, see this related method that does not involve physical presence: <a href="disable-win32-tpm.md"><strong>Disable</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-126"><dt>3-5</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-126"><dt>3</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-127">Активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-127">Activate the TPM.</span></span><br/> <span data-ttu-id="284d2-128">Эта операция обращена к операции 4.</span><span class="sxs-lookup"><span data-stu-id="284d2-128">This operation is reversed by operation 4.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-129"><dt>четырех</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-129"><dt>4</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-130">Отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-130">Deactivate the TPM.</span></span><br/> <span data-ttu-id="284d2-131">Эта операция обращена к операции 3.</span><span class="sxs-lookup"><span data-stu-id="284d2-131">This operation is reversed by operation 3.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-132"><dt>5.0</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-132"><dt>5</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-133">Очистите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-133">Clear the TPM.</span></span><br/> <span data-ttu-id="284d2-134">Эта операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="284d2-134">This operation cannot be reversed.</span></span> <br/> <span data-ttu-id="284d2-135">Дополнительные сведения см. в этом связанном методе, который не участвует в физическом присутствии: <a href="clear-win32-tpm.md"><strong>clear</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="284d2-135">For more information, see this related method that does not involve physical presence: <a href="clear-win32-tpm.md"><strong>Clear</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-136"><dt>1-6</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-136"><dt>6</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-137">Включите и активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-137">Enable and activate the TPM.</span></span><br/> <span data-ttu-id="284d2-138">Эта операция обращена к операции 7.</span><span class="sxs-lookup"><span data-stu-id="284d2-138">This operation is reversed by operation 7.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-139"><dt>7</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-139"><dt>7</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-140">Деактивируйте и отключите доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-140">Deactivate and disable the TPM.</span></span><br/> <span data-ttu-id="284d2-141">Эта операция отменена операцией 6.</span><span class="sxs-lookup"><span data-stu-id="284d2-141">This operation is reversed by operation 6.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-142"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-142"><dt>8</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-143">Разрешить установку владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-143">Allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="284d2-144">Эта операция обращена к операции 9.</span><span class="sxs-lookup"><span data-stu-id="284d2-144">This operation is reversed by operation 9.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-145"><dt>8</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-145"><dt>9</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-146">Запрещает установку владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-146">Prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="284d2-147">Эта операция обращена к операции 8.</span><span class="sxs-lookup"><span data-stu-id="284d2-147">This operation is reversed by operation 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-148"><dt>штук</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-148"><dt>10</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-149">Включение, активация и разрешение установки владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-149">Enable, activate, and allow the installation of a TPM owner.</span></span><br/> <span data-ttu-id="284d2-150">Эта операция обращена к операции 11.</span><span class="sxs-lookup"><span data-stu-id="284d2-150">This operation is reversed by operation 11.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-151"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-151"><dt>11</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-152">Отключение, отключение и предотвращение установки владельца доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-152">Deactivate, disable, and prevent the installation of a TPM owner.</span></span><br/> <span data-ttu-id="284d2-153">Эта операция обращена к операции 10.</span><span class="sxs-lookup"><span data-stu-id="284d2-153">This operation is reversed by operation 10.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span></span><dl> <span data-ttu-id="284d2-154"><dt><strong></strong></dt><dt>12</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-154"><dt><strong></strong></dt> <dt>12</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-155">Отложенная физическая Пресенцеуновнедфиелдупграде</span><span class="sxs-lookup"><span data-stu-id="284d2-155">Deferred Physical PresenceunownedFieldUpgrade</span></span><br/> <span data-ttu-id="284d2-156">Параметр физического присутствия обновлен.</span><span class="sxs-lookup"><span data-stu-id="284d2-156">Physical presence setting has been updated.</span></span><br/> <span data-ttu-id="284d2-157"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-157"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-158"><dt>открыт</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-158"><dt>14</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-159">Очистите, включите и активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-159">Clear, enable, and activate the TPM.</span></span><br/> <span data-ttu-id="284d2-160">Эта операция не может быть отменена.</span><span class="sxs-lookup"><span data-stu-id="284d2-160">This operation cannot be reversed.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-161"><dt>15</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-161"><dt>15</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-162">SetNoPPIProvision_False</span><span class="sxs-lookup"><span data-stu-id="284d2-162">SetNoPPIProvision_False</span></span><br/> <span data-ttu-id="284d2-163">Задает назначение, которое должно быть физическим присутствием для задания доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-163">Sets the provision that you must be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="284d2-164">Эта операция обращена к операции 16.</span><span class="sxs-lookup"><span data-stu-id="284d2-164">This operation is reversed by operation 16.</span></span><br/> <span data-ttu-id="284d2-165"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-165"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-166"><dt>глубин</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-166"><dt>16</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-167">SetNoPPIProvision_True</span><span class="sxs-lookup"><span data-stu-id="284d2-167">SetNoPPIProvision_True</span></span><br/> <span data-ttu-id="284d2-168">Задает назначение, которое не обязательно должно быть физическим присутствием для задания доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-168">Sets the provision that you don't need to be physically presence to set the TPM.</span></span><br/> <span data-ttu-id="284d2-169">Эта операция обращена к операции 15.</span><span class="sxs-lookup"><span data-stu-id="284d2-169">This operation is reversed by operation 15.</span></span><br/> <span data-ttu-id="284d2-170"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-170"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-171"><dt>широкоэкранны</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-171"><dt>17</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-172">SetNoPPIClear_False</span><span class="sxs-lookup"><span data-stu-id="284d2-172">SetNoPPIClear_False</span></span><br/> <span data-ttu-id="284d2-173">Задает назначение, которое должно быть физическим присутствием для очистки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-173">Sets the provision that you must be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="284d2-174">Эта операция обращена к операции 18.</span><span class="sxs-lookup"><span data-stu-id="284d2-174">This operation is reversed by operation 18.</span></span><br/> <span data-ttu-id="284d2-175"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-175"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-176"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-176"><dt>18</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-177">SetNoPPIClear_True</span><span class="sxs-lookup"><span data-stu-id="284d2-177">SetNoPPIClear_True</span></span><br/> <span data-ttu-id="284d2-178">Задает назначение, которое не должно быть физическим присутствием для очистки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-178">Sets the provision that you don't need to be physically presence to clear the TPM.</span></span><br/> <span data-ttu-id="284d2-179">Эта операция обращена к операции 17.</span><span class="sxs-lookup"><span data-stu-id="284d2-179">This operation is reversed by operation 17.</span></span><br/> <span data-ttu-id="284d2-180"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-180"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-181"><dt>стр</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-181"><dt>19</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-182">SetNoPPIMaintenance_False</span><span class="sxs-lookup"><span data-stu-id="284d2-182">SetNoPPIMaintenance_False</span></span><br/> <span data-ttu-id="284d2-183">Задает назначение, которое должно быть физическим присутствием для поддержки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-183">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="284d2-184">Эта операция обращена к операции 20.</span><span class="sxs-lookup"><span data-stu-id="284d2-184">This operation is reversed by operation 20.</span></span><br/> <span data-ttu-id="284d2-185"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-185"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-186"><dt>20</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-186"><dt>20</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-187">SetNoPPIMaintenance_True</span><span class="sxs-lookup"><span data-stu-id="284d2-187">SetNoPPIMaintenance_True</span></span><br/> <span data-ttu-id="284d2-188">Задает назначение, которое должно быть физическим присутствием для поддержки доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-188">Sets the provision that you must be physically presence to maintain the TPM.</span></span><br/> <span data-ttu-id="284d2-189">Эта операция обращена к операции 19.</span><span class="sxs-lookup"><span data-stu-id="284d2-189">This operation is reversed by operation 19.</span></span><br/> <span data-ttu-id="284d2-190"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-190"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="284d2-191"><dt>открыт</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-191"><dt>21</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-192">Включить + активировать + очистить</span><span class="sxs-lookup"><span data-stu-id="284d2-192">Enable + Activate + Clear</span></span><br/> <span data-ttu-id="284d2-193">Включение, активация и очистка доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-193">Enable, activate, and clear the TPM.</span></span><br/> <span data-ttu-id="284d2-194"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-194"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="284d2-195"><dt>максималь</dt> </span><span class="sxs-lookup"><span data-stu-id="284d2-195"><dt>22</dt> </span></span></dl></td>
<td><span data-ttu-id="284d2-196">Включить + активировать + очистить + включить + активировать</span><span class="sxs-lookup"><span data-stu-id="284d2-196">Enable + Activate + Clear + Enable + Activate</span></span><br/> <span data-ttu-id="284d2-197">Включите, активируйте и очистите доверенный платформенный модуль, а затем включите и повторно активируйте доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="284d2-197">Enable, activate, and clear the TPM, and then enable and reactivate the TPM.</span></span><br/> <span data-ttu-id="284d2-198"><strong>Windows 7, Windows server 2008 R2, Windows Vista и Windows server 2008:</strong> Это значение не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="284d2-198"><strong>Windows 7, Windows Server 2008 R2, Windows Vista and Windows Server 2008:</strong> This value is not supported.</span></span><br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="284d2-199">*Ответ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="284d2-199">*Response* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="284d2-200">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284d2-200">Type: **uint32**</span></span>

<span data-ttu-id="284d2-201">Целочисленное значение, указывающее результаты выполнения операции физического присутствия TPM.</span><span class="sxs-lookup"><span data-stu-id="284d2-201">An integer value that specifies the results of performing the TPM physical presence operation.</span></span>

<span data-ttu-id="284d2-202">Операция физического присутствия завершается успешно, если физически представленный пользователь подтверждает операцию и если операция выполняется без ошибок.</span><span class="sxs-lookup"><span data-stu-id="284d2-202">A physical presence operation is successful if a physically present user confirms the operation and if the operation runs without errors.</span></span>

<span data-ttu-id="284d2-203">Это значение может содержать любую ошибку доверенного платформенного модуля.</span><span class="sxs-lookup"><span data-stu-id="284d2-203">This value may contain any TPM error.</span></span> <span data-ttu-id="284d2-204">В следующей таблице перечислены некоторые распространенные ответы об ошибках.</span><span class="sxs-lookup"><span data-stu-id="284d2-204">The following table lists some of the common error responses.</span></span>



| <span data-ttu-id="284d2-205">Значение</span><span class="sxs-lookup"><span data-stu-id="284d2-205">Value</span></span>                                                                                                                                                                                                                                                                    | <span data-ttu-id="284d2-206">Значение</span><span class="sxs-lookup"><span data-stu-id="284d2-206">Meaning</span></span>                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="284d2-207"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-207"><dt>0</dt></span></span> </dl>                                                                                                                                                                                             | <span data-ttu-id="284d2-208">Запрошенная операция TPM выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="284d2-208">The requested TPM operation was successful.</span></span><br/>              |
| <span id="TPM_E_PPI_USER_ABORT"></span><span id="tpm_e_ppi_user_abort"></span><dl> <span data-ttu-id="284d2-209"><dt>**Доверенный платформенный модуль \_ \_ \_ Пользовательское \_ прерывание по PPI**</dt> <dt>2150171393 (0x80290301)</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-209"><dt>**TPM\_E\_PPI\_USER\_ABORT**</dt> <dt>2150171393 (0x80290301)</dt></span></span> </dl>       | <span data-ttu-id="284d2-210">Пользователь отклонил запрошенную операцию TPM.</span><span class="sxs-lookup"><span data-stu-id="284d2-210">The user rejected the requested TPM operation.</span></span><br/>           |
| <span id="TPM_E_PPI_BIOS_FAILURE"></span><span id="tpm_e_ppi_bios_failure"></span><dl> <span data-ttu-id="284d2-211"><dt>**Доверенный платформенный модуль \_ E \_ PPI \_ BIOS \_ сбой**</dt> <dt>2150171394 (0x80290302)</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-211"><dt>**TPM\_E\_PPI\_BIOS\_FAILURE**</dt> <dt>2150171394 (0x80290302)</dt></span></span> </dl> | <span data-ttu-id="284d2-212">Ошибка BIOS при выполнении операции TPM.</span><span class="sxs-lookup"><span data-stu-id="284d2-212">A BIOS failure occurred while running the TPM operation.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="284d2-213">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="284d2-213">Return value</span></span>

<span data-ttu-id="284d2-214">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="284d2-214">Type: **uint32**</span></span>

<span data-ttu-id="284d2-215">Могут возвращаться все ошибки доверенного платформенного модуля, а также ошибки, относящиеся к базовым службам TPM.</span><span class="sxs-lookup"><span data-stu-id="284d2-215">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="284d2-216">В следующей таблице перечислены некоторые распространенные коды возврата.</span><span class="sxs-lookup"><span data-stu-id="284d2-216">The following table lists some of the common return codes.</span></span>



| <span data-ttu-id="284d2-217">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="284d2-217">Return code/value</span></span>                                                                                                                                                                      | <span data-ttu-id="284d2-218">Описание</span><span class="sxs-lookup"><span data-stu-id="284d2-218">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="284d2-219"><dt>**С \_ ОК**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-219"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl>                                      | <span data-ttu-id="284d2-220">Метод успешно выполнен.</span><span class="sxs-lookup"><span data-stu-id="284d2-220">The method was successful.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="284d2-221"><dt>**Доверенный платформенный модуль \_ E \_ PPI \_ ACPI \_ сбой**</dt> <dt>2150171392 (0x80290300)</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-221"><dt>**TPM\_E\_PPI\_ACPI\_FAILURE**</dt> <dt>2150171392 (0x80290300)</dt></span></span> </dl> | <span data-ttu-id="284d2-222">Произошла ошибка оборудования.</span><span class="sxs-lookup"><span data-stu-id="284d2-222">A hardware failure occurred.</span></span> <span data-ttu-id="284d2-223">Для получения дополнительных сведений обратитесь к изготовителю компьютера.</span><span class="sxs-lookup"><span data-stu-id="284d2-223">Consult your computer manufacturer for more information.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="284d2-224">Комментарии</span><span class="sxs-lookup"><span data-stu-id="284d2-224">Remarks</span></span>

<span data-ttu-id="284d2-225">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="284d2-225">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="284d2-226">MOF-файлы не устанавливаются в составе Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="284d2-226">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="284d2-227">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="284d2-227">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="284d2-228">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="284d2-228">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="284d2-229">Требования</span><span class="sxs-lookup"><span data-stu-id="284d2-229">Requirements</span></span>



| <span data-ttu-id="284d2-230">Требование</span><span class="sxs-lookup"><span data-stu-id="284d2-230">Requirement</span></span> | <span data-ttu-id="284d2-231">Значение</span><span class="sxs-lookup"><span data-stu-id="284d2-231">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="284d2-232">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="284d2-232">Minimum supported client</span></span><br/> | <span data-ttu-id="284d2-233">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="284d2-233">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="284d2-234">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="284d2-234">Minimum supported server</span></span><br/> | <span data-ttu-id="284d2-235">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="284d2-235">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="284d2-236">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="284d2-236">Namespace</span></span><br/>                | <span data-ttu-id="284d2-237">Корневой \\ CIMV2 \\ безопасности \\ микрософттпм</span><span class="sxs-lookup"><span data-stu-id="284d2-237">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="284d2-238">MOF</span><span class="sxs-lookup"><span data-stu-id="284d2-238">MOF</span></span><br/>                      | <dl> <span data-ttu-id="284d2-239"><dt>Win32 \_ TPM. mof</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-239"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="284d2-240">DLL</span><span class="sxs-lookup"><span data-stu-id="284d2-240">DLL</span></span><br/>                      | <dl> <span data-ttu-id="284d2-241"><dt>\_tpm.dllWin32</dt></span><span class="sxs-lookup"><span data-stu-id="284d2-241"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="284d2-242">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="284d2-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="284d2-243">**\_TPM Win32**</span><span class="sxs-lookup"><span data-stu-id="284d2-243">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="284d2-244">**Открытым**</span><span class="sxs-lookup"><span data-stu-id="284d2-244">**Clear**</span></span>](clear-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="284d2-245">**Отключить**</span><span class="sxs-lookup"><span data-stu-id="284d2-245">**Disable**</span></span>](disable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="284d2-246">**Включить**</span><span class="sxs-lookup"><span data-stu-id="284d2-246">**Enable**</span></span>](enable-win32-tpm.md)
</dt> <dt>

[<span data-ttu-id="284d2-247">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="284d2-247">**IsEnabled**</span></span>](isenabled-win32-tpm.md)
</dt> </dl>

 

 
