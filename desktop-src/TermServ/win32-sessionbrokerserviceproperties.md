---
title: Класс Win32_SessionBrokerServiceProperties
description: Определяет запрос для службы посредника сеансов.
ms.assetid: fe7a0317-8b52-4685-9d0d-2f81058b4561
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerServiceProperties, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties
- Win32_SessionBrokerServiceProperties.SBNetworkName
- Win32_SessionBrokerServiceProperties.SBDbConnectionString
- Win32_SessionBrokerServiceProperties.SBDbSecondaryConnectionString
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 507c4211b9506e0635966e9541167d24495735ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535366"
---
# <a name="win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="04d3b-105">\_Класс Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="04d3b-105">Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="04d3b-106">Определяет запрос для службы посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="04d3b-106">Defines the query for a session broker service.</span></span>

<span data-ttu-id="04d3b-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="04d3b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d3b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="04d3b-108">Syntax</span></span>

``` syntax
[dynamic, singleton, provider("Win32_WIN32_SESSIONBROKERSERVICEPROPERTIES_Prov"), AMENDMENT]
class Win32_SessionBrokerServiceProperties
{
  string SBNetworkName;
  string SBDbConnectionString;
  string SBDbSecondaryConnectionString;
};
```

## <a name="members"></a><span data-ttu-id="04d3b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="04d3b-109">Members</span></span>

<span data-ttu-id="04d3b-110">Класс **Win32 \_ сессионброкерсервицепропертиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="04d3b-110">The **Win32\_SessionBrokerServiceProperties** class has these types of members:</span></span>

-   [<span data-ttu-id="04d3b-111">Методы</span><span class="sxs-lookup"><span data-stu-id="04d3b-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="04d3b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="04d3b-112">Properties</span></span>](/windows)

### <a name="methods"></a><span data-ttu-id="04d3b-113">Методы</span><span class="sxs-lookup"><span data-stu-id="04d3b-113">Methods</span></span>

<span data-ttu-id="04d3b-114">Класс **Win32 \_ сессионброкерсервицепропертиес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="04d3b-114">The **Win32\_SessionBrokerServiceProperties** class has these methods.</span></span>



| <span data-ttu-id="04d3b-115">Метод</span><span class="sxs-lookup"><span data-stu-id="04d3b-115">Method</span></span>                                                                                                | <span data-ttu-id="04d3b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="04d3b-116">Description</span></span>                                                                                                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04d3b-117">**делетесбдбконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="04d3b-117">**DeleteSBDbConnectionString**</span></span>](win32-sessionbrokerserviceproperties-deletesbdbconnectionstring.md) | <span data-ttu-id="04d3b-118">Удаляет строки подключения к базе данных (первичные и вторичные) из реестра.</span><span class="sxs-lookup"><span data-stu-id="04d3b-118">Deletes DB connection strings (primary and secondary) from the registry.</span></span><br/> <span data-ttu-id="04d3b-119">**Windows server 2012 R2, Windows server 2012 и Windows server 2008 R2:** Этот метод недоступен до Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04d3b-119">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/> |
| [<span data-ttu-id="04d3b-120">**инсталлброкердатабасе**</span><span class="sxs-lookup"><span data-stu-id="04d3b-120">**InstallBrokerDatabase**</span></span>](win32-sessionbrokerserviceproperties-installbrokerdatabase.md)           | <span data-ttu-id="04d3b-121">Устанавливает RDCB DB на Центральный SQL Server</span><span class="sxs-lookup"><span data-stu-id="04d3b-121">Installs RD Connection Broker DB on central SQL Server</span></span><br/>                                                                                                                                                                    |
| [<span data-ttu-id="04d3b-122">**исдбреачабле**</span><span class="sxs-lookup"><span data-stu-id="04d3b-122">**IsDbReachable**</span></span>](win32-sessionbrokerserviceproperties-isdbreachable.md)                           | <span data-ttu-id="04d3b-123">Проверяет доступность базы данных</span><span class="sxs-lookup"><span data-stu-id="04d3b-123">Checks if DB is reachable</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="04d3b-124">**сетброкерхамоде**</span><span class="sxs-lookup"><span data-stu-id="04d3b-124">**SetBrokerHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokerhamode.md)                       | <span data-ttu-id="04d3b-125">Переносит данные из локальной базы данных WID в новую базу данных на основе SQL Server.</span><span class="sxs-lookup"><span data-stu-id="04d3b-125">Migrates data from local WID DB to the new SQL Server based DB.</span></span> <span data-ttu-id="04d3b-126">Он также настраивает сервер брокера для использования центрального SQL Server</span><span class="sxs-lookup"><span data-stu-id="04d3b-126">It also configures the broker server to use the central SQL Server</span></span><br/>                                                                                        |
| [<span data-ttu-id="04d3b-127">**сетброкернонхамоде**</span><span class="sxs-lookup"><span data-stu-id="04d3b-127">**SetBrokerNonHAMode**</span></span>](win32-sessionbrokerserviceproperties-setbrokernonhamode.md)                 | <span data-ttu-id="04d3b-128">Переносит данные из центрального SQL Server в локальную базу данных.</span><span class="sxs-lookup"><span data-stu-id="04d3b-128">Migrates data from central SQL Server to local DB.</span></span> <span data-ttu-id="04d3b-129">Он также настраивает сервер брокера для использования локальной базы данных.</span><span class="sxs-lookup"><span data-stu-id="04d3b-129">It also configures the broker server to use the local DB.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="04d3b-130">**сетсбдбконнектионстрингс**</span><span class="sxs-lookup"><span data-stu-id="04d3b-130">**SetSBDbConnectionStrings**</span></span>](win32-sessionbrokerserviceproperties-setsbdbconnectionstrings.md)     | <span data-ttu-id="04d3b-131">Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.</span><span class="sxs-lookup"><span data-stu-id="04d3b-131">Saves DB connection strings (primary and secondary) in the registry.</span></span><br/> <span data-ttu-id="04d3b-132">**Windows server 2012 R2, Windows server 2012 и Windows server 2008 R2:** Этот метод недоступен до Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04d3b-132">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This method is not available prior to Windows Server 2016</span></span><br/>     |



 

### <a name="properties"></a><span data-ttu-id="04d3b-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="04d3b-133">Properties</span></span>

<span data-ttu-id="04d3b-134">Класс **Win32 \_ сессионброкерсервицепропертиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="04d3b-134">The **Win32\_SessionBrokerServiceProperties** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="04d3b-135">**сбдбконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="04d3b-135">**SBDbConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d3b-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="04d3b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d3b-137">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="04d3b-137">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="04d3b-138">Строка подключения к базе данных, используемая службой посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="04d3b-138">Database connection string used by Session Broker service.</span></span>

<span data-ttu-id="04d3b-139">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="04d3b-139">**Windows Server 2008 R2:** This property is not available prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="04d3b-140">**сбдбсекондариконнектионстринг**</span><span class="sxs-lookup"><span data-stu-id="04d3b-140">**SBDbSecondaryConnectionString**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d3b-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="04d3b-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d3b-142">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="04d3b-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="04d3b-143">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="04d3b-143">Optional.</span></span> <span data-ttu-id="04d3b-144">Строка подключения к базе данных-получателю, используемая службой посредника сеансов для поддержки истечения срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="04d3b-144">Secondary database connection string, used by Session Broker service to support password expiration.</span></span>

<span data-ttu-id="04d3b-145">**Windows server 2012 R2, Windows server 2012 и Windows server 2008 R2:** Это свойство недоступно до Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="04d3b-145">**Windows Server 2012 R2, Windows Server 2012 and Windows Server 2008 R2:** This property is not available prior to Windows Server 2016</span></span>

</dd> <dt>

<span data-ttu-id="04d3b-146">**сбнетворкнаме**</span><span class="sxs-lookup"><span data-stu-id="04d3b-146">**SBNetworkName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="04d3b-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="04d3b-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="04d3b-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="04d3b-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="04d3b-149">Сетевое имя, используемое службой посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="04d3b-149">The network name used by the session broker service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04d3b-150">Требования</span><span class="sxs-lookup"><span data-stu-id="04d3b-150">Requirements</span></span>



| <span data-ttu-id="04d3b-151">Требование</span><span class="sxs-lookup"><span data-stu-id="04d3b-151">Requirement</span></span> | <span data-ttu-id="04d3b-152">Значение</span><span class="sxs-lookup"><span data-stu-id="04d3b-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="04d3b-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="04d3b-153">Minimum supported client</span></span><br/> | <span data-ttu-id="04d3b-154">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="04d3b-154">None supported</span></span><br/>                                                              |
| <span data-ttu-id="04d3b-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="04d3b-155">Minimum supported server</span></span><br/> | <span data-ttu-id="04d3b-156">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="04d3b-156">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="04d3b-157">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="04d3b-157">Namespace</span></span><br/>                | <span data-ttu-id="04d3b-158">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="04d3b-158">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="04d3b-159">MOF</span><span class="sxs-lookup"><span data-stu-id="04d3b-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04d3b-160"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="04d3b-160"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="04d3b-161">DLL</span><span class="sxs-lookup"><span data-stu-id="04d3b-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04d3b-162"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04d3b-162"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

