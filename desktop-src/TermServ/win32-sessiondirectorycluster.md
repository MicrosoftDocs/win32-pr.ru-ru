---
title: Класс Win32_SessionDirectoryCluster
description: Предоставляет свойства для просмотра свойств фермы в подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: a4a924fd-88ea-46db-968e-378c3dc46cfc
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryCluster службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryCluster, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryCluster
- Win32_SessionDirectoryCluster.ClusterName
- Win32_SessionDirectoryCluster.NumberOfServers
- Win32_SessionDirectoryCluster.SingleSessionMode
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3979dbe5403ca8f18e941b01e95774dabefe3211
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490095"
---
# <a name="win32_sessiondirectorycluster-class"></a><span data-ttu-id="d9072-105">\_Класс Win32 сессиондиректориклустер</span><span class="sxs-lookup"><span data-stu-id="d9072-105">Win32\_SessionDirectoryCluster class</span></span>

<span data-ttu-id="d9072-106">Предоставляет свойства для просмотра свойств фермы в подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="d9072-106">Provides properties for viewing the properties of a farm in Remote Desktop Connection Broker (RD Connection Broker).</span></span>

> [!Note]  
> <span data-ttu-id="d9072-107">В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB.</span><span class="sxs-lookup"><span data-stu-id="d9072-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="d9072-108">Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="d9072-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d9072-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d9072-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYCLUSTER_Prov"), AMENDMENT]
class Win32_SessionDirectoryCluster
{
  string ClusterName;
  uint32 NumberOfServers;
  uint32 SingleSessionMode;
};
```

## <a name="members"></a><span data-ttu-id="d9072-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d9072-110">Members</span></span>

<span data-ttu-id="d9072-111">Класс **Win32 \_ сессиондиректориклустер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d9072-111">The **Win32\_SessionDirectoryCluster** class has these types of members:</span></span>

-   [<span data-ttu-id="d9072-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9072-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9072-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d9072-113">Properties</span></span>

<span data-ttu-id="d9072-114">Класс **Win32 \_ сессиондиректориклустер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d9072-114">The **Win32\_SessionDirectoryCluster** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9072-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="d9072-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9072-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d9072-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9072-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9072-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9072-118">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="d9072-118">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="d9072-119">Имя фермы в RDCB.</span><span class="sxs-lookup"><span data-stu-id="d9072-119">Name of the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="d9072-120">**нумберофсерверс**</span><span class="sxs-lookup"><span data-stu-id="d9072-120">**NumberOfServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9072-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9072-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9072-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9072-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9072-123">Количество серверов в ферме в RDCB.</span><span class="sxs-lookup"><span data-stu-id="d9072-123">Number of servers in the farm in RD Connection Broker.</span></span>

</dd> <dt>

<span data-ttu-id="d9072-124">**синглесессионмоде**</span><span class="sxs-lookup"><span data-stu-id="d9072-124">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9072-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d9072-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d9072-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d9072-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9072-127">Односеансовый режим фермы в RDCB.</span><span class="sxs-lookup"><span data-stu-id="d9072-127">Single session mode of the farm in RD Connection Broker.</span></span>

<dt>

<span data-ttu-id="d9072-128">0</span><span class="sxs-lookup"><span data-stu-id="d9072-128">0</span></span>
</dt> <dd>

<span data-ttu-id="d9072-129">Ферма в RDCB не находится в режиме одиночного сеанса.</span><span class="sxs-lookup"><span data-stu-id="d9072-129">The farm in RD Connection Broker is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="d9072-130">1</span><span class="sxs-lookup"><span data-stu-id="d9072-130">1</span></span>
</dt> <dd>

<span data-ttu-id="d9072-131">Ферма в RDCB находится в режиме одиночного сеанса.</span><span class="sxs-lookup"><span data-stu-id="d9072-131">The farm in RD Connection Broker is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9072-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d9072-132">Remarks</span></span>

<span data-ttu-id="d9072-133">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="d9072-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d9072-134">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="d9072-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d9072-135">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="d9072-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d9072-136">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d9072-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d9072-137">Требования</span><span class="sxs-lookup"><span data-stu-id="d9072-137">Requirements</span></span>



| <span data-ttu-id="d9072-138">Требование</span><span class="sxs-lookup"><span data-stu-id="d9072-138">Requirement</span></span> | <span data-ttu-id="d9072-139">Значение</span><span class="sxs-lookup"><span data-stu-id="d9072-139">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9072-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d9072-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d9072-141">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d9072-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d9072-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d9072-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d9072-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9072-143">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d9072-144">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d9072-144">Namespace</span></span><br/>                | <span data-ttu-id="d9072-145">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="d9072-145">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="d9072-146">MOF</span><span class="sxs-lookup"><span data-stu-id="d9072-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9072-147"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9072-147"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9072-148">DLL</span><span class="sxs-lookup"><span data-stu-id="d9072-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9072-149"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9072-149"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9072-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d9072-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9072-151">**\_Сессиондиректорисервер Win32**</span><span class="sxs-lookup"><span data-stu-id="d9072-151">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> <dt>

[<span data-ttu-id="d9072-152">**\_Сессиондиректорисессион Win32**</span><span class="sxs-lookup"><span data-stu-id="d9072-152">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

