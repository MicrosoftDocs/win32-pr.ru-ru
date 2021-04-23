---
description: Эта Ассоциация устанавливает точку доступа к службе (SAP) в качестве запрашивающей службы протокола из конечной точки протокола.
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Класс Msvm_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2fa01c8e9e7df40a2907e6e43a9cb4b507a53d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999334"
---
# <a name="msvm_bindstolanendpoint-class"></a><span data-ttu-id="22080-103">\_Класс мсвм биндстоланендпоинт</span><span class="sxs-lookup"><span data-stu-id="22080-103">Msvm\_BindsToLANEndpoint class</span></span>

<span data-ttu-id="22080-104">Эта Ассоциация устанавливает точку доступа к службе (SAP) в качестве запрашивающей службы протокола из конечной точки протокола.</span><span class="sxs-lookup"><span data-stu-id="22080-104">This association establishes a service access point (SAP) as a requester of protocol services from a protocol endpoint.</span></span> <span data-ttu-id="22080-105">Как правило, эта ассоциация выполняется между SAPs и конечными точками в одной системе.</span><span class="sxs-lookup"><span data-stu-id="22080-105">Typically, this association runs between SAPs and endpoints on a single system.</span></span> <span data-ttu-id="22080-106">Так как конечная точка протокола является разновидностью SAP, эту привязку можно использовать для установки слоев двух протоколов с верхним уровнем, представленным **зависимым** и нижним слоями, представленными **предшествующей** задачей.</span><span class="sxs-lookup"><span data-stu-id="22080-106">Because a protocol endpoint is a kind of SAP, this binding can be used to establish a layering of two protocols, with the upper layer represented by the **Dependent** and the lower layer represented by the **Antecedent**.</span></span>

<span data-ttu-id="22080-107">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="22080-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="22080-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="22080-108">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a><span data-ttu-id="22080-109">Члены</span><span class="sxs-lookup"><span data-stu-id="22080-109">Members</span></span>

<span data-ttu-id="22080-110">Класс **мсвм \_ биндстоланендпоинт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="22080-110">The **Msvm\_BindsToLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="22080-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="22080-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="22080-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="22080-112">Properties</span></span>

<span data-ttu-id="22080-113">Класс **мсвм \_ биндстоланендпоинт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="22080-113">The **Msvm\_BindsToLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="22080-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="22080-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22080-115">Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="22080-115">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="22080-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22080-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22080-117">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="22080-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="22080-118">Ссылка на класс [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="22080-118">A reference to an [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the switch port.</span></span> <span data-ttu-id="22080-119">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="22080-119">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="22080-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="22080-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22080-121">Тип данных: **[ **мсвм \_ вланендпоинт**](msvm-vlanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="22080-121">Data type: **[**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="22080-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22080-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="22080-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="22080-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="22080-124">Ссылка на [**мсвм \_ вланендпоинт**](msvm-vlanendpoint.md) , связанный с портом коммутатора.</span><span class="sxs-lookup"><span data-stu-id="22080-124">A reference to the [**Msvm\_VLANEndpoint**](msvm-vlanendpoint.md) associated with the switch port.</span></span> <span data-ttu-id="22080-125">Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).</span><span class="sxs-lookup"><span data-stu-id="22080-125">This property is inherited from [**CIM\_Dependency**](/windows/desktop/CIMWin32Prov/cim-dependency).</span></span>

</dd> <dt>

<span data-ttu-id="22080-126">**фраметипе**</span><span class="sxs-lookup"><span data-stu-id="22080-126">**FrameType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="22080-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="22080-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="22080-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="22080-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="22080-129">Описывает метод кадрирования для SAP или конечной точки верхнего уровня, привязанной к конечной точке локальной сети.</span><span class="sxs-lookup"><span data-stu-id="22080-129">Describes the framing method for the upper layer SAP or endpoint that is bound to the LAN endpoint.</span></span> <span data-ttu-id="22080-130">Это свойство наследуется от **CIM \_ биндстоланендпоинт** и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="22080-130">This property is inherited from **CIM\_BindsToLANEndpoint**, and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="22080-131">Требования</span><span class="sxs-lookup"><span data-stu-id="22080-131">Requirements</span></span>



| <span data-ttu-id="22080-132">Требование</span><span class="sxs-lookup"><span data-stu-id="22080-132">Requirement</span></span> | <span data-ttu-id="22080-133">Значение</span><span class="sxs-lookup"><span data-stu-id="22080-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22080-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="22080-134">Minimum supported client</span></span><br/> | <span data-ttu-id="22080-135">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="22080-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="22080-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="22080-136">Minimum supported server</span></span><br/> | <span data-ttu-id="22080-137">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="22080-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="22080-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="22080-138">Namespace</span></span><br/>                | <span data-ttu-id="22080-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="22080-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="22080-140">MOF</span><span class="sxs-lookup"><span data-stu-id="22080-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="22080-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="22080-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="22080-142">DLL</span><span class="sxs-lookup"><span data-stu-id="22080-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22080-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="22080-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

