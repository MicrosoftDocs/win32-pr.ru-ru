---
description: '\_Класс WMI взаимосвязей Win32 логжедонусер связывает сеанс и учетную запись пользователя.'
ms.assetid: b1233f90-4898-4ced-84d2-0858027e935a
ms.tgt_platform: multiple
title: Класс Win32_LoggedOnUser
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LoggedOnUser
- Win32_LoggedOnUser.Dependent
- Win32_LoggedOnUser.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0f851c85563095a66197b0dde8e6cbddc9581f07
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896358"
---
# <a name="win32_loggedonuser-class"></a><span data-ttu-id="b6c51-103">\_Класс Win32 логжедонусер</span><span class="sxs-lookup"><span data-stu-id="b6c51-103">Win32\_LoggedOnUser class</span></span>

<span data-ttu-id="b6c51-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логжедонусер** связывает сеанс и учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="b6c51-104">The **Win32\_LoggedOnUser** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a session and a user account.</span></span>

<span data-ttu-id="b6c51-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="b6c51-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="b6c51-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b6c51-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6c51-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b6c51-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8BB5B3EC-E1F7-4b39-942A-605D5F55789A}"), AMENDMENT]
class Win32_LoggedOnUser : CIM_Dependency
{
  Win32_LogonSession REF Dependent;
  Win32_Account      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="b6c51-108">Члены</span><span class="sxs-lookup"><span data-stu-id="b6c51-108">Members</span></span>

<span data-ttu-id="b6c51-109">Класс **Win32 \_ логжедонусер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b6c51-109">The **Win32\_LoggedOnUser** class has these types of members:</span></span>

-   [<span data-ttu-id="b6c51-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6c51-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6c51-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b6c51-111">Properties</span></span>

<span data-ttu-id="b6c51-112">Класс **Win32 \_ логжедонусер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b6c51-112">The **Win32\_LoggedOnUser** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6c51-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="b6c51-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c51-114">Тип данных: **\_ учетная запись Win32**</span><span class="sxs-lookup"><span data-stu-id="b6c51-114">Data type: **Win32\_Account**</span></span>
</dt> <dt>

<span data-ttu-id="b6c51-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6c51-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c51-116">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6c51-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6c51-117">[**\_ Учетная запись Win32**](win32-account.md) , которая описывает учетную запись, используемую при инициации этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6c51-117">A [**Win32\_Account**](win32-account.md) that describes the account used in the initiation of this session.</span></span> <span data-ttu-id="b6c51-118">Учетная запись может быть либо учетной записью пользователя, либо системной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="b6c51-118">The account could be either a user account or a system account.</span></span>

</dd> <dt>

<span data-ttu-id="b6c51-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="b6c51-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6c51-120">Тип данных: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="b6c51-120">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="b6c51-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b6c51-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b6c51-122">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимое), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b6c51-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b6c51-123">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) , описывающий сеанс, который используется в данный момент учетной записью.</span><span class="sxs-lookup"><span data-stu-id="b6c51-123">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that describes the session that the account is currently using.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6c51-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b6c51-124">Remarks</span></span>

<span data-ttu-id="b6c51-125">Класс **Win32 \_ логжедонусер** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="b6c51-125">The **Win32\_LoggedOnUser** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b6c51-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="b6c51-126">Examples</span></span>

<span data-ttu-id="b6c51-127">Пример [функции Get-логжедонусер](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell получает пользователей, вошедших в систему на локальном или удаленном компьютере, со сведениями о сеансе.</span><span class="sxs-lookup"><span data-stu-id="b6c51-127">The [get-loggedonuser function](https://Gallery.TechNet.Microsoft.Com/scriptcenter/0e43993a-895a-4afe-a2b2-045a5146048a) PowerShell sample gets the logged on users on a local or remote computer, with session information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6c51-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b6c51-128">Requirements</span></span>



| <span data-ttu-id="b6c51-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b6c51-129">Requirement</span></span> | <span data-ttu-id="b6c51-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b6c51-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c51-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b6c51-131">Minimum supported client</span></span><br/> | <span data-ttu-id="b6c51-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6c51-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6c51-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b6c51-133">Minimum supported server</span></span><br/> | <span data-ttu-id="b6c51-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6c51-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6c51-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b6c51-135">Namespace</span></span><br/>                | <span data-ttu-id="b6c51-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b6c51-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6c51-137">MOF</span><span class="sxs-lookup"><span data-stu-id="b6c51-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6c51-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6c51-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6c51-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b6c51-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6c51-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6c51-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6c51-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b6c51-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6c51-142">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="b6c51-142">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="b6c51-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6c51-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

