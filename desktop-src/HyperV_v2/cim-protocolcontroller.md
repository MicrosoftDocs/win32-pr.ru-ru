---
description: Представляет группу контроллеров, управляющих работой и функцией устройств, инициирующих протоколы.
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: Класс CIM_ProtocolController
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 27372bc57ad36f37689d75b3963ec0c4b1106956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662140"
---
# <a name="cim_protocolcontroller-class"></a><span data-ttu-id="81316-103">\_Класс CIM протоколконтроллер</span><span class="sxs-lookup"><span data-stu-id="81316-103">CIM\_ProtocolController class</span></span>

<span data-ttu-id="81316-104">Представляет группу контроллеров, управляющих работой и функцией устройств, инициирующих протоколы.</span><span class="sxs-lookup"><span data-stu-id="81316-104">Represents a group of controllers that control the operation and function of devices that initiate protocols.</span></span>

## <a name="syntax"></a><span data-ttu-id="81316-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="81316-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a><span data-ttu-id="81316-106">Члены</span><span class="sxs-lookup"><span data-stu-id="81316-106">Members</span></span>

<span data-ttu-id="81316-107">Класс **CIM \_ протоколконтроллер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="81316-107">The **CIM\_ProtocolController** class has these types of members:</span></span>

-   [<span data-ttu-id="81316-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="81316-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="81316-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="81316-109">Properties</span></span>

<span data-ttu-id="81316-110">Класс **CIM \_ протоколконтроллер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="81316-110">The **CIM\_ProtocolController** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="81316-111">**максунитсконтроллед**</span><span class="sxs-lookup"><span data-stu-id="81316-111">**MaxUnitsControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="81316-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="81316-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="81316-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="81316-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="81316-114">Максимальное число единиц, которое может управляться или доступно через контроллер протокола.</span><span class="sxs-lookup"><span data-stu-id="81316-114">The maximum number of units that can be controlled by or accessed through the protocol controller.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81316-115">Требования</span><span class="sxs-lookup"><span data-stu-id="81316-115">Requirements</span></span>



| <span data-ttu-id="81316-116">Требование</span><span class="sxs-lookup"><span data-stu-id="81316-116">Requirement</span></span> | <span data-ttu-id="81316-117">Значение</span><span class="sxs-lookup"><span data-stu-id="81316-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81316-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="81316-118">Minimum supported client</span></span><br/> | <span data-ttu-id="81316-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="81316-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="81316-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="81316-120">Minimum supported server</span></span><br/> | <span data-ttu-id="81316-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="81316-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="81316-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="81316-122">Namespace</span></span><br/>                | <span data-ttu-id="81316-123">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="81316-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="81316-124">MOF</span><span class="sxs-lookup"><span data-stu-id="81316-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="81316-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="81316-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="81316-126">DLL</span><span class="sxs-lookup"><span data-stu-id="81316-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81316-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="81316-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="81316-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="81316-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81316-129">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="81316-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




