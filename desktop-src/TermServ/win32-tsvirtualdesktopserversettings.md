---
title: Класс Win32_TSVirtualDesktopServerSettings
description: Содержит сведения о конфигурации для сервера Узел виртуализации удаленных рабочих столов (узла виртуализации удаленных рабочих столов).
ms.assetid: 749018aa-a8aa-433e-985b-40b44ef8aa7f
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSVirtualDesktopServerSettings службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSVirtualDesktopServerSettings, описание
topic_type:
- apiref
api_name:
- Win32_TSVirtualDesktopServerSettings
- Win32_TSVirtualDesktopServerSettings.SessionBrokerName
- Win32_TSVirtualDesktopServerSettings.PolicySourceSessionBrokerName
- Win32_TSVirtualDesktopServerSettings.Concurrency
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c39635aee7b32430ace0ead0e3b007051a3c049d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803599"
---
# <a name="win32_tsvirtualdesktopserversettings-class"></a><span data-ttu-id="c2e87-105">\_Класс Win32 тсвиртуалдесктопсерверсеттингс</span><span class="sxs-lookup"><span data-stu-id="c2e87-105">Win32\_TSVirtualDesktopServerSettings class</span></span>

<span data-ttu-id="c2e87-106">Содержит сведения о конфигурации для сервера Узел виртуализации удаленных рабочих столов (узла виртуализации удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="c2e87-106">Contains configuration information for a Remote Desktop Virtualization Host (RD Virtualization Host) server.</span></span>

<span data-ttu-id="c2e87-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c2e87-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e87-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2e87-108">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVirtualDesktopServerSettings
{
  string SessionBrokerName;
  sint32 PolicySourceSessionBrokerName;
  uint32 Concurrency;
};
```

## <a name="members"></a><span data-ttu-id="c2e87-109">Члены</span><span class="sxs-lookup"><span data-stu-id="c2e87-109">Members</span></span>

<span data-ttu-id="c2e87-110">Класс **Win32 \_ тсвиртуалдесктопсерверсеттингс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2e87-110">The **Win32\_TSVirtualDesktopServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="c2e87-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2e87-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2e87-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2e87-112">Properties</span></span>

<span data-ttu-id="c2e87-113">Класс **Win32 \_ тсвиртуалдесктопсерверсеттингс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2e87-113">The **Win32\_TSVirtualDesktopServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2e87-114">**Параллелизм**</span><span class="sxs-lookup"><span data-stu-id="c2e87-114">**Concurrency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e87-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c2e87-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e87-116">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2e87-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2e87-117">Максимально допустимое количество одновременных запросов на подготовку для этого сервера виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c2e87-117">The maximum allowed concurrent provisioning requests for this Virtual Desktop Server.</span></span>

</dd> <dt>

<span data-ttu-id="c2e87-118">**полицисаурцесессионброкернаме**</span><span class="sxs-lookup"><span data-stu-id="c2e87-118">**PolicySourceSessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e87-119">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="c2e87-119">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="c2e87-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2e87-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c2e87-121">Если задано значение 0, указывает, что свойство **сессионброкернаме** настроено сервером. Если задано значение 1, указывает, что свойство **сессионброкернаме** настроено групповой политикой.</span><span class="sxs-lookup"><span data-stu-id="c2e87-121">If set to 0, indicates that the **SessionBrokerName** property is configured by the server; if set to 1, indicates the **SessionBrokerName** property is configured by a group policy.</span></span>

</dd> <dt>

<span data-ttu-id="c2e87-122">**сессионброкернаме**</span><span class="sxs-lookup"><span data-stu-id="c2e87-122">**SessionBrokerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2e87-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c2e87-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c2e87-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="c2e87-124">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="c2e87-125">Полное различающееся имя посредника сеансов для сервера узла виртуализации удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c2e87-125">The fully qualified distinguished name of the session broker for the RD Virtualization Host server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2e87-126">Требования</span><span class="sxs-lookup"><span data-stu-id="c2e87-126">Requirements</span></span>



| <span data-ttu-id="c2e87-127">Требование</span><span class="sxs-lookup"><span data-stu-id="c2e87-127">Requirement</span></span> | <span data-ttu-id="c2e87-128">Значение</span><span class="sxs-lookup"><span data-stu-id="c2e87-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2e87-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2e87-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2e87-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c2e87-130">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="c2e87-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2e87-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2e87-132">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c2e87-132">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="c2e87-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2e87-133">Namespace</span></span><br/>                | <span data-ttu-id="c2e87-134">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="c2e87-134">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="c2e87-135">MOF</span><span class="sxs-lookup"><span data-stu-id="c2e87-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2e87-136"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2e87-136"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c2e87-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c2e87-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2e87-138"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2e87-138"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

 





