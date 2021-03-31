---
description: Предоставляет дополнительные сведения для использования с методом Експортреференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Класс Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081708"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a><span data-ttu-id="037d8-103">\_Класс мсвм виртуалсистемреференцепоинтекспортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="037d8-103">Msvm\_VirtualSystemReferencePointExportSettingData class</span></span>

<span data-ttu-id="037d8-104">Предоставляет дополнительные сведения для использования с методом [**експортреференцепоинт**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) класса [**\_ виртуалсистемреференцепоинтсервице мсвм**](msvm-virtualsystemreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="037d8-104">Provides additional information to be used with the [**ExportReferencePoint**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md) class.</span></span>

<span data-ttu-id="037d8-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="037d8-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="037d8-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="037d8-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="037d8-107">Члены</span><span class="sxs-lookup"><span data-stu-id="037d8-107">Members</span></span>

<span data-ttu-id="037d8-108">Класс **мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="037d8-108">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="037d8-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="037d8-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="037d8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="037d8-110">Properties</span></span>

<span data-ttu-id="037d8-111">Класс **мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="037d8-111">The **Msvm\_VirtualSystemReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="037d8-112">**басереференцепоинт**</span><span class="sxs-lookup"><span data-stu-id="037d8-112">**BaseReferencePoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="037d8-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="037d8-113">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="037d8-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="037d8-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="037d8-115">Путь к базовой опорной точке относительно того, в какой операции следует выполнить экспорт.</span><span class="sxs-lookup"><span data-stu-id="037d8-115">Path of the base reference point with respect to which export should be performed.</span></span>

</dd> <dt>

<span data-ttu-id="037d8-116">**дискстоекспорт**</span><span class="sxs-lookup"><span data-stu-id="037d8-116">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="037d8-117">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="037d8-117">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="037d8-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="037d8-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="037d8-119">Идентификаторы экземпляров WMI для дисков, для которых необходимо экспортировать данные.</span><span class="sxs-lookup"><span data-stu-id="037d8-119">WMI instance IDs of the disks for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="037d8-120">Требования</span><span class="sxs-lookup"><span data-stu-id="037d8-120">Requirements</span></span>



| <span data-ttu-id="037d8-121">Требование</span><span class="sxs-lookup"><span data-stu-id="037d8-121">Requirement</span></span> | <span data-ttu-id="037d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="037d8-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="037d8-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="037d8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="037d8-124">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="037d8-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="037d8-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="037d8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="037d8-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="037d8-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="037d8-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="037d8-127">Namespace</span></span><br/>                | <span data-ttu-id="037d8-128">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="037d8-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="037d8-129">MOF</span><span class="sxs-lookup"><span data-stu-id="037d8-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="037d8-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="037d8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="037d8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="037d8-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="037d8-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="037d8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="037d8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="037d8-134">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="037d8-134">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




