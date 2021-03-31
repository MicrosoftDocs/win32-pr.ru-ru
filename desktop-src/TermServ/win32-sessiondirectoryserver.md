---
title: Класс Win32_SessionDirectoryServer
description: Предоставляет свойства для просмотра свойств сервера подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryServer, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988512"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="9ac4e-105">\_Класс Win32 сессиондиректорисервер</span><span class="sxs-lookup"><span data-stu-id="9ac4e-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="9ac4e-106">Предоставляет свойства для просмотра свойств сервера подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="9ac4e-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="9ac4e-107">В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="9ac4e-108">Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="9ac4e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9ac4e-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="9ac4e-110">Члены</span><span class="sxs-lookup"><span data-stu-id="9ac4e-110">Members</span></span>

<span data-ttu-id="9ac4e-111">Класс **Win32 \_ сессиондиректорисервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9ac4e-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="9ac4e-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ac4e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9ac4e-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9ac4e-113">Properties</span></span>

<span data-ttu-id="9ac4e-114">Класс **Win32 \_ сессиондиректорисервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9ac4e-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-118">Имя фермы, содержащей сервер.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-119">**лоадиндикатор**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-122">Относительный номер, представляющий нагрузку на сервер узла сеансов удаленных рабочих столов при использовании алгоритма балансировки нагрузки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="9ac4e-123">Значение свойства *лоадиндикатор* основано на количестве сеансов, количестве ожидающих запросов на перенаправление и значении веса сервера.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-124">**нумберофсессионс**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-125">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-127">Число сеансов на сервере RDCB.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-128">**нумпендредир**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-131">Число ожидающих запросов на перенаправление.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-132">**серверипаддресс**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-135">IP-адрес сервера RDCB.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="9ac4e-136">Если сервер настроен для адресов IPv4 и IPv6, он будет содержать IPv4-адрес.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-140">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9ac4e-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-141">Имя сервера RDCB.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-142">**сервервеигхт**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-145">Значение веса сервера, используемое при балансировке нагрузки.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-146">**синглесессионмоде**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9ac4e-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="9ac4e-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="9ac4e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9ac4e-149">Параметр режима одиночного сеанса RDCB сервера.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="9ac4e-150">0</span><span class="sxs-lookup"><span data-stu-id="9ac4e-150">0</span></span>
</dt> <dd>

<span data-ttu-id="9ac4e-151">Ферма не находится в режиме одиночного сеанса.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="9ac4e-152">1</span><span class="sxs-lookup"><span data-stu-id="9ac4e-152">1</span></span>
</dt> <dd>

<span data-ttu-id="9ac4e-153">Ферма в находится в режиме одиночного сеанса.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ac4e-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9ac4e-154">Remarks</span></span>

<span data-ttu-id="9ac4e-155">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="9ac4e-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9ac4e-156">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="9ac4e-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ac4e-157">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="9ac4e-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9ac4e-158">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9ac4e-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ac4e-159">Требования</span><span class="sxs-lookup"><span data-stu-id="9ac4e-159">Requirements</span></span>



| <span data-ttu-id="9ac4e-160">Требование</span><span class="sxs-lookup"><span data-stu-id="9ac4e-160">Requirement</span></span> | <span data-ttu-id="9ac4e-161">Значение</span><span class="sxs-lookup"><span data-stu-id="9ac4e-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ac4e-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9ac4e-162">Minimum supported client</span></span><br/> | <span data-ttu-id="9ac4e-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9ac4e-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9ac4e-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9ac4e-164">Minimum supported server</span></span><br/> | <span data-ttu-id="9ac4e-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ac4e-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9ac4e-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9ac4e-166">Namespace</span></span><br/>                | <span data-ttu-id="9ac4e-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="9ac4e-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="9ac4e-168">MOF</span><span class="sxs-lookup"><span data-stu-id="9ac4e-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ac4e-169"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9ac4e-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ac4e-170">DLL</span><span class="sxs-lookup"><span data-stu-id="9ac4e-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ac4e-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ac4e-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ac4e-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9ac4e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ac4e-173">**\_Сессиондиректориклустер Win32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="9ac4e-174">**\_Сессиондиректорисессион Win32**</span><span class="sxs-lookup"><span data-stu-id="9ac4e-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

