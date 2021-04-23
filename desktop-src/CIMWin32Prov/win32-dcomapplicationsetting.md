---
description: '&Win32 \_ дкомаппликатионсеттинг \# 8194; Класс WMI представляет параметры DCOM-приложения.'
ms.assetid: afa23faa-bf4d-4f54-9ee9-227956ff3292
ms.tgt_platform: multiple
title: Класс Win32_DCOMApplicationSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DCOMApplicationSetting
- Win32_DCOMApplicationSetting.Caption
- Win32_DCOMApplicationSetting.Description
- Win32_DCOMApplicationSetting.SettingID
- Win32_DCOMApplicationSetting.AppID
- Win32_DCOMApplicationSetting.AuthenticationLevel
- Win32_DCOMApplicationSetting.CustomSurrogate
- Win32_DCOMApplicationSetting.EnableAtStorageActivation
- Win32_DCOMApplicationSetting.LocalService
- Win32_DCOMApplicationSetting.RemoteServerName
- Win32_DCOMApplicationSetting.RunAsUser
- Win32_DCOMApplicationSetting.ServiceParameters
- Win32_DCOMApplicationSetting.UseSurrogate
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 085304c5319811ba87979124613c7d8e83fd7479
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656061"
---
# <a name="win32_dcomapplicationsetting-class"></a><span data-ttu-id="7b940-103">\_Класс Win32 дкомаппликатионсеттинг</span><span class="sxs-lookup"><span data-stu-id="7b940-103">Win32\_DCOMApplicationSetting class</span></span>

<span data-ttu-id="7b940-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ дкомаппликатионсеттинг для Win32** представляет параметры DCOM-приложения.</span><span class="sxs-lookup"><span data-stu-id="7b940-104">The **Win32\_DCOMApplicationSetting** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents the settings of a DCOM application.</span></span> <span data-ttu-id="7b940-105">В нем содержатся параметры конфигурации DCOM, связанные с ключом **AppID** в реестре.</span><span class="sxs-lookup"><span data-stu-id="7b940-105">It contains DCOM configuration options associated with the **AppID** key in the registry.</span></span> <span data-ttu-id="7b940-106">Эти параметры действительны для компонентов, логически сгруппированных в данном классе приложения.</span><span class="sxs-lookup"><span data-stu-id="7b940-106">These options are valid on the components logically grouped under the given application class.</span></span>

<span data-ttu-id="7b940-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7b940-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="7b940-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7b940-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b940-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b940-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{E5D8A561-F6C0-11d2-B35E-00105A1F8569}"), AMENDMENT]
class Win32_DCOMApplicationSetting : Win32_COMSetting
{
  string  Caption;
  string  Description;
  string  SettingID;
  string  AppID;
  uint32  AuthenticationLevel;
  string  CustomSurrogate;
  boolean EnableAtStorageActivation;
  string  LocalService;
  string  RemoteServerName;
  string  RunAsUser;
  string  ServiceParameters;
  boolean UseSurrogate;
};
```

## <a name="members"></a><span data-ttu-id="7b940-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7b940-110">Members</span></span>

<span data-ttu-id="7b940-111">Класс **Win32 \_ дкомаппликатионсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b940-111">The **Win32\_DCOMApplicationSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="7b940-112">Методы</span><span class="sxs-lookup"><span data-stu-id="7b940-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b940-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b940-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b940-114">Методы</span><span class="sxs-lookup"><span data-stu-id="7b940-114">Methods</span></span>

<span data-ttu-id="7b940-115">Класс **Win32 \_ дкомаппликатионсеттинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7b940-115">The **Win32\_DCOMApplicationSetting** class has these methods.</span></span>



| <span data-ttu-id="7b940-116">Метод</span><span class="sxs-lookup"><span data-stu-id="7b940-116">Method</span></span>                                                                                                                        | <span data-ttu-id="7b940-117">Описание</span><span class="sxs-lookup"><span data-stu-id="7b940-117">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b940-118">**жетакцесссекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-118">**GetAccessSecurityDescriptor**</span></span>](getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="7b940-119">Возвращает дескриптор безопасности, управляющий доступом к приложению DCOM.</span><span class="sxs-lookup"><span data-stu-id="7b940-119">Gets the security descriptor that controls who is allowed to access a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="7b940-120">**жетконфигуратионсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-120">**GetConfigurationSecurityDescriptor**</span></span>](getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="7b940-121">Возвращает дескриптор безопасности, определяющий, кому разрешено настраивать DCOM-приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-121">Gets the security descriptor that controls who is allowed to configure a DCOM application.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="7b940-122">**жетлаунчсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-122">**GetLaunchSecurityDescriptor**</span></span>](getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting.md)                      | <span data-ttu-id="7b940-123">Возвращает дескриптор безопасности, определяющий, кому разрешено запускать DCOM-приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-123">Gets the security descriptor that controls who is allowed to launch a DCOM application.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="7b940-124">**сетакцесссекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-124">**SetAccessSecurityDescriptor**</span></span>](setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="7b940-125">Обновляет дескриптор безопасности доступа DCOM-приложения с новым дескриптором безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7b940-125">Updates the access security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |
| [<span data-ttu-id="7b940-126">**сетконфигуратионсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-126">**SetConfigurationSecurityDescriptor**</span></span>](setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md) | <span data-ttu-id="7b940-127">Обновляет дескриптор безопасности конфигурации приложения DCOM с помощью нового дескриптора безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7b940-127">Updates the configuration security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/> |
| [<span data-ttu-id="7b940-128">**сетлаунчсекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="7b940-128">**SetLaunchSecurityDescriptor**</span></span>](setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting.md)               | <span data-ttu-id="7b940-129">Обновляет дескриптор безопасности запуска приложения DCOM с помощью нового дескриптора безопасности, который определяется экземпляром класса [**\_ SecurityDescriptor Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) .</span><span class="sxs-lookup"><span data-stu-id="7b940-129">Updates the launch security descriptor of the DCOM application with a new security descriptor that is defined by an instance of the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class.</span></span><br/>        |



 

### <a name="properties"></a><span data-ttu-id="7b940-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b940-130">Properties</span></span>

<span data-ttu-id="7b940-131">Класс **Win32 \_ дкомаппликатионсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b940-131">The **Win32\_DCOMApplicationSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b940-132">**AppID**</span><span class="sxs-lookup"><span data-stu-id="7b940-132">**AppID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-135">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ . \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ AppID \\ \\ {GUID} \[ Default \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[Default\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-136">Глобальный уникальный идентификатор (GUID) для этого DCOM-приложения.</span><span class="sxs-lookup"><span data-stu-id="7b940-136">Globally unique identifier (GUID) for this DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-137">**аусентикатионлевел**</span><span class="sxs-lookup"><span data-stu-id="7b940-137">**AuthenticationLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b940-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7b940-139">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b940-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ аусентикатионлевел \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[AuthenticationLevel\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-141">Минимальный уровень проверки подлинности клиента, необходимый для этого COM-сервера.</span><span class="sxs-lookup"><span data-stu-id="7b940-141">Minimum client authentication level required by this COM server.</span></span> <span data-ttu-id="7b940-142">Если **значение равно NULL**, используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7b940-142">If **NULL**, the default values are used.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="7b940-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Нет** (1)</span><span class="sxs-lookup"><span data-stu-id="7b940-143"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (1)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-144">Нет (проверка подлинности не выполняется)</span><span class="sxs-lookup"><span data-stu-id="7b940-144">None (no authentication is performed)</span></span>

</dd> <dt>

<span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>

<span data-ttu-id="7b940-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Подключение** (2)</span><span class="sxs-lookup"><span data-stu-id="7b940-145"><span id="Connect"></span><span id="connect"></span><span id="CONNECT"></span>**Connect** (2)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-146">Connect (проверка подлинности выполняется только в том случае, если клиент устанавливает связь с приложением)</span><span class="sxs-lookup"><span data-stu-id="7b940-146">Connect (authentication is performed only when the client establishes a relationship with the application)</span></span>

</dd> <dt>

<span id="Call"></span><span id="call"></span><span id="CALL"></span>

<span data-ttu-id="7b940-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Вызов** (3)</span><span class="sxs-lookup"><span data-stu-id="7b940-147"><span id="Call"></span><span id="call"></span><span id="CALL"></span>**Call** (3)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-148">Вызов (проверка подлинности выполняется только в начале каждого вызова, когда приложение получает запрос)</span><span class="sxs-lookup"><span data-stu-id="7b940-148">Call (authentication is performed only at the beginning of each call when the application receives the request)</span></span>

</dd> <dt>

<span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>

<span data-ttu-id="7b940-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Пакет** (4)</span><span class="sxs-lookup"><span data-stu-id="7b940-149"><span id="Packet"></span><span id="packet"></span><span id="PACKET"></span>**Packet** (4)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-150">Пакет (проверка подлинности выполняется для всех данных, полученных от клиента).</span><span class="sxs-lookup"><span data-stu-id="7b940-150">Packet (authentication is performed on all of the data received from the client)</span></span>

</dd> <dt>

<span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>

<span data-ttu-id="7b940-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**Паккетинтегрити** (5)</span><span class="sxs-lookup"><span data-stu-id="7b940-151"><span id="PacketIntegrity"></span><span id="packetintegrity"></span><span id="PACKETINTEGRITY"></span>**PacketIntegrity** (5)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-152">Паккетинтегрити (все данные, передаваемые между клиентом и приложением, проходят проверку подлинности и проверяются)</span><span class="sxs-lookup"><span data-stu-id="7b940-152">PacketIntegrity (all of the data transferred between the client and the application is authenticated and verified)</span></span>

</dd> <dt>

<span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>

<span data-ttu-id="7b940-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**Паккетприваци** (6)</span><span class="sxs-lookup"><span data-stu-id="7b940-153"><span id="PacketPrivacy"></span><span id="packetprivacy"></span><span id="PACKETPRIVACY"></span>**PacketPrivacy** (6)</span></span>


</dt> <dd>

<span data-ttu-id="7b940-154">Паккетприваци (используются свойства других уровней проверки подлинности, и все данные шифруются)</span><span class="sxs-lookup"><span data-stu-id="7b940-154">PacketPrivacy (the properties of the other authentication levels are used and all of the data is encrypted)</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7b940-155">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7b940-155">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-158">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="7b940-158">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="7b940-159">Краткое текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7b940-159">Short textual description of the current object.</span></span>

<span data-ttu-id="7b940-160">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7b940-160">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b940-161">**кустомсуррогате**</span><span class="sxs-lookup"><span data-stu-id="7b940-161">**CustomSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ дллсуррогате \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-165">Имя пользовательского суррогата, в котором активируется внутрипроцессный DCOM-приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-165">Name of the custom surrogate in which the in-process DCOM application is activated.</span></span> <span data-ttu-id="7b940-166">Если это значение равно **null** , а ключ **Усесуррогате** имеет **значение true**, система предоставляет суррогатный процесс.</span><span class="sxs-lookup"><span data-stu-id="7b940-166">If this value is **NULL** and the **UseSurrogate** key is **TRUE**, then the system provides a surrogate process.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-167">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7b940-167">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b940-170">Текстовое описание текущего объекта.</span><span class="sxs-lookup"><span data-stu-id="7b940-170">Textual description of the current object.</span></span>

<span data-ttu-id="7b940-171">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7b940-171">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b940-172">**енаблеатсторажеактиватион**</span><span class="sxs-lookup"><span data-stu-id="7b940-172">**EnableAtStorageActivation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-173">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b940-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-175">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ активатеатстораже \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ActivateAtStorage\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-176">DCOM-приложение получает сохраненное состояние приложения или начинается с состояния, в котором сначала инициализируется приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-176">DCOM application retrieves the saved state of the application or begins from the state in which the application is first initialized.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-177">**локальная служба.**</span><span class="sxs-lookup"><span data-stu-id="7b940-177">**LocalService**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-180">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ , \_ \\ \\ программные классы на локальном компьютере \\ \\ \\ \\ AppID \\ \\ {GUID} \[ LocalService \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-180">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[LocalService\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-181">Имя для служб, предоставляемых приложением DCOM.</span><span class="sxs-lookup"><span data-stu-id="7b940-181">Name for the services provided by the DCOM application.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-182">**ремотесервернаме**</span><span class="sxs-lookup"><span data-stu-id="7b940-182">**RemoteServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-183">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-184">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7b940-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b940-185">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ ремотесервернаме \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-185">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RemoteServerName\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-186">Имя удаленного сервера, на котором активировано приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-186">Name of the remote server where the application is activated.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-187">**RunAsUser**</span><span class="sxs-lookup"><span data-stu-id="7b940-187">**RunAsUser**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-189">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-190">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ . \_ \\ \\ классы программного обеспечения локального компьютера \\ \\ \\ \\ AppID \\ \\ {GUID} \[ runas \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-190">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[RunAs\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-191">Учетная запись конкретного пользователя, под которой приложение должно запускаться при активации.</span><span class="sxs-lookup"><span data-stu-id="7b940-191">Specific user account under which the application is to be run on activation.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-192">**сервицепараметерс**</span><span class="sxs-lookup"><span data-stu-id="7b940-192">**ServiceParameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-193">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-195">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ сервицепараметерс \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[ServiceParameters\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-196">Параметры командной строки, передаваемые в DCOM-приложение.</span><span class="sxs-lookup"><span data-stu-id="7b940-196">Command-line parameters passed to the DCOM application.</span></span> <span data-ttu-id="7b940-197">Это допустимо только в том случае, если приложение написано как служба на основе Windows.</span><span class="sxs-lookup"><span data-stu-id="7b940-197">This is valid only if the application is written as a Windows-based service.</span></span>

</dd> <dt>

<span data-ttu-id="7b940-198">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="7b940-198">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b940-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b940-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b940-201">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="7b940-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="7b940-202">Идентификатор, по которому известен текущий объект.</span><span class="sxs-lookup"><span data-stu-id="7b940-202">Identifier by which the current object is known.</span></span>

<span data-ttu-id="7b940-203">Это свойство наследуется [**от \_ параметра CIM**](cim-setting.md).</span><span class="sxs-lookup"><span data-stu-id="7b940-203">This property is inherited from [**CIM\_Setting**](cim-setting.md).</span></span>

</dd> <dt>

<span data-ttu-id="7b940-204">**усесуррогате**</span><span class="sxs-lookup"><span data-stu-id="7b940-204">**UseSurrogate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b940-205">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b940-205">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b940-206">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7b940-206">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7b940-207">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry \| hKey \_ Local \_ Machine \\ \\ Software \\ \\ Classes \\ \\ AppID \\ \\ {GUID} \[ дллсуррогате \] ")</span><span class="sxs-lookup"><span data-stu-id="7b940-207">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|HKEY\_LOCAL\_MACHINE\\\\SOFTWARE\\\\Classes\\\\AppID\\\\{GUID}\[DllSurrogate\]")</span></span>
</dt> </dl>

<span data-ttu-id="7b940-208">DCOM-приложение может быть активировано как сервер вне процесса с помощью суррогатного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="7b940-208">DCOM application can be activated as an out-of-process server by use of a surrogate executable file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b940-209">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7b940-209">Remarks</span></span>

<span data-ttu-id="7b940-210">Класс **Win32 \_ дкомаппликатионсеттинг** является производным от [**Win32 \_ комсеттинг**](win32-comsetting.md).</span><span class="sxs-lookup"><span data-stu-id="7b940-210">The **Win32\_DCOMApplicationSetting** class is derived from [**Win32\_COMSetting**](win32-comsetting.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b940-211">Требования</span><span class="sxs-lookup"><span data-stu-id="7b940-211">Requirements</span></span>



| <span data-ttu-id="7b940-212">Требование</span><span class="sxs-lookup"><span data-stu-id="7b940-212">Requirement</span></span> | <span data-ttu-id="7b940-213">Значение</span><span class="sxs-lookup"><span data-stu-id="7b940-213">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b940-214">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b940-214">Minimum supported client</span></span><br/> | <span data-ttu-id="7b940-215">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b940-215">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7b940-216">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b940-216">Minimum supported server</span></span><br/> | <span data-ttu-id="7b940-217">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b940-217">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7b940-218">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b940-218">Namespace</span></span><br/>                | <span data-ttu-id="7b940-219">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7b940-219">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7b940-220">MOF</span><span class="sxs-lookup"><span data-stu-id="7b940-220">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b940-221"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b940-221"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b940-222">DLL</span><span class="sxs-lookup"><span data-stu-id="7b940-222">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b940-223"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b940-223"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b940-224">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7b940-224">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b940-225">**\_Комсеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="7b940-225">**Win32\_COMSetting**</span></span>](win32-comsetting.md)
</dt> <dt>

<span data-ttu-id="7b940-226">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b940-226">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7b940-227">**Константы прав доступа**</span><span class="sxs-lookup"><span data-stu-id="7b940-227">**Privilege Constants**</span></span>](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[<span data-ttu-id="7b940-228">Объекты дескрипторов безопасности WMI</span><span class="sxs-lookup"><span data-stu-id="7b940-228">WMI Security Descriptor Objects</span></span>](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[<span data-ttu-id="7b940-229">Изменение параметров безопасности доступа для защищаемых объектов</span><span class="sxs-lookup"><span data-stu-id="7b940-229">Changing Access Security on Securable Objects</span></span>](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> </dl>

 

