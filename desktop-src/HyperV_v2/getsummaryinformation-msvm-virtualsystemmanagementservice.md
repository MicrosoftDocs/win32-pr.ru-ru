---
description: Возвращает сводные данные о виртуальной машине.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Метод Жетсуммаринформатион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: efa879cd3da0f5e8a4cc8cf1e9873390c94a94bae0eef3dd8d36c59c9e1680e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253654"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Жетсуммаринформатион \_ класса Виртуалсистемманажементсервице мсвм

Возвращает сводные данные о виртуальной машине.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SettingData* \[ окне\]
</dt> <dd>

Тип: **CIM \_ виртуалсистемсеттингдата \[ \]**

Массив экземпляров [**\_ виртуалсистемсеттингдата CIM**](/previous-versions//cc136954(v=vs.85)) , указывающих виртуальные машины или моментальные снимки, для которых необходимо получить сведения. Если этот параметр имеет **значение NULL**, то извлекаются сведения обо всех виртуальных машинах.

</dd> <dt>

*Рекуестединформатион* \[ окне\]
</dt> <dd>

Тип: **UInt32 \[ \]**

Массив значений перечисления, соответствующих свойствам в классе [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , которые указывают данные для получения для виртуальных машин и моментальных снимков, указанных в массиве *SettingData* .

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Имя** (0)


</dt> <dd>

Это соответствует свойству **Name** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Имя элемента** (1)


</dt> <dd>

Это соответствует свойству **ElementName** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Время создания** (2)


</dt> <dd>

Это соответствует свойству **CreationTime** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Примечания** (3)


</dt> <dd>

Это соответствует свойству **Notes** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Число процессоров** (4)


</dt> <dd>

Это соответствует свойству **NumberOfProcessors** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Маленький эскиз изображения (80x60)** (5)


</dt> <dd>

Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) . Будет получен эскиз изображения с размерами 80 60.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Средний эскиз изображения (160x120)** (6)


</dt> <dd>

Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) . Будет получен эскиз изображения с размерами 160 120.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Изображение крупного эскиза (320x240)** (7)


</dt> <dd>

Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) . Будет получен эскиз изображения с размерами 320 240.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**Аллокатедгпу** (8)


</dt> <dd>

Это соответствует свойству **аллокатедгпу** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**Виртуалсвитчнамес** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Версия** (10)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10 и Windows Server 2016.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Экранированная** (11)


</dt> <dd>

> [!Note]  
> добавлено в Windows 10, версии 1703 и Windows Server 2016.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)


</dt> <dd>

Это соответствует свойству **EnabledState** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**Процессорлоад** (101)


</dt> <dd>

Это соответствует свойству **процессорлоад** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**Процессорлоадхистори** (102)


</dt> <dd>

Это соответствует свойству **процессорлоадхистори** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Это соответствует свойству **MemoryUsage** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Пульс** (104)


</dt> <dd>

Это соответствует свойству **пульса** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Время бесперебойной работы** (105)


</dt> <dd>

Это соответствует свойству **время работоспособности** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**Гуестоператингсистем** (106)


</dt> <dd>

Это соответствует свойству **гуестоператингсистем** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Моментальные снимки** (107)


</dt> <dd>

Это соответствует свойству **моментальных снимков** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**Асинчронаустаскс** (108)


</dt> <dd>

Это соответствует свойству **асинчронаустаскс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Это соответствует свойству **HealthState** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Это соответствует свойству **OperationalStatus** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**Статусдескриптионс** (111)


</dt> <dd>

Это соответствует свойству **статусдескриптионс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**Меморяваилабле** (112)


</dt> <dd>

Это соответствует свойству **меморяваилабле** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**Аваилаблемеморибуффер** (113)


</dt> <dd>

Это соответствует свойству **аваилаблемеморибуффер** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Режим репликации** (114)


</dt> <dd>

Это соответствует свойству **ReplicationMode** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Состояние репликации** (115)


</dt> <dd>

Это соответствует свойству **ReplicationState** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Репликация системы реплики хеалстест** (116)


</dt> <dd>

Это соответствует свойству **репликатионхеалс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Работоспособность приложения** (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**Репликатионстатикс** (118)


</dt> <dd>

Это соответствует свойству **ReplicationState** класса [**\_ репликатионрелатионшип мсвм**](msvm-replicationrelationship.md) . Это массив для всех значений состояния репликации в первичной и расширенной связях. 0 значение индекса всегда используется для первичной связи, а если расширенная репликация включена, она возвращается в индекс 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**Репликатионхеалсекс** (119)


</dt> <dd>

Это соответствует свойству **репликатионхеалс** класса [**\_ репликатионрелатионшип мсвм**](msvm-replicationrelationship.md) . Это массив для всех значений работоспособности репликации в первичной и расширенной связях. 0 значение индекса всегда используется для первичной связи, а если расширенная репликация включена, она возвращается в индекс 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**Свапфилесинусе** (120)


</dt> <dd>

Это соответствует свойству **свапфилесинусе** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Интегратионсервицесверсионстате** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Это соответствует свойству **Name** класса [**мсвм \_ репликатионпровидер**](msvm-replicationprovider.md) .

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**Мемориспансфисикалнуманодес** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Интегратионсервицесверсионстате** (132)


</dt> <dd>

Это соответствует свойству **интегратионсервицесверсионстате** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**Осеренабледстате** (132)


</dt> <dd>

Это соответствует свойству **осеренабледстате** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ заполняет\]
</dt> <dd>

Тип: **[ **мсвм \_ суммаринформатионбасе**](msvm-summaryinformationbase.md)\[\]**

Массив экземпляров [**мсвм \_ суммаринформатионбасе**](msvm-summaryinformationbase.md) , содержащих запрашиваемые сведения для виртуальных машин и (или) моментальных снимков, указанных в массиве *SettingData* . Этот массив будет иметь то же количество элементов, что и массив *SettingData* . Каждая из этих записей будет содержать свойство **Name** , даже если это свойство не было запрошено. Если виртуальную машину или моментальный снимок не удается найти или он недоступен, свойство **имя** соответствующей записи сводки будет пустым.

Свойства, не указанные в параметре *рекуестединформатион* , будут иметь значение **null** .

> [!Note]  
> тип данных, обновленный из в Windows 10 версии 1703 из [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **UInt32**

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> </dl>

## <a name="remarks"></a>Remarks

Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей. Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Примеры

В следующем примере кода C# отображаются сводные данные. Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**Мсвм \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

