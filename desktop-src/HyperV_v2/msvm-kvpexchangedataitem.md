---
description: Представляет пару "ключ-значение".
ms.assetid: B13E9C5F-5B13-4EE5-AE5F-F51B61BDB9B7
title: Класс Msvm_KvpExchangeDataItem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_KvpExchangeDataItem
- Msvm_KvpExchangeDataItem.InstanceID
- Msvm_KvpExchangeDataItem.Caption
- Msvm_KvpExchangeDataItem.Description
- Msvm_KvpExchangeDataItem.ElementName
- Msvm_KvpExchangeDataItem.Source
- Msvm_KvpExchangeDataItem.Name
- Msvm_KvpExchangeDataItem.Data
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 540c54a694dab1c80a32f9648a90c5b5bf1e48a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684476"
---
# <a name="msvm_kvpexchangedataitem-class"></a><span data-ttu-id="93aae-103">\_Класс мсвм квпексчанжедатаитем</span><span class="sxs-lookup"><span data-stu-id="93aae-103">Msvm\_KvpExchangeDataItem class</span></span>

<span data-ttu-id="93aae-104">Представляет пару "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="93aae-104">Represents a key/value pair.</span></span>

<span data-ttu-id="93aae-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="93aae-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93aae-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="93aae-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_KvpExchangeDataItem : CIM_ManagedElement
{
  string InstanceID;
  string Caption = "Key-Value Pair Exchange Data Item";
  string Description = "Microsoft Key-Value Pair Exchange Data Item";
  string ElementName = "Key-Value Pair Exchange Data Item";
  uint16 Source;
  string Name;
  string Data;
};
```

## <a name="members"></a><span data-ttu-id="93aae-107">Члены</span><span class="sxs-lookup"><span data-stu-id="93aae-107">Members</span></span>

<span data-ttu-id="93aae-108">Класс **мсвм \_ квпексчанжедатаитем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="93aae-108">The **Msvm\_KvpExchangeDataItem** class has these types of members:</span></span>

-   [<span data-ttu-id="93aae-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="93aae-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93aae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="93aae-110">Properties</span></span>

<span data-ttu-id="93aae-111">Класс **мсвм \_ квпексчанжедатаитем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="93aae-111">The **Msvm\_KvpExchangeDataItem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93aae-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="93aae-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93aae-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93aae-115">A short description of the object.</span></span> <span data-ttu-id="93aae-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93aae-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93aae-117">**Data**</span><span class="sxs-lookup"><span data-stu-id="93aae-117">**Data**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93aae-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="93aae-120">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="93aae-121">Часть значения пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="93aae-121">The value portion of the key/value pair.</span></span>

</dd> <dt>

<span data-ttu-id="93aae-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="93aae-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93aae-125">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="93aae-125">A description of the object.</span></span> <span data-ttu-id="93aae-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93aae-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93aae-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93aae-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93aae-130">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="93aae-130">A display name for the object.</span></span> <span data-ttu-id="93aae-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93aae-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93aae-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93aae-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93aae-135">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="93aae-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93aae-136">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="93aae-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93aae-137">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93aae-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93aae-138">**Name**</span><span class="sxs-lookup"><span data-stu-id="93aae-138">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="93aae-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93aae-141">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="93aae-141">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="93aae-142">Ключевая часть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="93aae-142">The key portion of the key/value pair.</span></span>



| <span data-ttu-id="93aae-143">Ключ</span><span class="sxs-lookup"><span data-stu-id="93aae-143">Key</span></span>                                                                                                     | <span data-ttu-id="93aae-144">Описание</span><span class="sxs-lookup"><span data-stu-id="93aae-144">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93aae-145"><dt>"Ксдверсион"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-145"><dt>"CSDVersion"</dt></span></span> </dl>                 | <span data-ttu-id="93aae-146">Строка, представляющая последний пакет обновления, установленный в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="93aae-146">A string that represents the latest service pack installed on the guest system.</span></span> <span data-ttu-id="93aae-147">Например, "пакет обновления 2".</span><span class="sxs-lookup"><span data-stu-id="93aae-147">For example, "Service Pack 2".</span></span> <span data-ttu-id="93aae-148">Если пакет обновления не установлен, эта строка пуста.</span><span class="sxs-lookup"><span data-stu-id="93aae-148">If no service pack has been installed, this string is empty.</span></span><br/>                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="93aae-149"><dt>FullyQualifiedDomainName</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-149"><dt>"FullyQualifiedDomainName"</dt></span></span> </dl>   | <span data-ttu-id="93aae-150">Строка, представляющая полное DNS-имя, однозначно идентифицирующее локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="93aae-150">A string that represents the fully qualified DNS name that uniquely identifies the local computer.</span></span> <span data-ttu-id="93aae-151">Это имя представляет собой сочетание имени узла DNS и имени домена DNS с использованием формата *HostName*. *Имя_домена*.</span><span class="sxs-lookup"><span data-stu-id="93aae-151">This name is a combination of the DNS host name and the DNS domain name, using the format *HostName*.*DomainName*.</span></span> <span data-ttu-id="93aae-152">Если локальный компьютер является узлом кластера, это значение является полным DNS-именем виртуального сервера кластера.</span><span class="sxs-lookup"><span data-stu-id="93aae-152">If the local computer is a node in a cluster, this value is the fully qualified DNS name of the cluster virtual server.</span></span> <span data-ttu-id="93aae-153">Это значение совпадает с именем, возвращенным функцией [**предполагался сбой getcomputernameex**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) , если параметр *Наметипе* равен "компутернамеднсфулликуалифиед".</span><span class="sxs-lookup"><span data-stu-id="93aae-153">This value matches the name returned by the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function when the *NameType* parameter is "ComputerNameDnsFullyQualified".</span></span><br/> |
| <dl> <span data-ttu-id="93aae-154"><dt>"Интегратионсервицесверсион"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-154"><dt>"IntegrationServicesVersion"</dt></span></span> </dl> | <span data-ttu-id="93aae-155">Строка, представляющая версию Integration Services в данный момент установлена на гостевой виртуальной машине (например, "6.1.7000.0").</span><span class="sxs-lookup"><span data-stu-id="93aae-155">A string representing the version of the Integration Services currently installed in the guest virtual machine (for example, "6.1.7000.0").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="93aae-156"><dt>"NetworkAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-156"><dt>"NetworkAddressIPv4"</dt></span></span> </dl>         | <span data-ttu-id="93aae-157">Строка, содержащая разделенный точками с запятой список IPv4-адресов, которые в настоящее время назначены гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-157">A string that contains a semicolon-delimited list of the IPv4 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="93aae-158">Список обновляется автоматически при каждом изменении конфигурации TCP/IP на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-158">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="93aae-159">Каждый адрес представлен в точечно-десятичной нотации.</span><span class="sxs-lookup"><span data-stu-id="93aae-159">Each address is represented in dot-decimal notation.</span></span> <br/>                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="93aae-160"><dt>"NetworkAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-160"><dt>"NetworkAddressIPv6"</dt></span></span> </dl>         | <span data-ttu-id="93aae-161">Строка, содержащая разделенный точками с запятой список IPv6-адресов, которые в настоящее время назначены гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-161">A string that contains a semicolon-delimited list of the IPv6 addresses currently assigned to the guest virtual machine.</span></span> <span data-ttu-id="93aae-162">Список обновляется автоматически при каждом изменении конфигурации TCP/IP на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-162">The list is automatically updated whenever a TCP/IP configuration change occurs on the guest virtual machine.</span></span> <span data-ttu-id="93aae-163">Каждый адрес представлен в шестнадцатеричном формате с двоеточием.</span><span class="sxs-lookup"><span data-stu-id="93aae-163">Each address is represented in colon-hexadecimal notation.</span></span> <span data-ttu-id="93aae-164">Списки IPv4 и IPv6 не обязательно должны быть синхронизированы постоянно.</span><span class="sxs-lookup"><span data-stu-id="93aae-164">The IPv4 and IPv6 lists are not guaranteed to be in sync at all times.</span></span><br/>                                                                                                                                             |
| <dl> <span data-ttu-id="93aae-165"><dt>"Осбуилднумбер"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-165"><dt>"OSBuildNumber"</dt></span></span> </dl>              | <span data-ttu-id="93aae-166">Строка, представляющая номер сборки операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-166">A string that represents the build number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="93aae-167"><dt>"Оседитионид"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-167"><dt>"OSEditionId"</dt></span></span> </dl>                | <span data-ttu-id="93aae-168">Строка, представляющая выпуск (SKU) операционной системы гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93aae-168">A string representing the edition (SKU) of the guest virtual machine operating system.</span></span> <span data-ttu-id="93aae-169">Список возможных значений см. в описании функции [**жетпродуктинфо**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) .</span><span class="sxs-lookup"><span data-stu-id="93aae-169">For a list of possible values, see the [**GetProductInfo**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getproductinfo) function.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="93aae-170"><dt>OSName</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-170"><dt>"OSName"</dt></span></span> </dl>                     | <span data-ttu-id="93aae-171">Строка, представляющая имя операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-171">A string that represents the name of the operating system.</span></span> <span data-ttu-id="93aae-172">Это значение берется из следующей записи реестра: **hKey \_ Local \_ Machine** \\ **Software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProductName**</span><span class="sxs-lookup"><span data-stu-id="93aae-172">This value comes from the following registry entry: **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**ProductName**</span></span><br/> <br/>                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="93aae-173"><dt>Дочерний osmajorversion</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-173"><dt>"OSMajorVersion"</dt></span></span> </dl>             | <span data-ttu-id="93aae-174">Строка, представляющая основной номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-174">A string that represents the major version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="93aae-175"><dt>Дочерний osminorversion</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-175"><dt>"OSMinorVersion"</dt></span></span> </dl>             | <span data-ttu-id="93aae-176">Строка, представляющая дополнительный номер версии операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-176">A string that represents the minor version number of the operating system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="93aae-177"><dt>"Осплатформид"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-177"><dt>"OSPlatformId"</dt></span></span> </dl>               | <span data-ttu-id="93aae-178">Строка, представляющая платформу операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-178">A string that represents the operating system platform.</span></span> <span data-ttu-id="93aae-179">Возможные значения свойства **Data** — "1", чтобы указать на неподдерживаемую систему Windows и "2" для обозначения поддерживаемой системы Windows.</span><span class="sxs-lookup"><span data-stu-id="93aae-179">The possible values of the **Data** property are "1" to indicate an unsupported Windows system and "2" to indicate a supported Windows system.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="93aae-180"><dt>OSVersion</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-180"><dt>"OSVersion"</dt></span></span> </dl>                  | <span data-ttu-id="93aae-181">Строка, представляющая версию операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-181">A string that represents the operating system version.</span></span> <span data-ttu-id="93aae-182">Формат этой строки — *majorversion*. *Minorversion*. *BuildNumber*.</span><span class="sxs-lookup"><span data-stu-id="93aae-182">The format of this string is *MajorVersion*.*MinorVersion*.*BuildNumber*.</span></span> <span data-ttu-id="93aae-183">Например, "5.2.3790" для Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="93aae-183">For example, "5.2.3790" for Windows Server 2003.</span></span><br/>                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="93aae-184"><dt>ProcessorArchitecture</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-184"><dt>"ProcessorArchitecture"</dt></span></span> </dl>      | <span data-ttu-id="93aae-185">Строка, представляющая архитектуру процессора операционной системы.</span><span class="sxs-lookup"><span data-stu-id="93aae-185">A string that represents the processor architecture of the operating system.</span></span> <span data-ttu-id="93aae-186">Список значений см. в описании элемента **впроцессорарчитектуре** в структуре [**системных \_ сведений**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) .</span><span class="sxs-lookup"><span data-stu-id="93aae-186">For a list of values, see the **wProcessorArchitecture** member of the [**SYSTEM\_INFO**](/windows/desktop/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <dl> <span data-ttu-id="93aae-187"><dt>"Продукттипе"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-187"><dt>"ProductType"</dt></span></span> </dl>                | <span data-ttu-id="93aae-188">Строка, представляющая тип продукта.</span><span class="sxs-lookup"><span data-stu-id="93aae-188">A string that represents the product type.</span></span> <span data-ttu-id="93aae-189">Список значений см. в описании элемента **впродукттипе** структуры [**осверсионинфоекс**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="93aae-189">For a list of values, see the **wProductType** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="93aae-190"><dt>"RDPAddressIPv4"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-190"><dt>"RDPAddressIPv4"</dt></span></span> </dl>             | <span data-ttu-id="93aae-191">Строка, содержащая разделенный точками с запятой список IPv4-адресов, на которых в настоящее время прослушивается стек RDP гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93aae-191">A string that contains a semicolon-delimited list of the IPv4 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="93aae-192">Если стек RDP в данный момент не выполняется, строка будет пустой.</span><span class="sxs-lookup"><span data-stu-id="93aae-192">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="93aae-193">Список автоматически обновляется всякий раз, когда изменение конфигурации TCP/IP влияет на стек RDP на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-193">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="93aae-194">Каждый адрес представлен в точечно-десятичной нотации.</span><span class="sxs-lookup"><span data-stu-id="93aae-194">Each address is represented in dot-decimal notation.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="93aae-195"><dt>"RDPAddressIPv6"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-195"><dt>"RDPAddressIPv6"</dt></span></span> </dl>             | <span data-ttu-id="93aae-196">Строка, содержащая разделенный точками с запятой список IPv6-адресов, на которых в настоящее время прослушивается стек RDP гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93aae-196">A string that contains a semicolon-delimited list of the IPv6 addresses that the guest virtual machine RDP stack is currently listening on.</span></span> <span data-ttu-id="93aae-197">Если стек RDP в данный момент не выполняется, строка будет пустой.</span><span class="sxs-lookup"><span data-stu-id="93aae-197">If the RDP stack is not currently running, the string will be empty.</span></span> <span data-ttu-id="93aae-198">Список автоматически обновляется всякий раз, когда изменение конфигурации TCP/IP влияет на стек RDP на гостевой виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="93aae-198">The list is automatically updated whenever a TCP/IP configuration change affects the RDP stack on the guest virtual machine.</span></span> <span data-ttu-id="93aae-199">Каждый адрес представлен в шестнадцатеричном формате с двоеточием.</span><span class="sxs-lookup"><span data-stu-id="93aae-199">Each address is represented in colon-hexadecimal notation.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="93aae-200"><dt>"Сервицепаккмажор"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-200"><dt>"ServicePackMajor"</dt></span></span> </dl>           | <span data-ttu-id="93aae-201">Строка, представляющая основной номер версии последнего пакета обновления, установленного в системе.</span><span class="sxs-lookup"><span data-stu-id="93aae-201">A string that represents the major version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="93aae-202"><dt>"Сервицепаккминор"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-202"><dt>"ServicePackMinor"</dt></span></span> </dl>           | <span data-ttu-id="93aae-203">Строка, представляющая дополнительный номер версии последнего пакета обновления, установленного в системе.</span><span class="sxs-lookup"><span data-stu-id="93aae-203">A string that represents the minor version number of the latest service pack installed on the system.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                |
| <dl> <span data-ttu-id="93aae-204"><dt>"Суитемаск"</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-204"><dt>"SuiteMask"</dt></span></span> </dl>                  | <span data-ttu-id="93aae-205">Строка, представляющая наборы продуктов, доступные в системе.</span><span class="sxs-lookup"><span data-stu-id="93aae-205">A string that represents the product suites available on the system.</span></span> <span data-ttu-id="93aae-206">Эта строка представляет собой сочетание любого из значений элемента **всуитемаск** структуры [**осверсионинфоекс**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) .</span><span class="sxs-lookup"><span data-stu-id="93aae-206">This string is a combination of any of the values of the **wSuiteMask** member of the [**OSVERSIONINFOEX**](/windows/desktop/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span><br/>                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="93aae-207">**Источник**</span><span class="sxs-lookup"><span data-stu-id="93aae-207">**Source**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93aae-208">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="93aae-208">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="93aae-209">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="93aae-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93aae-210">Источник данных.</span><span class="sxs-lookup"><span data-stu-id="93aae-210">The source of the data.</span></span>



| <span data-ttu-id="93aae-211">Значение</span><span class="sxs-lookup"><span data-stu-id="93aae-211">Value</span></span>                                                                        | <span data-ttu-id="93aae-212">Значение</span><span class="sxs-lookup"><span data-stu-id="93aae-212">Meaning</span></span>                                                                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93aae-213"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-213"><dt>0</dt></span></span> </dl> | <span data-ttu-id="93aae-214">"Хостексчанжеитемс" при передаче узлом.</span><span class="sxs-lookup"><span data-stu-id="93aae-214">"HostExchangeItems" when pushed by the host.</span></span><br/>                                                                                                                                                                                      |
| <dl> <span data-ttu-id="93aae-215"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-215"><dt>1</dt></span></span> </dl> | <span data-ttu-id="93aae-216">"Гуестексчанжеитемс" при передаче гостевой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="93aae-216">"GuestExchangeItems" when pushed by the guest virtual machine.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="93aae-217"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-217"><dt>2</dt></span></span> </dl> | <span data-ttu-id="93aae-218">"Гуестинтринсицексчанжеитемс" при автоматическом заполнении гостевой виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="93aae-218">"GuestIntrinsicExchangeItems" when automatically populated by the guest virtual machine.</span></span><br/>                                                                                                                                          |
| <dl> <span data-ttu-id="93aae-219"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-219"><dt>4</dt></span></span> </dl> | <span data-ttu-id="93aae-220">Указывает, что элемент является только узлом и не является общим для гостевой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="93aae-220">Indicates that the item is host-only and not shared with the guest virtual machine.</span></span> <span data-ttu-id="93aae-221">Используется со свойством **хостонлитемс** класса [**\_ квпексчанжекомпонентсеттингдата мсвм**](msvm-kvpexchangecomponentsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="93aae-221">Used with the **HostOnlyItems** property of the [**Msvm\_KvpExchangeComponentSettingData**](msvm-kvpexchangecomponentsettingdata.md) class.</span></span> <br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93aae-222">Комментарии</span><span class="sxs-lookup"><span data-stu-id="93aae-222">Remarks</span></span>

<span data-ttu-id="93aae-223">Доступ к классу **\_ квпексчанжедатаитем мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="93aae-223">Access to the **Msvm\_KvpExchangeDataItem** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="93aae-224">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="93aae-224">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="93aae-225">Требования</span><span class="sxs-lookup"><span data-stu-id="93aae-225">Requirements</span></span>



| <span data-ttu-id="93aae-226">Требование</span><span class="sxs-lookup"><span data-stu-id="93aae-226">Requirement</span></span> | <span data-ttu-id="93aae-227">Значение</span><span class="sxs-lookup"><span data-stu-id="93aae-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93aae-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="93aae-228">Minimum supported client</span></span><br/> | <span data-ttu-id="93aae-229">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="93aae-229">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="93aae-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="93aae-230">Minimum supported server</span></span><br/> | <span data-ttu-id="93aae-231">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="93aae-231">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="93aae-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="93aae-232">Namespace</span></span><br/>                | <span data-ttu-id="93aae-233">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="93aae-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93aae-234">MOF</span><span class="sxs-lookup"><span data-stu-id="93aae-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93aae-235"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93aae-236">DLL</span><span class="sxs-lookup"><span data-stu-id="93aae-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93aae-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93aae-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="93aae-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="93aae-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93aae-239">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="93aae-239">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> <dt>

[<span data-ttu-id="93aae-240">**\_МАНАЖЕДЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="93aae-240">**CIM\_ManagedElement**</span></span>](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)
</dt> </dl>

 

