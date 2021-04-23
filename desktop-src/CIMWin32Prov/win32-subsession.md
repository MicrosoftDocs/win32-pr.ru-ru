---
description: '\_Ассоциация Подсеансов Win32 определяет связи между сеансами, в которых один сеанс является частью, или использует другой сеанс, например, когда сеанс терминала использует сеанс входа в систему.'
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Класс Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539218"
---
# <a name="win32_subsession-class"></a><span data-ttu-id="0f380-103">\_Класс Подсеанса Win32</span><span class="sxs-lookup"><span data-stu-id="0f380-103">Win32\_SubSession class</span></span>

<span data-ttu-id="0f380-104">\_Ассоциация Подсеансов Win32 определяет связи между сеансами, в которых один сеанс является частью, или использует другой сеанс, например, когда сеанс терминала использует сеанс входа в систему.</span><span class="sxs-lookup"><span data-stu-id="0f380-104">The Win32\_SubSession association defines relationships between sessions where one session is a part of or utilizes another session for example where a Terminal session uses a Logon Session.</span></span>

<span data-ttu-id="0f380-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="0f380-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f380-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f380-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0f380-107">Члены</span><span class="sxs-lookup"><span data-stu-id="0f380-107">Members</span></span>

<span data-ttu-id="0f380-108">Класс **\_ подсеанса Win32** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f380-108">The **Win32\_SubSession** class has these types of members:</span></span>

-   [<span data-ttu-id="0f380-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f380-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f380-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f380-110">Properties</span></span>

<span data-ttu-id="0f380-111">Класс **\_ подсеанса Win32** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f380-111">The **Win32\_SubSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f380-112">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="0f380-112">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f380-113">Тип данных: **\_ сеанс Win32**</span><span class="sxs-lookup"><span data-stu-id="0f380-113">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="0f380-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f380-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f380-115">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span><span class="sxs-lookup"><span data-stu-id="0f380-115">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Antecedent)</span></span>
</dt> </dl>

<span data-ttu-id="0f380-116">[**\_ Сеанс Win32**](win32-session.md) , описывающий сеанс, который имеет вложенный сеанс.</span><span class="sxs-lookup"><span data-stu-id="0f380-116">A [**Win32\_Session**](win32-session.md) that describes the session that has a subsession.</span></span>

</dd> <dt>

<span data-ttu-id="0f380-117">**Него**</span><span class="sxs-lookup"><span data-stu-id="0f380-117">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f380-118">Тип данных: **\_ сеанс Win32**</span><span class="sxs-lookup"><span data-stu-id="0f380-118">Data type: **Win32\_Session**</span></span>
</dt> <dt>

<span data-ttu-id="0f380-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f380-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f380-120">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) (зависимый)</span><span class="sxs-lookup"><span data-stu-id="0f380-120">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) (Dependent)</span></span>
</dt> </dl>

<span data-ttu-id="0f380-121">[**\_ Сеанс Win32**](win32-session.md) , описывающий сеанс, который является подсеансом.</span><span class="sxs-lookup"><span data-stu-id="0f380-121">A [**Win32\_Session**](win32-session.md) that describes the session that is the subsession.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f380-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0f380-122">Requirements</span></span>



| <span data-ttu-id="0f380-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0f380-123">Requirement</span></span> | <span data-ttu-id="0f380-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0f380-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f380-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f380-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0f380-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f380-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f380-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f380-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0f380-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f380-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f380-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f380-129">Namespace</span></span><br/>                | <span data-ttu-id="0f380-130">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0f380-130">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0f380-131">MOF</span><span class="sxs-lookup"><span data-stu-id="0f380-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f380-132"><dt>CimWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f380-132"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f380-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0f380-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f380-134"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f380-134"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f380-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f380-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f380-136">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="0f380-136">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

 
