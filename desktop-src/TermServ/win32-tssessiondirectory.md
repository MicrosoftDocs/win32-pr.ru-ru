---
title: Класс Win32_TSSessionDirectory
description: Определяет параметры конфигурации подключение к удаленному рабочему столу Broker (RDCB) для \_ класса Win32 тссессиондиректорисеттинг.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSessionDirectory, описание
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988507"
---
# <a name="win32_tssessiondirectory-class"></a><span data-ttu-id="0ce7a-105">\_Класс Win32 тссессиондиректори</span><span class="sxs-lookup"><span data-stu-id="0ce7a-105">Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="0ce7a-106">Определяет параметры конфигурации подключение к удаленному рабочему столу Broker (RDCB) для класса [**Win32 \_ тссессиондиректорисеттинг**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="0ce7a-106">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

> [!Note]  
> <span data-ttu-id="0ce7a-107">В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="0ce7a-108">Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

<span data-ttu-id="0ce7a-109">Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-109">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="0ce7a-110">Справочные сведения о методах см. в таблице методов далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-110">For reference information about methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ce7a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ce7a-111">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a><span data-ttu-id="0ce7a-112">Члены</span><span class="sxs-lookup"><span data-stu-id="0ce7a-112">Members</span></span>

<span data-ttu-id="0ce7a-113">Класс **Win32 \_ тссессиондиректори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0ce7a-113">The **Win32\_TSSessionDirectory** class has these types of members:</span></span>

-   [<span data-ttu-id="0ce7a-114">Методы</span><span class="sxs-lookup"><span data-stu-id="0ce7a-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="0ce7a-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ce7a-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0ce7a-116">Методы</span><span class="sxs-lookup"><span data-stu-id="0ce7a-116">Methods</span></span>

<span data-ttu-id="0ce7a-117">Класс **Win32 \_ тссессиондиректори** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-117">The **Win32\_TSSessionDirectory** class has these methods.</span></span>



| <span data-ttu-id="0ce7a-118">Метод</span><span class="sxs-lookup"><span data-stu-id="0ce7a-118">Method</span></span>                                                                                                  | <span data-ttu-id="0ce7a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="0ce7a-119">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0ce7a-120">**креатеусердисктемплате**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-120">**CreateUserDiskTemplate**</span></span>](createuserdisktemplate-win32-tssessiondirectory.md)                       | <span data-ttu-id="0ce7a-121">Создает шаблон диска пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-121">Creates a user disk template.</span></span><br/>                                                                     |
| [<span data-ttu-id="0ce7a-122">**дисаблеусервхд**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-122">**DisableUserVhd**</span></span>](disableuservhd-win32-tssessiondirectory.md)                                       | <span data-ttu-id="0ce7a-123">Отключает виртуальный жесткий диск профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-123">Disables a user profile VHD.</span></span><br/>                                                                      |
| [<span data-ttu-id="0ce7a-124">**енаблеусервхд**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-124">**EnableUserVhd**</span></span>](enableuservhd-win32-tssessiondirectory.md)                                         | <span data-ttu-id="0ce7a-125">Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-125">Enables a user profile VHD on an RDSH server.</span></span><br/>                                                     |
| [<span data-ttu-id="0ce7a-126">**жеткуррентредиректаблеаддрессес**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-126">**GetCurrentRedirectableAddresses**</span></span>](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="0ce7a-127">Получает настроенный в данный момент список доступных адресов DNS и тип перенаправления.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-127">Obtains the currently configured list of DNS eligible addresses, and the redirection type.</span></span><br/>        |
| [<span data-ttu-id="0ce7a-128">**жетредиректаблеаддрессес**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-128">**GetRedirectableAddresses**</span></span>](getredirectableaddresses-win32-tssessiondirectory.md)                   | <span data-ttu-id="0ce7a-129">Получает полный список доступных адресов DNS.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-129">Obtains the entire list of DNS eligible addresses.</span></span><br/>                                                |
| [<span data-ttu-id="0ce7a-130">**пингсессиондиректори**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-130">**PingSessionDirectory**</span></span>](pingsessiondirectory-win32-tssessiondirectory.md)                           | <span data-ttu-id="0ce7a-131">Проверяет, доступен ли сервер RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-131">Checks whether the RD Connection Broker server is available.</span></span><br/>                                      |
| [<span data-ttu-id="0ce7a-132">**сеткуррентредиректаблеаддрессес**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-132">**SetCurrentRedirectableAddresses**</span></span>](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | <span data-ttu-id="0ce7a-133">Задает настроенный список доступных адресов DNS и тип перенаправления.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-133">Sets the configured list of DNS eligible addresses, and the redirection type.</span></span><br/>                     |
| [<span data-ttu-id="0ce7a-134">**сетлоадбаланЦингстате**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-134">**SetLoadBalancingState**</span></span>](setloadbalancingstate-win32-tssessiondirectory.md)                         | <span data-ttu-id="0ce7a-135">Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-135">Sets the value to indicate if the server will participate in RD Connection Broker load balancing.</span></span><br/> |
| [<span data-ttu-id="0ce7a-136">**сетсервервеигхт**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-136">**SetServerWeight**</span></span>](setserverweight-win32-tssessiondirectory.md)                                     | <span data-ttu-id="0ce7a-137">Задает значение веса сервера для балансировки нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-137">Sets the server weight value for RD Connection Broker load balancing.</span></span><br/>                             |
| [<span data-ttu-id="0ce7a-138">**сетсессиондиректоряктиве**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-138">**SetSessionDirectoryActive**</span></span>](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | <span data-ttu-id="0ce7a-139">Отключает и включает RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-139">Disables and enables the RD Connection Broker.</span></span><br/>                                                    |
| [<span data-ttu-id="0ce7a-140">**сетсессиондиректорекспосесерверип**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-140">**SetSessionDirectoryExposeServerIP**</span></span>](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | <span data-ttu-id="0ce7a-141">Задает свойство **сессиондиректорекспосесерверип** .</span><span class="sxs-lookup"><span data-stu-id="0ce7a-141">Sets the **SessionDirectoryExposeServerIP** property.</span></span><br/>                                             |
| [<span data-ttu-id="0ce7a-142">**сетсессиондиректорипроперти**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-142">**SetSessionDirectoryProperty**</span></span>](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | <span data-ttu-id="0ce7a-143">Задает свойство **сессиондиректорилокатион** или свойство **сессиондиректориклустернаме** .</span><span class="sxs-lookup"><span data-stu-id="0ce7a-143">Sets the **SessionDirectoryLocation** property or the **SessionDirectoryClusterName** property.</span></span><br/>   |
| [<span data-ttu-id="0ce7a-144">**сеттсредиректормоде**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-144">**SetTSRedirectorMode**</span></span>](settsredirectormode-win32-tssessiondirectory.md)                             | <span data-ttu-id="0ce7a-145">Этот метод недоступен.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-145">This method is not available.</span></span><br/>                                                                     |



 

### <a name="properties"></a><span data-ttu-id="0ce7a-146">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ce7a-146">Properties</span></span>

<span data-ttu-id="0ce7a-147">Класс **Win32 \_ тссессиондиректори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-147">The **Win32\_TSSessionDirectory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0ce7a-148">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-148">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-151">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-152">Краткое описание (однострочная строка) объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-152">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0ce7a-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-154">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-154">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-157">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-157">Description of the object.</span></span>

<span data-ttu-id="0ce7a-158">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-159">**жетлоадбаланЦингстате**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-159">**GetLoadBalancingState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-160">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-162">Указывает, настроен ли сервер для участия в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-162">Indicates if the server is configured to participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="0ce7a-163">0</span><span class="sxs-lookup"><span data-stu-id="0ce7a-163">0</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-164">Сервер не настроен для участия в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-164">The server is not configured to participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-165">1</span><span class="sxs-lookup"><span data-stu-id="0ce7a-165">1</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-166">Сервер настроен для участия в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-166">The server is configured to participate in RD Connection Broker load balancing.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-167">**жетсервервеигхт**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-167">**GetServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-168">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-170">Возвращает значение веса сервера, используемое в балансировке нагрузки RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-170">Retrieves the server weight value that is used in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-171">**жеттсредиректормоде**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-171">**GetTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-172">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-174">Указывает, настроен ли сервер для работы в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-174">Indicates if the server is configured to act as a Remote Desktop Services redirector.</span></span>

<dt>

<span data-ttu-id="0ce7a-175">0</span><span class="sxs-lookup"><span data-stu-id="0ce7a-175">0</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-176">Сервер настроен на работу в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-176">The server is configured to act as a Remote Desktop Services redirector.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-177">1</span><span class="sxs-lookup"><span data-stu-id="0ce7a-177">1</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-178">Сервер не настроен на работу в качестве перенаправления службы удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-178">The server is not configured to act as a Remote Desktop Services redirector.</span></span>

</dd> </dl>

<span data-ttu-id="0ce7a-179">**Windows Server 2008:** Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-179">**Windows Server 2008:** This property is not available.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-180">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-180">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-181">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-181">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-182">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-183">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF</span><span class="sxs-lookup"><span data-stu-id="0ce7a-183">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-184">Дата установки объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-184">The date the object was installed.</span></span> <span data-ttu-id="0ce7a-185">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-185">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0ce7a-186">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-186">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-187">**Name**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-187">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-188">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-188">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-190">Имя объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-190">The name of the object.</span></span>

<span data-ttu-id="0ce7a-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-192">**полицисаурцелоадбаланЦинг**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-192">**PolicySourceLoadBalancing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-193">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-193">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-195">Указывает, настроено ли свойство **жетлоадбаланЦингстате** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-195">Indicates if the **GetLoadBalancingState** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-196">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-196">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-197">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-197">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-198">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-198">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-199">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-199">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-200">**полицисаурцесессиондиректоряктиве**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-200">**PolicySourceSessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-201">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-201">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-202">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-202">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-203">Указывает, настроено ли свойство **сессиондиректоряктиве** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-203">Indicates if the **SessionDirectoryActive** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-204">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-204">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-205">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-205">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-206">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-206">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-207">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-207">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-208">**полицисаурцесессиондиректориклустернаме**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-208">**PolicySourceSessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-209">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-209">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-211">Указывает, настроено ли свойство **сессиондиректориклустернаме** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-211">Indicates if the **SessionDirectoryClusterName** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-212">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-212">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-213">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-213">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-214">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-214">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-215">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-215">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-216">**полицисаурцесессиондиректорекспосесерверип**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-216">**PolicySourceSessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-217">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-217">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-218">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-219">Указывает, настроено ли свойство **сессиондиректорекспосесерверип** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-219">Indicates if the **SessionDirectoryExposeServerIP** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-220">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-220">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-221">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-221">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-222">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-222">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-223">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-223">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-224">**полицисаурцесессиондиректорилокатион**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-224">**PolicySourceSessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-225">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-225">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-227">Указывает, настроено ли свойство **сессиондиректорилокатион** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-227">Indicates if the **SessionDirectoryLocation** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-228">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-228">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-229">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-229">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-230">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-230">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-231">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-231">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-232">**полицисаурцетсредиректормоде**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-232">**PolicySourceTSRedirectorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-233">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-233">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-235">Это свойство недоступно.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-235">This property is not available.</span></span>

<span data-ttu-id="0ce7a-236">**Windows Server 2008 R2:** Указывает, настроено ли свойство **жеттсредиректормоде** сервером или групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-236">**Windows Server 2008 R2:** Indicates if the **GetTSRedirectorMode** property is configured by the server or by group policy.</span></span>

<dt>

<span data-ttu-id="0ce7a-237">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-237">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-238">Сервер</span><span class="sxs-lookup"><span data-stu-id="0ce7a-238">Server</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-239">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-239">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="0ce7a-240">Групповая политика</span><span class="sxs-lookup"><span data-stu-id="0ce7a-240">Group policy</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-241">**сессиондиректоряктиве**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-241">**SessionDirectoryActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-242">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-242">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-243">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-244">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-244">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-245">Указывает, участвует ли службы удаленных рабочих столов в RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-245">Specifies if Remote Desktop Services participates in the RD Connection Broker.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0ce7a-246"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-246"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0ce7a-247">Службы удаленных рабочих столов участие в RDCB отключено.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-247">Remote Desktop Services participation in the RD Connection Broker is disabled.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0ce7a-248"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-248"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0ce7a-249">Службы удаленных рабочих столов участие в RDCB включено.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-249">Remote Desktop Services participation in the RD Connection Broker is enabled.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-250">**сессиондиректориклустернаме**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-250">**SessionDirectoryClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-251">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-251">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-253">Виртуальный IP-адрес кластера, к которому принадлежит сервер узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-253">The virtual IP address of the cluster to which the RD Session Host server belongs.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-254">**сессиондиректорекспосесерверип**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-254">**SessionDirectoryExposeServerIP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-255">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-255">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-256">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-257">Указывает, разрешено ли получение IP-адреса RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-257">Specifies if retrieval of the IP address of the RD Connection Broker is allowed.</span></span>

<dt>

<span id="FALSE"></span><span id="false"></span>

<span data-ttu-id="0ce7a-258"><span id="FALSE"></span><span id="false"></span>**False** (0)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-258"><span id="FALSE"></span><span id="false"></span>**FALSE** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0ce7a-259">Получение запрещено.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-259">Retrieval is denied.</span></span>

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span data-ttu-id="0ce7a-260"><span id="TRUE"></span><span id="true"></span>**True** (1)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-260"><span id="TRUE"></span><span id="true"></span>**TRUE** (1)</span></span>


</dt> <dd>

<span data-ttu-id="0ce7a-261">Извлечение разрешено.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-261">Retrieval is allowed.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="0ce7a-262">**сессиондиректорипаддресс**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-262">**SessionDirectoryIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-263">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-263">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-264">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="0ce7a-264">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-265">IP-адрес адаптера локальной сети, используемого каталогом сеансов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-265">The IP address of the LAN adapter used by the session directory.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-266">**сессиондиректорилокатион**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-266">**SessionDirectoryLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-267">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-267">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-268">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-269">Сетевое DNS-имя или IP-адрес сервера, на котором запущена служба RDCB.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-269">The network DNS name or IP address of the server where the RD Connection Broker service is running.</span></span>

</dd> <dt>

<span data-ttu-id="0ce7a-270">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-270">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0ce7a-271">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-271">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0ce7a-272">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0ce7a-273">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0ce7a-273">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0ce7a-274">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-274">Current status of the object.</span></span> <span data-ttu-id="0ce7a-275">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-275">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0ce7a-276">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-276">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0ce7a-277">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="0ce7a-277">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0ce7a-278">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-278">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0ce7a-279">Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-279">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0ce7a-280">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-280">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0ce7a-281">("ОК")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-281">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-282">("Ошибка")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-282">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-283">("Пониженное состояние")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-283">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-284">("Неизвестно")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-284">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-285">("Пред Fail")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-285">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-286">("Запуск")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-286">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-287">("Остановка")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-287">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0ce7a-288">("Служба")</span><span class="sxs-lookup"><span data-stu-id="0ce7a-288">("Service")</span></span>


<span data-ttu-id="0ce7a-289"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ce7a-289"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="0ce7a-290">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ce7a-290">Remarks</span></span>

<span data-ttu-id="0ce7a-291">Чтобы подключиться к \\ \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-291">To connect to the \\\\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="0ce7a-292">Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**".</span><span class="sxs-lookup"><span data-stu-id="0ce7a-292">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="0ce7a-293">Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-293">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of six.</span></span>

<span data-ttu-id="0ce7a-294">В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-294">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="0ce7a-295">В Windows Server 2008 имя функции каталога сеансов служб терминалов было изменено на посредник сеансов служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-295">In Windows Server 2008, the name of the Terminal Services Session Directory feature was changed to Terminal Services Session Broker.</span></span>

<span data-ttu-id="0ce7a-296">В Windows Server 2008 R2 имя компонента посредника сеансов служб терминалов изменилось на подключение к удаленному рабочему столу Broker.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-296">In Windows Server 2008 R2, the name of the Terminal Services Session Broker feature was changed to Remote Desktop Connection Broker.</span></span>

<span data-ttu-id="0ce7a-297">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-297">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0ce7a-298">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-298">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0ce7a-299">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="0ce7a-299">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0ce7a-300">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0ce7a-300">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ce7a-301">Требования</span><span class="sxs-lookup"><span data-stu-id="0ce7a-301">Requirements</span></span>



| <span data-ttu-id="0ce7a-302">Требование</span><span class="sxs-lookup"><span data-stu-id="0ce7a-302">Requirement</span></span> | <span data-ttu-id="0ce7a-303">Значение</span><span class="sxs-lookup"><span data-stu-id="0ce7a-303">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ce7a-304">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ce7a-304">Minimum supported client</span></span><br/> | <span data-ttu-id="0ce7a-305">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0ce7a-305">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0ce7a-306">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ce7a-306">Minimum supported server</span></span><br/> | <span data-ttu-id="0ce7a-307">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ce7a-307">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ce7a-308">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ce7a-308">Namespace</span></span><br/>                | <span data-ttu-id="0ce7a-309">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0ce7a-309">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0ce7a-310">MOF</span><span class="sxs-lookup"><span data-stu-id="0ce7a-310">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ce7a-311"><dt>Тскфгвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ce7a-311"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ce7a-312">DLL</span><span class="sxs-lookup"><span data-stu-id="0ce7a-312">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ce7a-313"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ce7a-313"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ce7a-314">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ce7a-314">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ce7a-315">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-315">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dt>

[<span data-ttu-id="0ce7a-316">**\_Тссессиондиректорисеттинг Win32**</span><span class="sxs-lookup"><span data-stu-id="0ce7a-316">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

