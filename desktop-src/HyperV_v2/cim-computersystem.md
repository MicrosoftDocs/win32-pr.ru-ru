---
description: Представляет коллекцию, которая предоставляет вычислительные возможности и состоит из \_ объектов CIM манажедсистемелемент.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: Класс CIM_ComputerSystem (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684562"
---
# <a name="cim_computersystem-class-hyper-v-management"></a><span data-ttu-id="4efd5-103">Класс CIM_ComputerSystem (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="4efd5-103">CIM_ComputerSystem class (Hyper-V management)</span></span>

<span data-ttu-id="4efd5-104">Представляет коллекцию, которая предоставляет вычислительные возможности и состоит из объектов [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md) .</span><span class="sxs-lookup"><span data-stu-id="4efd5-104">Represents a collection that provides computing capabilities and consists of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="4efd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4efd5-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="4efd5-106">Члены</span><span class="sxs-lookup"><span data-stu-id="4efd5-106">Members</span></span>

<span data-ttu-id="4efd5-107">Класс **CIM \_ ComputerSystem** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4efd5-107">The **CIM\_ComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="4efd5-108">Методы</span><span class="sxs-lookup"><span data-stu-id="4efd5-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="4efd5-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4efd5-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4efd5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="4efd5-110">Methods</span></span>

<span data-ttu-id="4efd5-111">Класс **CIM \_ ComputerSystem** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4efd5-111">The **CIM\_ComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="4efd5-112">Метод</span><span class="sxs-lookup"><span data-stu-id="4efd5-112">Method</span></span>                                                    | <span data-ttu-id="4efd5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4efd5-113">Description</span></span>                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4efd5-114">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="4efd5-114">**SetPowerState**</span></span>](cim-computersystem-setpowerstate.md) | <span data-ttu-id="4efd5-115">Этот метод является устаревшим.</span><span class="sxs-lookup"><span data-stu-id="4efd5-115">This method is deprecated.</span></span> <span data-ttu-id="4efd5-116">Вместо этого используйте метод **рекуестповерстатечанже** в классе **CIM \_ поверманажементсервице** .</span><span class="sxs-lookup"><span data-stu-id="4efd5-116">Instead, use the **RequestPowerStateChange** method in the **CIM\_PowerManagementService** class.</span></span><br/> <span data-ttu-id="4efd5-117">**Нерекомендуемое описание:** Задает состояние электропитания компьютера.</span><span class="sxs-lookup"><span data-stu-id="4efd5-117">**Deprecated description:** Sets the power state of the computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4efd5-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="4efd5-118">Properties</span></span>

<span data-ttu-id="4efd5-119">Класс **CIM \_ ComputerSystem** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4efd5-119">The **CIM\_ComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4efd5-120">**Выделенные**</span><span class="sxs-lookup"><span data-stu-id="4efd5-120">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4efd5-121">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4efd5-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4efd5-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-123">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. ИНЦИТС-T11 \| Platform \| PlatformType "), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Осердедикатеддескриптионс**")</span><span class="sxs-lookup"><span data-stu-id="4efd5-123">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.sysServices", "FC-GS.INCITS-T11 \| Platform \| PlatformType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**OtherDedicatedDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="4efd5-124">Назначение и функции компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="4efd5-124">The purpose and features of the computer system.</span></span> <span data-ttu-id="4efd5-125">Например, система, предназначенная для печати, может указать «11» (печать).</span><span class="sxs-lookup"><span data-stu-id="4efd5-125">For example, a system dedicated to printing could specify "11" (Print).</span></span> <span data-ttu-id="4efd5-126">Системе общего назначения с возможностями печати можно присвоить значение "0" (не выделенное) и "11" (печать).</span><span class="sxs-lookup"><span data-stu-id="4efd5-126">A general purpose system with printing capabilities can be set to "0" (Not Dedicated) and "11" (Print).</span></span>

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span data-ttu-id="4efd5-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Не выделено** (0)</span><span class="sxs-lookup"><span data-stu-id="4efd5-127"><span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Not Dedicated** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4efd5-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="4efd5-128"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4efd5-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (2)</span><span class="sxs-lookup"><span data-stu-id="4efd5-129"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span data-ttu-id="4efd5-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Хранилище** (3)</span><span class="sxs-lookup"><span data-stu-id="4efd5-130"><span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Storage** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span data-ttu-id="4efd5-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Маршрутизатор** (4)</span><span class="sxs-lookup"><span data-stu-id="4efd5-131"><span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span data-ttu-id="4efd5-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span><span class="sxs-lookup"><span data-stu-id="4efd5-132"><span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span data-ttu-id="4efd5-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Переключатель уровня 3** (6)</span><span class="sxs-lookup"><span data-stu-id="4efd5-133"><span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3 Switch** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span data-ttu-id="4efd5-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Центральный офисный коммутатор** (7)</span><span class="sxs-lookup"><span data-stu-id="4efd5-134"><span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Central Office Switch** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span data-ttu-id="4efd5-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Концентратор** (8)</span><span class="sxs-lookup"><span data-stu-id="4efd5-135"><span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span data-ttu-id="4efd5-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Сервер доступа** (9)</span><span class="sxs-lookup"><span data-stu-id="4efd5-136"><span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Access Server** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span data-ttu-id="4efd5-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Брандмауэр** (10)</span><span class="sxs-lookup"><span data-stu-id="4efd5-137"><span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="4efd5-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Печать** (11)</span><span class="sxs-lookup"><span data-stu-id="4efd5-138"><span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Print** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span data-ttu-id="4efd5-139"><span id="I_O"></span><span id="i_o"></span>**Ввод-вывод** (12)</span><span class="sxs-lookup"><span data-stu-id="4efd5-139"><span id="I_O"></span><span id="i_o"></span>**I/O** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span data-ttu-id="4efd5-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Веб-кэширование** (13)</span><span class="sxs-lookup"><span data-stu-id="4efd5-140"><span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Web Caching** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span data-ttu-id="4efd5-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Управление** (14)</span><span class="sxs-lookup"><span data-stu-id="4efd5-141"><span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Management** (14)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-142">Этот экземпляр предназначен для размещения программного обеспечения управления системой</span><span class="sxs-lookup"><span data-stu-id="4efd5-142">This instance is dedicated to hosting system management software</span></span>

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span data-ttu-id="4efd5-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Блокировка сервера** (15)</span><span class="sxs-lookup"><span data-stu-id="4efd5-143"><span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span data-ttu-id="4efd5-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Файловый сервер** (16)</span><span class="sxs-lookup"><span data-stu-id="4efd5-144"><span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**File Server** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span data-ttu-id="4efd5-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Мобильное устройство пользователя** (17)</span><span class="sxs-lookup"><span data-stu-id="4efd5-145"><span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobile User Device** (17)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-146">Примером выделенного устройства пользователя является мобильный телефон или сканер штрихкодов в магазине, который взаимодействует через радиочастоту.</span><span class="sxs-lookup"><span data-stu-id="4efd5-146">An example of a dedicated user device is a mobile phone or a barcode scanner in a store that communicates via radio frequency.</span></span> <span data-ttu-id="4efd5-147">Эти системы весьма ограничены функциональными возможностями и программируемостью и не считаются вычислительными платформами общего назначения.</span><span class="sxs-lookup"><span data-stu-id="4efd5-147">These systems are quite limited in functionality and programmability, and are not considered 'general purpose' computing platforms.</span></span> <span data-ttu-id="4efd5-148">В качестве альтернативы, пример мобильной системы, которая является "общей целью" (т. е. не является выделенной), — это компьютер, удерживаемый вручную.</span><span class="sxs-lookup"><span data-stu-id="4efd5-148">Alternately, an example of a mobile system that is 'general purpose' (i.e., is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="4efd5-149">Хотя это и ограничено программируемостью, можно скачать новое программное обеспечение и его функциональность, развернутую пользователем.</span><span class="sxs-lookup"><span data-stu-id="4efd5-149">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span>

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span data-ttu-id="4efd5-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span><span class="sxs-lookup"><span data-stu-id="4efd5-150"><span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span data-ttu-id="4efd5-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Мост/расширитель** (19)</span><span class="sxs-lookup"><span data-stu-id="4efd5-151"><span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span data-ttu-id="4efd5-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Шлюз** (20)</span><span class="sxs-lookup"><span data-stu-id="4efd5-152"><span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span data-ttu-id="4efd5-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Виртуализация хранилища** (21)</span><span class="sxs-lookup"><span data-stu-id="4efd5-153"><span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Storage Virtualizer** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span data-ttu-id="4efd5-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Библиотека мультимедиа** (22)</span><span class="sxs-lookup"><span data-stu-id="4efd5-154"><span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Media Library** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span data-ttu-id="4efd5-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**Екстендерноде** (23)</span><span class="sxs-lookup"><span data-stu-id="4efd5-155"><span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**ExtenderNode** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span data-ttu-id="4efd5-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**Головка NAS** (24)</span><span class="sxs-lookup"><span data-stu-id="4efd5-156"><span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS Head** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span data-ttu-id="4efd5-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Автономный NAS** (25)</span><span class="sxs-lookup"><span data-stu-id="4efd5-157"><span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Self-contained NAS** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span data-ttu-id="4efd5-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span><span class="sxs-lookup"><span data-stu-id="4efd5-158"><span id="UPS"></span><span id="ups"></span>**UPS** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span data-ttu-id="4efd5-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP-телефон** (27)</span><span class="sxs-lookup"><span data-stu-id="4efd5-159"><span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP Phone** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span data-ttu-id="4efd5-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Контроллер управления** (28)</span><span class="sxs-lookup"><span data-stu-id="4efd5-160"><span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Management Controller** (28)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-161">Этот экземпляр представляет специализированное оборудование, выделенное для управления системами (например, контроллер управления основной платой (BMC) или процессор служб).</span><span class="sxs-lookup"><span data-stu-id="4efd5-161">This instance represents specialized hardware dedicated to systems management (i.e., a Baseboard Management Controller (BMC) or service processor).</span></span>

<span data-ttu-id="4efd5-162">Областью управления "контроллер управления" обычно является единая управляемая система, в которой он содержится.</span><span class="sxs-lookup"><span data-stu-id="4efd5-162">The management scope of a "Management Controller" is typically a single managed system in which it is contained.</span></span>

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span data-ttu-id="4efd5-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Диспетчер корпусов** (29)</span><span class="sxs-lookup"><span data-stu-id="4efd5-163"><span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis Manager** (29)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-164">Этот экземпляр представляет систему, предназначенную для управления блейд-корпусом и содержащимися в нем устройствами.</span><span class="sxs-lookup"><span data-stu-id="4efd5-164">This instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="4efd5-165">Это значение будет использоваться для представления контроллера полки.</span><span class="sxs-lookup"><span data-stu-id="4efd5-165">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="4efd5-166">"Диспетчер шасси" — это точка статистической обработки для управления, которая может полагаться на подчиненные контроллеры управления для управления составляющими частями.</span><span class="sxs-lookup"><span data-stu-id="4efd5-166">A "Chassis Manager" is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span>

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span data-ttu-id="4efd5-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**RAID-контроллер на основе узла** (30)</span><span class="sxs-lookup"><span data-stu-id="4efd5-167"><span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host-based RAID controller** (30)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-168">Этот экземпляр представляет контроллер хранилища RAID, содержащийся на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4efd5-168">This instance represents a RAID storage controller contained within a host computer.</span></span>

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span data-ttu-id="4efd5-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Корпус устройства хранения данных** (31)</span><span class="sxs-lookup"><span data-stu-id="4efd5-169"><span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Storage Device Enclosure** (31)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-170">Этот экземпляр представляет корпус, содержащий устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="4efd5-170">This instance represents an enclosure that contains storage devices.</span></span>

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span data-ttu-id="4efd5-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Рабочий стол** (32)</span><span class="sxs-lookup"><span data-stu-id="4efd5-171"><span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span data-ttu-id="4efd5-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Портативный компьютер** (33)</span><span class="sxs-lookup"><span data-stu-id="4efd5-172"><span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span data-ttu-id="4efd5-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Виртуальная ленточная библиотека** (34)</span><span class="sxs-lookup"><span data-stu-id="4efd5-173"><span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Virtual Tape Library** (34)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-174">Эмуляция ленточной библиотеки с помощью виртуальной системы библиотеки.</span><span class="sxs-lookup"><span data-stu-id="4efd5-174">The emulation of a tape library by a Virtual Library System.</span></span>

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span data-ttu-id="4efd5-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Виртуальная система библиотеки** (35)</span><span class="sxs-lookup"><span data-stu-id="4efd5-175"><span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtual Library System** (35)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-176">Использует дисковый накопитель для эмуляции ленточных библиотек</span><span class="sxs-lookup"><span data-stu-id="4efd5-176">Uses disk storage to emulate tape libraries</span></span>

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span data-ttu-id="4efd5-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Сетевой компьютер или тонкий клиент** (36)</span><span class="sxs-lookup"><span data-stu-id="4efd5-177"><span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Network PC/Thin Client** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span data-ttu-id="4efd5-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**Коммутатор FC** (37)</span><span class="sxs-lookup"><span data-stu-id="4efd5-178"><span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC Switch** (37)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-179">Выделен для переключения на кадры Fibre Channel уровня 2.</span><span class="sxs-lookup"><span data-stu-id="4efd5-179">Dedicated to switching layer 2 fibre channel frames.</span></span>

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span data-ttu-id="4efd5-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Коммутатор Ethernet** (38)</span><span class="sxs-lookup"><span data-stu-id="4efd5-180"><span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet Switch** (38)</span></span>


</dt> <dd>

<span data-ttu-id="4efd5-181">Выделен для переключения кадров Ethernet уровня 2</span><span class="sxs-lookup"><span data-stu-id="4efd5-181">Dedicated to switching layer 2 ethernet frames</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4efd5-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="4efd5-182"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4efd5-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32568.. 65535)</span><span class="sxs-lookup"><span data-stu-id="4efd5-183"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32568..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4efd5-184">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="4efd5-184">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4efd5-185">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4efd5-185">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-186">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4efd5-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-187">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("намеформат")</span><span class="sxs-lookup"><span data-stu-id="4efd5-187">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")</span></span>
</dt> </dl>

<span data-ttu-id="4efd5-188">Формат имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="4efd5-188">The format of the computer system name.</span></span>

<dt>



 <span data-ttu-id="4efd5-189">("Другое")</span><span class="sxs-lookup"><span data-stu-id="4efd5-189">("Other")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-190">("IP")</span><span class="sxs-lookup"><span data-stu-id="4efd5-190">("IP")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-191">("Набрать")</span><span class="sxs-lookup"><span data-stu-id="4efd5-191">("Dial")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-192">("HID")</span><span class="sxs-lookup"><span data-stu-id="4efd5-192">("HID")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-193">("НВА")</span><span class="sxs-lookup"><span data-stu-id="4efd5-193">("NWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-194">("Хва")</span><span class="sxs-lookup"><span data-stu-id="4efd5-194">("HWA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-195">("X25")</span><span class="sxs-lookup"><span data-stu-id="4efd5-195">("X25")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-196">("ISDN")</span><span class="sxs-lookup"><span data-stu-id="4efd5-196">("ISDN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-197">("IPX")</span><span class="sxs-lookup"><span data-stu-id="4efd5-197">("IPX")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-198">("ДКК")</span><span class="sxs-lookup"><span data-stu-id="4efd5-198">("DCC")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-199">("ICD")</span><span class="sxs-lookup"><span data-stu-id="4efd5-199">("ICD")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-200">("E. 164")</span><span class="sxs-lookup"><span data-stu-id="4efd5-200">("E.164")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-201">("SNA")</span><span class="sxs-lookup"><span data-stu-id="4efd5-201">("SNA")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-202">("OID/OSI")</span><span class="sxs-lookup"><span data-stu-id="4efd5-202">("OID/OSI")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-203">("WWN")</span><span class="sxs-lookup"><span data-stu-id="4efd5-203">("WWN")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4efd5-204">("УДАЛЯЕМ")</span><span class="sxs-lookup"><span data-stu-id="4efd5-204">("NAA")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4efd5-205">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="4efd5-205">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4efd5-206">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="4efd5-206">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-207">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4efd5-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-208">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ComputerSystem**.**Выделенный**")</span><span class="sxs-lookup"><span data-stu-id="4efd5-208">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ComputerSystem**.**Dedicated**")</span></span>
</dt> </dl>

<span data-ttu-id="4efd5-209">Описывает, как или почему система выделяется, когда **выделенный** массив включает значение 2 (другое).</span><span class="sxs-lookup"><span data-stu-id="4efd5-209">Describes how or why the system is dedicated when the **Dedicated** array includes the value 2 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="4efd5-210">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="4efd5-210">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4efd5-211">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="4efd5-211">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-212">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4efd5-212">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-213">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ поверманажементкапабилитиес. поверкапабилитиес"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Элементы управления питанием системы DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="4efd5-213">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM\_PowerManagementCapabilities.PowerCapabilities"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Power Controls\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="4efd5-214">Это свойство использовать не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="4efd5-214">This property is deprecated.</span></span> <span data-ttu-id="4efd5-215">Вместо этого используйте метод **поверчанжекапабилитиес** в классе **CIM \_ поверманажементкапабилитиесЦим \_ поверманажементсервице** .</span><span class="sxs-lookup"><span data-stu-id="4efd5-215">Instead, use the **PowerChangeCapabilities** method in the **CIM\_PowerManagementCapabilitiesCIM\_PowerManagementService** class.</span></span>

<span data-ttu-id="4efd5-216">**Нерекомендуемое описание:** Возможности системы по управлению питанием.</span><span class="sxs-lookup"><span data-stu-id="4efd5-216">**Deprecated description:** The power management capabilities of the system.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4efd5-217">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="4efd5-217">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="4efd5-218">**Не поддерживается** (1)</span><span class="sxs-lookup"><span data-stu-id="4efd5-218">**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4efd5-219">**Отключено** (2)</span><span class="sxs-lookup"><span data-stu-id="4efd5-219">**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4efd5-220">**Включено** (3)</span><span class="sxs-lookup"><span data-stu-id="4efd5-220">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="4efd5-221">**Режимы энергосбережения** записываются автоматически (4)</span><span class="sxs-lookup"><span data-stu-id="4efd5-221">**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="4efd5-222">**Настраиваемое состояние питания** (5)</span><span class="sxs-lookup"><span data-stu-id="4efd5-222">**Power State Settable** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="4efd5-223">**Поддержка циклов электропитания** (6)</span><span class="sxs-lookup"><span data-stu-id="4efd5-223">**Power Cycling Supported** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="4efd5-224">**Поддерживается время включения** (7)</span><span class="sxs-lookup"><span data-stu-id="4efd5-224">**Timed Power On Supported** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4efd5-225">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="4efd5-225">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4efd5-226">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4efd5-226">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-227">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4efd5-227">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4efd5-228">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| System Security аппаратная безопасность \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="4efd5-228">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Hardware Security\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="4efd5-229">Указывает, поддерживает ли система аппаратную операцию сброса.</span><span class="sxs-lookup"><span data-stu-id="4efd5-229">Indicates whether the system supports the hardware reset operation.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4efd5-230">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="4efd5-230">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="4efd5-231">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="4efd5-231">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="4efd5-232">**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="4efd5-232">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="4efd5-233">**Включено** (4)</span><span class="sxs-lookup"><span data-stu-id="4efd5-233">**Enabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

<span data-ttu-id="4efd5-234">**Не реализовано** (5)</span><span class="sxs-lookup"><span data-stu-id="4efd5-234">**Not Implemented** (5)</span></span>


<span data-ttu-id="4efd5-235"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="4efd5-235"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="4efd5-236">Требования</span><span class="sxs-lookup"><span data-stu-id="4efd5-236">Requirements</span></span>



| <span data-ttu-id="4efd5-237">Требование</span><span class="sxs-lookup"><span data-stu-id="4efd5-237">Requirement</span></span> | <span data-ttu-id="4efd5-238">Значение</span><span class="sxs-lookup"><span data-stu-id="4efd5-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4efd5-239">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4efd5-239">Minimum supported client</span></span><br/> | <span data-ttu-id="4efd5-240">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4efd5-240">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4efd5-241">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4efd5-241">Minimum supported server</span></span><br/> | <span data-ttu-id="4efd5-242">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4efd5-242">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4efd5-243">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4efd5-243">Namespace</span></span><br/>                | <span data-ttu-id="4efd5-244">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4efd5-244">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4efd5-245">MOF</span><span class="sxs-lookup"><span data-stu-id="4efd5-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4efd5-246"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4efd5-246"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4efd5-247">DLL</span><span class="sxs-lookup"><span data-stu-id="4efd5-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4efd5-248"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4efd5-248"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4efd5-249">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4efd5-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4efd5-250">**\_Система CIM**</span><span class="sxs-lookup"><span data-stu-id="4efd5-250">**CIM\_System**</span></span>](cim-system.md)
</dt> </dl>

 

