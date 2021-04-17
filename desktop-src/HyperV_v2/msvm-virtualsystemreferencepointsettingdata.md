---
description: Предоставляет дополнительные сведения для использования с методом Креатереференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Класс Msvm_VirtualSystemReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664795"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a><span data-ttu-id="4b5fc-103">\_Класс мсвм виртуалсистемреференцепоинтсеттингдата</span><span class="sxs-lookup"><span data-stu-id="4b5fc-103">Msvm\_VirtualSystemReferencePointSettingData class</span></span>

<span data-ttu-id="4b5fc-104">Предоставляет дополнительные сведения для использования с методом [**креатереференцепоинт**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) класса [**\_ виртуалсистемреференцепоинтсервице мсвм**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="4b5fc-104">Provides additional information to be used with the [**CreateReferencePoint**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="4b5fc-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4b5fc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5fc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b5fc-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a><span data-ttu-id="4b5fc-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4b5fc-107">Members</span></span>

<span data-ttu-id="4b5fc-108">Класс **мсвм \_ виртуалсистемреференцепоинтсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4b5fc-108">The **Msvm\_VirtualSystemReferencePointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4b5fc-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b5fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4b5fc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b5fc-110">Properties</span></span>

<span data-ttu-id="4b5fc-111">Класс **мсвм \_ виртуалсистемреференцепоинтсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4b5fc-111">The **Msvm\_VirtualSystemReferencePointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4b5fc-112">**ConsistencyLevel**</span><span class="sxs-lookup"><span data-stu-id="4b5fc-112">**ConsistencyLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4b5fc-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="4b5fc-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="4b5fc-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4b5fc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4b5fc-115">Уровень согласованности контрольной точки.</span><span class="sxs-lookup"><span data-stu-id="4b5fc-115">The consistency level of the reference point.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b5fc-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4b5fc-116">Requirements</span></span>



| <span data-ttu-id="4b5fc-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4b5fc-117">Requirement</span></span> | <span data-ttu-id="4b5fc-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4b5fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b5fc-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4b5fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4b5fc-120">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="4b5fc-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="4b5fc-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4b5fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4b5fc-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4b5fc-122">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="4b5fc-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4b5fc-123">Namespace</span></span><br/>                | <span data-ttu-id="4b5fc-124">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="4b5fc-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4b5fc-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4b5fc-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4b5fc-126"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4b5fc-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4b5fc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4b5fc-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4b5fc-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4b5fc-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4b5fc-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b5fc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b5fc-130">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="4b5fc-130">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




