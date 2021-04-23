---
description: Представляет параметры для службы метрики. Свойства этого класса нельзя изменить напрямую. Клиент должен вызвать метод Модифисервицесеттингс, чтобы изменить любое из этих свойств.
ms.assetid: 578ddda7-4c8e-498e-8612-29c392390b73
title: Класс Msvm_MetricServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceSettingData
- Msvm_MetricServiceSettingData.InstanceID
- Msvm_MetricServiceSettingData.Caption
- Msvm_MetricServiceSettingData.Description
- Msvm_MetricServiceSettingData.ElementName
- Msvm_MetricServiceSettingData.MetricsFlushInterval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4a1211b19692761dd8b92de69cf42e4ad55246f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683175"
---
# <a name="msvm_metricservicesettingdata-class"></a><span data-ttu-id="e2141-105">\_Класс мсвм метриксервицесеттингдата</span><span class="sxs-lookup"><span data-stu-id="e2141-105">Msvm\_MetricServiceSettingData class</span></span>

<span data-ttu-id="e2141-106">Представляет параметры для службы метрики.</span><span class="sxs-lookup"><span data-stu-id="e2141-106">Represents the settings for the metric service.</span></span> <span data-ttu-id="e2141-107">Свойства этого класса нельзя изменить напрямую.</span><span class="sxs-lookup"><span data-stu-id="e2141-107">The properties for this class cannot be modified directly.</span></span> <span data-ttu-id="e2141-108">Клиент должен вызвать метод [**модифисервицесеттингс**](modifyservicesettings-msvm-metricservice.md) , чтобы изменить любое из этих свойств.</span><span class="sxs-lookup"><span data-stu-id="e2141-108">The client must call the [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) method to modify any of these properties.</span></span>

<span data-ttu-id="e2141-109">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e2141-109">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2141-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2141-110">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Hyper-V Metric Service Settings";
  string   Description = "Defines Hyper-V Metric Service Settings";
  string   ElementName = "Hyper-V Metric Service Settings";
  datetime MetricsFlushInterval;
};
```

## <a name="members"></a><span data-ttu-id="e2141-111">Члены</span><span class="sxs-lookup"><span data-stu-id="e2141-111">Members</span></span>

<span data-ttu-id="e2141-112">Класс **мсвм \_ метриксервицесеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e2141-112">The **Msvm\_MetricServiceSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="e2141-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2141-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e2141-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="e2141-114">Properties</span></span>

<span data-ttu-id="e2141-115">Класс **мсвм \_ метриксервицесеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e2141-115">The **Msvm\_MetricServiceSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e2141-116">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e2141-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2141-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2141-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2141-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2141-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2141-119">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e2141-119">A short description of the object.</span></span> <span data-ttu-id="e2141-120">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2141-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e2141-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e2141-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2141-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2141-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2141-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2141-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2141-124">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="e2141-124">A description of the object.</span></span> <span data-ttu-id="e2141-125">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "определяет параметры службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2141-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Defines Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e2141-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="e2141-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2141-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2141-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2141-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2141-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2141-129">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="e2141-129">A display name for the object.</span></span> <span data-ttu-id="e2141-130">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры службы метрик Hyper-V".</span><span class="sxs-lookup"><span data-stu-id="e2141-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Hyper-V Metric Service Settings".</span></span>

</dd> <dt>

<span data-ttu-id="e2141-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e2141-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2141-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e2141-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e2141-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2141-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e2141-134">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="e2141-134">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="e2141-135">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="e2141-135">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="e2141-136">Это свойство наследуется [**от \_ SettingData в CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e2141-136">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="e2141-137">**метриксфлушинтервал**</span><span class="sxs-lookup"><span data-stu-id="e2141-137">**MetricsFlushInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e2141-138">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e2141-138">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="e2141-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e2141-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e2141-140">Определяет интервал, по истечении которого метрики должны быть сброшены на диск.</span><span class="sxs-lookup"><span data-stu-id="e2141-140">Defines the interval at which metrics should be flushed to disk.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2141-141">Требования</span><span class="sxs-lookup"><span data-stu-id="e2141-141">Requirements</span></span>



| <span data-ttu-id="e2141-142">Требование</span><span class="sxs-lookup"><span data-stu-id="e2141-142">Requirement</span></span> | <span data-ttu-id="e2141-143">Значение</span><span class="sxs-lookup"><span data-stu-id="e2141-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2141-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2141-144">Minimum supported client</span></span><br/> | <span data-ttu-id="e2141-145">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="e2141-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="e2141-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2141-146">Minimum supported server</span></span><br/> | <span data-ttu-id="e2141-147">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="e2141-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e2141-148">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e2141-148">Namespace</span></span><br/>                | <span data-ttu-id="e2141-149">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="e2141-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="e2141-150">MOF</span><span class="sxs-lookup"><span data-stu-id="e2141-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e2141-151"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e2141-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e2141-152">DLL</span><span class="sxs-lookup"><span data-stu-id="e2141-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2141-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e2141-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e2141-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2141-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2141-155">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="e2141-155">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="e2141-156">**модифисервицесеттингс**</span><span class="sxs-lookup"><span data-stu-id="e2141-156">**ModifyServiceSettings**</span></span>](modifyservicesettings-msvm-metricservice.md)
</dt> </dl>

 

