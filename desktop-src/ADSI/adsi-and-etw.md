---
title: Трассировка событий в ADSI
description: В Windows Server 2008 и Windows Vista появилась трассировка событий в Active Directory интерфейсах служб (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- интерфейс ADSI трассировки событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654351"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="2da73-104">Трассировка событий в ADSI</span><span class="sxs-lookup"><span data-stu-id="2da73-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="2da73-105">В Windows Server 2008 и Windows Vista появилась [Трассировка событий](/windows/desktop/ETW/event-tracing-portal) в [Active Directory интерфейсах служб](active-directory-service-interfaces-adsi.md) (ADSI).</span><span class="sxs-lookup"><span data-stu-id="2da73-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="2da73-106">Некоторые области поставщика ADSI LDAP имеют базовую реализацию, которая является сложной или включает последовательность действий, что затрудняет диагностику проблем.</span><span class="sxs-lookup"><span data-stu-id="2da73-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="2da73-107">Для помощи в устранении неполадок, связанных с разработчиками приложений, в следующие области была добавлена трассировка событий.</span><span class="sxs-lookup"><span data-stu-id="2da73-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="2da73-108">Синтаксический анализ и загрузка схемы</span><span class="sxs-lookup"><span data-stu-id="2da73-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="2da73-109">Интерфейс IADs в ADSI требует, чтобы схема LDAP была кэширована на клиенте, чтобы атрибуты можно было правильно маршалировать (как описано в [модели схемы ADSI](adsi-schema-model.md)).</span><span class="sxs-lookup"><span data-stu-id="2da73-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="2da73-110">Для этого ADSI загружает схему для каждого процесса (и для каждого LDAP-сервера или домена) в память из файла схемы (. SCH), сохраненного на локальном диске, или путем его загрузки с LDAP-сервера.</span><span class="sxs-lookup"><span data-stu-id="2da73-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="2da73-111">Различные процессы на одном клиентском компьютере используют кэшированную схему на диске, если она доступна и применима.</span><span class="sxs-lookup"><span data-stu-id="2da73-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="2da73-112">Если схема не может быть получена с диска или с сервера, ADSI использует жестко закодированную схему по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2da73-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="2da73-113">В этом случае атрибуты, которые не являются частью этой схемы по умолчанию, не могут быть упакованы, и при получении этих атрибутов ADSI возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="2da73-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="2da73-114">Это может быть вызвано несколькими причинами, в том числе проблемами при анализе схемы и недостаточными привилегиями для загрузки схемы.</span><span class="sxs-lookup"><span data-stu-id="2da73-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="2da73-115">Часто бывает трудно определить, почему используется определенная схема по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2da73-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="2da73-116">Использование трассировки событий в этой области поможет вам быстрее диагностировать проблему и устранить ее.</span><span class="sxs-lookup"><span data-stu-id="2da73-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="2da73-117">Изменение и установка пароля</span><span class="sxs-lookup"><span data-stu-id="2da73-117">Changing and Setting the Password</span></span>

<span data-ttu-id="2da73-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) и [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) используют более одного механизма для выполнения запрошенной операции на основе доступной конфигурации (как описано в разделе [Настройка и изменение ПАРОЛЕЙ пользователей с помощью поставщика LDAP](setting-user-passwords-for-ldap-providers.md)).</span><span class="sxs-lookup"><span data-stu-id="2da73-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="2da73-119">При сбое **ChangePassword** и **SetPassword** может быть трудно определить причину, и трассировка событий поможет устранить проблемы с этими методами.</span><span class="sxs-lookup"><span data-stu-id="2da73-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="2da73-120">Кэш привязки ADSI</span><span class="sxs-lookup"><span data-stu-id="2da73-120">ADSI Bind Cache</span></span>

<span data-ttu-id="2da73-121">ADSI внутренне пытается повторно использовать LDAP-подключения везде, где это возможно (см. раздел [кэширование подключения](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="2da73-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="2da73-122">При устранении неполадок полезно отслеживать, было ли открыто новое соединение для связи с сервером или использовалось ли существующее соединение.</span><span class="sxs-lookup"><span data-stu-id="2da73-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="2da73-123">Также может быть полезно отслеживать жизненный цикл кэша подключений (иногда называемый кэшем привязки), его создание или закрытие и наличие ссылки на соединение.</span><span class="sxs-lookup"><span data-stu-id="2da73-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="2da73-124">В случае [бессерверной привязки](/windows/desktop/AD/serverless-binding-and-rootdse)ADSI вызывает локатор контроллера домена, чтобы выбрать сервер для домена контекста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2da73-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="2da73-125">Затем ADSI поддерживает кэш сопоставления сервера домена для последующих подключений.</span><span class="sxs-lookup"><span data-stu-id="2da73-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="2da73-126">Трассировка событий позволяет отслеживать выбор контроллера домена и, следовательно, помогает устранять проблемы, связанные с подключением.</span><span class="sxs-lookup"><span data-stu-id="2da73-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="2da73-127">Включение трассировки и запуск сеанса трассировки</span><span class="sxs-lookup"><span data-stu-id="2da73-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="2da73-128">Чтобы включить трассировку ADSI, создайте следующий раздел реестра:</span><span class="sxs-lookup"><span data-stu-id="2da73-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="2da73-129">**HKey \_ Локальная система \_ машин** \\  \\ **CurrentControlSet** \\ **Services** \\ **ADSI**, \\ **Трассировка** \\ ***processName***</span><span class="sxs-lookup"><span data-stu-id="2da73-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="2da73-130">*ProcessName* — это полное имя процесса, который необходимо отследить, включая его расширение (например, "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="2da73-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="2da73-131">Кроме того, в этом разделе можно поместить необязательное значение типа **DWORD** с именем PID.</span><span class="sxs-lookup"><span data-stu-id="2da73-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="2da73-132">Настоятельно рекомендуется задать это значение и, таким образом, отслеживать только конкретный процесс.</span><span class="sxs-lookup"><span data-stu-id="2da73-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="2da73-133">В противном случае будут отслеживаться все экземпляры приложения, заданные параметром *processName* .</span><span class="sxs-lookup"><span data-stu-id="2da73-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="2da73-134">Затем выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2da73-134">Then execute the following command:</span></span>

<span data-ttu-id="2da73-135">**tracelog.exe-Start** *sessionname*  \* *-GUID \# \* \* \* \* \_ GUID поставщика* **-f** *имя_файла* **-флаг** *флагов трассировки* **-Level** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="2da73-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="2da73-136">*sessionname* — это просто произвольный идентификатор, который используется для обозначения сеанса трассировки (в дальнейшем необходимо будет ссылаться на это имя сеанса, когда вы останавливаете сеанс трассировки).</span><span class="sxs-lookup"><span data-stu-id="2da73-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="2da73-137">Идентификатор GUID для поставщика отслеживания ADSI — "7288c9f8-d63c-4932-A345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="2da73-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="2da73-138">*filename* указывает файл журнала, в который будут записываться события.</span><span class="sxs-lookup"><span data-stu-id="2da73-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="2da73-139">*флагов трассировки* должно иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2da73-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="2da73-140">**ОТЛАДКа \_ схемы**</span><span class="sxs-lookup"><span data-stu-id="2da73-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="2da73-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2da73-141">0x00000001</span></span><br/> |
| <span data-ttu-id="2da73-142">**ОТЛАДКа \_ чанжепвд**</span><span class="sxs-lookup"><span data-stu-id="2da73-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="2da73-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2da73-143">0x00000002</span></span><br/> |
| <span data-ttu-id="2da73-144">**ОТЛАДКа \_ сетпвд**</span><span class="sxs-lookup"><span data-stu-id="2da73-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="2da73-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2da73-145">0x00000004</span></span><br/> |
| <span data-ttu-id="2da73-146">**ОТЛАДКа \_ биндкаче**</span><span class="sxs-lookup"><span data-stu-id="2da73-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="2da73-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2da73-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="2da73-148">Эти флаги определяют, какие методы [ADSI](active-directory-service-interfaces-adsi.md) будут трассироваться, в соответствии со следующей таблицей.</span><span class="sxs-lookup"><span data-stu-id="2da73-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2da73-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="2da73-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="2da73-150">лдапжетсчема</span><span class="sxs-lookup"><span data-stu-id="2da73-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="2da73-151">жетсчемаинфотиме</span><span class="sxs-lookup"><span data-stu-id="2da73-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="2da73-152">лдапреадсчемаинфофромсервер</span><span class="sxs-lookup"><span data-stu-id="2da73-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="2da73-153">процесссчемаинфо</span><span class="sxs-lookup"><span data-stu-id="2da73-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="2da73-154">хелперреадлдапсчемаинфо</span><span class="sxs-lookup"><span data-stu-id="2da73-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="2da73-155">процессклассинфоаррай</span><span class="sxs-lookup"><span data-stu-id="2da73-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="2da73-156">реадсчемаинфофромрегистри</span><span class="sxs-lookup"><span data-stu-id="2da73-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="2da73-157">сторесчемаинфофромрегистри</span><span class="sxs-lookup"><span data-stu-id="2da73-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="2da73-158">аттрибутетипедескриптион</span><span class="sxs-lookup"><span data-stu-id="2da73-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="2da73-159">обжектклассдескриптион</span><span class="sxs-lookup"><span data-stu-id="2da73-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="2da73-160">дитконтентруледескриптион</span><span class="sxs-lookup"><span data-stu-id="2da73-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="2da73-161">директористринг</span><span class="sxs-lookup"><span data-stu-id="2da73-161">DirectoryString</span></span></li>
<li><span data-ttu-id="2da73-162">директористрингс</span><span class="sxs-lookup"><span data-stu-id="2da73-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="2da73-163">дитконтентруледескриптион</span><span class="sxs-lookup"><span data-stu-id="2da73-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2da73-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="2da73-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="2da73-165">Кадсусер:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="2da73-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2da73-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="2da73-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="2da73-167">Кадсусер:: SetPassword</span><span class="sxs-lookup"><span data-stu-id="2da73-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2da73-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="2da73-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="2da73-169">жетсервербаседобжект</span><span class="sxs-lookup"><span data-stu-id="2da73-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="2da73-170">жетсерверлессбаседобжект</span><span class="sxs-lookup"><span data-stu-id="2da73-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="2da73-171">жетгкдомаиннаме</span><span class="sxs-lookup"><span data-stu-id="2da73-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="2da73-172">жетдефаултдомаиннаме</span><span class="sxs-lookup"><span data-stu-id="2da73-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="2da73-173">жетусердомаинфлатнаме</span><span class="sxs-lookup"><span data-stu-id="2da73-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="2da73-174">биндкачелукуп</span><span class="sxs-lookup"><span data-stu-id="2da73-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="2da73-175">екуивалентпортнумберс</span><span class="sxs-lookup"><span data-stu-id="2da73-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="2da73-176">канкредентиалсбереусед</span><span class="sxs-lookup"><span data-stu-id="2da73-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="2da73-177">биндкачеадд</span><span class="sxs-lookup"><span data-stu-id="2da73-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="2da73-178">биндкачеаддреф</span><span class="sxs-lookup"><span data-stu-id="2da73-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="2da73-179">аддреферраллинк</span><span class="sxs-lookup"><span data-stu-id="2da73-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="2da73-180">коммонремовинтри</span><span class="sxs-lookup"><span data-stu-id="2da73-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="2da73-181">биндкачедерефхелпер</span><span class="sxs-lookup"><span data-stu-id="2da73-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="2da73-182">нотифиневконнектион</span><span class="sxs-lookup"><span data-stu-id="2da73-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="2da73-183">куерифорконнектион</span><span class="sxs-lookup"><span data-stu-id="2da73-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="2da73-184">лдапопенбиндвискредентиалс</span><span class="sxs-lookup"><span data-stu-id="2da73-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="2da73-185">лдапопенбиндвисдефаулткредентиалс</span><span class="sxs-lookup"><span data-stu-id="2da73-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2da73-186">Можно объединить флаги, объединив соответствующие биты в аргументе *флагов трассировки* .</span><span class="sxs-lookup"><span data-stu-id="2da73-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="2da73-187">Например, чтобы указать **отладочную \_ схему** и флаги **отладки \_ биндкаче** , соответствующее значение *флагов трассировки* будет 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="2da73-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="2da73-188">Наконец, флаг *TraceLevel* должен иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="2da73-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="2da73-189">**\_ошибка уровня \_ трассировки**</span><span class="sxs-lookup"><span data-stu-id="2da73-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="2da73-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2da73-190">0x00000002</span></span><br/> |
| <span data-ttu-id="2da73-191">**\_ \_ сведения об уровне трассировки**</span><span class="sxs-lookup"><span data-stu-id="2da73-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="2da73-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2da73-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="2da73-193">**Трассировка событий \_ \_Сведения об уровне** приводят к тому, что процесс трассировки записывает все события, в то время как **\_ \_ ошибка уровня трассировки** приводит к тому, что процесс трассировки записывает только события ошибок.</span><span class="sxs-lookup"><span data-stu-id="2da73-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="2da73-194">Чтобы завершить трассировку, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2da73-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="2da73-195">**tracelog.exe-закончить** *сеанс*</span><span class="sxs-lookup"><span data-stu-id="2da73-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="2da73-196">В предыдущем примере имя *сеанса sessionname* совпадает с именем, предоставленным командой, в которой был запущен раздел трассировки.</span><span class="sxs-lookup"><span data-stu-id="2da73-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="2da73-197">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2da73-197">Remarks</span></span>

<span data-ttu-id="2da73-198">Более эффективно отслеживать только определенные процессы, указывая определенный PID, чем отслеживать все процессы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="2da73-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="2da73-199">Если необходимо выполнить трассировку нескольких приложений на одном компьютере, это может повлиять на производительность. в разделах кода, ориентированных на производительность, содержится важный результат отладки.</span><span class="sxs-lookup"><span data-stu-id="2da73-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="2da73-200">Кроме того, администраторы должны быть внимательны, чтобы правильно задавать разрешения для файлов журнала при трассировке нескольких процессов. в противном случае любой пользователь сможет читать журналы трассировки, а другие пользователи смогут отслеживать процессы, содержащие безопасную информацию.</span><span class="sxs-lookup"><span data-stu-id="2da73-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="2da73-201">Например, предположим, что администратор настроит трассировку для приложения «Test.exe» и не укажет идентификатор процесса в реестре для трассировки нескольких экземпляров процесса.</span><span class="sxs-lookup"><span data-stu-id="2da73-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="2da73-202">Теперь другой пользователь хочет выполнить трассировку приложения "Secure.exe".</span><span class="sxs-lookup"><span data-stu-id="2da73-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="2da73-203">Если файлы журнала трассировки не ограничены должным образом, все, что нужно сделать, — это переименовать "Secure.exe" в "Test.exe" и будет отслеживаться.</span><span class="sxs-lookup"><span data-stu-id="2da73-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="2da73-204">Как правило, при устранении неполадок рекомендуется отслеживать только определенные процессы, а также удалять раздел реестра трассировки, как только это делается.</span><span class="sxs-lookup"><span data-stu-id="2da73-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="2da73-205">Поскольку при включении трассировки событий создаются дополнительные файлы журналов, администраторы должны внимательно отслеживать размеры файлов журнала. нехватка дискового пространства на локальном компьютере может привести к отказу в обслуживании.</span><span class="sxs-lookup"><span data-stu-id="2da73-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="2da73-206">Примеры сценариев</span><span class="sxs-lookup"><span data-stu-id="2da73-206">Example Scenarios</span></span>

<span data-ttu-id="2da73-207">Сценарий 1. администратор видит непредвиденную ошибку в приложении, которое устанавливает пароли для учетных записей пользователей, поэтому для решения проблемы с помощью трассировки событий необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="2da73-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="2da73-208">Напишите сценарий, который воссоздает проблему, и создайте раздел реестра.</span><span class="sxs-lookup"><span data-stu-id="2da73-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="2da73-209">**HKey \_ \_** \\  \\  \\  \\  \\  \\ **cscript.exeа** трассировки ADSI CurrentControlSet Services System на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="2da73-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="2da73-210">Запустите сеанс трассировки, установив для *флагов трассировки* значение 0X2 (**Отладка \_ чанжепассвд**) и *TraceLevel* в 0x4 **( \_ \_ сведения на уровне трассировки**), используя следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2da73-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="2da73-211">**tracelog.exe-Start скрипттраце-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-флаг 0x2 — уровень 0x4**</span><span class="sxs-lookup"><span data-stu-id="2da73-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="2da73-212">Запустите cscript.exe с помощью тестового скрипта, чтобы воспроизвести проблему, а затем завершите сеанс трассировки:</span><span class="sxs-lookup"><span data-stu-id="2da73-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="2da73-213">**tracelog.exe скрипттраце**</span><span class="sxs-lookup"><span data-stu-id="2da73-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="2da73-214">Удаление раздела реестра</span><span class="sxs-lookup"><span data-stu-id="2da73-214">Delete the registry key</span></span>

    <span data-ttu-id="2da73-215">**HKey \_ \_** \\  \\  \\  \\  \\  \\ **cscript.exeа** трассировки ADSI CurrentControlSet Services System на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="2da73-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="2da73-216">Запустите средство ETW Tracerpt.exe, чтобы проанализировать данные трассировки из журнала:</span><span class="sxs-lookup"><span data-stu-id="2da73-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="2da73-217">**tracelog.exe-Start скрипттраце-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-флаг 0x2 — уровень 0x4**</span><span class="sxs-lookup"><span data-stu-id="2da73-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="2da73-218">Сценарий 2. администратор хочет отслеживать операции анализа и скачивания схемы в приложении [ASP](https://msdn.microsoft.com/asp.net/default.aspx) с именем w3wp.exe, которое уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="2da73-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="2da73-219">Для этого администратор должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2da73-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="2da73-220">Создание раздела реестра</span><span class="sxs-lookup"><span data-stu-id="2da73-220">Create the registry key</span></span>

    <span data-ttu-id="2da73-221">**HKey \_ \_** \\  \\  \\  \\  \\  \\ **w3wp.exeа** трассировки ADSI CurrentControlSet Services System на локальном компьютере</span><span class="sxs-lookup"><span data-stu-id="2da73-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="2da73-222">в этом разделе Создайте значение типа DWORD с именем PID и задайте для него идентификатор процесса экземпляра w3wp.exe, который в данный момент выполняется на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="2da73-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="2da73-223">Затем они создают сеанс трассировки, устанавливая для *флагов трассировки* значение 0x1 **( \_ схема отладки**) и *TraceLevel* в 0x4 **( \_ \_ сведения на уровне трассировки**):</span><span class="sxs-lookup"><span data-stu-id="2da73-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="2da73-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ w3wp. ETL-флаг 0x1 — уровень 0x4**</span><span class="sxs-lookup"><span data-stu-id="2da73-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="2da73-225">Воспроизведите операцию, требующую устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="2da73-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="2da73-226">Завершение сеанса трассировки:</span><span class="sxs-lookup"><span data-stu-id="2da73-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="2da73-227">**tracelog.exe w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="2da73-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="2da73-228">Удалите раздел реестра **hKey \_ локальный \_ компьютер** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Трассировка** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="2da73-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="2da73-229">Запустите средство ETW tracerpt.exe, чтобы проанализировать данные трассировки из журнала:</span><span class="sxs-lookup"><span data-stu-id="2da73-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="2da73-230">**tracerpt.exe. \\ w3wp. ETL-o-отчет**</span><span class="sxs-lookup"><span data-stu-id="2da73-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

