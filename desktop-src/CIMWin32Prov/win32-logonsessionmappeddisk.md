---
description: Класс Win32 \_ логонсессионмаппеддиск представляет связь между сеансом входа и сопоставленными логическими дисками, определенными в сеансе.
ms.assetid: 013ae55e-6dd1-42fb-bcba-74d6afa1b905
ms.tgt_platform: multiple
title: Класс Win32_LogonSessionMappedDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogonSessionMappedDisk
- Win32_LogonSessionMappedDisk.Antecedent
- Win32_LogonSessionMappedDisk.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 203c9dd783dece52fa19905d51ece3bc26584dc6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539353"
---
# <a name="win32_logonsessionmappeddisk-class"></a><span data-ttu-id="4428f-103">\_Класс Win32 логонсессионмаппеддиск</span><span class="sxs-lookup"><span data-stu-id="4428f-103">Win32\_LogonSessionMappedDisk class</span></span>

<span data-ttu-id="4428f-104">Класс Win32 \_ логонсессионмаппеддиск представляет связь между сеансом входа и сопоставленными логическими дисками, определенными в сеансе.</span><span class="sxs-lookup"><span data-stu-id="4428f-104">The Win32\_LogonSessionMappedDisk class represents an association between a logon session and the mapped logical disks defined within the session.</span></span>

<span data-ttu-id="4428f-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4428f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4428f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4428f-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_LogonSessionMappedDisk : CIM_Dependency
{
  Win32_LogonSession      REF Antecedent;
  Win32_MappedLogicalDisk REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4428f-107">Члены</span><span class="sxs-lookup"><span data-stu-id="4428f-107">Members</span></span>

<span data-ttu-id="4428f-108">Класс **Win32 \_ логонсессионмаппеддиск** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4428f-108">The **Win32\_LogonSessionMappedDisk** class has these types of members:</span></span>

-   [<span data-ttu-id="4428f-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="4428f-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4428f-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="4428f-110">Properties</span></span>

<span data-ttu-id="4428f-111">Класс **Win32 \_ логонсессионмаппеддиск** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4428f-111">The **Win32\_LogonSessionMappedDisk** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4428f-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4428f-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4428f-113">Тип данных: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="4428f-113">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="4428f-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4428f-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4428f-115">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4428f-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4428f-116">Свойство Antecedent ссылается на сеанс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="4428f-116">The Antecedent property references a logon session.</span></span>

</dd> <dt>

<span data-ttu-id="4428f-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="4428f-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4428f-118">Тип данных: **Win32 \_ маппедлогикалдиск**</span><span class="sxs-lookup"><span data-stu-id="4428f-118">Data type: **Win32\_MappedLogicalDisk**</span></span>
</dt> <dt>

<span data-ttu-id="4428f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4428f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4428f-120">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4428f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4428f-121">Свойство Dependent ссылается на сопоставленный логический диск, определенный в сеансе, на который ссылается свойство Antecedent.</span><span class="sxs-lookup"><span data-stu-id="4428f-121">The Dependent property references a mapped logical disk defined within the session referenced by the Antecedent property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4428f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="4428f-122">Requirements</span></span>



| <span data-ttu-id="4428f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="4428f-123">Requirement</span></span> | <span data-ttu-id="4428f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="4428f-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4428f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4428f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4428f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4428f-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4428f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4428f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4428f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4428f-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4428f-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4428f-129">Namespace</span></span><br/>                | <span data-ttu-id="4428f-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4428f-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4428f-131">MOF</span><span class="sxs-lookup"><span data-stu-id="4428f-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4428f-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4428f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4428f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4428f-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4428f-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4428f-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4428f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4428f-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="4428f-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

