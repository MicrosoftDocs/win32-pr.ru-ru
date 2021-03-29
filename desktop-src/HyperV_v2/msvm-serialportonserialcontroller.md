---
description: Связывает последовательный порт с последовательным контроллером.
ms.assetid: A07DE787-2600-4C40-9CE2-7D96D6A58E53
title: Класс Msvm_SerialPortOnSerialController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SerialPortOnSerialController
- Msvm_SerialPortOnSerialController.Antecedent
- Msvm_SerialPortOnSerialController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 357192bfb3dc4e901dd40a0cb6d7884152c3afc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897818"
---
# <a name="msvm_serialportonserialcontroller-class"></a><span data-ttu-id="38b7b-103">\_Класс мсвм сериалпортонсериалконтроллер</span><span class="sxs-lookup"><span data-stu-id="38b7b-103">Msvm\_SerialPortOnSerialController class</span></span>

<span data-ttu-id="38b7b-104">Связывает последовательный порт с последовательным контроллером.</span><span class="sxs-lookup"><span data-stu-id="38b7b-104">Associates a serial port with a serial controller.</span></span>

<span data-ttu-id="38b7b-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="38b7b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b7b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="38b7b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SerialPortOnSerialController : CIM_PortOnDevice
{
  CIM_LogicalDevice REF Antecedent;
  CIM_LogicalPort   REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="38b7b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="38b7b-107">Members</span></span>

<span data-ttu-id="38b7b-108">Класс **мсвм \_ сериалпортонсериалконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="38b7b-108">The **Msvm\_SerialPortOnSerialController** class has these types of members:</span></span>

-   [<span data-ttu-id="38b7b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="38b7b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38b7b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="38b7b-110">Properties</span></span>

<span data-ttu-id="38b7b-111">Класс **мсвм \_ сериалпортонсериалконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="38b7b-111">The **Msvm\_SerialPortOnSerialController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38b7b-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="38b7b-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b7b-113">Тип данных: CIM с типом " **[ **модель \_** "](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="38b7b-113">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="38b7b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38b7b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38b7b-115">Последовательный контроллер, к которому подключен порт.</span><span class="sxs-lookup"><span data-stu-id="38b7b-115">The serial controller to which the port is connected.</span></span> <span data-ttu-id="38b7b-116">Это свойство наследуется от [**CIM \_ портондевице**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="38b7b-116">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> <dt>

<span data-ttu-id="38b7b-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="38b7b-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38b7b-118">Тип данных: **[ **CIM \_ логикалпорт**](/previous-versions//cc136869(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="38b7b-118">Data type: **[**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="38b7b-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="38b7b-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38b7b-120">Порт последовательного контроллера.</span><span class="sxs-lookup"><span data-stu-id="38b7b-120">The port of the serial controller.</span></span> <span data-ttu-id="38b7b-121">Это свойство наследуется от [**CIM \_ портондевице**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span><span class="sxs-lookup"><span data-stu-id="38b7b-121">This property is inherited from [**CIM\_PortOnDevice**](/previous-versions/windows/desktop/clushyperv/cim-portondevice).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38b7b-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="38b7b-122">Remarks</span></span>

<span data-ttu-id="38b7b-123">Доступ к классу **\_ сериалпортонсериалконтроллер мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="38b7b-123">Access to the **Msvm\_SerialPortOnSerialController** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="38b7b-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="38b7b-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="38b7b-125">Требования</span><span class="sxs-lookup"><span data-stu-id="38b7b-125">Requirements</span></span>



| <span data-ttu-id="38b7b-126">Требование</span><span class="sxs-lookup"><span data-stu-id="38b7b-126">Requirement</span></span> | <span data-ttu-id="38b7b-127">Значение</span><span class="sxs-lookup"><span data-stu-id="38b7b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38b7b-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="38b7b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="38b7b-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="38b7b-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="38b7b-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="38b7b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="38b7b-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="38b7b-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="38b7b-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="38b7b-132">Namespace</span></span><br/>                | <span data-ttu-id="38b7b-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="38b7b-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="38b7b-134">MOF</span><span class="sxs-lookup"><span data-stu-id="38b7b-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38b7b-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38b7b-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="38b7b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="38b7b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38b7b-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="38b7b-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="38b7b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="38b7b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38b7b-139">**\_ПОРТОНДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="38b7b-139">**CIM\_PortOnDevice**</span></span>](cim-portondevice.md)
</dt> <dt>

[<span data-ttu-id="38b7b-140">**\_ПОРТОНДЕВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="38b7b-140">**CIM\_PortOnDevice**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-portondevice)
</dt> <dt>

[<span data-ttu-id="38b7b-141">Классы последовательных устройств</span><span class="sxs-lookup"><span data-stu-id="38b7b-141">Serial Devices Classes</span></span>](serial-devices-classes.md)
</dt> </dl>

 

