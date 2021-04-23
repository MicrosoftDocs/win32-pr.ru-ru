---
title: Класс Win32_SessionBrokerTarget
description: Определяет запрос для целевого объекта посредника сеанса.
ms.assetid: 35de25da-cb89-4836-be14-9544b1264248
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerTarget службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerTarget, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTarget
- Win32_SessionBrokerTarget.PluginName
- Win32_SessionBrokerTarget.TargetName
- Win32_SessionBrokerTarget.FarmName
- Win32_SessionBrokerTarget.Guid
- Win32_SessionBrokerTarget.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ceca0df64eeb9cd285737fee7c6ca6fa3a2e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892654"
---
# <a name="win32_sessionbrokertarget-class"></a><span data-ttu-id="c189d-105">\_Класс Win32 сессионброкертаржет</span><span class="sxs-lookup"><span data-stu-id="c189d-105">Win32\_SessionBrokerTarget class</span></span>

<span data-ttu-id="c189d-106">Определяет запрос для целевого объекта посредника сеанса.</span><span class="sxs-lookup"><span data-stu-id="c189d-106">Defines the query for a session broker target.</span></span>

<span data-ttu-id="c189d-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c189d-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c189d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c189d-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONBROKERTARGET_Prov"), AMENDMENT]
class Win32_SessionBrokerTarget
{
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="c189d-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c189d-109">Members</span></span>

<span data-ttu-id="c189d-110">Класс **Win32 \_ сессионброкертаржет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c189d-110">The **Win32\_SessionBrokerTarget** class has these types of members:</span></span>

-   [<span data-ttu-id="c189d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c189d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c189d-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c189d-112">Properties</span></span>

<span data-ttu-id="c189d-113">Класс **Win32 \_ сессионброкертаржет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c189d-113">The **Win32\_SessionBrokerTarget** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c189d-114">**Среда**</span><span class="sxs-lookup"><span data-stu-id="c189d-114">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c189d-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c189d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c189d-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c189d-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c189d-117">Имя среды.</span><span class="sxs-lookup"><span data-stu-id="c189d-117">The environment name.</span></span> <span data-ttu-id="c189d-118">В случае целевого объекта виртуальной машины это может быть имя узла виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c189d-118">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

</dd> <dt>

<span data-ttu-id="c189d-119">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="c189d-119">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c189d-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c189d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c189d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c189d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c189d-122">Имя фермы, которой принадлежит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="c189d-122">The name of the farm the target belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="c189d-123">**Устройства**</span><span class="sxs-lookup"><span data-stu-id="c189d-123">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c189d-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c189d-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c189d-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c189d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c189d-126">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c189d-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c189d-127">Идентификатор GUID (если он есть) целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="c189d-127">The GUID (if any) of the target.</span></span>

</dd> <dt>

<span data-ttu-id="c189d-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="c189d-128">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c189d-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c189d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c189d-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c189d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c189d-131">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c189d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c189d-132">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c189d-132">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="c189d-133">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="c189d-133">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c189d-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c189d-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c189d-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c189d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c189d-136">Имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="c189d-136">The name of the target.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c189d-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="c189d-137">Examples</span></span>

<span data-ttu-id="c189d-138">Следующая строка запроса демонстрирует использование \_ класса Win32 сессионброкертаржет в запросе.</span><span class="sxs-lookup"><span data-stu-id="c189d-138">The following query string demonstrates how the Win32\_SessionBrokerTarget class is used in a query.</span></span>


```CSharp
queryString = string.Format("SELECT * FROM Win32_SessionBrokerTarget WHERE PluginName = '{0}'", pluginName);
```



## <a name="requirements"></a><span data-ttu-id="c189d-139">Требования</span><span class="sxs-lookup"><span data-stu-id="c189d-139">Requirements</span></span>



| <span data-ttu-id="c189d-140">Требование</span><span class="sxs-lookup"><span data-stu-id="c189d-140">Requirement</span></span> | <span data-ttu-id="c189d-141">Значение</span><span class="sxs-lookup"><span data-stu-id="c189d-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c189d-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c189d-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c189d-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c189d-143">None supported</span></span><br/>                                                              |
| <span data-ttu-id="c189d-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c189d-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c189d-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c189d-145">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="c189d-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c189d-146">Namespace</span></span><br/>                | <span data-ttu-id="c189d-147">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c189d-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="c189d-148">MOF</span><span class="sxs-lookup"><span data-stu-id="c189d-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c189d-149"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c189d-149"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c189d-150">DLL</span><span class="sxs-lookup"><span data-stu-id="c189d-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c189d-151"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c189d-151"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

