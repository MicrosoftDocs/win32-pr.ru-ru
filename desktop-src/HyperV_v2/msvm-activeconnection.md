---
description: Подключает порт коммутатора к конечной точке локальной сети, к которой подключен порт.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Класс Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911924"
---
# <a name="msvm_activeconnection-class"></a><span data-ttu-id="4dcaa-103">\_Класс мсвм ActiveConnection</span><span class="sxs-lookup"><span data-stu-id="4dcaa-103">Msvm\_ActiveConnection class</span></span>

<span data-ttu-id="4dcaa-104">Подключает порт коммутатора к конечной точке локальной сети, к которой подключен порт.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-104">Connects a switch port to the LAN endpoint to which the port is connected.</span></span> <span data-ttu-id="4dcaa-105">Наличие этого объекта означает, что порт коммутатора и конечная точка локальной сети активно подключены, а порт Ethernet, связанный с конечной точкой локальной сети, может взаимодействовать с сетью через порт коммутатора.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-105">The existence of this object means that the switch port and the LAN endpoint are actively connected and the Ethernet port associated with the LAN endpoint can communicate with the network through the switch port.</span></span>

<span data-ttu-id="4dcaa-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4dcaa-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4dcaa-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a><span data-ttu-id="4dcaa-108">Члены</span><span class="sxs-lookup"><span data-stu-id="4dcaa-108">Members</span></span>

<span data-ttu-id="4dcaa-109">Класс **мсвм \_ ActiveConnection** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4dcaa-109">The **Msvm\_ActiveConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="4dcaa-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4dcaa-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4dcaa-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4dcaa-111">Properties</span></span>

<span data-ttu-id="4dcaa-112">Класс **мсвм \_ ActiveConnection** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-112">The **Msvm\_ActiveConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4dcaa-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dcaa-114">Тип данных: **[ **мсвм \_ ланендпоинт**](msvm-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-114">Data type: **[**Msvm\_LANEndpoint**](msvm-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dcaa-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-116">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="4dcaa-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="4dcaa-117">Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](msvm-lanendpoint.md) , представляющий точку доступа к службе (SAP), настроенную для обмена данными или активно взаимодействующая с зависимым SAP.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-117">A reference to an instance of the [**Msvm\_LANEndpoint**](msvm-lanendpoint.md) class that represents the service access point (SAP) that is configured to communicate or is actively communicating with the dependent SAP.</span></span> <span data-ttu-id="4dcaa-118">В однонаправленном соединении это SAP является передающим.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-118">In an unidirectional connection, this SAP is the one that is transmitting.</span></span>

</dd> <dt>

<span data-ttu-id="4dcaa-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dcaa-120">Тип данных: **[ **CIM \_ ланендпоинт**](cim-lanendpoint.md)**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-120">Data type: **[**CIM\_LANEndpoint**](cim-lanendpoint.md)**</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dcaa-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="4dcaa-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="4dcaa-123">Ссылка на экземпляр класса [**мсвм \_ ланендпоинт**](cim-lanendpoint.md) , представляющий SAP, настроенный для обмена данными или активно взаимодействующий с предшествующей SAP.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-123">A reference to an instance of the [**Msvm\_LANEndpoint**](cim-lanendpoint.md) class that represents the SAP that is configured to communicate or is actively communicating with the antecedent SAP.</span></span> <span data-ttu-id="4dcaa-124">В однонаправленном соединении этот SAP является получаемым.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-124">In an unidirectional connection, this SAP is the one that is receiving.</span></span>

</dd> <dt>

<span data-ttu-id="4dcaa-125">**По поднаправлению**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-125">**IsUnidirectional**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dcaa-126">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-126">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dcaa-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dcaa-128">Если это свойство имеет **значение true**, это соединение является однонаправленным; в противном случае это соединение является двунаправленным.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-128">If this property is **True**, this connection is unidirectional; otherwise, this connection is bidirectional.</span></span> <span data-ttu-id="4dcaa-129">При однонаправленном соединении «докладчик» должен быть определен как ссылка **Antecedent** .</span><span class="sxs-lookup"><span data-stu-id="4dcaa-129">When a connection is unidirectional, the "speaker" should be defined as the **Antecedent** reference.</span></span> <span data-ttu-id="4dcaa-130">В двунаправленном соединении не имеет значения, является ли выбранная точка доступа **предшествующей** или **зависимой**.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-130">In a bidirectional connection, it does not matter whether the selected access point is the **Antecedent** or **Dependent**.</span></span> <span data-ttu-id="4dcaa-131">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="4dcaa-131">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="4dcaa-132">**осертраффикдескриптион**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-132">**OtherTrafficDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dcaa-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dcaa-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dcaa-135">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-135">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="4dcaa-136">**ТипТрафика**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-136">**TrafficType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4dcaa-137">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-137">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4dcaa-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4dcaa-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4dcaa-139">Это свойство наследуется от [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), но не используется.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-139">This property is inherited from [**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85)), but it is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4dcaa-140">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4dcaa-140">Remarks</span></span>

<span data-ttu-id="4dcaa-141">Доступ к классу **\_ ActiveConnection мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="4dcaa-141">Access to the **Msvm\_ActiveConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="4dcaa-142">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="4dcaa-142">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="4dcaa-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="4dcaa-143">Examples</span></span>

<span data-ttu-id="4dcaa-144">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4dcaa-144">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4dcaa-145">Требования</span><span class="sxs-lookup"><span data-stu-id="4dcaa-145">Requirements</span></span>



| <span data-ttu-id="4dcaa-146">Требование</span><span class="sxs-lookup"><span data-stu-id="4dcaa-146">Requirement</span></span> | <span data-ttu-id="4dcaa-147">Значение</span><span class="sxs-lookup"><span data-stu-id="4dcaa-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dcaa-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4dcaa-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4dcaa-149">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4dcaa-149">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4dcaa-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4dcaa-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4dcaa-151">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4dcaa-151">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4dcaa-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4dcaa-152">Namespace</span></span><br/>                | <span data-ttu-id="4dcaa-153">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4dcaa-153">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4dcaa-154">MOF</span><span class="sxs-lookup"><span data-stu-id="4dcaa-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4dcaa-155"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4dcaa-155"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4dcaa-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4dcaa-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4dcaa-157"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4dcaa-157"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4dcaa-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4dcaa-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dcaa-159">**\_ACTIVECONNECTION CIM**</span><span class="sxs-lookup"><span data-stu-id="4dcaa-159">**CIM\_ActiveConnection**</span></span>](cim-activeconnection.md)
</dt> <dt>

<span data-ttu-id="4dcaa-160">[**\_ACTIVECONNECTION CIM**](/previous-versions//cc136779(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4dcaa-160">[**CIM\_ActiveConnection**](/previous-versions//cc136779(v=vs.85))</span></span>
</dt> </dl>

 

