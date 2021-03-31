---
title: Класс Win32_SessionBrokerFarm
description: Определяет запрос для фермы посредников сеансов.
ms.assetid: 55a2a7ea-e891-4723-b919-ee3c908eaffb
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerFarm службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerFarm, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarm
- Win32_SessionBrokerFarm.PluginName
- Win32_SessionBrokerFarm.FarmName
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a3ccbb5e1e08a036fb9973d552db73ee1607c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490587"
---
# <a name="win32_sessionbrokerfarm-class"></a><span data-ttu-id="97204-105">\_Класс Win32 сессионброкерфарм</span><span class="sxs-lookup"><span data-stu-id="97204-105">Win32\_SessionBrokerFarm class</span></span>

<span data-ttu-id="97204-106">Определяет запрос для фермы посредников сеансов.</span><span class="sxs-lookup"><span data-stu-id="97204-106">Defines the query for a session broker farm.</span></span>

<span data-ttu-id="97204-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="97204-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="97204-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="97204-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERFARM_Prov"), AMENDMENT]
class Win32_SessionBrokerFarm
{
  string PluginName;
  string FarmName;
};
```

## <a name="members"></a><span data-ttu-id="97204-109">Члены</span><span class="sxs-lookup"><span data-stu-id="97204-109">Members</span></span>

<span data-ttu-id="97204-110">Класс **Win32 \_ сессионброкерфарм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="97204-110">The **Win32\_SessionBrokerFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="97204-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="97204-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="97204-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="97204-112">Properties</span></span>

<span data-ttu-id="97204-113">Класс **Win32 \_ сессионброкерфарм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="97204-113">The **Win32\_SessionBrokerFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="97204-114">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="97204-114">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97204-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97204-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97204-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97204-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97204-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97204-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="97204-118">Имя фермы посредника сеансов, к которой необходимо получить запрос.</span><span class="sxs-lookup"><span data-stu-id="97204-118">The name of the session broker farm that needs to be queried.</span></span>

</dd> <dt>

<span data-ttu-id="97204-119">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="97204-119">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97204-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="97204-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="97204-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="97204-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="97204-122">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="97204-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="97204-123">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="97204-123">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="97204-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="97204-124">Examples</span></span>

<span data-ttu-id="97204-125">Следующая строка запроса демонстрирует использование класса **Win32 \_ сессионброкерфарм** в запросе.</span><span class="sxs-lookup"><span data-stu-id="97204-125">The following query string demonstrates how the **Win32\_SessionBrokerFarm** class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerFarm WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="97204-126">Требования</span><span class="sxs-lookup"><span data-stu-id="97204-126">Requirements</span></span>



| <span data-ttu-id="97204-127">Требование</span><span class="sxs-lookup"><span data-stu-id="97204-127">Requirement</span></span> | <span data-ttu-id="97204-128">Значение</span><span class="sxs-lookup"><span data-stu-id="97204-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="97204-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97204-129">Minimum supported client</span></span><br/> | <span data-ttu-id="97204-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="97204-130">None supported</span></span><br/>                                                              |
| <span data-ttu-id="97204-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97204-131">Minimum supported server</span></span><br/> | <span data-ttu-id="97204-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="97204-132">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="97204-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="97204-133">Namespace</span></span><br/>                | <span data-ttu-id="97204-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="97204-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="97204-135">MOF</span><span class="sxs-lookup"><span data-stu-id="97204-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97204-136"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97204-136"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="97204-137">DLL</span><span class="sxs-lookup"><span data-stu-id="97204-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97204-138"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97204-138"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

