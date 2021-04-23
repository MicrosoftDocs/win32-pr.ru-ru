---
title: Класс Win32_RDMSDeploymentSettings
description: Управляет параметрами развертывания для коллекции виртуальных рабочих столов.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSDeploymentSettings, описание
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534010"
---
# <a name="win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c8bf0-105">\_Класс Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="c8bf0-105">Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c8bf0-106">Управляет параметрами развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-106">Manages deployment settings for a virtual desktop collection.</span></span>

<span data-ttu-id="c8bf0-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bf0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c8bf0-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a><span data-ttu-id="c8bf0-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c8bf0-109">Members</span></span>

<span data-ttu-id="c8bf0-110">Класс **Win32 \_ рдмсдеплойментсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c8bf0-110">The **Win32\_RDMSDeploymentSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="c8bf0-111">Методы</span><span class="sxs-lookup"><span data-stu-id="c8bf0-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8bf0-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c8bf0-112">Methods</span></span>

<span data-ttu-id="c8bf0-113">Класс **Win32 \_ рдмсдеплойментсеттингс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-113">The **Win32\_RDMSDeploymentSettings** class has these methods.</span></span>



| <span data-ttu-id="c8bf0-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c8bf0-114">Method</span></span>                                                                                                  | <span data-ttu-id="c8bf0-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c8bf0-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8bf0-116">**жетбасевхдпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-116">**GetBaseVHDPath**</span></span>](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="c8bf0-117">Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-117">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="c8bf0-118">**ConnectionString**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-118">**GetConnectionString**</span></span>](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | <span data-ttu-id="c8bf0-119">Извлекает строку подключения к базе данных на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-119">Retrieves the deployment-level database connection string.</span></span><br/>                                                             |
| [<span data-ttu-id="c8bf0-120">**жетдиффвхдпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-120">**GetDiffVHDPath**</span></span>](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="c8bf0-121">Возвращает путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-121">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>            |
| [<span data-ttu-id="c8bf0-122">**жетекспортпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-122">**GetExportPath**</span></span>](getexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="c8bf0-123">Извлекает путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-123">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                  |
| [<span data-ttu-id="c8bf0-124">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-124">**GetInt32Property**</span></span>](getint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="c8bf0-125">Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-125">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                             |
| [<span data-ttu-id="c8bf0-126">**жетсекондариконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-126">**GetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | <span data-ttu-id="c8bf0-127">Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-127">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span><br/> |
| [<span data-ttu-id="c8bf0-128">**жетсмбпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-128">**GetSMBPath**</span></span>](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="c8bf0-129">Возвращает UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-129">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>      |
| [<span data-ttu-id="c8bf0-130">**жетстрингаррайдеплойментсеттинг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-130">**GetStringArrayDeploymentSetting**</span></span>](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="c8bf0-131">Извлекает параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-131">Retrieves the deployment settings for a virtual desktop collection.</span></span><br/>                                                    |
| [<span data-ttu-id="c8bf0-132">**жетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-132">**GetStringProperty**</span></span>](getstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="c8bf0-133">Извлекает строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-133">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="c8bf0-134">**ремоведеплойментсеттинг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-134">**RemoveDeploymentSetting**</span></span>](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | <span data-ttu-id="c8bf0-135">Удаляет параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-135">Deletes the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="c8bf0-136">**сетбасевхдпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-136">**SetBaseVHDPath**</span></span>](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="c8bf0-137">Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-137">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span><br/>                 |
| [<span data-ttu-id="c8bf0-138">**сетконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-138">**SetConnectionString**</span></span>](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | <span data-ttu-id="c8bf0-139">Задает строку подключения к базе данных на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-139">Sets the deployment-level database connection string.</span></span><br/>                                                                  |
| [<span data-ttu-id="c8bf0-140">**сетдиффвхдпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-140">**SetDiffVHDPath**</span></span>](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | <span data-ttu-id="c8bf0-141">Обновляет путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-141">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span><br/>              |
| [<span data-ttu-id="c8bf0-142">**сетекспортпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-142">**SetExportPath**</span></span>](setexportpath-win32-rdmsdeploymentsettings.md)                                     | <span data-ttu-id="c8bf0-143">Обновляет путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-143">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span><br/>                    |
| [<span data-ttu-id="c8bf0-144">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-144">**SetInt32Property**</span></span>](setint32property-win32-rdmsdeploymentsettings.md)                               | <span data-ttu-id="c8bf0-145">Обновляет целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-145">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span><br/>                               |
| [<span data-ttu-id="c8bf0-146">**сетсекондариконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-146">**SetSecondaryConnectionString**</span></span>](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | <span data-ttu-id="c8bf0-147">Задает вторичную строку подключения базы данных на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-147">Sets the deployment-level database secondary connection string.</span></span><br/>                                                        |
| [<span data-ttu-id="c8bf0-148">**сетсмбпас**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-148">**SetSMBPath**</span></span>](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | <span data-ttu-id="c8bf0-149">Обновляет UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-149">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span><br/>        |
| [<span data-ttu-id="c8bf0-150">**сетстрингаррайдеплойментсеттинг**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-150">**SetStringArrayDeploymentSetting**</span></span>](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | <span data-ttu-id="c8bf0-151">Обновляет параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-151">Updates the deployment settings for a virtual desktop collection.</span></span><br/>                                                      |
| [<span data-ttu-id="c8bf0-152">**сетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="c8bf0-152">**SetStringProperty**</span></span>](setstringproperty-win32-rdmsdeploymentsettings.md)                             | <span data-ttu-id="c8bf0-153">Обновляет строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c8bf0-153">Updates a string property for the deployment settings of a virtual desktop collection.</span></span><br/>                                 |



 

## <a name="requirements"></a><span data-ttu-id="c8bf0-154">Требования</span><span class="sxs-lookup"><span data-stu-id="c8bf0-154">Requirements</span></span>



| <span data-ttu-id="c8bf0-155">Требование</span><span class="sxs-lookup"><span data-stu-id="c8bf0-155">Requirement</span></span> | <span data-ttu-id="c8bf0-156">Значение</span><span class="sxs-lookup"><span data-stu-id="c8bf0-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bf0-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c8bf0-157">Minimum supported client</span></span><br/> | <span data-ttu-id="c8bf0-158">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c8bf0-158">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c8bf0-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c8bf0-159">Minimum supported server</span></span><br/> | <span data-ttu-id="c8bf0-160">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c8bf0-160">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c8bf0-161">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c8bf0-161">Namespace</span></span><br/>                | <span data-ttu-id="c8bf0-162">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="c8bf0-162">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c8bf0-163">MOF</span><span class="sxs-lookup"><span data-stu-id="c8bf0-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8bf0-164"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8bf0-164"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8bf0-165">DLL</span><span class="sxs-lookup"><span data-stu-id="c8bf0-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8bf0-166"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bf0-166"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c8bf0-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c8bf0-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bf0-168">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="c8bf0-168">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

 





