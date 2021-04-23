---
description: Связь Win32 \_ сессионресаурце представляет связь между сеансом и ресурсами, к которым предоставляет доступ сеанс.
ms.assetid: 39c195cf-e70b-4e93-b46b-61ed4f08f57e
ms.tgt_platform: multiple
title: Класс Win32_SessionResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionResource
- Win32_SessionResource.Antecedent
- Win32_SessionResource.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 3962c8523863bb97710bf21be38906d3897beea3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807739"
---
# <a name="win32_sessionresource-class"></a><span data-ttu-id="d9cdd-103">\_Класс Win32 сессионресаурце</span><span class="sxs-lookup"><span data-stu-id="d9cdd-103">Win32\_SessionResource class</span></span>

<span data-ttu-id="d9cdd-104">Связь Win32 \_ сессионресаурце представляет связь между сеансом и ресурсами, к которым предоставляет доступ сеанс.</span><span class="sxs-lookup"><span data-stu-id="d9cdd-104">The Win32\_SessionResource association represents the relationship between a session and the resources that the session provides access to.</span></span>

<span data-ttu-id="d9cdd-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d9cdd-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9cdd-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9cdd-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SessionResource : CIM_Dependency
{
  Win32_LogicalElement REF Antecedent;
  Win32_Session        REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="d9cdd-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d9cdd-107">Members</span></span>

<span data-ttu-id="d9cdd-108">Класс **Win32 \_ сессионресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9cdd-108">The **Win32\_SessionResource** class has these types of members:</span></span>

-   [<span data-ttu-id="d9cdd-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9cdd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9cdd-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9cdd-110">Properties</span></span>

<span data-ttu-id="d9cdd-111">Класс **Win32 \_ сессионресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9cdd-111">The **Win32\_SessionResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9cdd-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d9cdd-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9cdd-113">Тип данных: **Win32 \_ логикалелемент**</span><span class="sxs-lookup"><span data-stu-id="d9cdd-113">Data type: **Win32\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="d9cdd-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9cdd-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9cdd-115">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d9cdd-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d9cdd-116">Ссылка Antecedent представляет ресурсы, используемые этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="d9cdd-116">The Antecedent reference represents resources used by this session.</span></span>

</dd> <dt>

<span data-ttu-id="d9cdd-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="d9cdd-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9cdd-118">Тип данных: **\_ сеанс Win32**</span><span class="sxs-lookup"><span data-stu-id="d9cdd-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="d9cdd-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9cdd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9cdd-120">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="d9cdd-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d9cdd-121">Зависимая ссылка представляет сеанс, использующий ресурс.</span><span class="sxs-lookup"><span data-stu-id="d9cdd-121">The Dependent reference represents the session using the resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9cdd-122">Требования</span><span class="sxs-lookup"><span data-stu-id="d9cdd-122">Requirements</span></span>



| <span data-ttu-id="d9cdd-123">Требование</span><span class="sxs-lookup"><span data-stu-id="d9cdd-123">Requirement</span></span> | <span data-ttu-id="d9cdd-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d9cdd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9cdd-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9cdd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d9cdd-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9cdd-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9cdd-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9cdd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d9cdd-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9cdd-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9cdd-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9cdd-129">Namespace</span></span><br/>                | <span data-ttu-id="d9cdd-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d9cdd-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9cdd-131">MOF</span><span class="sxs-lookup"><span data-stu-id="d9cdd-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9cdd-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9cdd-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9cdd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d9cdd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9cdd-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9cdd-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9cdd-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9cdd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9cdd-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="d9cdd-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
