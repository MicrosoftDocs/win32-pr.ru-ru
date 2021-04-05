---
description: Присоединение компьютерной системы к домену или рабочей группе.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Метод Жоиндомаинорворкграуп класса Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896294"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a><span data-ttu-id="1c858-103">Метод Жоиндомаинорворкграуп \_ класса ComputerSystem Win32</span><span class="sxs-lookup"><span data-stu-id="1c858-103">JoinDomainOrWorkgroup method of the Win32\_ComputerSystem class</span></span>

<span data-ttu-id="1c858-104">Метод **жоиндомаинорворкграуп** присоединяет компьютер к домену или рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="1c858-104">The **JoinDomainOrWorkgroup** method joins a computer system to a domain or workgroup.</span></span>

<span data-ttu-id="1c858-105">В этом разделе используется синтаксис MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="1c858-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1c858-106">Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1c858-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c858-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c858-107">Syntax</span></span>


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a><span data-ttu-id="1c858-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1c858-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c858-109">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c858-109">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c858-110">Указывает домен или рабочую группу для приподключения.</span><span class="sxs-lookup"><span data-stu-id="1c858-110">Specifies the domain or workgroup to join.</span></span> <span data-ttu-id="1c858-111">Не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c858-111">Cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-112">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c858-112">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c858-113">Если параметр *username* указывает имя учетной записи, параметр *Password* должен указывать на пароль, используемый при подключении к контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-113">If the *UserName* parameter specifies an account name, the *Password* parameter must point to the password to use when connecting to the domain controller.</span></span> <span data-ttu-id="1c858-114">В противном случае этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c858-114">Otherwise, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-115">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c858-115">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c858-116">Указатель на постоянную строку символов, завершающуюся **нулем**, которая указывает имя учетной записи, используемой при подключении к контроллеру домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-116">Pointer to a constant **null**-terminated character string that specifies the account name to use when connecting to the domain controller.</span></span> <span data-ttu-id="1c858-117">Необходимо указать NetBIOS-имя домена и учетную запись пользователя, например " \\ пользователь домена".</span><span class="sxs-lookup"><span data-stu-id="1c858-117">Must specify a domain NetBIOS name and user account, for example, Domain\\user.</span></span> <span data-ttu-id="1c858-118">Если этот параметр имеет **значение NULL**, используются сведения о вызывающем объекте.</span><span class="sxs-lookup"><span data-stu-id="1c858-118">If this parameter is **NULL**, the caller information is used.</span></span>

<span data-ttu-id="1c858-119">Также можно использовать имя участника-пользователя (увеличила) в форме user@domain .</span><span class="sxs-lookup"><span data-stu-id="1c858-119">You can also use the user principal name (UPPED) in the form user@domain.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-120">*Аккаунтау* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c858-120">*AccountOU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c858-121">Задает указатель на постоянную строку символов, завершающуюся **нулем**, которая содержит имя формата [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) для учетной записи компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c858-121">Specifies the pointer to a constant **null**-terminated character string that contains the [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) format name of the organizational unit (OU) for the computer account.</span></span> <span data-ttu-id="1c858-122">Если указать этот параметр, строка должна содержать полный путь, в противном случае *диакритические знаки* должны быть **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="1c858-122">If you specify this parameter, the string must contain a full path, otherwise *Accent* must be **NULL**.</span></span>

<span data-ttu-id="1c858-123">Пример: "OU = Тестау; DC = домен; DC = домен; DC = com "</span><span class="sxs-lookup"><span data-stu-id="1c858-123">Example: "OU=testOU; DC=domain; DC=Domain; DC=com"</span></span>

</dd> <dt>

<span data-ttu-id="1c858-124">*Фжоиноптионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1c858-124">*FJoinOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c858-125">Набор битовых флагов, определяющих параметры объединения.</span><span class="sxs-lookup"><span data-stu-id="1c858-125">Set of bit flags that define the join options.</span></span>

<dt>



 <span data-ttu-id="1c858-126"> (0)</span><span class="sxs-lookup"><span data-stu-id="1c858-126">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c858-127">Default.</span></span> <span data-ttu-id="1c858-128">Нет параметров объединения.</span><span class="sxs-lookup"><span data-stu-id="1c858-128">No join options.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span data-ttu-id="1c858-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Нетсетуп \_ Присоединение к \_ домену** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="1c858-129"><span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**NETSETUP\_JOIN\_DOMAIN** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-130">Присоединяет компьютер к домену.</span><span class="sxs-lookup"><span data-stu-id="1c858-130">Joins the computer to a domain.</span></span> <span data-ttu-id="1c858-131">Если это значение не указано, присоединяет компьютер к Рабочей группе.</span><span class="sxs-lookup"><span data-stu-id="1c858-131">If this value is not specified, joins the computer to a workgroup.</span></span>

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span data-ttu-id="1c858-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Нетсетуп \_ \_Создание acct** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="1c858-132"><span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**NETSETUP\_ACCT\_CREATE** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-133">Создает учетную запись в домене.</span><span class="sxs-lookup"><span data-stu-id="1c858-133">Creates the account on the domain.</span></span>

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span data-ttu-id="1c858-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Нетсетуп \_ \_Обновление Win9x** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="1c858-134"><span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**NETSETUP\_WIN9X\_UPGRADE** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-135">Операция Join выполняется в процессе обновления.</span><span class="sxs-lookup"><span data-stu-id="1c858-135">The join operation is occurring as part of an upgrade.</span></span>

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span data-ttu-id="1c858-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Нетсетуп \_ Присоединение к ДОМЕНу \_ \_ при \_ присоединении** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="1c858-136"><span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**NETSETUP\_DOMAIN\_JOIN\_IF\_JOINED** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-137">Позволяет присоединиться к новому домену, даже если компьютер уже присоединен к домену.</span><span class="sxs-lookup"><span data-stu-id="1c858-137">Allows a join to a new domain even if the computer is already joined to a domain.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span data-ttu-id="1c858-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Нетсетуп \_ \_НЕбезопасный присоединение** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="1c858-138"><span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**NETSETUP\_JOIN\_UNSECURE** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-139">Выполняет незащищенное присоединение.</span><span class="sxs-lookup"><span data-stu-id="1c858-139">Performs an unsecured join.</span></span>

<span data-ttu-id="1c858-140">Этот параметр запрашивает присоединение домена к предварительно созданной учетной записи без проверки подлинности с учетными данными пользователя домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-140">This option requests a domain join to a pre-created account without authenticating with domain user credentials.</span></span> <span data-ttu-id="1c858-141">Этот параметр можно использовать в сочетании с параметром **нетсетуп \_ Machine \_ PWD \_ Passed** .</span><span class="sxs-lookup"><span data-stu-id="1c858-141">This option can be used in conjunction with **NETSETUP\_MACHINE\_PWD\_PASSED** option.</span></span> <span data-ttu-id="1c858-142">В этом случае *Password* — это пароль предварительно созданной учетной записи компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c858-142">In this case, *Password* is the password of the pre-created machine account.</span></span>

<span data-ttu-id="1c858-143">До выхода Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008 небезопасное соединение не проходило проверку подлинности на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-143">Prior to Windows Vista with SP1 and Windows Server 2008, an unsecure join did not authenticate to the domain controller.</span></span> <span data-ttu-id="1c858-144">Все взаимодействие было выполнено с использованием сеанса со значением NULL (без проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="1c858-144">All communication was performed using a null (unauthenticated) session.</span></span> <span data-ttu-id="1c858-145">Начиная с Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008, имя учетной записи компьютера и пароль используются для проверки подлинности на контроллере домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-145">Starting with Windows Vista with SP1 and Windows Server 2008, the machine account name and password are used to authenticate to the domain controller.</span></span>

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span data-ttu-id="1c858-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Нетсетуп \_ Пароль компьютера (0x00000080) \_ \_ успешно пройден**</span><span class="sxs-lookup"><span data-stu-id="1c858-146"><span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**NETSETUP\_MACHINE\_PWD\_PASSED** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-147">Указывает, что параметр *Password* задает пароль учетной записи локального компьютера, а не пароль пользователя.</span><span class="sxs-lookup"><span data-stu-id="1c858-147">Indicates that the *Password* parameter specifies a local machine account password rather than a user password.</span></span> <span data-ttu-id="1c858-148">Этот флаг допустим только для незащищенных соединений, которые необходимо указать, установив \_ \_ флаг небезопасного нетсетуп JOIN.</span><span class="sxs-lookup"><span data-stu-id="1c858-148">This flag is valid only for unsecured joins, which you must indicate by also setting the NETSETUP\_JOIN\_UNSECURE flag.</span></span>

<span data-ttu-id="1c858-149">Если установить этот флаг, то после выполнения операции присоединение пароль компьютера будет установлен в значение *Password*, если это значение является допустимым паролем компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c858-149">If you set this flag, then after the join operation succeeds, the machine password will be set to the value of *Password*, if that value is a valid machine password.</span></span>

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span data-ttu-id="1c858-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Нетсетуп \_ Задержать \_ \_ набор SPN** (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="1c858-150"><span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**NETSETUP\_DEFER\_SPN\_SET** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-151">Указывает, что имя участника-службы (SPN) и свойства DnsHostName на объекте-компьютере не должны обновляться в данный момент.</span><span class="sxs-lookup"><span data-stu-id="1c858-151">Indicates that the service principal name (SPN) and the DnsHostName properties on the computer object should not be updated at this time.</span></span>

<span data-ttu-id="1c858-152">Как правило, эти свойства обновляются во время операции JOIN.</span><span class="sxs-lookup"><span data-stu-id="1c858-152">Typically, these properties are updated during the join operation.</span></span> <span data-ttu-id="1c858-153">Вместо этого эти свойства следует обновлять во время последующего вызова метода [**Rename**](rename-method-in-class-win32-computersystem.md) .</span><span class="sxs-lookup"><span data-stu-id="1c858-153">Instead, these properties should be updated during a subsequent call to the [**Rename**](rename-method-in-class-win32-computersystem.md) method.</span></span> <span data-ttu-id="1c858-154">Эти свойства всегда обновляются во время операции переименования.</span><span class="sxs-lookup"><span data-stu-id="1c858-154">These properties are always updated during the rename operation.</span></span>

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span data-ttu-id="1c858-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Нетсетуп \_ Присоединение \_ \_ учетной записи контроллера домена** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="1c858-155"><span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**NETSETUP\_JOIN\_DC\_ACCOUNT** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-156">Разрешить присоединение к домену, если существующая учетная запись является контроллером домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-156">Allow the domain join if existing account is a domain controller.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-157">Этот флаг поддерживается в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-157">This flag is supported on Windows Vista and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span data-ttu-id="1c858-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Нетсетуп \_ НЕОДНОЗНАЧНЫй \_ контроллер домена** (0x00001000)</span><span class="sxs-lookup"><span data-stu-id="1c858-158"><span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**NETSETUP\_AMBIGUOUS\_DC** (0x00001000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-159">При присоединении к домену не пытайтесь задать в реестре предпочитаемый контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="1c858-159">When joining the domain don't try to set the preferred domain controller in the registry.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-160">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-160">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span data-ttu-id="1c858-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Нетсетуп \_ НЕТ \_ \_ кэша Netlogon** (0x00002000)</span><span class="sxs-lookup"><span data-stu-id="1c858-161"><span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**NETSETUP\_NO\_NETLOGON\_CACHE** (0x00002000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-162">При присоединении к домену кэш Netlogon не создается.</span><span class="sxs-lookup"><span data-stu-id="1c858-162">When joining the domain don't create the Netlogon cache.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-163">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-163">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span data-ttu-id="1c858-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Нетсетуп \_ \_ \_ Службы управления не** (0x00004000)</span><span class="sxs-lookup"><span data-stu-id="1c858-164"><span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**NETSETUP\_DONT\_CONTROL\_SERVICES** (0x00004000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-165">При присоединении к домену Служба Netlogon не будет принудительно запущена.</span><span class="sxs-lookup"><span data-stu-id="1c858-165">When joining the domain don't force Netlogon service to start.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-166">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-166">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span data-ttu-id="1c858-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Нетсетуп \_ ЗАДАТЬ \_ \_ имя компьютера** (0x00008000)</span><span class="sxs-lookup"><span data-stu-id="1c858-167"><span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**NETSETUP\_SET\_MACHINE\_NAME** (0x00008000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-168">При присоединении к домену только для автономного соединения задайте имя узла и NetBIOS целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c858-168">When joining the domain for offline join only, set target machine hostname and NetBIOS name.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-169">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-169">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span data-ttu-id="1c858-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Нетсетуп \_ FORCE \_ \_ Set SPN** (0x00010000)</span><span class="sxs-lookup"><span data-stu-id="1c858-170"><span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**NETSETUP\_FORCE\_SPN\_SET** (0x00010000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-171">При присоединении к домену переопределите другие параметры во время присоединения к домену и задайте имя участника-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="1c858-171">When joining the domain, override other settings during domain join and set the service principal name (SPN).</span></span>

> [!Note]  
> <span data-ttu-id="1c858-172">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-172">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span data-ttu-id="1c858-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Нетсетуп \_ БЕЗ \_ \_ повторного использования** (0x00020000)</span><span class="sxs-lookup"><span data-stu-id="1c858-173"><span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**NETSETUP\_NO\_ACCT\_REUSE** (0x00020000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-174">При присоединении к домену не следует повторно использовать имеющуюся учетную запись.</span><span class="sxs-lookup"><span data-stu-id="1c858-174">When joining the domain, do not reuse an existing account.</span></span>

> [!Note]  
> <span data-ttu-id="1c858-175">Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="1c858-175">This flag is supported on Windows 7, Windows Server 2008 R2, and later.</span></span>

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span data-ttu-id="1c858-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Нетсетуп \_ ИГНОРИРОВАТЬ \_ неподдерживаемые \_ Флаги** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="1c858-176"><span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**NETSETUP\_IGNORE\_UNSUPPORTED\_FLAGS** (0x10000000)</span></span>


</dt> <dd>

<span data-ttu-id="1c858-177">Если этот бит задан, нераспознанные флаги будут игнорироваться функцией **жоиндомаинорворкграуп** , и [**нетжоиндомаин**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) будет вести себя так, как если бы не были заданы флаги.</span><span class="sxs-lookup"><span data-stu-id="1c858-177">If this bit is set, unrecognized flags will be ignored by the **JoinDomainOrWorkgroup** function and [**NetJoinDomain**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) will behave as if the flags were not set.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c858-178">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1c858-178">Return value</span></span>

<span data-ttu-id="1c858-179">Возвращает [код системной ошибки](/windows/desktop/Debug/system-error-codes), который может включать одно из следующих числовых значений.</span><span class="sxs-lookup"><span data-stu-id="1c858-179">Returns a [system error code](/windows/desktop/Debug/system-error-codes), which may include one of the following numeric values.</span></span> <span data-ttu-id="1c858-180">Любое другое значение указывает на ошибку.</span><span class="sxs-lookup"><span data-stu-id="1c858-180">Any other number indicates an error.</span></span> <span data-ttu-id="1c858-181">Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span><span class="sxs-lookup"><span data-stu-id="1c858-181">For additional error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span>

<dl> <dt>

<span data-ttu-id="1c858-182">**Успешно**</span><span class="sxs-lookup"><span data-stu-id="1c858-182">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-183">0</span><span class="sxs-lookup"><span data-stu-id="1c858-183">0</span></span>

</dd> <dt>

<span data-ttu-id="1c858-184">**5**</span><span class="sxs-lookup"><span data-stu-id="1c858-184">**5**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-185">Отказано в доступе".</span><span class="sxs-lookup"><span data-stu-id="1c858-185">Access is denied.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-186">**87**</span><span class="sxs-lookup"><span data-stu-id="1c858-186">**87**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-187">Неправильный параметр".</span><span class="sxs-lookup"><span data-stu-id="1c858-187">The parameter is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-188">**110**</span><span class="sxs-lookup"><span data-stu-id="1c858-188">**110**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-189">система не может открыть указанный объект.</span><span class="sxs-lookup"><span data-stu-id="1c858-189">he system cannot open the specified object.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-190">**1323**</span><span class="sxs-lookup"><span data-stu-id="1c858-190">**1323**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-191">Не удалось обновить пароль.</span><span class="sxs-lookup"><span data-stu-id="1c858-191">Unable to update the password.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-192">**1326**</span><span class="sxs-lookup"><span data-stu-id="1c858-192">**1326**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-193">Ошибка входа: неизвестное имя пользователя или неправильный пароль.</span><span class="sxs-lookup"><span data-stu-id="1c858-193">Logon failure: unknown username or bad password.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-194">**1355**</span><span class="sxs-lookup"><span data-stu-id="1c858-194">**1355**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-195">Указанный домен не существует, или к нему не удалось подключиться.</span><span class="sxs-lookup"><span data-stu-id="1c858-195">The specified domain either does not exist or could not be contacted.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-196">**2224**</span><span class="sxs-lookup"><span data-stu-id="1c858-196">**2224**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-197">Учетная запись уже существует.</span><span class="sxs-lookup"><span data-stu-id="1c858-197">The account already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-198">**2691**</span><span class="sxs-lookup"><span data-stu-id="1c858-198">**2691**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-199">Компьютер уже присоединен к домену.</span><span class="sxs-lookup"><span data-stu-id="1c858-199">The machine is already joined to the domain.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-200">**2692**</span><span class="sxs-lookup"><span data-stu-id="1c858-200">**2692**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-201">Компьютер в настоящее время не присоединен к домену.</span><span class="sxs-lookup"><span data-stu-id="1c858-201">The machine is not currently joined to a domain.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-202">**\_ \_ требуется зашифрованное \_ Подключение WBEM E \_**</span><span class="sxs-lookup"><span data-stu-id="1c858-202">**WBEM\_E\_ENCRYPTED\_CONNECTION\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-203">0x80041087</span><span class="sxs-lookup"><span data-stu-id="1c858-203">0x80041087</span></span>

<span data-ttu-id="1c858-204">Указаны *пароль* и *имя пользователя* , но уровень проверки подлинности не является **\_ \_ AUTHN \_ уровнем \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="1c858-204">*Password* and *UserName* are specified but the authentication level is not **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="1c858-205">Для Visual Basic возвращается **вбемерренкриптедконнектионрекуиред** .</span><span class="sxs-lookup"><span data-stu-id="1c858-205">For Visual Basic, **wbemErrEncryptedConnectionRequired** is returned.</span></span>

</dd> <dt>

<span data-ttu-id="1c858-206">**Другое**</span><span class="sxs-lookup"><span data-stu-id="1c858-206">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="1c858-207">1 4294967295</span><span class="sxs-lookup"><span data-stu-id="1c858-207">1 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c858-208">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c858-208">Remarks</span></span>

<span data-ttu-id="1c858-209">При перемещении компьютера из домена в рабочую группу необходимо удалить компьютер из домена (с помощью вызова [**унжоиндомаинорворкграуп**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) перед вызовом этого метода для приподключения к Рабочей группе (с вызовом **жоиндомаинорворкграуп**).</span><span class="sxs-lookup"><span data-stu-id="1c858-209">When moving a computer from a domain to a workgroup, you must remove the computer from the domain (with a call to [**UnjoinDomainOrWorkgroup**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) before calling this method to join a workgroup (with a call to **JoinDomainOrWorkgroup**).</span></span> <span data-ttu-id="1c858-210">После вызова этого метода перезагрузите затронутый компьютер, чтобы применить изменения.</span><span class="sxs-lookup"><span data-stu-id="1c858-210">After calling this method, restart the affected computer to apply the changes.</span></span>

<span data-ttu-id="1c858-211">*Имя пользователя* и *пароль* можно оставить **пустыми**.</span><span class="sxs-lookup"><span data-stu-id="1c858-211">*UserName* and *Password* can be left **null**.</span></span> <span data-ttu-id="1c858-212">Однако проверка подлинности соединения с WMI должна быть равна 6 в скрипте или **вбемаусентикатионлевелпктприваци** в Visual Basic и других языках, которые могут использовать библиотеку [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) .</span><span class="sxs-lookup"><span data-stu-id="1c858-212">However, the authentication of the connection to WMI must be 6 in script or **WbemAuthenticationLevelPktPrivacy** in Visual Basic and other languages that can use the [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) library.</span></span> <span data-ttu-id="1c858-213">Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span><span class="sxs-lookup"><span data-stu-id="1c858-213">For more information, see [Setting the Default Process Security Level Using VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).</span></span>

<span data-ttu-id="1c858-214">В C++ для подключения к прокси-серверу [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) [**на**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) **уровне RPC \_ C \_ AUTHN \_ уровня \_ \_** "для всех процессов или в методе [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)можно задать конфиденциальность.</span><span class="sxs-lookup"><span data-stu-id="1c858-214">In C++, set the authentication at **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** either in [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity), for the entire process, or in [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), for a connection to the [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) proxy.</span></span> <span data-ttu-id="1c858-215">Дополнительные сведения см. в статьях [Настройка проверки подлинности с помощью C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) и [Настройка параметров безопасности для IWbemServices и других прокси-серверов](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span><span class="sxs-lookup"><span data-stu-id="1c858-215">For more information, see [Setting Authentication Using C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) and [Setting the Security on IWbemServices and Other Proxies](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).</span></span>

## <a name="examples"></a><span data-ttu-id="1c858-216">Примеры</span><span class="sxs-lookup"><span data-stu-id="1c858-216">Examples</span></span>

<span data-ttu-id="1c858-217">В примере [Присоединение компьютера к домену](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell присоединяет компьютер к домену.</span><span class="sxs-lookup"><span data-stu-id="1c858-217">The [Join a computer to a domain](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell example joins a computer to a domain.</span></span>

<span data-ttu-id="1c858-218">Следующий пример кода VBScript присоединяет компьютер к домену и создает учетную запись компьютера в Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c858-218">The following VBScript code example joins a computer to a domain and creates the computer's account in Active Directory.</span></span>


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



## <a name="requirements"></a><span data-ttu-id="1c858-219">Требования</span><span class="sxs-lookup"><span data-stu-id="1c858-219">Requirements</span></span>



| <span data-ttu-id="1c858-220">Требование</span><span class="sxs-lookup"><span data-stu-id="1c858-220">Requirement</span></span> | <span data-ttu-id="1c858-221">Значение</span><span class="sxs-lookup"><span data-stu-id="1c858-221">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c858-222">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c858-222">Minimum supported client</span></span><br/> | <span data-ttu-id="1c858-223">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c858-223">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c858-224">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c858-224">Minimum supported server</span></span><br/> | <span data-ttu-id="1c858-225">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c858-225">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c858-226">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c858-226">Namespace</span></span><br/>                | <span data-ttu-id="1c858-227">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c858-227">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c858-228">MOF</span><span class="sxs-lookup"><span data-stu-id="1c858-228">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c858-229"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c858-229"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c858-230">DLL</span><span class="sxs-lookup"><span data-stu-id="1c858-230">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c858-231"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c858-231"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c858-232">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c858-232">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c858-233">**Win32 \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1c858-233">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
</dt> <dt>

[<span data-ttu-id="1c858-234">**Метод Унжоиндомаинорворкграуп**</span><span class="sxs-lookup"><span data-stu-id="1c858-234">**UnjoinDomainOrWorkgroup method**</span></span>](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

