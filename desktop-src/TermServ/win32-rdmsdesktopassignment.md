---
title: Класс Win32_RDMSDesktopAssignment
description: Описание назначения пользовательского рабочего стола коллекции удаленных рабочих столов.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDMSDesktopAssignment, описание
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72bb252bd2efb71e3192ebd16160cecf18196cb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340655"
---
# <a name="win32_rdmsdesktopassignment-class"></a><span data-ttu-id="7a5c8-105">\_Класс Win32 рдмсдесктопассигнмент</span><span class="sxs-lookup"><span data-stu-id="7a5c8-105">Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="7a5c8-106">Описание назначения пользовательского рабочего стола коллекции удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-106">Describes the RD collection User Desktop assignment.</span></span>

<span data-ttu-id="7a5c8-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a5c8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a5c8-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a><span data-ttu-id="7a5c8-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7a5c8-109">Members</span></span>

<span data-ttu-id="7a5c8-110">Класс **Win32 \_ рдмсдесктопассигнмент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a5c8-110">The **Win32\_RDMSDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="7a5c8-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7a5c8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7a5c8-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a5c8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7a5c8-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7a5c8-113">Methods</span></span>

<span data-ttu-id="7a5c8-114">Класс **Win32 \_ рдмсдесктопассигнмент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-114">The **Win32\_RDMSDesktopAssignment** class has these methods.</span></span>



| <span data-ttu-id="7a5c8-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7a5c8-115">Method</span></span>                                                                                 | <span data-ttu-id="7a5c8-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7a5c8-116">Description</span></span>                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [<span data-ttu-id="7a5c8-117">**адддесктопассигнмент**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-117">**AddDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-adddesktopassignment.md)       | <span data-ttu-id="7a5c8-118">Добавляет назначение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-118">Adds a desktop assignment.</span></span><br/>    |
| [<span data-ttu-id="7a5c8-119">**ремоведесктопассигнмент**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-119">**RemoveDesktopAssignment**</span></span>](win32-rdmsdesktopassignment-removedesktopassignment.md) | <span data-ttu-id="7a5c8-120">Удаляет назначение рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-120">Removes a desktop assignment.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="7a5c8-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a5c8-121">Properties</span></span>

<span data-ttu-id="7a5c8-122">Класс **Win32 \_ рдмсдесктопассигнмент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-122">The **Win32\_RDMSDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a5c8-123">**коллектионалиас**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-123">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a5c8-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7a5c8-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a5c8-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7a5c8-127">Псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-127">Alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="7a5c8-128">**десктопнаме**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-128">**DesktopName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a5c8-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7a5c8-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a5c8-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7a5c8-132">Имя рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-132">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="7a5c8-133">**Доменпользователя**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-133">**UserDomain**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a5c8-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-135">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7a5c8-135">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-136">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a5c8-136">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7a5c8-137">Доменное имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-137">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="7a5c8-138">**UserName**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-138">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a5c8-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7a5c8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="7a5c8-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="7a5c8-141">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7a5c8-141">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7a5c8-142">Имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="7a5c8-142">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a5c8-143">Требования</span><span class="sxs-lookup"><span data-stu-id="7a5c8-143">Requirements</span></span>



| <span data-ttu-id="7a5c8-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7a5c8-144">Requirement</span></span> | <span data-ttu-id="7a5c8-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7a5c8-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a5c8-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a5c8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7a5c8-147">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7a5c8-147">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7a5c8-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a5c8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7a5c8-149">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="7a5c8-149">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="7a5c8-150">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a5c8-150">Namespace</span></span><br/>                | <span data-ttu-id="7a5c8-151">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a5c8-151">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7a5c8-152">MOF</span><span class="sxs-lookup"><span data-stu-id="7a5c8-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a5c8-153"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a5c8-153"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a5c8-154">DLL</span><span class="sxs-lookup"><span data-stu-id="7a5c8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a5c8-155"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a5c8-155"><dt>RDMS.dll</dt></span></span> </dl>         |



 

