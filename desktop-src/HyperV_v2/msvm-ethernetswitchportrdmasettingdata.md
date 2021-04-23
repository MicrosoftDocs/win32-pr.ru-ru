---
description: Представляет данные о параметре функции RDMA порта.
ms.assetid: a9b8c98f-194e-4eec-8d4a-961b1a439e62
title: Класс Msvm_EthernetSwitchPortRdmaSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRdmaSettingData
- Msvm_EthernetSwitchPortRdmaSettingData.RdmaOffloadWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98d4f06923bfcfa16d564b296e3b544d9aad6275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913891"
---
# <a name="msvm_ethernetswitchportrdmasettingdata-class"></a><span data-ttu-id="4314f-103">\_Класс мсвм есернетсвитчпортрдмасеттингдата</span><span class="sxs-lookup"><span data-stu-id="4314f-103">Msvm\_EthernetSwitchPortRdmaSettingData class</span></span>

<span data-ttu-id="4314f-104">Представляет данные о параметре функции RDMA порта.</span><span class="sxs-lookup"><span data-stu-id="4314f-104">Represents the port RDMA feature setting data.</span></span>

<span data-ttu-id="4314f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4314f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4314f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4314f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("7A498FC4-8572-4FDC-92AB-7A6FC7042D53"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Rdma Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRdmaSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32 RdmaOffloadWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="4314f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4314f-107">Members</span></span>

<span data-ttu-id="4314f-108">Класс **мсвм \_ есернетсвитчпортрдмасеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4314f-108">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4314f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4314f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4314f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4314f-110">Properties</span></span>

<span data-ttu-id="4314f-111">Класс **мсвм \_ есернетсвитчпортрдмасеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4314f-111">The **Msvm\_EthernetSwitchPortRdmaSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4314f-112">**рдмаоффлоадвеигхт**</span><span class="sxs-lookup"><span data-stu-id="4314f-112">**RdmaOffloadWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4314f-113">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4314f-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4314f-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4314f-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4314f-115">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="4314f-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4314f-116">Вес, назначенный этому порту для гостевого RDMA.</span><span class="sxs-lookup"><span data-stu-id="4314f-116">The weight assigned to this port for Guest RDMA.</span></span> <span data-ttu-id="4314f-117">Вес — это относительная важность при назначении ресурсов RDMA.</span><span class="sxs-lookup"><span data-stu-id="4314f-117">The weight is the relative importance when assigning RDMA resources.</span></span> <span data-ttu-id="4314f-118">Установка значения 0 для свойства **рдмаоффлоадвеигхт** отключает RDMA на порте.</span><span class="sxs-lookup"><span data-stu-id="4314f-118">Setting the **RdmaOffloadWeight** property to 0 disables RDMA on the port.</span></span> <span data-ttu-id="4314f-119">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="4314f-119">The default is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4314f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="4314f-120">Requirements</span></span>



| <span data-ttu-id="4314f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="4314f-121">Requirement</span></span> | <span data-ttu-id="4314f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="4314f-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4314f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4314f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4314f-124">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="4314f-124">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="4314f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4314f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4314f-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4314f-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4314f-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4314f-127">Namespace</span></span><br/>                | <span data-ttu-id="4314f-128">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4314f-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4314f-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4314f-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4314f-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4314f-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4314f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4314f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4314f-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4314f-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4314f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4314f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4314f-134">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="4314f-134">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

 




