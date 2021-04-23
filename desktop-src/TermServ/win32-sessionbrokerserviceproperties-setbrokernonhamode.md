---
title: Метод Сетброкернонхамоде класса Win32_SessionBrokerServiceProperties
description: Переносит данные из центрального SQL Server в локальную базу данных. Он также настраивает сервер брокера для использования локальной базы данных.
ms.assetid: a73908be-0cc8-4512-842c-439d5cf18ed4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетброкернонхамоде
- Службы удаленных рабочих столов метода Сетброкернонхамоде, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетброкернонхамоде
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetBrokerNonHAMode
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ef811bf8024f8e89f9739461dfa8499891077f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681881"
---
# <a name="setbrokernonhamode-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="84706-107">Метод Сетброкернонхамоде \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="84706-107">SetBrokerNonHAMode method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="84706-108">Переносит данные из центрального SQL Server в локальную базу данных.</span><span class="sxs-lookup"><span data-stu-id="84706-108">Migrates data from central SQL Server to a local database.</span></span> <span data-ttu-id="84706-109">Он также настраивает сервер брокера для использования локальной базы данных.</span><span class="sxs-lookup"><span data-stu-id="84706-109">It also configures the broker server to use the local database.</span></span>

## <a name="syntax"></a><span data-ttu-id="84706-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84706-110">Syntax</span></span>


```mof
uint32 SetBrokerNonHAMode(
  [in] string connStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="84706-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="84706-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84706-112">*коннстрингтоцентралдбрдкмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="84706-112">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84706-113">Строка подключения к центральной базе данных.</span><span class="sxs-lookup"><span data-stu-id="84706-113">Connection string to the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="84706-114">Требования</span><span class="sxs-lookup"><span data-stu-id="84706-114">Requirements</span></span>



| <span data-ttu-id="84706-115">Требование</span><span class="sxs-lookup"><span data-stu-id="84706-115">Requirement</span></span> | <span data-ttu-id="84706-116">Значение</span><span class="sxs-lookup"><span data-stu-id="84706-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84706-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="84706-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84706-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="84706-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="84706-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="84706-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84706-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="84706-120">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="84706-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="84706-121">Namespace</span></span><br/>                | <span data-ttu-id="84706-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="84706-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="84706-123">MOF</span><span class="sxs-lookup"><span data-stu-id="84706-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84706-124"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="84706-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="84706-125">DLL</span><span class="sxs-lookup"><span data-stu-id="84706-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84706-126"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84706-126"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84706-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="84706-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84706-128">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="84706-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





