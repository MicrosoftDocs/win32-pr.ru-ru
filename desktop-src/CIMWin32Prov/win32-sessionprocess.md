---
description: '\_Класс WMI взаимосвязей Win32 сессионпроцесс представляет связь между сеансом входа и процессами, связанными с этим сеансом.'
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Класс Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f4090da88e8f5d31b0940b0c7d217a930a364b63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655669"
---
# <a name="win32_sessionprocess-class"></a><span data-ttu-id="894a9-103">\_Класс Win32 сессионпроцесс</span><span class="sxs-lookup"><span data-stu-id="894a9-103">Win32\_SessionProcess class</span></span>

<span data-ttu-id="894a9-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сессионпроцесс** представляет связь между сеансом входа и процессами, связанными с этим сеансом.</span><span class="sxs-lookup"><span data-stu-id="894a9-104">The **Win32\_SessionProcess** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between a logon session and the processes associated with that session.</span></span>

<span data-ttu-id="894a9-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="894a9-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="894a9-106">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="894a9-106">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="894a9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="894a9-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="894a9-108">Члены</span><span class="sxs-lookup"><span data-stu-id="894a9-108">Members</span></span>

<span data-ttu-id="894a9-109">Класс **Win32 \_ сессионпроцесс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="894a9-109">The **Win32\_SessionProcess** class has these types of members:</span></span>

-   [<span data-ttu-id="894a9-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="894a9-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="894a9-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="894a9-111">Properties</span></span>

<span data-ttu-id="894a9-112">Класс **Win32 \_ сессионпроцесс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="894a9-112">The **Win32\_SessionProcess** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="894a9-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="894a9-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="894a9-114">Тип данных: **Win32 \_ LogonSession**</span><span class="sxs-lookup"><span data-stu-id="894a9-114">Data type: **Win32\_LogonSession**</span></span>
</dt> <dt>

<span data-ttu-id="894a9-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="894a9-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="894a9-116">Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="894a9-116">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="894a9-117">[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) , представляющий сеанс, связанный с процессом.</span><span class="sxs-lookup"><span data-stu-id="894a9-117">A [**Win32\_LogonSession**](win32-logonsessionmappeddisk.md) that represents the session which is related to the process.</span></span>

</dd> <dt>

<span data-ttu-id="894a9-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="894a9-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="894a9-119">Тип данных: **\_ процесс Win32**</span><span class="sxs-lookup"><span data-stu-id="894a9-119">Data type: **Win32\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="894a9-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="894a9-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="894a9-121">Квалификаторы: [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**ключ**](../wmisdk/key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="894a9-121">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**Key**](../wmisdk/key-qualifier.md)</span></span>
</dt> </dl>

<span data-ttu-id="894a9-122">[**\_ Процесс Win32**](win32-processor.md) , представляющий процесс, связанный с сеансом.</span><span class="sxs-lookup"><span data-stu-id="894a9-122">A [**Win32\_Process**](win32-processor.md) that represents the process associated with the session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="894a9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="894a9-123">Remarks</span></span>

<span data-ttu-id="894a9-124">**Win32 \_ Сессионпроцесс** возвращает все сеансы для администратора при входе в систему с повышенными правами или при удаленном запуске.</span><span class="sxs-lookup"><span data-stu-id="894a9-124">**Win32\_SessionProcess** returns all session for the administrator when logged in elevated or when run remotely.</span></span> <span data-ttu-id="894a9-125">Это расширение поведения класса.</span><span class="sxs-lookup"><span data-stu-id="894a9-125">This is an extension to the behavior of the class.</span></span>

## <a name="requirements"></a><span data-ttu-id="894a9-126">Требования</span><span class="sxs-lookup"><span data-stu-id="894a9-126">Requirements</span></span>



| <span data-ttu-id="894a9-127">Требование</span><span class="sxs-lookup"><span data-stu-id="894a9-127">Requirement</span></span> | <span data-ttu-id="894a9-128">Значение</span><span class="sxs-lookup"><span data-stu-id="894a9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="894a9-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="894a9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="894a9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="894a9-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="894a9-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="894a9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="894a9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="894a9-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="894a9-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="894a9-133">Namespace</span></span><br/>                | <span data-ttu-id="894a9-134">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="894a9-134">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="894a9-135">MOF</span><span class="sxs-lookup"><span data-stu-id="894a9-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="894a9-136"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="894a9-136"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="894a9-137">DLL</span><span class="sxs-lookup"><span data-stu-id="894a9-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="894a9-138"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="894a9-138"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="894a9-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="894a9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894a9-140">**\_Сессионресаурце Win32**</span><span class="sxs-lookup"><span data-stu-id="894a9-140">**Win32\_SessionResource**</span></span>](win32-sessionresource.md)
</dt> <dt>

[<span data-ttu-id="894a9-141">Классы операционной системы</span><span class="sxs-lookup"><span data-stu-id="894a9-141">Operating System Classes</span></span>](./operating-system-classes.md)
</dt> </dl>

 

 
