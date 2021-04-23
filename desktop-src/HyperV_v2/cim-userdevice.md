---
description: Представляет логическое устройство, позволяющее пользователю вводить, просматривать или слышать данные в компьютерной системе.
ms.assetid: 95f88a63-3a2a-4b8c-9849-564dac254933
title: Класс CIM_UserDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UserDevice
- CIM_UserDevice.IsLocked
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8776c0b5e9ddf1653747b82e94040197e4c56f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908728"
---
# <a name="cim_userdevice-class-hyper-v-management"></a><span data-ttu-id="eca94-103">Класс CIM_UserDevice (Управление Hyper-V)</span><span class="sxs-lookup"><span data-stu-id="eca94-103">CIM_UserDevice class (Hyper-V management)</span></span>

<span data-ttu-id="eca94-104">Представляет логическое устройство, позволяющее пользователю вводить, просматривать или слышать данные в компьютерной системе.</span><span class="sxs-lookup"><span data-stu-id="eca94-104">Represents a logical device that allows a user to input, view or hear data on the computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="eca94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eca94-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::UserDevices"), AMENDMENT]
class CIM_UserDevice : CIM_LogicalDevice
{
  boolean IsLocked;
};
```

## <a name="members"></a><span data-ttu-id="eca94-106">Члены</span><span class="sxs-lookup"><span data-stu-id="eca94-106">Members</span></span>

<span data-ttu-id="eca94-107">Класс **CIM \_ усердевице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="eca94-107">The **CIM\_UserDevice** class has these types of members:</span></span>

-   [<span data-ttu-id="eca94-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="eca94-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="eca94-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="eca94-109">Properties</span></span>

<span data-ttu-id="eca94-110">Класс **CIM \_ усердевице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="eca94-110">The **CIM\_UserDevice** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="eca94-111">**IsLocked**</span><span class="sxs-lookup"><span data-stu-id="eca94-111">**IsLocked**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="eca94-112">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="eca94-112">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="eca94-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="eca94-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="eca94-114">**значение true** , если устройство заблокировано, что препятствует вводу или выходу пользователя. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="eca94-114">**true** if the device is locked, preventing user input or output; otherwise, **false**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eca94-115">Требования</span><span class="sxs-lookup"><span data-stu-id="eca94-115">Requirements</span></span>



| <span data-ttu-id="eca94-116">Требование</span><span class="sxs-lookup"><span data-stu-id="eca94-116">Requirement</span></span> | <span data-ttu-id="eca94-117">Значение</span><span class="sxs-lookup"><span data-stu-id="eca94-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eca94-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="eca94-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eca94-119">Windows 8</span><span class="sxs-lookup"><span data-stu-id="eca94-119">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="eca94-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="eca94-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eca94-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="eca94-121">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="eca94-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="eca94-122">Namespace</span></span><br/>                | <span data-ttu-id="eca94-123">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="eca94-123">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="eca94-124">MOF</span><span class="sxs-lookup"><span data-stu-id="eca94-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eca94-125"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eca94-125"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="eca94-126">DLL</span><span class="sxs-lookup"><span data-stu-id="eca94-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eca94-127"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="eca94-127"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="eca94-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="eca94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eca94-129">**Модель \_ CIM**</span><span class="sxs-lookup"><span data-stu-id="eca94-129">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




