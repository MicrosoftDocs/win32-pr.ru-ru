---
description: Эта Ассоциация указывает, что подкласс логического устройства (например, тома хранилища) подключен через конкретный контроллер протокола.
ms.assetid: 93025450-BE6C-48DC-913C-2050674DF81A
title: Класс Msvm_ProtocolControllerForUnit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ProtocolControllerForUnit
- Msvm_ProtocolControllerForUnit.Antecedent
- Msvm_ProtocolControllerForUnit.Dependent
- Msvm_ProtocolControllerForUnit.DeviceNumber
- Msvm_ProtocolControllerForUnit.AccessPriority
- Msvm_ProtocolControllerForUnit.AccessState
- Msvm_ProtocolControllerForUnit.DeviceAccess
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1470192fc4f10e60bdfef013146483b47cbfa7f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683173"
---
# <a name="msvm_protocolcontrollerforunit-class"></a><span data-ttu-id="7d427-103">\_Класс мсвм протоколконтроллерфорунит</span><span class="sxs-lookup"><span data-stu-id="7d427-103">Msvm\_ProtocolControllerForUnit class</span></span>

<span data-ttu-id="7d427-104">Эта Ассоциация указывает, что подкласс логического устройства (например, тома хранилища) подключен через конкретный контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="7d427-104">This association indicates that a subclass of logical device (for example a storage volume) is connected through a specific protocol controller.</span></span> <span data-ttu-id="7d427-105">Во многих ситуациях (например, Маскирование LUN хранилища) для связи с различными объектами могут использоваться многие из этих ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="7d427-105">In many situations (for example storage LUN masking), there may be many of these associations used to relate to different objects.</span></span> <span data-ttu-id="7d427-106">Таким образом, подклассы определены для оптимизации перечисления ассоциаций.</span><span class="sxs-lookup"><span data-stu-id="7d427-106">Therefore, subclasses have been defined to optimize enumeration of the associations.</span></span>

<span data-ttu-id="7d427-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7d427-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d427-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d427-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ProtocolControllerForUnit : CIM_ProtocolControllerForUnit
{
  CIM_ProtocolController REF Antecedent;
  CIM_LogicalDevice      REF Dependent;
  string                     DeviceNumber;
  uint16                     AccessPriority;
  uint16                     AccessState;
  uint16                     DeviceAccess;
};
```

## <a name="members"></a><span data-ttu-id="7d427-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7d427-109">Members</span></span>

<span data-ttu-id="7d427-110">Класс **мсвм \_ протоколконтроллерфорунит** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7d427-110">The **Msvm\_ProtocolControllerForUnit** class has these types of members:</span></span>

-   [<span data-ttu-id="7d427-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d427-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7d427-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7d427-112">Properties</span></span>

<span data-ttu-id="7d427-113">Класс **мсвм \_ протоколконтроллерфорунит** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7d427-113">The **Msvm\_ProtocolControllerForUnit** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7d427-114">**акцессприорити**</span><span class="sxs-lookup"><span data-stu-id="7d427-114">**AccessPriority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-115">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d427-115">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-117">Приоритет, предоставляемый для доступа к устройству через этот контроллер.</span><span class="sxs-lookup"><span data-stu-id="7d427-117">The priority given to accesses of the device through this controller.</span></span> <span data-ttu-id="7d427-118">Путь с наивысшим приоритетом будет иметь самое низкое значение для этого параметра.</span><span class="sxs-lookup"><span data-stu-id="7d427-118">The highest priority path will have the lowest value for this parameter.</span></span> <span data-ttu-id="7d427-119">Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.</span><span class="sxs-lookup"><span data-stu-id="7d427-119">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> <dt>

<span data-ttu-id="7d427-120">**акцессстате**</span><span class="sxs-lookup"><span data-stu-id="7d427-120">**AccessState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-121">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d427-121">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-123">Указывает, является ли контроллер активной командой или доступом к устройству (2) или нет (3).</span><span class="sxs-lookup"><span data-stu-id="7d427-123">Indicates whether the controller is actively commanding or accessing the device (2) or not (3).</span></span> <span data-ttu-id="7d427-124">Кроме того, можно определить значение 0 (неизвестно).</span><span class="sxs-lookup"><span data-stu-id="7d427-124">Also, the value, 0 (Unknown), can be defined.</span></span> <span data-ttu-id="7d427-125">Эти сведения необходимы в том случае, если логическое устройство может быть командо с помощью нескольких контроллеров протокола или доступно через несколько.</span><span class="sxs-lookup"><span data-stu-id="7d427-125">This information is necessary when a logical device can be commanded by, or accessed through, multiple protocol controllers.</span></span> <span data-ttu-id="7d427-126">Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.</span><span class="sxs-lookup"><span data-stu-id="7d427-126">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

<dl> <dt>

<span data-ttu-id="7d427-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7d427-127"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7d427-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Активно** (2)</span><span class="sxs-lookup"><span data-stu-id="7d427-128"><span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>**Active** (2)</span></span>
</dt> <dt>

<span data-ttu-id="7d427-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Неактивно** (3)</span><span class="sxs-lookup"><span data-stu-id="7d427-129"><span id="Inactive_"></span><span id="inactive_"></span><span id="INACTIVE_"></span>**Inactive** (3 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7d427-130">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7d427-130">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-131">Тип данных: **[ **CIM \_ протоколконтроллер**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span><span class="sxs-lookup"><span data-stu-id="7d427-131">Data type: **[**CIM\_ProtocolController**](/previous-versions/windows/desktop/iscsitarg/cim-protocolcontroller)**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-133">Контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="7d427-133">The protocol controller.</span></span> <span data-ttu-id="7d427-134">Этот класс наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7d427-134">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7d427-135">**Него**</span><span class="sxs-lookup"><span data-stu-id="7d427-135">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-136">Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="7d427-136">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-138">Управляемое устройство.</span><span class="sxs-lookup"><span data-stu-id="7d427-138">The controlled device.</span></span> <span data-ttu-id="7d427-139">Этот класс наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="7d427-139">This class is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="7d427-140">**девицеакцесс**</span><span class="sxs-lookup"><span data-stu-id="7d427-140">**DeviceAccess**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-141">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7d427-141">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-143">Права доступа, предоставленные устройству через этот контроллер.</span><span class="sxs-lookup"><span data-stu-id="7d427-143">The access rights granted to the device through this controller.</span></span> <span data-ttu-id="7d427-144">Этот класс наследуется от **CIM \_ протоколконтроллерфорунит**.</span><span class="sxs-lookup"><span data-stu-id="7d427-144">This class is inherited from **CIM\_ProtocolControllerForUnit**.</span></span>



| <span data-ttu-id="7d427-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7d427-145">Value</span></span>                                                                               | <span data-ttu-id="7d427-146">Значение</span><span class="sxs-lookup"><span data-stu-id="7d427-146">Meaning</span></span>                    |
|-------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7d427-147"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-147"><dt>0</dt></span></span> </dl>        | <span data-ttu-id="7d427-148">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="7d427-148">Unknown</span></span><br/>         |
| <dl> <span data-ttu-id="7d427-149"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-149"><dt>2</dt></span></span> </dl>        | <span data-ttu-id="7d427-150">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="7d427-150">Read/Write</span></span><br/>      |
| <dl> <span data-ttu-id="7d427-151"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-151"><dt>3</dt></span></span> </dl>        | <span data-ttu-id="7d427-152">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-152">Read-only</span></span><br/>       |
| <dl> <span data-ttu-id="7d427-153"><dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-153"><dt>4</dt></span></span> </dl>        | <span data-ttu-id="7d427-154">Нет доступа.</span><span class="sxs-lookup"><span data-stu-id="7d427-154">No access.</span></span><br/>      |
| <dl> <span data-ttu-id="7d427-155"><dt>5.. 15999</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-155"><dt>5..15999</dt></span></span> </dl> | <span data-ttu-id="7d427-156">Зарезервировано DMTF</span><span class="sxs-lookup"><span data-stu-id="7d427-156">DMTF Reserved</span></span><br/>   |
| <dl> <span data-ttu-id="7d427-157"><dt>16000..</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-157"><dt>16000..</dt></span></span> </dl>  | <span data-ttu-id="7d427-158">Поставщик зарезервирован</span><span class="sxs-lookup"><span data-stu-id="7d427-158">Vendor reserved</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="7d427-159">**девиценумбер**</span><span class="sxs-lookup"><span data-stu-id="7d427-159">**DeviceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7d427-160">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7d427-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7d427-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7d427-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7d427-162">Адрес связанного устройства в контексте предшествующего контроллера.</span><span class="sxs-lookup"><span data-stu-id="7d427-162">The address of the associated device in the context of the antecedent controller.</span></span> <span data-ttu-id="7d427-163">Этот класс наследуется от **CIM \_ протоколконтроллерфордевице**.</span><span class="sxs-lookup"><span data-stu-id="7d427-163">This class is inherited from **CIM\_ProtocolControllerForDevice**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d427-164">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d427-164">Remarks</span></span>

<span data-ttu-id="7d427-165">Доступ к классу **\_ протоколконтроллерфорунит мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="7d427-165">Access to the **Msvm\_ProtocolControllerForUnit** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7d427-166">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7d427-166">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7d427-167">Требования</span><span class="sxs-lookup"><span data-stu-id="7d427-167">Requirements</span></span>



| <span data-ttu-id="7d427-168">Требование</span><span class="sxs-lookup"><span data-stu-id="7d427-168">Requirement</span></span> | <span data-ttu-id="7d427-169">Значение</span><span class="sxs-lookup"><span data-stu-id="7d427-169">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d427-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d427-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7d427-171">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7d427-171">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7d427-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d427-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7d427-173">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7d427-173">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7d427-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7d427-174">Namespace</span></span><br/>                | <span data-ttu-id="7d427-175">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7d427-175">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7d427-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7d427-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d427-177"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-177"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d427-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7d427-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d427-179"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7d427-179"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7d427-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d427-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d427-181">**\_ПРОТОКОЛКОНТРОЛЛЕРФОРУНИТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7d427-181">**CIM\_ProtocolControllerForUnit**</span></span>](cim-protocolcontrollerforunit.md)
</dt> <dt>

<span data-ttu-id="7d427-182">[**\_ПРОТОКОЛКОНТРОЛЛЕРФОРУНИТ CIM**](/previous-versions//cc150672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7d427-182">[**CIM\_ProtocolControllerForUnit**](/previous-versions//cc150672(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7d427-183">Классы хранения</span><span class="sxs-lookup"><span data-stu-id="7d427-183">Storage Classes</span></span>](storage-classes.md)
</dt> </dl>

 

