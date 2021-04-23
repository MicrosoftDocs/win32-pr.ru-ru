---
title: Класс Win32_SessionDirectoryVirtualDesktopServer
description: Представляет Узел виртуализации удаленных рабочих столов сервер (узел виртуализации удаленных рабочих столов), присоединенный к посреднику сеансов.
ms.assetid: a09221bd-d1b1-465b-91bb-9ca400a796b1
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryVirtualDesktopServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryVirtualDesktopServer, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVirtualDesktopServer
- Win32_SessionDirectoryVirtualDesktopServer.Name
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2940679c13c5bd86f7d6b02340698f529e8149e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071342"
---
# <a name="win32_sessiondirectoryvirtualdesktopserver-class"></a><span data-ttu-id="e02e3-105">\_Класс Win32 сессиондиректоривиртуалдесктопсервер</span><span class="sxs-lookup"><span data-stu-id="e02e3-105">Win32\_SessionDirectoryVirtualDesktopServer class</span></span>

<span data-ttu-id="e02e3-106">Представляет Узел виртуализации удаленных рабочих столов сервер (узел виртуализации удаленных рабочих столов), присоединенный к посреднику сеансов.</span><span class="sxs-lookup"><span data-stu-id="e02e3-106">Represents a Remote Desktop Virtualization Host (RD Virtualization Host) server joined to a session broker.</span></span>

<span data-ttu-id="e02e3-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e02e3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e02e3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e02e3-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_SDVirtualDesktopServer_Prov"), AMENDMENT]
class Win32_SessionDirectoryVirtualDesktopServer
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="e02e3-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e02e3-109">Members</span></span>

<span data-ttu-id="e02e3-110">Класс **Win32 \_ сессиондиректоривиртуалдесктопсервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e02e3-110">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these types of members:</span></span>

-   [<span data-ttu-id="e02e3-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e02e3-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e02e3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e02e3-112">Properties</span></span>

<span data-ttu-id="e02e3-113">Класс **Win32 \_ сессиондиректоривиртуалдесктопсервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e02e3-113">The **Win32\_SessionDirectoryVirtualDesktopServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e02e3-114">**Name**</span><span class="sxs-lookup"><span data-stu-id="e02e3-114">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e02e3-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e02e3-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e02e3-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e02e3-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e02e3-117">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e02e3-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e02e3-118">DNS-имя сервера узла виртуализации удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e02e3-118">The DNS name of the RD Virtualization Host server.</span></span> <span data-ttu-id="e02e3-119">Это имя имеет вид "*MachineName*. *Domain*. com ".</span><span class="sxs-lookup"><span data-stu-id="e02e3-119">This name takes the form "*MachineName*.*Domain*.com".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e02e3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e02e3-120">Requirements</span></span>



| <span data-ttu-id="e02e3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e02e3-121">Requirement</span></span> | <span data-ttu-id="e02e3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e02e3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e02e3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e02e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e02e3-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e02e3-124">None supported</span></span><br/>                                                              |
| <span data-ttu-id="e02e3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e02e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e02e3-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e02e3-126">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="e02e3-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e02e3-127">Namespace</span></span><br/>                | <span data-ttu-id="e02e3-128">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="e02e3-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="e02e3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e02e3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e02e3-130"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e02e3-130"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e02e3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e02e3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e02e3-132"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e02e3-132"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

