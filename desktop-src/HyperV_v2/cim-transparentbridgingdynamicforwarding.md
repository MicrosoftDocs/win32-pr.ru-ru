---
description: Связывает прозрачную службу моста с записью своей базы данных пересылки.
ms.assetid: 6db93e71-c9b7-4710-a9ee-99a1055cfd82
title: Класс CIM_TransparentBridgingDynamicForwarding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingDynamicForwarding
- CIM_TransparentBridgingDynamicForwarding.Antecedent
- CIM_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d089ca662880ad269cb9d9c63cb0935ff6de0b5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662812"
---
# <a name="cim_transparentbridgingdynamicforwarding-class"></a><span data-ttu-id="ec1ba-103">\_Класс CIM транспарентбридгингдинамикфорвардинг</span><span class="sxs-lookup"><span data-stu-id="ec1ba-103">CIM\_TransparentBridgingDynamicForwarding class</span></span>

<span data-ttu-id="ec1ba-104">Связывает прозрачную службу моста с записью своей базы данных пересылки.</span><span class="sxs-lookup"><span data-stu-id="ec1ba-104">Associates a transparent bridging service with an entry of its forwarding database.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec1ba-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ec1ba-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingDynamicForwarding : CIM_Dependency
{
  CIM_TransparentBridgingService REF Antecedent;
  CIM_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="ec1ba-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ec1ba-106">Members</span></span>

<span data-ttu-id="ec1ba-107">Класс **CIM \_ транспарентбридгингдинамикфорвардинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ec1ba-107">The **CIM\_TransparentBridgingDynamicForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="ec1ba-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec1ba-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ec1ba-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec1ba-109">Properties</span></span>

<span data-ttu-id="ec1ba-110">Класс **CIM \_ транспарентбридгингдинамикфорвардинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ec1ba-110">The **CIM\_TransparentBridgingDynamicForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ec1ba-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ec1ba-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec1ba-112">Тип данных: **CIM \_ транспарентбридгингсервице**</span><span class="sxs-lookup"><span data-stu-id="ec1ba-112">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="ec1ba-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec1ba-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec1ba-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="ec1ba-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="ec1ba-115">Ссылка [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) на службу прозрачного моста.</span><span class="sxs-lookup"><span data-stu-id="ec1ba-115">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the transparent bridging service.</span></span>

</dd> <dt>

<span data-ttu-id="ec1ba-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="ec1ba-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ec1ba-117">Тип данных: **CIM \_ динамикфорвардинжентри**</span><span class="sxs-lookup"><span data-stu-id="ec1ba-117">Data type: **CIM\_DynamicForwardingEntry**</span></span>
</dt> <dt>

<span data-ttu-id="ec1ba-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec1ba-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ec1ba-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимый), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ec1ba-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ec1ba-120">Ссылка [**CIM \_ динамикфорвардинжентри**](cim-dynamicforwardingentry.md) на запись пересылки базы данных.</span><span class="sxs-lookup"><span data-stu-id="ec1ba-120">A [**CIM\_DynamicForwardingEntry**](cim-dynamicforwardingentry.md) reference to the forwarding database entry.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ec1ba-121">Требования</span><span class="sxs-lookup"><span data-stu-id="ec1ba-121">Requirements</span></span>



| <span data-ttu-id="ec1ba-122">Требование</span><span class="sxs-lookup"><span data-stu-id="ec1ba-122">Requirement</span></span> | <span data-ttu-id="ec1ba-123">Значение</span><span class="sxs-lookup"><span data-stu-id="ec1ba-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec1ba-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec1ba-124">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1ba-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="ec1ba-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="ec1ba-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec1ba-126">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1ba-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ec1ba-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="ec1ba-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ec1ba-128">Namespace</span></span><br/>                | <span data-ttu-id="ec1ba-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ec1ba-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ec1ba-130">MOF</span><span class="sxs-lookup"><span data-stu-id="ec1ba-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec1ba-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec1ba-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec1ba-132">DLL</span><span class="sxs-lookup"><span data-stu-id="ec1ba-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec1ba-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ec1ba-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ec1ba-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec1ba-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec1ba-135">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ec1ba-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

