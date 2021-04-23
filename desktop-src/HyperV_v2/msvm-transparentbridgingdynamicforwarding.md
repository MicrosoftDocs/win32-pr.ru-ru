---
description: Подключает службу прозрачного моста к динамической пересылке (известному MAC-адресу).
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Класс Msvm_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991373"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="20812-103">\_Класс мсвм транспарентбридгингдинамикфорвардинг</span><span class="sxs-lookup"><span data-stu-id="20812-103">Msvm\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="20812-104">Подключает службу прозрачного моста к динамической пересылке (известному MAC-адресу).</span><span class="sxs-lookup"><span data-stu-id="20812-104">Connects a transparent bridging service to a dynamic forward entry (learned MAC address).</span></span>

<span data-ttu-id="20812-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="20812-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="20812-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20812-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="20812-107">Члены</span><span class="sxs-lookup"><span data-stu-id="20812-107">Members</span></span>

<span data-ttu-id="20812-108">Класс **мсвм \_ транспарентбридгингдинамикфорвардинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="20812-108">The **Msvm\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="20812-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="20812-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="20812-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="20812-110">Properties</span></span>

<span data-ttu-id="20812-111">Класс **мсвм \_ транспарентбридгингдинамикфорвардинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="20812-111">The **Msvm\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="20812-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="20812-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20812-113">Тип данных: **[ **мсвм \_ транспарентбридгингсервице**](msvm-transparentbridgingservice.md)**</span><span class="sxs-lookup"><span data-stu-id="20812-113">Data type: **[**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="20812-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20812-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20812-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="20812-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="20812-116">Ссылка на экземпляр класса [**мсвм \_ транспарентбридгингсервице**](msvm-transparentbridgingservice.md) , представляющий прозрачную службу моста.</span><span class="sxs-lookup"><span data-stu-id="20812-116">A reference to an instance of the [**Msvm\_TransparentBridgingService**](msvm-transparentbridgingservice.md) class that represents the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="20812-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="20812-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="20812-118">Тип данных: **[ **мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md)**</span><span class="sxs-lookup"><span data-stu-id="20812-118">Data type: **[**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**</span></span>
</dt> <dt>

<span data-ttu-id="20812-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="20812-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="20812-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="20812-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="20812-121">Ссылка на экземпляр класса [**мсвм \_ динамикфорвардинжентри**](msvm-dynamicforwardingentry.md) , представляющий динамическую запись пересылки базы данных пересылки.</span><span class="sxs-lookup"><span data-stu-id="20812-121">A reference to an instance of the [**Msvm\_DynamicForwardingEntry**](msvm-dynamicforwardingentry.md) class that represents the dynamic forwarding entry of the forwarding database.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20812-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20812-122">Remarks</span></span>

<span data-ttu-id="20812-123">Доступ к классу **\_ транспарентбридгингдинамикфорвардинг мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="20812-123">Access to the **Msvm\_TransparentBridgingDynamicForwarding** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="20812-124">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="20812-124">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="20812-125">Требования</span><span class="sxs-lookup"><span data-stu-id="20812-125">Requirements</span></span>



| <span data-ttu-id="20812-126">Требование</span><span class="sxs-lookup"><span data-stu-id="20812-126">Requirement</span></span> | <span data-ttu-id="20812-127">Значение</span><span class="sxs-lookup"><span data-stu-id="20812-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20812-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="20812-128">Minimum supported client</span></span><br/> | <span data-ttu-id="20812-129">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="20812-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20812-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="20812-130">Minimum supported server</span></span><br/> | <span data-ttu-id="20812-131">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="20812-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20812-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="20812-132">Namespace</span></span><br/>                | <span data-ttu-id="20812-133">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="20812-133">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20812-134">MOF</span><span class="sxs-lookup"><span data-stu-id="20812-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20812-135"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="20812-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20812-136">DLL</span><span class="sxs-lookup"><span data-stu-id="20812-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20812-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20812-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20812-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="20812-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20812-139">**\_ТРАНСПАРЕНТБРИДГИНГДИНАМИКФОРВАРДИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="20812-139">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[<span data-ttu-id="20812-140">**\_ТРАНСПАРЕНТБРИДГИНГДИНАМИКФОРВАРДИНГ CIM**</span><span class="sxs-lookup"><span data-stu-id="20812-140">**CIM\_TransparentBridgingDynamicForwarding**</span></span>](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

