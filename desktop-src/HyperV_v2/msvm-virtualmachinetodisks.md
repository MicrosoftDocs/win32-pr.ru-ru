---
description: Настройка передачи данных в виде массива в \_ класс мсвм коллектионреференцепоинтекспортсеттингдата.
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Класс Msvm_VirtualMachineToDisks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896834"
---
# <a name="msvm_virtualmachinetodisks-class"></a><span data-ttu-id="dc27b-103">\_Класс мсвм виртуалмачинетодискс</span><span class="sxs-lookup"><span data-stu-id="dc27b-103">Msvm\_VirtualMachineToDisks class</span></span>

<span data-ttu-id="dc27b-104">Настройка передачи данных в виде массива в класс [**мсвм \_ коллектионреференцепоинтекспортсеттингдата**](msvm-collectionreferencepointexportsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="dc27b-104">Setting data to be passed as an array to the [**Msvm\_CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) class.</span></span>

<span data-ttu-id="dc27b-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="dc27b-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc27b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc27b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a><span data-ttu-id="dc27b-107">Члены</span><span class="sxs-lookup"><span data-stu-id="dc27b-107">Members</span></span>

<span data-ttu-id="dc27b-108">Класс **мсвм \_ виртуалмачинетодискс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="dc27b-108">The **Msvm\_VirtualMachineToDisks** class has these types of members:</span></span>

-   [<span data-ttu-id="dc27b-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc27b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dc27b-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="dc27b-110">Properties</span></span>

<span data-ttu-id="dc27b-111">Класс **мсвм \_ виртуалмачинетодискс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="dc27b-111">The **Msvm\_VirtualMachineToDisks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dc27b-112">**дискстоекспорт**</span><span class="sxs-lookup"><span data-stu-id="dc27b-112">**DisksToExport**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc27b-113">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="dc27b-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="dc27b-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="dc27b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dc27b-115">Идентификаторы экземпляров WMI для дисков, которые относятся к заданному ИДЕНТИФИКАТОРу виртуальной машины, для которой необходимо экспортировать данные.</span><span class="sxs-lookup"><span data-stu-id="dc27b-115">The WMI instance IDs of the disks those belong to given Virtual Machine ID for which data needs to be exported.</span></span>

</dd> <dt>

<span data-ttu-id="dc27b-116">**виртуалмачинеид**</span><span class="sxs-lookup"><span data-stu-id="dc27b-116">**VirtualMachineId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dc27b-117">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="dc27b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="dc27b-118">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="dc27b-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="dc27b-119">ИДЕНТИФИКАТОР виртуальной машины, с которой связаны виртуальные диски.</span><span class="sxs-lookup"><span data-stu-id="dc27b-119">A Virtual Machine ID that virtual disks are associated with.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc27b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="dc27b-120">Requirements</span></span>



| <span data-ttu-id="dc27b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="dc27b-121">Requirement</span></span> | <span data-ttu-id="dc27b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="dc27b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc27b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc27b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dc27b-124">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dc27b-124">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="dc27b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc27b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dc27b-126">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dc27b-126">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="dc27b-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="dc27b-127">Namespace</span></span><br/>                | <span data-ttu-id="dc27b-128">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="dc27b-128">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="dc27b-129">MOF</span><span class="sxs-lookup"><span data-stu-id="dc27b-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc27b-130"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc27b-130"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc27b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dc27b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc27b-132"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="dc27b-132"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

 




