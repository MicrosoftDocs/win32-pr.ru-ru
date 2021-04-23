---
title: Класс Win32_TSGatewayServer
description: Используется для конкретных операций сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSGatewayServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSGatewayServer, описание
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490275"
---
# <a name="win32_tsgatewayserver-class"></a><span data-ttu-id="55b05-105">\_Класс Win32 тсгатевайсервер</span><span class="sxs-lookup"><span data-stu-id="55b05-105">Win32\_TSGatewayServer class</span></span>

<span data-ttu-id="55b05-106">Используется для конкретных операций сервера шлюза удаленный рабочий стол (шлюз удаленных рабочих столов).</span><span class="sxs-lookup"><span data-stu-id="55b05-106">Used for Remote Desktop Gateway (RD Gateway) server-specific operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b05-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55b05-107">Syntax</span></span>

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a><span data-ttu-id="55b05-108">Члены</span><span class="sxs-lookup"><span data-stu-id="55b05-108">Members</span></span>

<span data-ttu-id="55b05-109">Класс **Win32 \_ тсгатевайсервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55b05-109">The **Win32\_TSGatewayServer** class has these types of members:</span></span>

-   [<span data-ttu-id="55b05-110">Методы</span><span class="sxs-lookup"><span data-stu-id="55b05-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55b05-111">Методы</span><span class="sxs-lookup"><span data-stu-id="55b05-111">Methods</span></span>

<span data-ttu-id="55b05-112">Класс **Win32 \_ тсгатевайсервер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="55b05-112">The **Win32\_TSGatewayServer** class has these methods.</span></span>



| <span data-ttu-id="55b05-113">Метод</span><span class="sxs-lookup"><span data-stu-id="55b05-113">Method</span></span>                                                                                   | <span data-ttu-id="55b05-114">Описание</span><span class="sxs-lookup"><span data-stu-id="55b05-114">Description</span></span>                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55b05-115">**креатеселфсигнедцертификате**</span><span class="sxs-lookup"><span data-stu-id="55b05-115">**CreateSelfSignedCertificate**</span></span>](createselfsignedcertificate-win32-tsgatewayserver.md) | <span data-ttu-id="55b05-116">Создает самозаверяющий сертификат с указанным именем субъекта и возвращает хэш сертификата как параметр "out".</span><span class="sxs-lookup"><span data-stu-id="55b05-116">Creates a self-signed certificate with a given subject name and returns the certificate hash as an "out" parameter.</span></span><br/> |
| [<span data-ttu-id="55b05-117">**Экспорт**</span><span class="sxs-lookup"><span data-stu-id="55b05-117">**Export**</span></span>](export-win32-tsgatewayserver.md)                                           | <span data-ttu-id="55b05-118">Возвращает конфигурацию сервера шлюза удаленных рабочих столов в виде XML-строки.</span><span class="sxs-lookup"><span data-stu-id="55b05-118">Returns the RD Gateway server configuration as an XML string.</span></span><br/>                                                       |
| [<span data-ttu-id="55b05-119">**Импорт**</span><span class="sxs-lookup"><span data-stu-id="55b05-119">**Import**</span></span>](import-win32-tsgatewayserver.md)                                           | <span data-ttu-id="55b05-120">Импортирует заданную конфигурацию на сервер шлюза удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="55b05-120">Imports a given configuration to the RD Gateway server.</span></span><br/>                                                             |



 

## <a name="remarks"></a><span data-ttu-id="55b05-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55b05-121">Remarks</span></span>

<span data-ttu-id="55b05-122">Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="55b05-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="55b05-123">MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK).</span><span class="sxs-lookup"><span data-stu-id="55b05-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="55b05-124">Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера.</span><span class="sxs-lookup"><span data-stu-id="55b05-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="55b05-125">Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="55b05-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="55b05-126">Требования</span><span class="sxs-lookup"><span data-stu-id="55b05-126">Requirements</span></span>



| <span data-ttu-id="55b05-127">Требование</span><span class="sxs-lookup"><span data-stu-id="55b05-127">Requirement</span></span> | <span data-ttu-id="55b05-128">Значение</span><span class="sxs-lookup"><span data-stu-id="55b05-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b05-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55b05-129">Minimum supported client</span></span><br/> | <span data-ttu-id="55b05-130">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="55b05-130">None supported</span></span><br/>                                                                |
| <span data-ttu-id="55b05-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55b05-131">Minimum supported server</span></span><br/> | <span data-ttu-id="55b05-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55b05-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="55b05-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="55b05-133">Namespace</span></span><br/>                | <span data-ttu-id="55b05-134">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="55b05-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="55b05-135">MOF</span><span class="sxs-lookup"><span data-stu-id="55b05-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b05-136"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b05-136"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="55b05-137">DLL</span><span class="sxs-lookup"><span data-stu-id="55b05-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b05-138"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b05-138"><dt>AagWmi.dll</dt></span></span> </dl>    |



 

