---
title: Класс Win32_TSLogonSetting
description: Определяет параметры конфигурации для \_ класса терминала Win32, связанного с входом клиента.
ms.assetid: a2ccb419-da1a-44d1-8a7a-4d0266fc1be8
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSLogonSetting службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSLogonSetting, описание
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting
- Win32_TSLogonSetting.Caption
- Win32_TSLogonSetting.Description
- Win32_TSLogonSetting.InstallDate
- Win32_TSLogonSetting.Name
- Win32_TSLogonSetting.Status
- Win32_TSLogonSetting.TerminalName
- Win32_TSLogonSetting.ClientLogonInfoPolicy
- Win32_TSLogonSetting.Domain
- Win32_TSLogonSetting.Password
- Win32_TSLogonSetting.PolicySourceDomain
- Win32_TSLogonSetting.PolicySourcePromptForPassword
- Win32_TSLogonSetting.PolicySourceUserName
- Win32_TSLogonSetting.PromptForPassword
- Win32_TSLogonSetting.UserName
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e656f3913bb7320253dc9dbca6710f37e0cbdded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415832"
---
# <a name="win32_tslogonsetting-class"></a><span data-ttu-id="ad6a6-105">\_Класс Win32 тслогонсеттинг</span><span class="sxs-lookup"><span data-stu-id="ad6a6-105">Win32\_TSLogonSetting class</span></span>

<span data-ttu-id="ad6a6-106">Класс **WMI \_ Тслогонсеттинг для Win32** определяет параметры конфигурации для класса [**\_ терминала Win32**](win32-terminal.md) , связанного с входом клиента.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-106">The **Win32\_TSLogonSetting** WMI class defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

<span data-ttu-id="ad6a6-107">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="ad6a6-108">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad6a6-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad6a6-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSLOGONSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSLogonSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientLogonInfoPolicy;
  string   Domain;
  string   Password;
  uint32   PolicySourceDomain;
  uint32   PolicySourcePromptForPassword;
  uint32   PolicySourceUserName;
  uint32   PromptForPassword;
  string   UserName;
};
```

## <a name="members"></a><span data-ttu-id="ad6a6-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ad6a6-110">Members</span></span>

<span data-ttu-id="ad6a6-111">Класс **Win32 \_ тслогонсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ad6a6-111">The **Win32\_TSLogonSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="ad6a6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ad6a6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="ad6a6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad6a6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ad6a6-114">Методы</span><span class="sxs-lookup"><span data-stu-id="ad6a6-114">Methods</span></span>

<span data-ttu-id="ad6a6-115">Класс **Win32 \_ тслогонсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-115">The **Win32\_TSLogonSetting** class has these methods.</span></span>



| <span data-ttu-id="ad6a6-116">Метод</span><span class="sxs-lookup"><span data-stu-id="ad6a6-116">Method</span></span>                                                                    | <span data-ttu-id="ad6a6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="ad6a6-117">Description</span></span>                                                                    |
|:--------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="ad6a6-118">**експлиЦитлогон**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-118">**ExplicitLogon**</span></span>](win32-tslogonsetting-explicitlogon.md)               | <span data-ttu-id="ad6a6-119">Задает имя пользователя, пароль и учетные данные для проверки подлинности домена.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-119">Sets the UserName, Password, and Domain authentication credentials.</span></span><br/> |
| [<span data-ttu-id="ad6a6-120">**сетпромптфорпассворд**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-120">**SetPromptForPassword**</span></span>](win32-tslogonsetting-setpromptforpassword.md) | <span data-ttu-id="ad6a6-121">Задает свойство **промптфорпассворд** .</span><span class="sxs-lookup"><span data-stu-id="ad6a6-121">Sets the **PromptForPassword** property.</span></span><br/>                            |



 

### <a name="properties"></a><span data-ttu-id="ad6a6-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad6a6-122">Properties</span></span>

<span data-ttu-id="ad6a6-123">Класс **Win32 \_ тслогонсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-123">The **Win32\_TSLogonSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad6a6-124">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-128">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="ad6a6-129">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-130">**клиентлогонинфополици**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-130">**ClientLogonInfoPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-131">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ad6a6-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-133">Политика, используемая сервером для определения параметров подключения.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-133">The policy the server uses to determine connection settings.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="ad6a6-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**На пользователя** (0)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-134"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad6a6-135">Действуют индивидуальные параметры подключения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-135">Individual user connection settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="ad6a6-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Переопределение сервера** (1)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-136"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad6a6-137">Параметры подключения отдельных пользователей переопределяются сервером.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-137">Individual user connection settings are overridden by the server.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-141">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-141">Description of the object.</span></span>

<span data-ttu-id="ad6a6-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-142">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-143">**Доменная**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-143">**Domain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-146">Учетные данные проверки подлинности для входа в домен пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-146">The user's domain logon authentication credential.</span></span> <span data-ttu-id="ad6a6-147">Это домен, в котором находится компьютер пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-147">This is the domain in which the user's computer resides.</span></span> <span data-ttu-id="ad6a6-148">Длина этого свойства не может превышать 17 символов.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-148">This property cannot be longer than 17 characters.</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-149">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-149">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-150">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-152">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="ad6a6-152">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-153">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-153">The date the object was installed.</span></span> <span data-ttu-id="ad6a6-154">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-154">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="ad6a6-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-159">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-159">The name of the object.</span></span>

<span data-ttu-id="ad6a6-160">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-161">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-161">**Password**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-164">Учетные данные проверки подлинности входа для пароля пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-164">The user's password logon authentication credential.</span></span> <span data-ttu-id="ad6a6-165">Длина этого свойства не может превышать 14 символов.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-165">This property cannot be longer than 14 characters.</span></span> <span data-ttu-id="ad6a6-166">При запросе этого свойства рекомендуется установить уровень безопасности "конфиденциальность пакетов" (Вбемаусентикатионлевелпктприваци = 6).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-166">It is recommended that you set the security level to packet privacy (wbemAuthenticationLevelPktPrivacy = 6) if you query this property.</span></span> <span data-ttu-id="ad6a6-167">Это связано с тем, что пароль не шифруется в сети без такого уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-167">This is because the password is not encrypted on the wire without this level of security.</span></span> <span data-ttu-id="ad6a6-168">Дополнительные сведения о настройке уровней безопасности см. в разделе [Настройка безопасности процесса клиентского приложения](/windows/desktop/WmiSdk/setting-client-application-process-security) в документации по пакету SDK для инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-168">For more information about setting security levels, see [Setting Client Application Process Security](/windows/desktop/WmiSdk/setting-client-application-process-security) in the WMI SDK documentation.</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-169">**полицисаурцедомаин**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-169">**PolicySourceDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-170">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-170">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-171">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-172">Указывает, настроено ли свойство **домена** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-172">Indicates whether the **Domain** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad6a6-173">0</span><span class="sxs-lookup"><span data-stu-id="ad6a6-173">0</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-174">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad6a6-174">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-175">1</span><span class="sxs-lookup"><span data-stu-id="ad6a6-175">1</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-176">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad6a6-176">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-177">2</span><span class="sxs-lookup"><span data-stu-id="ad6a6-177">2</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-178">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad6a6-178">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-179">**полицисаурцепромптфорпассворд**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-179">**PolicySourcePromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-180">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-182">Указывает, настроено ли свойство **промптфорпассворд** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-182">Indicates whether the **PromptForPassword** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad6a6-183">0</span><span class="sxs-lookup"><span data-stu-id="ad6a6-183">0</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-184">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad6a6-184">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-185">1</span><span class="sxs-lookup"><span data-stu-id="ad6a6-185">1</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-186">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad6a6-186">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-187">2</span><span class="sxs-lookup"><span data-stu-id="ad6a6-187">2</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-188">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad6a6-188">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-189">**полицисаурцеусернаме**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-189">**PolicySourceUserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-190">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-190">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-191">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-191">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-192">Указывает, настроено ли свойство **username** сервером, групповой политикой или по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-192">Indicates whether the **UserName** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="ad6a6-193">0</span><span class="sxs-lookup"><span data-stu-id="ad6a6-193">0</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-194">Сервер</span><span class="sxs-lookup"><span data-stu-id="ad6a6-194">Server</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-195">1</span><span class="sxs-lookup"><span data-stu-id="ad6a6-195">1</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-196">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="ad6a6-196">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-197">2</span><span class="sxs-lookup"><span data-stu-id="ad6a6-197">2</span></span>
</dt> <dd>

<span data-ttu-id="ad6a6-198">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="ad6a6-198">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-199">**промптфорпассворд**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-199">**PromptForPassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-200">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-200">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-201">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-202">Указывает, будет ли пользователь всегда запрашивать пароль при входе на сервер.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-202">Specifies whether the user is always prompted for a password while logging into the server.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="ad6a6-203"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-203"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="ad6a6-204">Пользователю не предлагается ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-204">The user is not prompted for a password.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="ad6a6-205"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-205"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="ad6a6-206">Пользователю предлагается ввести пароль.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-206">The user is prompted for a password.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-207">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-207">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-208">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-209">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-210">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="ad6a6-210">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-211">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-211">Current status of the object.</span></span> <span data-ttu-id="ad6a6-212">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-212">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="ad6a6-213">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-213">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="ad6a6-214">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="ad6a6-214">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="ad6a6-215">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-215">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="ad6a6-216">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-216">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="ad6a6-217">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-217">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="ad6a6-218">("ОК")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-218">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-219">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-219">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-220">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-220">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-221">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-221">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-222">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-222">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-223">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-223">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-224">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-224">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ad6a6-225">("Служба")</span><span class="sxs-lookup"><span data-stu-id="ad6a6-225">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ad6a6-226">**терминалнаме**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-226">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-227">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-228">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-229">Имя терминала.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-229">The name of the terminal.</span></span>

<span data-ttu-id="ad6a6-230">Это свойство наследуется из [**Win32 \_ терминалсеттинг**](win32-terminalsetting.md).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-230">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> <dt>

<span data-ttu-id="ad6a6-231">**UserName**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-231">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad6a6-232">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ad6a6-233">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad6a6-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ad6a6-234">Учетные данные проверки подлинности имени пользователя для входа.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-234">The user's user name logon authentication credential.</span></span> <span data-ttu-id="ad6a6-235">Это свойство не может содержать более 20 символов.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-235">This property cannot be longer than 20 characters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad6a6-236">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad6a6-236">Remarks</span></span>

<span data-ttu-id="ad6a6-237">Имейте в виду, что Винстатионс, связанный с сеансом консоли, не может получить доступ к методам и свойствам этого класса.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-237">Be aware that Winstations associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="ad6a6-238">Если предпринимается попытка сделать это, указав "Console" в качестве значения свойства Терминалнаме, методы этого объекта возвращают **WBEM \_ E \_ не \_ поддерживаются**.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-238">If an attempt is made to do so by specifying "Console" as the value of the TerminalName property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="ad6a6-239">Этот код ошибки возвращается, если станция окна пытается вызвать методы этого объекта для добавления или изменения свойств безопасности учетных записей LocalSystem, LocalService или NetworkService.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-239">This error code is returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="ad6a6-240">Чтобы подключиться к \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-240">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="ad6a6-241">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="ad6a6-241">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="ad6a6-242">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением 6.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-242">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="ad6a6-243">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-243">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="ad6a6-244">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-244">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ad6a6-245">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-245">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ad6a6-246">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="ad6a6-246">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ad6a6-247">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ad6a6-247">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad6a6-248">Требования</span><span class="sxs-lookup"><span data-stu-id="ad6a6-248">Requirements</span></span>



| <span data-ttu-id="ad6a6-249">Требование</span><span class="sxs-lookup"><span data-stu-id="ad6a6-249">Requirement</span></span> | <span data-ttu-id="ad6a6-250">Значение</span><span class="sxs-lookup"><span data-stu-id="ad6a6-250">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad6a6-251">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad6a6-251">Minimum supported client</span></span><br/> | <span data-ttu-id="ad6a6-252">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad6a6-252">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad6a6-253">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad6a6-253">Minimum supported server</span></span><br/> | <span data-ttu-id="ad6a6-254">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad6a6-254">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad6a6-255">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad6a6-255">Namespace</span></span><br/>                | <span data-ttu-id="ad6a6-256">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="ad6a6-256">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ad6a6-257">MOF</span><span class="sxs-lookup"><span data-stu-id="ad6a6-257">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad6a6-258"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad6a6-258"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad6a6-259">DLL</span><span class="sxs-lookup"><span data-stu-id="ad6a6-259">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad6a6-260"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad6a6-260"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad6a6-261">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad6a6-261">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad6a6-262">**\_Терминал Win32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-262">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dt>

[<span data-ttu-id="ad6a6-263">**\_Терминалсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="ad6a6-263">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

