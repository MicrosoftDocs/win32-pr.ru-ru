---
description: Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Метод Тестрепликатионконнектион класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662215"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="a4f1b-103">Метод Тестрепликатионконнектион \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="a4f1b-103">TestReplicationConnection method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="a4f1b-104">Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-104">Verifies if the replication can be enabled from the current host system to the specified recovery system.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4f1b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a4f1b-105">Syntax</span></span>


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="a4f1b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a4f1b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4f1b-107">*Рековериконнектионпоинт* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-107">*RecoveryConnectionPoint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-108">Имя точки подключения.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-108">The name of the connection point.</span></span> <span data-ttu-id="a4f1b-109">Для кластера восстановления это имя ограничения брокера.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-109">For a recovery cluster, this is the broker CAP name.</span></span> <span data-ttu-id="a4f1b-110">Для изолированного сервера восстановления это имя системы узла.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-110">For a standalone recovery server, this is the host system name.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1b-111">*Рековерисерверпортнумбер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-111">*RecoveryServerPortNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-112">Номер порта точки подключения восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-112">The recovery connection point port number.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1b-113">*AuthenticationType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-113">*AuthenticationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-114">Схема проверки подлинности восстановления.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-114">The recovery authentication scheme.</span></span> <span data-ttu-id="a4f1b-115">Это должно быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-115">This must be one of the following values.</span></span>

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span data-ttu-id="a4f1b-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Встроенная проверка подлинности** (1)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-116"><span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Integrated authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a4f1b-117">Аутентификация Kerberos.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-117">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="a4f1b-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата** (2)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-118"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a4f1b-119">Проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-119">Certificate based authentication.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="a4f1b-120">*CertificateThumbPrint* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-120">*CertificateThumbPrint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-121">Отпечаток сертификата, используемый, если параметр *AuthenticationType* использует проверку подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-121">Certificate thumbprint to use when the *AuthenticationType* parameter is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1b-122">*Бипасспроксисервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-122">*BypassProxyServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-123">Обходить прокси-сервер при подключении к серверу реплики.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-123">Bypass the proxy server when connecting to the replica server.</span></span>

</dd> <dt>

<span data-ttu-id="a4f1b-124">*Задание* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4f1b-125">Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a4f1b-125">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4f1b-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a4f1b-126">Return value</span></span>

<span data-ttu-id="a4f1b-127">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a4f1b-127">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="a4f1b-128">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-128">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-129">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-129">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-130">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-130">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-131">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-131">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-132">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-132">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-133">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-133">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-134">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-134">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-135">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-135">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-136">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-136">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-137">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-137">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-138">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-138">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-139">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-139">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-140">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-140">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="a4f1b-141">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="a4f1b-141">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="a4f1b-142">Требования</span><span class="sxs-lookup"><span data-stu-id="a4f1b-142">Requirements</span></span>



| <span data-ttu-id="a4f1b-143">Требование</span><span class="sxs-lookup"><span data-stu-id="a4f1b-143">Requirement</span></span> | <span data-ttu-id="a4f1b-144">Значение</span><span class="sxs-lookup"><span data-stu-id="a4f1b-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4f1b-145">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a4f1b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a4f1b-146">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-146">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a4f1b-147">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a4f1b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a4f1b-148">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a4f1b-148">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a4f1b-149">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a4f1b-149">Namespace</span></span><br/>                | <span data-ttu-id="a4f1b-150">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a4f1b-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a4f1b-151">MOF</span><span class="sxs-lookup"><span data-stu-id="a4f1b-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a4f1b-152"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a4f1b-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a4f1b-153">DLL</span><span class="sxs-lookup"><span data-stu-id="a4f1b-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4f1b-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a4f1b-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a4f1b-155">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a4f1b-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4f1b-156">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="a4f1b-156">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

