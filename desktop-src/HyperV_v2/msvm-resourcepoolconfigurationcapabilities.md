---
description: Описывает возможности связанного \_ класса мсвм ресаурцепулконфигуратионсервице.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Класс Msvm_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b70d9e84e2c85d4c5b702a638982df0b47d62193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910728"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a><span data-ttu-id="ff675-103">\_Класс мсвм ресаурцепулконфигуратионкапабилитиес</span><span class="sxs-lookup"><span data-stu-id="ff675-103">Msvm\_ResourcePoolConfigurationCapabilities class</span></span>

<span data-ttu-id="ff675-104">Описывает возможности связанного класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) .</span><span class="sxs-lookup"><span data-stu-id="ff675-104">Describes the capabilities of the associated [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class.</span></span> <span data-ttu-id="ff675-105">Клиенты могут использовать экземпляры этого класса, чтобы определить, какие методы поддерживаются синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="ff675-105">Clients can use instances of this class to determine which methods are supported synchronously or asynchronously.</span></span> <span data-ttu-id="ff675-106">Один и тот же метод не должен находиться в обоих списках.</span><span class="sxs-lookup"><span data-stu-id="ff675-106">The same method must not be in both lists.</span></span> <span data-ttu-id="ff675-107">Реализации методов должны быть либо синхронными, либо асинхронными.</span><span class="sxs-lookup"><span data-stu-id="ff675-107">Method implementations must either be synchronous or asynchronous.</span></span>

<span data-ttu-id="ff675-108">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ff675-108">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff675-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff675-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a><span data-ttu-id="ff675-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ff675-110">Members</span></span>

<span data-ttu-id="ff675-111">Класс **мсвм \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ff675-111">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="ff675-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ff675-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff675-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ff675-113">Properties</span></span>

<span data-ttu-id="ff675-114">Класс **мсвм \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ff675-114">The **Msvm\_ResourcePoolConfigurationCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff675-115">**асинчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="ff675-115">**AsynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-116">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff675-116">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ff675-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff675-118">Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) , который поддерживается асинхронно реализацией.</span><span class="sxs-lookup"><span data-stu-id="ff675-118">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported asynchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ff675-119">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ff675-119">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-120">**CreatePool поддерживается** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff675-120">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-121">**Чанжепулресаурцес поддерживается** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff675-121">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-122">**Чанжепулсеттингс поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff675-122">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-123">**DeletePool поддерживается** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff675-123">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ff675-124">**Поставщик зарезервирован** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ff675-124">**Vendor Reserved** (32772..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="ff675-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ff675-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ff675-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff675-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff675-128">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ff675-128">A short description of the object.</span></span> <span data-ttu-id="ff675-129">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов".</span><span class="sxs-lookup"><span data-stu-id="ff675-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ff675-130">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ff675-130">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-131">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ff675-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff675-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff675-133">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ff675-133">A description of the object.</span></span> <span data-ttu-id="ff675-134">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="ff675-134">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ff675-135">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ff675-135">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-136">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ff675-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff675-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff675-138">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ff675-138">A display name for the object.</span></span> <span data-ttu-id="ff675-139">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов".</span><span class="sxs-lookup"><span data-stu-id="ff675-139">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Resource Pool Configuration Capabilities".</span></span>

</dd> <dt>

<span data-ttu-id="ff675-140">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ff675-140">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ff675-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff675-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff675-143">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ff675-143">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ff675-144">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ff675-144">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ff675-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ff675-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ff675-146">**синчронаусмесодссуппортед**</span><span class="sxs-lookup"><span data-stu-id="ff675-146">**SynchronousMethodsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff675-147">Тип данных: массив **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ff675-147">Data type: **uint32** array</span></span>
</dt> <dt>

<span data-ttu-id="ff675-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ff675-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff675-149">Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) , который поддерживается в синхронном режиме реализацией.</span><span class="sxs-lookup"><span data-stu-id="ff675-149">An array of method identifiers, each identifying a method of the [**Msvm\_ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md) class that is supported synchronously by the implementation.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="ff675-150">**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ff675-150">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-151">**CreatePool поддерживается** (32768)</span><span class="sxs-lookup"><span data-stu-id="ff675-151">**CreatePool is supported** (32768)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-152">**Чанжепулресаурцес поддерживается** (32769)</span><span class="sxs-lookup"><span data-stu-id="ff675-152">**ChangePoolResources is supported** (32769)</span></span>


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-153">**Чанжепулсеттингс поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="ff675-153">**ChangePoolSettings is supported** (32770)</span></span>


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

<span data-ttu-id="ff675-154">**DeletePool поддерживается** (32771)</span><span class="sxs-lookup"><span data-stu-id="ff675-154">**DeletePool is supported** (32771)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="ff675-155">**Поставщик зарезервирован** (32772.. 65535)</span><span class="sxs-lookup"><span data-stu-id="ff675-155">**Vendor Reserved** (32772..65535)</span></span>


<span data-ttu-id="ff675-156"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ff675-156"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ff675-157">Требования</span><span class="sxs-lookup"><span data-stu-id="ff675-157">Requirements</span></span>



| <span data-ttu-id="ff675-158">Требование</span><span class="sxs-lookup"><span data-stu-id="ff675-158">Requirement</span></span> | <span data-ttu-id="ff675-159">Значение</span><span class="sxs-lookup"><span data-stu-id="ff675-159">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff675-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff675-160">Minimum supported client</span></span><br/> | <span data-ttu-id="ff675-161">\[Только Windows 8.1 Классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff675-161">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ff675-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff675-162">Minimum supported server</span></span><br/> | <span data-ttu-id="ff675-163">Только классические приложения Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ff675-163">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="ff675-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ff675-164">Namespace</span></span><br/>                | <span data-ttu-id="ff675-165">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ff675-165">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ff675-166">MOF</span><span class="sxs-lookup"><span data-stu-id="ff675-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff675-167"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff675-167"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff675-168">DLL</span><span class="sxs-lookup"><span data-stu-id="ff675-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff675-169"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ff675-169"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

