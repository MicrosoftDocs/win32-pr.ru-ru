---
description: Связывает данные параметров с управляемым элементом.
ms.assetid: 3fdf111b-3ec1-4559-94ce-27d6a8cd0080
title: Класс CIM_SettingsDefineState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineState
- CIM_SettingsDefineState.ManagedElement
- CIM_SettingsDefineState.SettingData
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1931b365108bb7b3df4269ae6acbb78292a0401d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683859"
---
# <a name="cim_settingsdefinestate-class"></a><span data-ttu-id="d5784-103">\_Класс CIM сеттингсдефинестате</span><span class="sxs-lookup"><span data-stu-id="d5784-103">CIM\_SettingsDefineState class</span></span>

<span data-ttu-id="d5784-104">Связывает данные параметров с управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="d5784-104">Associates settings data with a managed element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5784-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5784-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Settings")]
class CIM_SettingsDefineState
{
  CIM_ManagedElement REF ManagedElement;
  CIM_SettingData    REF SettingData;
};
```

## <a name="members"></a><span data-ttu-id="d5784-106">Члены</span><span class="sxs-lookup"><span data-stu-id="d5784-106">Members</span></span>

<span data-ttu-id="d5784-107">Класс **CIM \_ сеттингсдефинестате** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d5784-107">The **CIM\_SettingsDefineState** class has these types of members:</span></span>

-   [<span data-ttu-id="d5784-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5784-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d5784-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d5784-109">Properties</span></span>

<span data-ttu-id="d5784-110">Класс **CIM \_ сеттингсдефинестате** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d5784-110">The **CIM\_SettingsDefineState** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d5784-111">**манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="d5784-111">**ManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5784-112">Тип данных: **CIM \_ манажеделемент**</span><span class="sxs-lookup"><span data-stu-id="d5784-112">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="d5784-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5784-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5784-114">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5784-114">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5784-115">Управляемый элемент в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d5784-115">The managed element in the association.</span></span>

</dd> <dt>

<span data-ttu-id="d5784-116">**SettingData**</span><span class="sxs-lookup"><span data-stu-id="d5784-116">**SettingData**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d5784-117">Тип данных: **\_ SettingData CIM**</span><span class="sxs-lookup"><span data-stu-id="d5784-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d5784-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d5784-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d5784-119">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d5784-119">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d5784-120">Данные параметров в ассоциации.</span><span class="sxs-lookup"><span data-stu-id="d5784-120">The settings data in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5784-121">Требования</span><span class="sxs-lookup"><span data-stu-id="d5784-121">Requirements</span></span>



| <span data-ttu-id="d5784-122">Требование</span><span class="sxs-lookup"><span data-stu-id="d5784-122">Requirement</span></span> | <span data-ttu-id="d5784-123">Значение</span><span class="sxs-lookup"><span data-stu-id="d5784-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5784-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5784-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d5784-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d5784-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d5784-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5784-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d5784-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d5784-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d5784-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5784-128">Namespace</span></span><br/>                | <span data-ttu-id="d5784-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d5784-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d5784-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d5784-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5784-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5784-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5784-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d5784-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5784-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d5784-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

