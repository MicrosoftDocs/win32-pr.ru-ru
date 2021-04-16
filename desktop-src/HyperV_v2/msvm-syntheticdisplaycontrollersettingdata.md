---
description: Описание параметров данных для виртуального искусственного контроллера экрана.
ms.assetid: cea79b24-4175-49db-a8b4-a9efb1fd0b96
title: Класс Msvm_SyntheticDisplayControllerSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticDisplayControllerSettingData
- Msvm_SyntheticDisplayControllerSettingData.ResolutionType
- Msvm_SyntheticDisplayControllerSettingData.HorizontalResolution
- Msvm_SyntheticDisplayControllerSettingData.VerticalResolution
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 52935800eda641eb9015247e9320f33f22b40251
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263851"
---
# <a name="msvm_syntheticdisplaycontrollersettingdata-class"></a><span data-ttu-id="7ccdf-103">\_Класс мсвм синсетикдисплайконтроллерсеттингдата</span><span class="sxs-lookup"><span data-stu-id="7ccdf-103">Msvm\_SyntheticDisplayControllerSettingData class</span></span>

<span data-ttu-id="7ccdf-104">Описание параметров данных для виртуального искусственного контроллера экрана.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-104">Describes the setting data for a virtual synthetic display controller.</span></span>

<span data-ttu-id="7ccdf-105">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ccdf-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ccdf-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticDisplayControllerSettingData : CIM_ResourceAllocationSettingData
{
  uint8  ResolutionType;
  uint16 HorizontalResolution;
  uint16 VerticalResolution;
};
```

## <a name="members"></a><span data-ttu-id="7ccdf-107">Члены</span><span class="sxs-lookup"><span data-stu-id="7ccdf-107">Members</span></span>

<span data-ttu-id="7ccdf-108">Класс **мсвм \_ синсетикдисплайконтроллерсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7ccdf-108">The **Msvm\_SyntheticDisplayControllerSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="7ccdf-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ccdf-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7ccdf-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="7ccdf-110">Properties</span></span>

<span data-ttu-id="7ccdf-111">Класс **мсвм \_ синсетикдисплайконтроллерсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-111">The **Msvm\_SyntheticDisplayControllerSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7ccdf-112">**HorizontalResolution**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-112">**HorizontalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ccdf-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ccdf-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7ccdf-114">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ccdf-115">Разрешение по горизонтали.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-115">The horizontal resolution.</span></span>

</dd> <dt>

<span data-ttu-id="7ccdf-116">**ресолутионтипе**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-116">**ResolutionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ccdf-117">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-117">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7ccdf-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7ccdf-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7ccdf-119">Тип разрешения.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-119">The resolution type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="7ccdf-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="7ccdf-120"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="7ccdf-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="7ccdf-121"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

<span data-ttu-id="7ccdf-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Максимум** (2)</span><span class="sxs-lookup"><span data-stu-id="7ccdf-122"><span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>**Maximum** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Single"></span><span id="single"></span><span id="SINGLE"></span>

<span data-ttu-id="7ccdf-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Один** (3)</span><span class="sxs-lookup"><span data-stu-id="7ccdf-123"><span id="Single"></span><span id="single"></span><span id="SINGLE"></span>**Single** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="7ccdf-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**По умолчанию** (4)</span><span class="sxs-lookup"><span data-stu-id="7ccdf-124"><span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Default** (4)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="7ccdf-125">Добавлено в Windows 10 версии 1703.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-125">Added in Windows 10, version 1703.</span></span>

 

</dd> </dl>

</dd> <dt>

<span data-ttu-id="7ccdf-126">**VerticalResolution**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-126">**VerticalResolution**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ccdf-127">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="7ccdf-128">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7ccdf-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="7ccdf-129">Разрешение по вертикали.</span><span class="sxs-lookup"><span data-stu-id="7ccdf-129">The vertical resolution.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ccdf-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7ccdf-130">Requirements</span></span>



| <span data-ttu-id="7ccdf-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7ccdf-131">Requirement</span></span> | <span data-ttu-id="7ccdf-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7ccdf-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccdf-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ccdf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccdf-134">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7ccdf-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="7ccdf-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ccdf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccdf-136">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7ccdf-136">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="7ccdf-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7ccdf-137">Namespace</span></span><br/>                | <span data-ttu-id="7ccdf-138">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="7ccdf-138">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="7ccdf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7ccdf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ccdf-140"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7ccdf-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ccdf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7ccdf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ccdf-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7ccdf-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7ccdf-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7ccdf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccdf-144">**\_РЕСАУРЦЕАЛЛОКАТИОНСЕТТИНГДАТА CIM**</span><span class="sxs-lookup"><span data-stu-id="7ccdf-144">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




