---
title: Класс Win32_SessionDirectorySession
description: Предоставляет свойства для просмотра свойств сеанса подключение к удаленному рабочему столу Broker (RDCB).
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectorySession службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectorySession, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415024"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="f5aa4-105">\_Класс Win32 сессиондиректорисессион</span><span class="sxs-lookup"><span data-stu-id="f5aa4-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="f5aa4-106">Предоставляет свойства для просмотра свойств сеанса подключение к удаленному рабочему столу Broker (RDCB).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="f5aa4-107">В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="f5aa4-108">Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="f5aa4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5aa4-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="f5aa4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f5aa4-110">Members</span></span>

<span data-ttu-id="f5aa4-111">Класс **Win32 \_ сессиондиректорисессион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f5aa4-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="f5aa4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5aa4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f5aa4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f5aa4-113">Properties</span></span>

<span data-ttu-id="f5aa4-114">Класс **Win32 \_ сессиондиректорисессион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f5aa4-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-118">Приложение запущено в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-118">Application started with this session.</span></span> <span data-ttu-id="f5aa4-119">Это то же самое, что и свойство **стартпрограм** объекта [**имстсксекуредсеттингс**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-120">**Clientareawidth**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-121">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-123">Глубина цвета сеанса, измеряемая в битах на пиксель.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-124">**креатетиме**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-125">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-127">Дата и время создания сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-127">Date and time the session was created.</span></span> <span data-ttu-id="f5aa4-128">Это значение не сбрасывается при отключении и повторном подключении сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-129">**дисконнекттиме**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-130">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-132">Дата и время отключения сеанса (если применимо).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-133">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-136">Доменное имя пользователя, вошедшего в этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-137">**ресолутионхеигхт**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-138">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-140">Высота сеанса (в пикселях) для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-141">**ресолутионвидс**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-144">Ширина сеанса (в пикселях) для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-145">**серверипаддресс**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-148">IP-адрес сервера RDCB для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-152">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5aa4-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-153">Имя сервера RDCB для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-155">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-157">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f5aa4-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-158">Идентификатор сеанса для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-162">Состояние этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-162">State of this session.</span></span>

<dt>

<span data-ttu-id="f5aa4-163">0</span><span class="sxs-lookup"><span data-stu-id="f5aa4-163">0</span></span>
</dt> <dd>

<span data-ttu-id="f5aa4-164">Сеанс активен.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-165">1</span><span class="sxs-lookup"><span data-stu-id="f5aa4-165">1</span></span>
</dt> <dd>

<span data-ttu-id="f5aa4-166">Сеанс отключен.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f5aa4-167">**тспротокол**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-170">Протокол для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="f5aa4-171">0</span><span class="sxs-lookup"><span data-stu-id="f5aa4-171">0</span></span>
</dt> <dd>

<span data-ttu-id="f5aa4-172">Этот сеанс работает на физической консоли.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-173">1</span><span class="sxs-lookup"><span data-stu-id="f5aa4-173">1</span></span>
</dt> <dd>

<span data-ttu-id="f5aa4-174">Для этого сеанса используется собственный протокол стороннего производителя.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="f5aa4-175">2</span><span class="sxs-lookup"><span data-stu-id="f5aa4-175">2</span></span>
</dt> <dd>

<span data-ttu-id="f5aa4-176">Для этого сеанса используется протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f5aa4-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f5aa4-178">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f5aa4-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f5aa4-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f5aa4-180">Имя пользователя, выполнившего вход в этот сеанс.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f5aa4-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5aa4-181">Remarks</span></span>

<span data-ttu-id="f5aa4-182">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f5aa4-183">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f5aa4-184">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="f5aa4-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f5aa4-185">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f5aa4-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aa4-186">Требования</span><span class="sxs-lookup"><span data-stu-id="f5aa4-186">Requirements</span></span>



| <span data-ttu-id="f5aa4-187">Требование</span><span class="sxs-lookup"><span data-stu-id="f5aa4-187">Requirement</span></span> | <span data-ttu-id="f5aa4-188">Значение</span><span class="sxs-lookup"><span data-stu-id="f5aa4-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aa4-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f5aa4-189">Minimum supported client</span></span><br/> | <span data-ttu-id="f5aa4-190">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f5aa4-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="f5aa4-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f5aa4-191">Minimum supported server</span></span><br/> | <span data-ttu-id="f5aa4-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f5aa4-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f5aa4-193">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f5aa4-193">Namespace</span></span><br/>                | <span data-ttu-id="f5aa4-194">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="f5aa4-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="f5aa4-195">MOF</span><span class="sxs-lookup"><span data-stu-id="f5aa4-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5aa4-196"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa4-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5aa4-197">DLL</span><span class="sxs-lookup"><span data-stu-id="f5aa4-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5aa4-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5aa4-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aa4-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5aa4-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5aa4-200">**\_Сессиондиректориклустер Win32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="f5aa4-201">**\_Сессиондиректорисервер Win32**</span><span class="sxs-lookup"><span data-stu-id="f5aa4-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

