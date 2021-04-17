---
description: Экспорт данных параметров, передаваемых в метод Експортреференцепоинт \_ класса мсвм коллектионреференцепоинтсервице.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Класс Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684270"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a><span data-ttu-id="a551c-103">\_Класс мсвм коллектионреференцепоинтекспортсеттингдата</span><span class="sxs-lookup"><span data-stu-id="a551c-103">Msvm\_CollectionReferencePointExportSettingData class</span></span>

<span data-ttu-id="a551c-104">Экспорт данных параметров, передаваемых в метод [**експортреференцепоинт**](msvm-collectionreferencepointservice-exportreferencepoint.md) класса [**мсвм \_ коллектионреференцепоинтсервице**](msvm-collectionreferencepointservice.md) .</span><span class="sxs-lookup"><span data-stu-id="a551c-104">Export setting data to be passed in to the [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md) method of the [**Msvm\_CollectionReferencePointService**](msvm-collectionreferencepointservice.md) class.</span></span>

<span data-ttu-id="a551c-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a551c-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a551c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a551c-106">Syntax</span></span>

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="a551c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="a551c-107">Members</span></span>

<span data-ttu-id="a551c-108">Класс **мсвм \_ коллектионреференцепоинтекспортсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a551c-108">The **Msvm\_CollectionReferencePointExportSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="a551c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a551c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a551c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a551c-110">Properties</span></span>

<span data-ttu-id="a551c-111">Класс **мсвм \_ коллектионреференцепоинтекспортсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a551c-111">The **Msvm\_CollectionReferencePointExportSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a551c-112">**басереференцепоинтколлектион**</span><span class="sxs-lookup"><span data-stu-id="a551c-112">**BaseReferencePointCollection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a551c-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a551c-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a551c-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a551c-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a551c-115">Путь к экземпляру [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) , который представляет базовую коллекцию опорных точек, используемую для разностного экспорта.</span><span class="sxs-lookup"><span data-stu-id="a551c-115">Path to a [**Msvm\_ReferencePointCollection**](msvm-referencepointcollection.md) instance that represents the base reference point collection to be used for differential export.</span></span>

</dd> <dt>

<span data-ttu-id="a551c-116">**виртуалмачинестодискстоекспорт**</span><span class="sxs-lookup"><span data-stu-id="a551c-116">**VirtualMachinesToDisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a551c-117">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="a551c-117">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a551c-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="a551c-118">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a551c-119">Квалификаторы: **хипервембеддединстанце** ("мсвм \_ виртуалмачинетодискс")</span><span class="sxs-lookup"><span data-stu-id="a551c-119">Qualifiers: **HyperVEmbeddedInstance** ("Msvm\_VirtualMachineToDisks")</span></span>
</dt> </dl>

<span data-ttu-id="a551c-120">Список сведений о сопоставлении "VirtualMachines со Дискстоекспорт", для которых необходимо экспортировать данные.</span><span class="sxs-lookup"><span data-stu-id="a551c-120">List of "VirtualMachines To DisksToExport" map information for which data needs to be exported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a551c-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a551c-121">Requirements</span></span>



| <span data-ttu-id="a551c-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a551c-122">Requirement</span></span> | <span data-ttu-id="a551c-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a551c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a551c-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a551c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a551c-125">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a551c-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="a551c-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a551c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a551c-127">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a551c-127">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="a551c-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a551c-128">Namespace</span></span><br/>                | <span data-ttu-id="a551c-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="a551c-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a551c-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a551c-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a551c-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a551c-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a551c-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a551c-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a551c-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a551c-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a551c-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a551c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a551c-135">**\_SETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="a551c-135">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

 




