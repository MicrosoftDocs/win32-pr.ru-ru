---
title: Класс Win32_TSLicenseServer
description: Предоставляет методы и свойства для просмотра и настройки лицензирования удаленный рабочий стол (лицензирования удаленных рабочих столов) на сервере лицензирования удаленный рабочий стол.
ms.assetid: 699ddd9f-a91a-450c-b131-a7471252a4cc
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLicenseServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLicenseServer, описание
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer
- Win32_TSLicenseServer.FirstName
- Win32_TSLicenseServer.LastName
- Win32_TSLicenseServer.Company
- Win32_TSLicenseServer.CountryRegion
- Win32_TSLicenseServer.eMail
- Win32_TSLicenseServer.OrgUnit
- Win32_TSLicenseServer.Address
- Win32_TSLicenseServer.City
- Win32_TSLicenseServer.State
- Win32_TSLicenseServer.PostalCode
- Win32_TSLicenseServer.ServerRole
- Win32_TSLicenseServer.DatabasePath
- Win32_TSLicenseServer.ProductId
- Win32_TSLicenseServer.Version
- Win32_TSLicenseServer.VersionNumber
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31951b943723e620414b2f714327db8c786f9ab9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988933"
---
# <a name="win32_tslicenseserver-class"></a><span data-ttu-id="40af8-105">\_Класс Win32 тслиценсесервер</span><span class="sxs-lookup"><span data-stu-id="40af8-105">Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="40af8-106">Предоставляет методы и свойства для просмотра и настройки лицензирования удаленный рабочий стол (лицензирования удаленных рабочих столов) на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-106">Provides methods and properties to view and configure Remote Desktop Licensing (RD Licensing) on a Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="40af8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="40af8-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseServer
{
  string FirstName;
  string LastName;
  string Company;
  string CountryRegion;
  string eMail;
  string OrgUnit;
  string Address;
  string City;
  string State;
  string PostalCode;
  uint32 ServerRole;
  string DatabasePath;
  string ProductId;
  string Version;
  string VersionNumber;
};
```

## <a name="members"></a><span data-ttu-id="40af8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="40af8-108">Members</span></span>

<span data-ttu-id="40af8-109">Класс **Win32 \_ тслиценсесервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="40af8-109">The **Win32\_TSLicenseServer** class has these types of members:</span></span>

-   [<span data-ttu-id="40af8-110">Методы</span><span class="sxs-lookup"><span data-stu-id="40af8-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="40af8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="40af8-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40af8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="40af8-112">Methods</span></span>

<span data-ttu-id="40af8-113">Класс **Win32 \_ тслиценсесервер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="40af8-113">The **Win32\_TSLicenseServer** class has these methods.</span></span>



| <span data-ttu-id="40af8-114">Метод</span><span class="sxs-lookup"><span data-stu-id="40af8-114">Method</span></span>                                                                                   | <span data-ttu-id="40af8-115">Описание</span><span class="sxs-lookup"><span data-stu-id="40af8-115">Description</span></span>                                                                                                                                                                                                                                   |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40af8-116">**активатесервер**</span><span class="sxs-lookup"><span data-stu-id="40af8-116">**ActivateServer**</span></span>](activateserver-win32-tslicenseserver.md)                           | <span data-ttu-id="40af8-117">Активация удаленный рабочий стол сервера лицензирования с помощью удаленный рабочий стол идентификатора сервера лицензирования, полученного по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="40af8-117">Activates the Remote Desktop license server by using a Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                           |
| [<span data-ttu-id="40af8-118">**активатесервераутоматик**</span><span class="sxs-lookup"><span data-stu-id="40af8-118">**ActivateServerAutomatic**</span></span>](activateserverautomatic-win32-tslicenseserver.md)         | <span data-ttu-id="40af8-119">Автоматически активирует сервер лицензий удаленный рабочий стол через Интернет.</span><span class="sxs-lookup"><span data-stu-id="40af8-119">Activates the Remote Desktop license server automatically over the Internet.</span></span> <span data-ttu-id="40af8-120">Свойства **FirstName**, **LastName**, **Company** и **страна** не должны быть пустыми при вызове этого метода, иначе метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="40af8-120">The **FirstName**, **LastName**, **Company**, and **CountryRegion** properties must not be empty when this method is called, or the method will fail.</span></span><br/> |
| [<span data-ttu-id="40af8-121">**аддлстотслсграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-121">**AddLStoTSLSGroup**</span></span>](addlstotslsgroup-win32-tslicenseserver.md)                       | <span data-ttu-id="40af8-122">Добавляет сервер лицензий удаленный рабочий стол в группу серверов лицензирования удаленный рабочий стол на контроллере домена в том же домене, что и сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-122">Adds the Remote Desktop license server to the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                                |
| [<span data-ttu-id="40af8-123">**ChangeRole**</span><span class="sxs-lookup"><span data-stu-id="40af8-123">**ChangeRole**</span></span>](changerole-win32-tslicenseserver.md)                                   | <span data-ttu-id="40af8-124">Изменяет область обнаружения сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-124">Changes the discovery scope of the Remote Desktop license server.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="40af8-125">**креатетскграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-125">**CreateTSCGroup**</span></span>](createtscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="40af8-126">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40af8-126">This method is not supported.</span></span><br/> <span data-ttu-id="40af8-127">**Windows server 2008 R2 и Windows server 2008:** Создает локальную группу "компьютеры сервера терминалов" на сервере лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-127">**Windows Server 2008 R2 and Windows Server 2008:** Creates the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                               |
| [<span data-ttu-id="40af8-128">**деактиватесервер**</span><span class="sxs-lookup"><span data-stu-id="40af8-128">**DeactivateServer**</span></span>](deactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="40af8-129">Деактивирует сервер лицензий удаленный рабочий стол, используя код подтверждения, полученный по телефону.</span><span class="sxs-lookup"><span data-stu-id="40af8-129">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="40af8-130">**деактиватесервераутоматик**</span><span class="sxs-lookup"><span data-stu-id="40af8-130">**DeactivateServerAutomatic**</span></span>](deactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="40af8-131">Деактивирует сервер лицензий удаленный рабочий стол через Интернет.</span><span class="sxs-lookup"><span data-stu-id="40af8-131">Deactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="40af8-132">При вызове этого метода свойства **FirstName** и **LastName** не должны быть пустыми, иначе метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="40af8-132">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="40af8-133">**жетактиватионстатус**</span><span class="sxs-lookup"><span data-stu-id="40af8-133">**GetActivationStatus**</span></span>](getactivationstatus-win32-tslicenseserver.md)                 | <span data-ttu-id="40af8-134">Возвращает текущее состояние активации.</span><span class="sxs-lookup"><span data-stu-id="40af8-134">Retrieves the current activation status.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="40af8-135">**жетлиценсесерверид**</span><span class="sxs-lookup"><span data-stu-id="40af8-135">**GetLicenseServerId**</span></span>](getlicenseserverid-win32-tslicenseserver.md)                   | <span data-ttu-id="40af8-136">Возвращает идентификатор сервера лицензирования удаленный рабочий стол, если сервер активирован в данный момент.</span><span class="sxs-lookup"><span data-stu-id="40af8-136">Retrieves a Remote Desktop license server ID if the server is currently activated.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="40af8-137">**ислсинтслсграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-137">**IsLSinTSLSGroup**</span></span>](islsintslsgroup-win32-tslicenseserver.md)                         | <span data-ttu-id="40af8-138">Возвращает значение, указывающее, входит ли сервер лицензий удаленный рабочий стол в группу "серверы лицензий удаленный рабочий стол" на контроллере домена в данном домене.</span><span class="sxs-lookup"><span data-stu-id="40af8-138">Retrieves whether the Remote Desktop license server is a member of the Remote Desktop License Servers group on a domain controller in a given domain.</span></span><br/>                                                                              |
| [<span data-ttu-id="40af8-139">**ислсондк**</span><span class="sxs-lookup"><span data-stu-id="40af8-139">**IsLSonDC**</span></span>](islsondc-win32-tslicenseserver.md)                                       | <span data-ttu-id="40af8-140">Возвращает значение, указывающее, установлена ли служба лицензирования удаленных рабочих столов на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="40af8-140">Retrieves whether RD Licensing is installed on a domain controller.</span></span><br/>                                                                                                                                                                |
| [<span data-ttu-id="40af8-141">**ислспревентупградегпенаблед**</span><span class="sxs-lookup"><span data-stu-id="40af8-141">**IsLSPreventUpgradeGPEnabled**</span></span>](islspreventupgradegpenabled-win32-tslicenseserver.md) | <span data-ttu-id="40af8-142">Получает значение, указывающее, включен ли параметр групповой политики "запретить обновление лицензий" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-142">Retrieves whether the "prevent license upgrade" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="40af8-143">**ислспублишед**</span><span class="sxs-lookup"><span data-stu-id="40af8-143">**IsLSPublished**</span></span>](islspublished-win32-tslicenseserver.md)                             | <span data-ttu-id="40af8-144">Возвращает значение, указывающее, опубликован ли сервер лицензирования удаленный рабочий стол в службах домен Active Directory Services (AD DS).</span><span class="sxs-lookup"><span data-stu-id="40af8-144">Retrieves whether the Remote Desktop license server is published in Active Directory Domain Services (AD DS).</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="40af8-145">**ислсрегистередтоскп**</span><span class="sxs-lookup"><span data-stu-id="40af8-145">**IsLSRegisteredToSCP**</span></span>](win32-tslicenseserver-islsregisteredtoscp.md)                 | <span data-ttu-id="40af8-146">Возвращает значение, указывающее, зарегистрирован ли сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40af8-146">Retrieves whether the Remote Desktop license server is registered as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                               |
| [<span data-ttu-id="40af8-147">**ислссекгрпгпенаблед**</span><span class="sxs-lookup"><span data-stu-id="40af8-147">**IsLSSecGrpGPEnabled**</span></span>](islssecgrpgpenabled-win32-tslicenseserver.md)                 | <span data-ttu-id="40af8-148">Возвращает значение, указывающее, включен ли параметр групповой политики "Группа безопасности сервера лицензирования" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-148">Retrieves whether the "license server security group" group policy setting is enabled on the Remote Desktop license server.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="40af8-149">**иссекуреакцессалловед**</span><span class="sxs-lookup"><span data-stu-id="40af8-149">**IsSecureAccessAllowed**</span></span>](issecureaccessallowed-win32-tslicenseserver.md)             | <span data-ttu-id="40af8-150">Получает значение, указывающее, разрешено ли серверу узла сеансов удаленных рабочих столов запрашивать службы удаленных рабочих столов клиентских лицензий (RDS CAL) с сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-150">Retrieves whether an RD Session Host server is allowed to request Remote Desktop Services client access licenses (RDS CALs) from the Remote Desktop license server.</span></span><br/>                                                                |
| [<span data-ttu-id="40af8-151">**истскграуппресент**</span><span class="sxs-lookup"><span data-stu-id="40af8-151">**IsTSCGroupPresent**</span></span>](istscgrouppresent-win32-tslicenseserver.md)                     | <span data-ttu-id="40af8-152">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40af8-152">This method is not supported.</span></span><br/> <span data-ttu-id="40af8-153">**Windows server 2008 R2 и Windows server 2008:** Возвращает значение, указывающее, существует ли локальная группа компьютеров сервера терминалов на удаленный рабочий стол сервере лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-153">**Windows Server 2008 R2 and Windows Server 2008:** Retrieves whether the Terminal Server Computers local group exists on the Remote Desktop license server.</span></span><br/>                              |
| [<span data-ttu-id="40af8-154">**истсинтскграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-154">**IsTSinTSCGroup**</span></span>](istsintscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="40af8-155">Получает значение, указывающее, входит ли сервер узла сеансов удаленных рабочих столов в локальную группу "компьютеры сервера терминалов" на сервере лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-155">Retrieves whether an RD Session Host server is a member of the Terminal Server Computers local group on the Remote Desktop license server.</span></span><br/>                                                                                         |
| [<span data-ttu-id="40af8-156">**публишлс**</span><span class="sxs-lookup"><span data-stu-id="40af8-156">**PublishLS**</span></span>](publishls-win32-tslicenseserver.md)                                     | <span data-ttu-id="40af8-157">Публикует сервер лицензий удаленный рабочий стол в AD DS.</span><span class="sxs-lookup"><span data-stu-id="40af8-157">Publishes the Remote Desktop license server in AD DS.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="40af8-158">**реактиватесервер**</span><span class="sxs-lookup"><span data-stu-id="40af8-158">**ReactivateServer**</span></span>](reactivateserver-win32-tslicenseserver.md)                       | <span data-ttu-id="40af8-159">Повторно активирует сервер лицензий удаленный рабочий стол, используя новый идентификатор сервера лицензирования удаленный рабочий стол, полученный по телефону или через Интернет.</span><span class="sxs-lookup"><span data-stu-id="40af8-159">Reactivates the Remote Desktop license server by using a new Remote Desktop license server ID that is obtained over the phone or the Internet.</span></span><br/>                                                                                     |
| [<span data-ttu-id="40af8-160">**реактиватесервераутоматик**</span><span class="sxs-lookup"><span data-stu-id="40af8-160">**ReactivateServerAutomatic**</span></span>](reactivateserverautomatic-win32-tslicenseserver.md)     | <span data-ttu-id="40af8-161">Повторно активирует сервер лицензий удаленный рабочий стол через Интернет.</span><span class="sxs-lookup"><span data-stu-id="40af8-161">Reactivates the Remote Desktop license server over the Internet.</span></span> <span data-ttu-id="40af8-162">При вызове этого метода свойства **FirstName** и **LastName** не должны быть пустыми, иначе метод завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="40af8-162">The **FirstName** and **LastName** properties must not be empty when this method is called, or the method will fail.</span></span><br/>                                              |
| [<span data-ttu-id="40af8-163">**регистерлстоскп**</span><span class="sxs-lookup"><span data-stu-id="40af8-163">**RegisterLSToSCP**</span></span>](win32-tslicenseserver-registerlstoscp.md)                         | <span data-ttu-id="40af8-164">Регистрирует сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40af8-164">Registers the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="40af8-165">**ремовелсфромтслсграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-165">**RemoveLSfromTSLSGroup**</span></span>](removelsfromtslsgroup-win32-tslicenseserver.md)             | <span data-ttu-id="40af8-166">Удаляет сервер лицензий удаленный рабочий стол из группы серверов лицензирования удаленный рабочий стол на контроллере домена в том же домене, что и сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-166">Removes the Remote Desktop license server from the Remote Desktop License Servers group on a domain controller in the same domain as the license server.</span></span><br/>                                                                           |
| [<span data-ttu-id="40af8-167">**ремоветскграуп**</span><span class="sxs-lookup"><span data-stu-id="40af8-167">**RemoveTSCGroup**</span></span>](removetscgroup-win32-tslicenseserver.md)                           | <span data-ttu-id="40af8-168">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40af8-168">This method is not supported.</span></span><br/> <span data-ttu-id="40af8-169">**Windows server 2008 R2 и Windows server 2008:** Удаляет локальную группу "компьютеры сервера терминалов" с сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-169">**Windows Server 2008 R2 and Windows Server 2008:** Removes the Terminal Server Computers local group from the Remote Desktop license server.</span></span><br/>                                             |
| [<span data-ttu-id="40af8-170">**унпублишлс**</span><span class="sxs-lookup"><span data-stu-id="40af8-170">**UnpublishLS**</span></span>](unpublishls-win32-tslicenseserver.md)                                 | <span data-ttu-id="40af8-171">Отменяет публикацию удаленный рабочий стол сервера лицензирования от AD DS.</span><span class="sxs-lookup"><span data-stu-id="40af8-171">Unpublishes a Remote Desktop license server from AD DS.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="40af8-172">**унрегистерлсфромскп**</span><span class="sxs-lookup"><span data-stu-id="40af8-172">**UnRegisterLSFromSCP**</span></span>](win32-tslicenseserver-unregisterlsfromscp.md)                 | <span data-ttu-id="40af8-173">Удаляет сервер лицензий удаленный рабочий стол в качестве точки подключения службы в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40af8-173">Removes the Remote Desktop license server as a service connection point in Active Directory Domain Services.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="40af8-174">Свойства</span><span class="sxs-lookup"><span data-stu-id="40af8-174">Properties</span></span>

<span data-ttu-id="40af8-175">Класс **Win32 \_ тслиценсесервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40af8-175">The **Win32\_TSLicenseServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="40af8-176">**Адрес**</span><span class="sxs-lookup"><span data-stu-id="40af8-176">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-177">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-178">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-179">Почтовый адрес контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-179">Street address of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-180">Это свойство используется при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-180">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="40af8-181">(Это свойство является необязательным при использовании метода **активатесервераутоматик** .)</span><span class="sxs-lookup"><span data-stu-id="40af8-181">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-182">**Город**</span><span class="sxs-lookup"><span data-stu-id="40af8-182">**City**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-184">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-185">Город контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-185">City of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-186">Это свойство используется при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-186">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="40af8-187">(Это свойство является необязательным при использовании метода **активатесервераутоматик** .)</span><span class="sxs-lookup"><span data-stu-id="40af8-187">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-188">**Company**</span><span class="sxs-lookup"><span data-stu-id="40af8-188">**Company**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-189">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-190">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-190">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-191">Организация контакта для лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-191">Company of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-192">Это свойство используется (и является обязательным) при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-192">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-193">**Страна**</span><span class="sxs-lookup"><span data-stu-id="40af8-193">**CountryRegion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-194">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-194">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-195">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-195">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-196">Страна или регион контакта для лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-196">Country/region of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-197">Это свойство используется (и является обязательным) при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-197">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-198">**DatabasePath**</span><span class="sxs-lookup"><span data-stu-id="40af8-198">**DatabasePath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40af8-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40af8-201">Путь к базе данных лицензирования RDS.</span><span class="sxs-lookup"><span data-stu-id="40af8-201">Path of the RDS Licensing database.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-202">**Отправить по электронной почте**</span><span class="sxs-lookup"><span data-stu-id="40af8-202">**eMail**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-203">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-204">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-204">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-205">Адрес электронной почты контакта для лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-205">Email address of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-206">Это свойство используется при вызове методов [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md), [**реактиватесервераутоматик**](reactivateserverautomatic-win32-tslicenseserver.md)или [**деактиватесервераутоматик**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-206">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span> <span data-ttu-id="40af8-207">(Это свойство является необязательным для этих вызовов метода.)</span><span class="sxs-lookup"><span data-stu-id="40af8-207">(This property is optional for these method calls.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-208">**FirstName**</span><span class="sxs-lookup"><span data-stu-id="40af8-208">**FirstName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-209">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-209">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-210">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-211">Имя контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-211">First name of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-212">Это свойство используется (и является обязательным) при вызове методов [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md), [**реактиватесервераутоматик**](reactivateserverautomatic-win32-tslicenseserver.md)или [**деактиватесервераутоматик**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-212">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-213">**LastName**</span><span class="sxs-lookup"><span data-stu-id="40af8-213">**LastName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-215">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-215">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-216">Фамилия контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-216">Last name of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-217">Это свойство используется (и является обязательным) при вызове методов [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md), [**реактиватесервераутоматик**](reactivateserverautomatic-win32-tslicenseserver.md)или [**деактиватесервераутоматик**](deactivateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-217">This property is used (and required) when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md), [**ReactivateServerAutomatic**](reactivateserverautomatic-win32-tslicenseserver.md), or [**DeactivateServerAutomatic**](deactivateserverautomatic-win32-tslicenseserver.md) methods are called.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-218">**OrgUnit**</span><span class="sxs-lookup"><span data-stu-id="40af8-218">**OrgUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-219">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-219">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-220">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-220">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-221">Подразделение контакта для лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-221">Organizational unit of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-222">Это свойство используется при вызове [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-222">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) is called.</span></span> <span data-ttu-id="40af8-223">(Это свойство является необязательным при использовании метода **активатесервераутоматик** .)</span><span class="sxs-lookup"><span data-stu-id="40af8-223">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-224">**PostalCode**</span><span class="sxs-lookup"><span data-stu-id="40af8-224">**PostalCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-225">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-226">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-226">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-227">Почтовый индекс контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-227">Postal code of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-228">Это свойство используется при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-228">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="40af8-229">(Это свойство является необязательным при использовании метода **активатесервераутоматик** .)</span><span class="sxs-lookup"><span data-stu-id="40af8-229">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-230">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="40af8-230">**ProductId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40af8-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40af8-233">Идентификатор продукта сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-233">Product ID of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-234">**ServerRole**</span><span class="sxs-lookup"><span data-stu-id="40af8-234">**ServerRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-235">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="40af8-235">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-236">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40af8-236">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40af8-237">Описание области лицензирования для сервера лицензирования удаленный рабочий стол в Организации.</span><span class="sxs-lookup"><span data-stu-id="40af8-237">Describes the licensing scope for the Remote Desktop license server within the organization.</span></span>

<dt>

<span data-ttu-id="40af8-238">0</span><span class="sxs-lookup"><span data-stu-id="40af8-238">0</span></span>
</dt> <dd>

<span data-ttu-id="40af8-239">Серверы узла сеансов удаленных рабочих столов в одной рабочей группе могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-239">RD Session Host servers in the same workgroup can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-240">1</span><span class="sxs-lookup"><span data-stu-id="40af8-240">1</span></span>
</dt> <dd>

<span data-ttu-id="40af8-241">Серверы узла сеансов удаленных рабочих столов в одном домене могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-241">RD Session Host servers in the same domain can discover the license server.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-242">2</span><span class="sxs-lookup"><span data-stu-id="40af8-242">2</span></span>
</dt> <dd>

<span data-ttu-id="40af8-243">Серверы узла сеансов удаленных рабочих столов из нескольких доменов в одном лесу могут обнаружить сервер лицензирования.</span><span class="sxs-lookup"><span data-stu-id="40af8-243">RD Session Host servers from multiple domains in the same forest can discover the license server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="40af8-244">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="40af8-244">**State**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-245">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-246">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="40af8-246">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="40af8-247">Состояние контакта для службы лицензирования удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="40af8-247">State of the contact for RD Licensing.</span></span> <span data-ttu-id="40af8-248">Это свойство используется при вызове метода [**активатесервераутоматик**](activateserverautomatic-win32-tslicenseserver.md) .</span><span class="sxs-lookup"><span data-stu-id="40af8-248">This property is used when the [**ActivateServerAutomatic**](activateserverautomatic-win32-tslicenseserver.md) method is called.</span></span> <span data-ttu-id="40af8-249">(Это свойство является необязательным при использовании метода **активатесервераутоматик** .)</span><span class="sxs-lookup"><span data-stu-id="40af8-249">(This property is optional when using the **ActivateServerAutomatic** method.)</span></span>

</dd> <dt>

<span data-ttu-id="40af8-250">**Version**</span><span class="sxs-lookup"><span data-stu-id="40af8-250">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40af8-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40af8-253">Версия сервера лицензирования удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-253">Version of the Remote Desktop license server.</span></span>

</dd> <dt>

<span data-ttu-id="40af8-254">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="40af8-254">**VersionNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="40af8-255">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="40af8-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="40af8-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="40af8-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="40af8-257">Номер версии сервера лицензий удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="40af8-257">Version number of the Remote Desktop license server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="40af8-258">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40af8-258">Remarks</span></span>

<span data-ttu-id="40af8-259">Этот класс является [Singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) -классом и может иметь только один экземпляр.</span><span class="sxs-lookup"><span data-stu-id="40af8-259">This class is a [singleton](/windows/desktop/WmiSdk/standard-wmi-qualifiers) class and can have only one instance.</span></span> <span data-ttu-id="40af8-260">Все методы, содержащиеся в этом классе, являются статическими.</span><span class="sxs-lookup"><span data-stu-id="40af8-260">All of the methods contained within this class are static.</span></span>

<span data-ttu-id="40af8-261">Для использования этого класса необходимо быть членом группы администраторов.</span><span class="sxs-lookup"><span data-stu-id="40af8-261">You must be a member of the Administrators group to use this class.</span></span> <span data-ttu-id="40af8-262">Если вызывающий объект не является членом группы администраторов, возвращаемые свойства будут пустыми.</span><span class="sxs-lookup"><span data-stu-id="40af8-262">If the caller is not a member of the Administrators group, the properties returned will be empty.</span></span>

<span data-ttu-id="40af8-263">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="40af8-263">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="40af8-264">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="40af8-264">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="40af8-265">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="40af8-265">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="40af8-266">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="40af8-266">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="40af8-267">Требования</span><span class="sxs-lookup"><span data-stu-id="40af8-267">Requirements</span></span>



| <span data-ttu-id="40af8-268">Требование</span><span class="sxs-lookup"><span data-stu-id="40af8-268">Requirement</span></span> | <span data-ttu-id="40af8-269">Значение</span><span class="sxs-lookup"><span data-stu-id="40af8-269">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="40af8-270">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40af8-270">Minimum supported client</span></span><br/> | <span data-ttu-id="40af8-271">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="40af8-271">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="40af8-272">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40af8-272">Minimum supported server</span></span><br/> | <span data-ttu-id="40af8-273">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="40af8-273">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="40af8-274">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="40af8-274">Namespace</span></span><br/>                | <span data-ttu-id="40af8-275">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="40af8-275">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="40af8-276">MOF</span><span class="sxs-lookup"><span data-stu-id="40af8-276">MOF</span></span><br/>                      | <dl> <span data-ttu-id="40af8-277"><dt>Тлсвмипров. mof</dt></span><span class="sxs-lookup"><span data-stu-id="40af8-277"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="40af8-278">DLL</span><span class="sxs-lookup"><span data-stu-id="40af8-278">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40af8-279"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40af8-279"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40af8-280">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40af8-280">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40af8-281">**\_Тсиссуедлиценсе Win32**</span><span class="sxs-lookup"><span data-stu-id="40af8-281">**Win32\_TSIssuedLicense**</span></span>](win32-tsissuedlicense.md)
</dt> <dt>

[<span data-ttu-id="40af8-282">**\_Тслиценсекэйпакк Win32**</span><span class="sxs-lookup"><span data-stu-id="40af8-282">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> <dt>

[<span data-ttu-id="40af8-283">**\_Тслиценсерепорт Win32**</span><span class="sxs-lookup"><span data-stu-id="40af8-283">**Win32\_TSLicenseReport**</span></span>](win32-tslicensereport.md)
</dt> <dt>

[<span data-ttu-id="40af8-284">**\_Тслиценсерепортентри Win32**</span><span class="sxs-lookup"><span data-stu-id="40af8-284">**Win32\_TSLicenseReportEntry**</span></span>](win32-tslicensereportentry.md)
</dt> </dl>

 

