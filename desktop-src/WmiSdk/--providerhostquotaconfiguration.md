---
description: Позволяет устанавливать ограничения на использование системных ресурсов в процессе узла.
ms.assetid: 5f5ed1c6-bd1a-406d-a682-7a52059d9450
ms.tgt_platform: multiple
title: Класс __ProviderHostQuotaConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ProviderHostQuotaConfiguration
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 443d66c8e508346444e98a92b341f1e7d67d8cd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264802"
---
# <a name="__providerhostquotaconfiguration-class"></a><span data-ttu-id="977aa-103">\_\_Класс Провидерхосткуотаконфигуратион</span><span class="sxs-lookup"><span data-stu-id="977aa-103">\_\_ProviderHostQuotaConfiguration class</span></span>

<span data-ttu-id="977aa-104">Класс System **\_ \_ провидерхосткуотаконфигуратион** является классом конфигурации для процессов поставщика узла.</span><span class="sxs-lookup"><span data-stu-id="977aa-104">The **\_\_ProviderHostQuotaConfiguration** system class is a configuration class for host provider processes.</span></span> <span data-ttu-id="977aa-105">Этот класс находится в корневом пространстве имен и позволяет устанавливать ограничения на использование системных ресурсов процессом узла.</span><span class="sxs-lookup"><span data-stu-id="977aa-105">This class resides in the root namespace and allows limits to be set on host process usage of system resources.</span></span>

<span data-ttu-id="977aa-106">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="977aa-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="977aa-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="977aa-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="977aa-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="977aa-108">Syntax</span></span>

``` syntax
class __ProviderHostQuotaConfiguration : __SystemClass
{
  uint32 ThreadsPerHost;
  uint32 HandlesPerHost;
  uint32 ProcessLimitAllHosts;
  uint64 MemoryPerHost;
  uint64 MemoryAllHosts;
};
```

## <a name="members"></a><span data-ttu-id="977aa-109">Члены</span><span class="sxs-lookup"><span data-stu-id="977aa-109">Members</span></span>

<span data-ttu-id="977aa-110">Класс **\_ \_ провидерхосткуотаконфигуратион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="977aa-110">The **\_\_ProviderHostQuotaConfiguration** class has these types of members:</span></span>

-   [<span data-ttu-id="977aa-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="977aa-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="977aa-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="977aa-112">Properties</span></span>

<span data-ttu-id="977aa-113">Класс **\_ \_ провидерхосткуотаконфигуратион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="977aa-113">The **\_\_ProviderHostQuotaConfiguration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="977aa-114">**хандлесперхост**</span><span class="sxs-lookup"><span data-stu-id="977aa-114">**HandlesPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977aa-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="977aa-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="977aa-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="977aa-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="977aa-117">Число дескрипторов объектов ядра, которые может иметь каждый узел.</span><span class="sxs-lookup"><span data-stu-id="977aa-117">Number of kernel object handles each host can have.</span></span>

</dd> <dt>

<span data-ttu-id="977aa-118">**меморяллхостс**</span><span class="sxs-lookup"><span data-stu-id="977aa-118">**MemoryAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977aa-119">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="977aa-119">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="977aa-120">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="977aa-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="977aa-121">Общий объем частной памяти в байтах, который может храниться на всех узлах.</span><span class="sxs-lookup"><span data-stu-id="977aa-121">Combined amount of private memory in bytes that can be held by all hosts.</span></span>

<span data-ttu-id="977aa-122">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="977aa-122">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="977aa-123">**мемориперхост**</span><span class="sxs-lookup"><span data-stu-id="977aa-123">**MemoryPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977aa-124">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="977aa-124">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="977aa-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="977aa-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="977aa-126">Объем частной памяти, который может храниться на каждом узле.</span><span class="sxs-lookup"><span data-stu-id="977aa-126">Amount of private memory that can be held by each host.</span></span>

<span data-ttu-id="977aa-127">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="977aa-127">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="977aa-128">**процесслимиталлхостс**</span><span class="sxs-lookup"><span data-stu-id="977aa-128">**ProcessLimitAllHosts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977aa-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="977aa-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="977aa-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="977aa-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="977aa-131">Общее количество ведущих процессов, которые могут выполняться одновременно.</span><span class="sxs-lookup"><span data-stu-id="977aa-131">Total number of host processes that can be executing concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="977aa-132">**среадсперхост**</span><span class="sxs-lookup"><span data-stu-id="977aa-132">**ThreadsPerHost**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="977aa-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="977aa-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="977aa-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="977aa-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="977aa-135">Число потоков, принадлежащих одному узлу.</span><span class="sxs-lookup"><span data-stu-id="977aa-135">Number of threads owned by any one host.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="977aa-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="977aa-136">Remarks</span></span>

<span data-ttu-id="977aa-137">Свойства, представляющие ограничения, можно изменить, но так как класс является singleton, все узлы поставщика имеют одинаковые ограничения.</span><span class="sxs-lookup"><span data-stu-id="977aa-137">The properties that represent limits can be changed but because the class is a singleton, all the provider hosts share the same limits.</span></span>

<span data-ttu-id="977aa-138">При настройке ограничений объекта задания для объекта задания узла используются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="977aa-138">The following parameters are used when configuring the job object limits for the host job object:</span></span>

-   <span data-ttu-id="977aa-139">**меморяллхостс**</span><span class="sxs-lookup"><span data-stu-id="977aa-139">**MemoryAllHosts**</span></span>
-   <span data-ttu-id="977aa-140">**мемориперхост**</span><span class="sxs-lookup"><span data-stu-id="977aa-140">**MemoryPerHost**</span></span>
-   <span data-ttu-id="977aa-141">**процесслимиталлхостс**</span><span class="sxs-lookup"><span data-stu-id="977aa-141">**ProcessLimitAllHosts**</span></span>
-   <span data-ttu-id="977aa-142">**среадсперхост**</span><span class="sxs-lookup"><span data-stu-id="977aa-142">**ThreadsPerHost**</span></span>

<span data-ttu-id="977aa-143">Ведущий процесс опрашивает использование и завершает процесс при нарушении квоты **хандлесперхост** .</span><span class="sxs-lookup"><span data-stu-id="977aa-143">The host process polls handle usage and exits the process if the **HandlesPerHost** quota is violated.</span></span> <span data-ttu-id="977aa-144">Изменения этих значений вступают в силу после перезагрузки компьютера.</span><span class="sxs-lookup"><span data-stu-id="977aa-144">Changes to these values take effect after the computer is restarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="977aa-145">Требования</span><span class="sxs-lookup"><span data-stu-id="977aa-145">Requirements</span></span>



| <span data-ttu-id="977aa-146">Требование</span><span class="sxs-lookup"><span data-stu-id="977aa-146">Requirement</span></span> | <span data-ttu-id="977aa-147">Значение</span><span class="sxs-lookup"><span data-stu-id="977aa-147">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="977aa-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="977aa-148">Minimum supported client</span></span><br/> | <span data-ttu-id="977aa-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="977aa-149">Windows Vista</span></span><br/>       |
| <span data-ttu-id="977aa-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="977aa-150">Minimum supported server</span></span><br/> | <span data-ttu-id="977aa-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="977aa-151">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="977aa-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="977aa-152">Namespace</span></span><br/>                | <span data-ttu-id="977aa-153">Все пространства имен WMI</span><span class="sxs-lookup"><span data-stu-id="977aa-153">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="977aa-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="977aa-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="977aa-155">**\_\_системкласс**</span><span class="sxs-lookup"><span data-stu-id="977aa-155">**\_\_SystemClass**</span></span>](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[<span data-ttu-id="977aa-156">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="977aa-156">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

