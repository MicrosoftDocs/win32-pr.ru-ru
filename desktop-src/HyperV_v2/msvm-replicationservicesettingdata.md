---
description: Представляет параметры для службы репликации на узле восстановления. Свойства этого класса нельзя изменить напрямую. Клиент должен вызвать \_ метод мсвм репликатионсервице. модифисервицесеттингс, чтобы изменить любое из этих свойств.
ms.assetid: a0c0b45a-3578-412a-910e-cd4b3ff0e262
title: Класс Msvm_ReplicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationServiceSettingData
- Msvm_ReplicationServiceSettingData.InstanceID
- Msvm_ReplicationServiceSettingData.Caption
- Msvm_ReplicationServiceSettingData.Description
- Msvm_ReplicationServiceSettingData.ElementName
- Msvm_ReplicationServiceSettingData.RecoveryServerEnabled
- Msvm_ReplicationServiceSettingData.AllowedAuthenticationType
- Msvm_ReplicationServiceSettingData.CertificateThumbPrint
- Msvm_ReplicationServiceSettingData.HttpsPort
- Msvm_ReplicationServiceSettingData.HttpPort
- Msvm_ReplicationServiceSettingData.MonitoringStartTime
- Msvm_ReplicationServiceSettingData.MonitoringInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e2886529ab74fed52ec0c6077bfa3d9222fca55c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910739"
---
# <a name="msvm_replicationservicesettingdata-class"></a><span data-ttu-id="3a78f-105">\_Класс мсвм репликатионсервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="3a78f-105">Msvm\_ReplicationServiceSettingData class</span></span>

<span data-ttu-id="3a78f-106">Представляет параметры для службы репликации на узле восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a78f-106">Represents the settings for the replication service on a recovery host.</span></span> <span data-ttu-id="3a78f-107">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="3a78f-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="3a78f-108">Клиент должен вызвать метод [**мсвм \_ Репликатионсервице. модифисервицесеттингс**](modifyservicesettings-msvm-replicationservice.md) , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="3a78f-108">The client must call the [**Msvm\_ReplicationService.ModifyServiceSettings**](modifyservicesettings-msvm-replicationservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="3a78f-109">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3a78f-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a78f-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a78f-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Replication Service Settings";
  string   Description = "Virtual Machine Replication Service Settings Data";
  string   ElementName = "Replication Service Settings";
  boolean  RecoveryServerEnabled = False;
  uint16   AllowedAuthenticationType = 0;
  string   CertificateThumbPrint;
  uint16   HttpsPort = 443;
  uint16   HttpPort = 80;
  datetime MonitoringStartTime;
  uint32   MonitoringInterval = 43200;
};
```

## <a name="members"></a><span data-ttu-id="3a78f-111">Члены</span><span class="sxs-lookup"><span data-stu-id="3a78f-111">Members</span></span>

<span data-ttu-id="3a78f-112">Класс **мсвм \_ репликатионсервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3a78f-112">The **Msvm\_ReplicationServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="3a78f-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a78f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3a78f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="3a78f-114">Properties</span></span>

<span data-ttu-id="3a78f-115">Класс **мсвм \_ репликатионсервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3a78f-115">The **Msvm\_ReplicationServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3a78f-116">**алловедаусентикатионтипе**</span><span class="sxs-lookup"><span data-stu-id="3a78f-116">**AllowedAuthenticationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a78f-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-119">Определите режимы проверки подлинности, разрешенные для подключения к серверу узла восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a78f-119">Define authentication modes allowed for connecting to recovery host server.</span></span>

<dt>

<span data-ttu-id="3a78f-120">0</span><span class="sxs-lookup"><span data-stu-id="3a78f-120">0</span></span>
</dt> <dd>

<span data-ttu-id="3a78f-121">Не определено.</span><span class="sxs-lookup"><span data-stu-id="3a78f-121">Not defined.</span></span>

</dd> <dt>

<span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="3a78f-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Проверка подлинности Kerberos** (1)</span><span class="sxs-lookup"><span data-stu-id="3a78f-122"><span id="Kerberos_authentication"></span><span id="kerberos_authentication"></span><span id="KERBEROS_AUTHENTICATION"></span>**Kerberos authentication** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a78f-123">Аутентификация Kerberos.</span><span class="sxs-lookup"><span data-stu-id="3a78f-123">Kerberos authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span data-ttu-id="3a78f-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата** (2)</span><span class="sxs-lookup"><span data-stu-id="3a78f-124"><span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Certificate based authentication** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a78f-125">Проверка подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="3a78f-125">Certificate based authentication.</span></span>

</dd> <dt>

<span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>

<span data-ttu-id="3a78f-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата и проверка подлинности Kerberos** (3)</span><span class="sxs-lookup"><span data-stu-id="3a78f-126"><span id="Certificate_based_authentication_and_kerberos_authentication"></span><span id="certificate_based_authentication_and_kerberos_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION_AND_KERBEROS_AUTHENTICATION"></span>**Certificate based authentication and kerberos authentication** (3)</span></span>


</dt> <dd>

<span data-ttu-id="3a78f-127">Проверка подлинности на основе сертификата и встроенная проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="3a78f-127">Both certificate based authentication and integrated authentication.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="3a78f-128">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="3a78f-128">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a78f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-131">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3a78f-131">A short description of the object.</span></span> <span data-ttu-id="3a78f-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры службы репликации".</span><span class="sxs-lookup"><span data-stu-id="3a78f-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-133">**CertificateThumbPrint**</span><span class="sxs-lookup"><span data-stu-id="3a78f-133">**CertificateThumbPrint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a78f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-136">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span><span class="sxs-lookup"><span data-stu-id="3a78f-136">Qualifiers: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (128)</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-137">Отпечаток сертификата, используемый, когда **AuthenticationType** является проверкой подлинности на основе сертификата.</span><span class="sxs-lookup"><span data-stu-id="3a78f-137">Certificate thumbprint to use when **AuthenticationType** is certificate based authentication.</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3a78f-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a78f-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-141">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="3a78f-141">A description of the object.</span></span> <span data-ttu-id="3a78f-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "данные параметров репликации виртуальной машины".</span><span class="sxs-lookup"><span data-stu-id="3a78f-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Virtual Machine Replication Settings Data".</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-143">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3a78f-143">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a78f-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-146">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="3a78f-146">A display name for the object.</span></span> <span data-ttu-id="3a78f-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры службы репликации".</span><span class="sxs-lookup"><span data-stu-id="3a78f-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Replication Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-148">**HttpPort**</span><span class="sxs-lookup"><span data-stu-id="3a78f-148">**HttpPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-149">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a78f-149">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-151">Номер порта сервера восстановления, используемый при принятии незащищенного соединения для репликации.</span><span class="sxs-lookup"><span data-stu-id="3a78f-151">Recovery server port number to use when accepting a nonsecure connection for replication.</span></span> <span data-ttu-id="3a78f-152">Значение по умолчанию равно 80.</span><span class="sxs-lookup"><span data-stu-id="3a78f-152">The default value is 80.</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-153">**HttpsPort**</span><span class="sxs-lookup"><span data-stu-id="3a78f-153">**HttpsPort**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-154">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3a78f-154">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-156">Номер порта сервера восстановления, используемый при принятии безопасного подключения для репликации.</span><span class="sxs-lookup"><span data-stu-id="3a78f-156">Recovery server port number to use when accepting secure connection for replication.</span></span> <span data-ttu-id="3a78f-157">Значение по умолчанию — 443.</span><span class="sxs-lookup"><span data-stu-id="3a78f-157">The default value is 443.</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-158">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3a78f-158">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3a78f-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-161">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="3a78f-161">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-162">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="3a78f-162">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3a78f-163">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3a78f-163">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-164">**мониторингинтервал**</span><span class="sxs-lookup"><span data-stu-id="3a78f-164">**MonitoringInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-165">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3a78f-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-167">Интервал в секундах, по истечении которого должна быть сброшена статистика репликации.</span><span class="sxs-lookup"><span data-stu-id="3a78f-167">The interval, in seconds, at which replication statistics should be reset.</span></span> <span data-ttu-id="3a78f-168">Интервал по умолчанию составляет 12 часов (43200 секунд).</span><span class="sxs-lookup"><span data-stu-id="3a78f-168">The default interval is 12 hours (43200 seconds).</span></span> <span data-ttu-id="3a78f-169">Минимальное допустимое значение — 60 минут (3600 секунд), а максимальное допустимое значение — 7 дней (604800 секунд).</span><span class="sxs-lookup"><span data-stu-id="3a78f-169">The minimum valid value is 60 minutes (3600 seconds), and the maximum valid value is 7 days (604800 seconds).</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-170">**мониторингстарттиме**</span><span class="sxs-lookup"><span data-stu-id="3a78f-170">**MonitoringStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-171">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3a78f-171">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-172">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-173">Время начала для мониторинга репликации в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="3a78f-173">The start time for replication monitoring, in UTC.</span></span> <span data-ttu-id="3a78f-174">Значение по умолчанию — 9:00 A.M., местное время, представленное в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="3a78f-174">The default value is 9:00 A.M., local time, represented in UTC.</span></span> <span data-ttu-id="3a78f-175">Элементы даты объекта **DateTime** должны быть равны нулю.</span><span class="sxs-lookup"><span data-stu-id="3a78f-175">The date elements of the **datetime** object must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3a78f-176">**рековерисерверенаблед**</span><span class="sxs-lookup"><span data-stu-id="3a78f-176">**RecoveryServerEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a78f-177">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3a78f-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3a78f-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3a78f-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3a78f-179">Указывает, включен ли узел Hyper-V в качестве сервера восстановления.</span><span class="sxs-lookup"><span data-stu-id="3a78f-179">Specifies whether the Hyper-V host is enabled as a recovery server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a78f-180">Требования</span><span class="sxs-lookup"><span data-stu-id="3a78f-180">Requirements</span></span>



| <span data-ttu-id="3a78f-181">Требование</span><span class="sxs-lookup"><span data-stu-id="3a78f-181">Requirement</span></span> | <span data-ttu-id="3a78f-182">Значение</span><span class="sxs-lookup"><span data-stu-id="3a78f-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a78f-183">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a78f-183">Minimum supported client</span></span><br/> | <span data-ttu-id="3a78f-184">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3a78f-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3a78f-185">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a78f-185">Minimum supported server</span></span><br/> | <span data-ttu-id="3a78f-186">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3a78f-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a78f-187">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a78f-187">Namespace</span></span><br/>                | <span data-ttu-id="3a78f-188">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3a78f-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3a78f-189">MOF</span><span class="sxs-lookup"><span data-stu-id="3a78f-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a78f-190"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a78f-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a78f-191">DLL</span><span class="sxs-lookup"><span data-stu-id="3a78f-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a78f-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3a78f-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="3a78f-193">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a78f-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a78f-194">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="3a78f-194">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="3a78f-195">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="3a78f-195">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-replicationservice.md)
</dt> </dl>

 

