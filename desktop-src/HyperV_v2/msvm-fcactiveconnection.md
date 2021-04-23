---
description: Подключает порт коммутатора к конечной точке Fibre Channel, к которой подключен порт.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Класс Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682866"
---
# <a name="msvm_fcactiveconnection-class"></a><span data-ttu-id="3f59d-103">\_Класс мсвм фкактивеконнектион</span><span class="sxs-lookup"><span data-stu-id="3f59d-103">Msvm\_FcActiveConnection class</span></span>

<span data-ttu-id="3f59d-104">Подключает порт коммутатора к конечной точке Fibre Channel, к которой подключен порт.</span><span class="sxs-lookup"><span data-stu-id="3f59d-104">Connects a switch port to the Fibre Channel endpoint to which the port is connected.</span></span> <span data-ttu-id="3f59d-105">Существование этого объекта означает, что порт коммутатора и конечная точка Fibre Channel активно подключены, а Fibre Channelный порт, связанный с конечной точкой Fibre Channel, может взаимодействовать с сетью через порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="3f59d-105">The existence of this object means that the switch port and the Fibre Channel endpoint are actively connected, and the Fibre Channel port associated with the Fibre Channel endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="3f59d-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="3f59d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f59d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f59d-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="3f59d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="3f59d-108">Members</span></span>

<span data-ttu-id="3f59d-109">Класс **мсвм \_ фкактивеконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3f59d-109">The **Msvm\_FcActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="3f59d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f59d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3f59d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3f59d-111">Properties</span></span>

<span data-ttu-id="3f59d-112">Класс **мсвм \_ фкактивеконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3f59d-112">The **Msvm\_FcActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3f59d-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="3f59d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f59d-114">Тип данных: **мсвм \_ фцендпоинт**</span><span class="sxs-lookup"><span data-stu-id="3f59d-114">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f59d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3f59d-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3f59d-117">Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий точку доступа к службе (SAP), настроенную для обмена данными или активно взаимодействующая с зависимым SAP.</span><span class="sxs-lookup"><span data-stu-id="3f59d-117">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="3f59d-118">В однонаправленном соединении это SAP является передающим.</span><span class="sxs-lookup"><span data-stu-id="3f59d-118">In a unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="3f59d-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="3f59d-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f59d-120">Тип данных: **мсвм \_ фцендпоинт**</span><span class="sxs-lookup"><span data-stu-id="3f59d-120">Data type: **Msvm\_FcEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f59d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="3f59d-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3f59d-123">Ссылка на экземпляр класса [**мсвм \_ фцендпоинт**](msvm-fcendpoint.md) , представляющий SAP, настроенный для обмена данными или активно взаимодействующий с предшествующей SAP.</span><span class="sxs-lookup"><span data-stu-id="3f59d-123">A reference to an instance of the [**Msvm\_FcEndpoint**](msvm-fcendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="3f59d-124">В однонаправленном соединении этот SAP является получаемым.</span><span class="sxs-lookup"><span data-stu-id="3f59d-124">In a unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="3f59d-125">**По поднаправлению**</span><span class="sxs-lookup"><span data-stu-id="3f59d-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f59d-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="3f59d-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f59d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f59d-128">Если это свойство имеет **значение true**, это соединение является однонаправленным; в противном случае это соединение является двунаправленным.</span><span class="sxs-lookup"><span data-stu-id="3f59d-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="3f59d-129">При однонаправленном соединении «докладчик» должен быть определен как ссылка **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="3f59d-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="3f59d-130">В двунаправленном соединении не имеет значения, является ли выбранная точка доступа **предшествующей** или **зависимой**.</span><span class="sxs-lookup"><span data-stu-id="3f59d-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="3f59d-131">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3f59d-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3f59d-132">**осертраффикдескриптион**</span><span class="sxs-lookup"><span data-stu-id="3f59d-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f59d-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="3f59d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f59d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f59d-135">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="3f59d-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3f59d-136">**ТипТрафика**</span><span class="sxs-lookup"><span data-stu-id="3f59d-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3f59d-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3f59d-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3f59d-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="3f59d-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3f59d-139">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="3f59d-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f59d-140">Требования</span><span class="sxs-lookup"><span data-stu-id="3f59d-140">Requirements</span></span>



| <span data-ttu-id="3f59d-141">Требование</span><span class="sxs-lookup"><span data-stu-id="3f59d-141">Requirement</span></span> | <span data-ttu-id="3f59d-142">Значение</span><span class="sxs-lookup"><span data-stu-id="3f59d-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f59d-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f59d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3f59d-144">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="3f59d-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3f59d-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f59d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3f59d-146">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="3f59d-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3f59d-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3f59d-147">Namespace</span></span><br/>                | <span data-ttu-id="3f59d-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="3f59d-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3f59d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="3f59d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3f59d-150"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3f59d-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3f59d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="3f59d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f59d-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3f59d-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

