---
title: Класс Win32_VirtualDesktopSession
description: Управляет сеансом виртуального рабочего стола.
ms.assetid: a5a0d2a4-6e19-42ac-988c-2d3787946325
ms.tgt_platform: multiple
keywords:
- Класс Win32_VirtualDesktopSession службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_VirtualDesktopSession, описание
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession.VMHostName
- Win32_VirtualDesktopSession.SessionId
- Win32_VirtualDesktopSession.VMName
- Win32_VirtualDesktopSession.ConnectState
- Win32_VirtualDesktopSession.UserName
- Win32_VirtualDesktopSession.DomainName
- Win32_VirtualDesktopSession.CollectionId
- Win32_VirtualDesktopSession.ClientMachineName
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f343c1dc022dcb4759f813de956ade27e1aff213
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489342"
---
# <a name="win32_virtualdesktopsession-class"></a><span data-ttu-id="58832-105">\_Класс Win32 виртуалдесктопсессион</span><span class="sxs-lookup"><span data-stu-id="58832-105">Win32\_VirtualDesktopSession class</span></span>

<span data-ttu-id="58832-106">Управляет сеансом виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="58832-106">Manages a virtual desktop session.</span></span>

<span data-ttu-id="58832-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="58832-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="58832-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58832-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_VirtualDesktopSession
{
  string VMHostName;
  uint32 SessionId;
  string VMName;
  uint32 ConnectState;
  string UserName;
  string DomainName;
  string CollectionId;
  string ClientMachineName;
};
```

## <a name="members"></a><span data-ttu-id="58832-109">Члены</span><span class="sxs-lookup"><span data-stu-id="58832-109">Members</span></span>

<span data-ttu-id="58832-110">Класс **Win32 \_ виртуалдесктопсессион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="58832-110">The **Win32\_VirtualDesktopSession** class has these types of members:</span></span>

-   [<span data-ttu-id="58832-111">Методы</span><span class="sxs-lookup"><span data-stu-id="58832-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="58832-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="58832-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="58832-113">Методы</span><span class="sxs-lookup"><span data-stu-id="58832-113">Methods</span></span>

<span data-ttu-id="58832-114">Класс **Win32 \_ виртуалдесктопсессион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="58832-114">The **Win32\_VirtualDesktopSession** class has these methods.</span></span>



| <span data-ttu-id="58832-115">Метод</span><span class="sxs-lookup"><span data-stu-id="58832-115">Method</span></span>                                                         | <span data-ttu-id="58832-116">Описание</span><span class="sxs-lookup"><span data-stu-id="58832-116">Description</span></span>                                                                |
|:---------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="58832-117">**Отключение**</span><span class="sxs-lookup"><span data-stu-id="58832-117">**Disconnect**</span></span>](disconnect-win32-virtualdesktopsession.md)   | <span data-ttu-id="58832-118">Отключает сеанс виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="58832-118">Disconnects the virtual desktop session.</span></span><br/>                        |
| [<span data-ttu-id="58832-119">**Выполнен**</span><span class="sxs-lookup"><span data-stu-id="58832-119">**Logoff**</span></span>](logoff-win32-virtualdesktopsession.md)           | <span data-ttu-id="58832-120">Выполнит выход пользователя из сеанса виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="58832-120">Logs off the user from the virtual desktop session.</span></span><br/>             |
| [<span data-ttu-id="58832-121">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="58832-121">**SendMessage**</span></span>](sendmessage-win32-virtualdesktopsession.md) | <span data-ttu-id="58832-122">Отправка сообщения пользователю через сеанс виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="58832-122">Send a message to the user through the virtual desktop session.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="58832-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="58832-123">Properties</span></span>

<span data-ttu-id="58832-124">Класс **Win32 \_ виртуалдесктопсессион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="58832-124">The **Win32\_VirtualDesktopSession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="58832-125">**ClientMachineName**</span><span class="sxs-lookup"><span data-stu-id="58832-125">**ClientMachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-128">Возвращает имя клиентского компьютера, подключенного к сеансу.</span><span class="sxs-lookup"><span data-stu-id="58832-128">Gets the name of the client machine that is connected to the session.</span></span>

</dd> <dt>

<span data-ttu-id="58832-129">**CollectionId**</span><span class="sxs-lookup"><span data-stu-id="58832-129">**CollectionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-132">Возвращает имя коллекции виртуальных рабочих столов, в которой размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="58832-132">Gets the name of the virtual desktop collection that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="58832-133">**коннектстате**</span><span class="sxs-lookup"><span data-stu-id="58832-133">**ConnectState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-134">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58832-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58832-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-136">Возвращает состояние соединения с сеансом.</span><span class="sxs-lookup"><span data-stu-id="58832-136">Gets the state of the connection to the session.</span></span>

</dd> <dt>

<span data-ttu-id="58832-137">**Имя_домена**</span><span class="sxs-lookup"><span data-stu-id="58832-137">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-140">Возвращает доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="58832-140">Gets the domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="58832-141">**SessionId**</span><span class="sxs-lookup"><span data-stu-id="58832-141">**SessionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-142">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="58832-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="58832-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58832-144">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58832-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58832-145">Возвращает идентификатор сеанса виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="58832-145">Gets the ID of the virtual desktop session.</span></span>

</dd> <dt>

<span data-ttu-id="58832-146">**UserName**</span><span class="sxs-lookup"><span data-stu-id="58832-146">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-149">Возвращает имя учетной записи пользователя, назначенной сеансу.</span><span class="sxs-lookup"><span data-stu-id="58832-149">Gets the name of the user account that is assigned to the session.</span></span>

</dd> <dt>

<span data-ttu-id="58832-150">**VMHostName**</span><span class="sxs-lookup"><span data-stu-id="58832-150">**VMHostName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="58832-153">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="58832-153">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="58832-154">Возвращает имя сервера узла виртуализации удаленный рабочий стол, на котором размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="58832-154">Gets the name of the Remote Desktop virtualization host server that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="58832-155">**VMName**</span><span class="sxs-lookup"><span data-stu-id="58832-155">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="58832-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="58832-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="58832-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="58832-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="58832-158">Возвращает имя виртуальной машины, назначенной сеансу.</span><span class="sxs-lookup"><span data-stu-id="58832-158">Gets the name of the virtual machine that is assigned to the session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="58832-159">Требования</span><span class="sxs-lookup"><span data-stu-id="58832-159">Requirements</span></span>



| <span data-ttu-id="58832-160">Требование</span><span class="sxs-lookup"><span data-stu-id="58832-160">Requirement</span></span> | <span data-ttu-id="58832-161">Значение</span><span class="sxs-lookup"><span data-stu-id="58832-161">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="58832-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58832-162">Minimum supported client</span></span><br/> | <span data-ttu-id="58832-163">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="58832-163">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="58832-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58832-164">Minimum supported server</span></span><br/> | <span data-ttu-id="58832-165">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="58832-165">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="58832-166">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="58832-166">Namespace</span></span><br/>                | <span data-ttu-id="58832-167">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="58832-167">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="58832-168">MOF</span><span class="sxs-lookup"><span data-stu-id="58832-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="58832-169"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="58832-169"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="58832-170">DLL</span><span class="sxs-lookup"><span data-stu-id="58832-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58832-171"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58832-171"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="58832-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58832-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58832-173">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="58832-173">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

