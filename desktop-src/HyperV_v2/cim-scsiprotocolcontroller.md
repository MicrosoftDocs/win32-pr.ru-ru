---
description: Представляет контроллер протокола, управляющий интерфейсом SCSI.
ms.assetid: 01ef85fc-2f05-4453-b524-7d63b647f6fb
title: Класс CIM_SCSIProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SCSIProtocolController
- CIM_SCSIProtocolController.NameFormat
- CIM_SCSIProtocolController.OtherNameFormat
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d6479b405d3ca499615981d62744b1eaf25c7598
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682809"
---
# <a name="cim_scsiprotocolcontroller-class"></a><span data-ttu-id="c919e-103">\_Класс CIM сксипротоколконтроллер</span><span class="sxs-lookup"><span data-stu-id="c919e-103">CIM\_SCSIProtocolController class</span></span>

<span data-ttu-id="c919e-104">Представляет контроллер протокола, управляющий интерфейсом SCSI.</span><span class="sxs-lookup"><span data-stu-id="c919e-104">Represents a protocol controller that manages a SCSI interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="c919e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c919e-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.1000"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_SCSIProtocolController : CIM_ProtocolController
{
  uint16 NameFormat;
  string OtherNameFormat;
};
```

## <a name="members"></a><span data-ttu-id="c919e-106">Члены</span><span class="sxs-lookup"><span data-stu-id="c919e-106">Members</span></span>

<span data-ttu-id="c919e-107">Класс **CIM \_ сксипротоколконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c919e-107">The **CIM\_SCSIProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="c919e-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="c919e-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c919e-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c919e-109">Properties</span></span>

<span data-ttu-id="c919e-110">Класс **CIM \_ сксипротоколконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c919e-110">The **CIM\_SCSIProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c919e-111">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="c919e-111">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919e-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c919e-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c919e-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c919e-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c919e-114">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сксипротоколконтроллер**.**Name**","**CIM \_ сксипротоколконтроллер**.**Осернамеформат**")</span><span class="sxs-lookup"><span data-stu-id="c919e-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**OtherNameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="c919e-115">Формат свойства **Name** объекта **CIM \_ сксипротоколконтроллер**.</span><span class="sxs-lookup"><span data-stu-id="c919e-115">The format of the **Name** property of the **CIM\_SCSIProtocolController**.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="c919e-116">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="c919e-116">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="c919e-117">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="c919e-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_Port_WWN"></span><span id="fc_port_wwn"></span><span id="FC_PORT_WWN"></span>

<span data-ttu-id="c919e-118">**WWN порта FC** (2)</span><span class="sxs-lookup"><span data-stu-id="c919e-118">**FC Port WWN** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_Name"></span><span id="iscsi_name"></span><span id="ISCSI_NAME"></span>

<span data-ttu-id="c919e-119">**имя iSCSI** (3)</span><span class="sxs-lookup"><span data-stu-id="c919e-119">**iSCSI Name** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c919e-120">**осернамеформат**</span><span class="sxs-lookup"><span data-stu-id="c919e-120">**OtherNameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c919e-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c919e-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c919e-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c919e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c919e-123">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ сксипротоколконтроллер**.**Name**","**CIM \_ сксипротоколконтроллер**.**Намеформат**")</span><span class="sxs-lookup"><span data-stu-id="c919e-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SCSIProtocolController**.**Name**", "**CIM\_SCSIProtocolController**.**NameFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="c919e-124">Описание свойства **намеформат** , когда параметру **намеформат** присвоено значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="c919e-124">A description of the **NameFormat** property when **NameFormat** is set to "1" (other).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c919e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c919e-125">Requirements</span></span>



| <span data-ttu-id="c919e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c919e-126">Requirement</span></span> | <span data-ttu-id="c919e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c919e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c919e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c919e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c919e-129">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c919e-129">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c919e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c919e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c919e-131">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c919e-131">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c919e-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c919e-132">Namespace</span></span><br/>                | <span data-ttu-id="c919e-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="c919e-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c919e-134">MOF</span><span class="sxs-lookup"><span data-stu-id="c919e-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c919e-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c919e-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c919e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c919e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c919e-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c919e-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c919e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c919e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c919e-139">**\_ПРОТОКОЛКОНТРОЛЛЕР CIM**</span><span class="sxs-lookup"><span data-stu-id="c919e-139">**CIM\_ProtocolController**</span></span>](cim-protocolcontroller.md)
</dt> </dl>

 

