---
title: Метод Делетесбдбконнектионстринг класса Win32_SessionBrokerServiceProperties
description: Удаляет строки подключения к базе данных (первичной или вторичной) из реестра.
ms.assetid: 275dd790-bdc7-46d1-a07d-54ec6fa33e44
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Делетесбдбконнектионстринг
- Службы удаленных рабочих столов метода Делетесбдбконнектионстринг, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Делетесбдбконнектионстринг
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.DeleteSBDbConnectionString
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2a9701afebe150f0c8dc0e4bf437dd23586c3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672655"
---
# <a name="deletesbdbconnectionstring-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="463a6-106">Метод Делетесбдбконнектионстринг \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="463a6-106">DeleteSBDbConnectionString method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="463a6-107">Удаляет строки подключения к базе данных (первичной или вторичной) из реестра.</span><span class="sxs-lookup"><span data-stu-id="463a6-107">Deletes DB connection strings (primary or secondary) from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="463a6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="463a6-108">Syntax</span></span>


```mof
uint32 DeleteSBDbConnectionString(
  [in] boolean IsSecondaryConnString
);
```



## <a name="parameters"></a><span data-ttu-id="463a6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="463a6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="463a6-110">*Иссекондариконнстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="463a6-110">*IsSecondaryConnString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="463a6-111">Если **значение — true**, вторичная строка подключения удаляется.</span><span class="sxs-lookup"><span data-stu-id="463a6-111">If **True**, secondary connection string is removed.</span></span> <span data-ttu-id="463a6-112">Если **значение равно false**, то основная строка подключения удаляется.</span><span class="sxs-lookup"><span data-stu-id="463a6-112">If **False**, primary connection string is removed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="463a6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="463a6-113">Requirements</span></span>



| <span data-ttu-id="463a6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="463a6-114">Requirement</span></span> | <span data-ttu-id="463a6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="463a6-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="463a6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="463a6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="463a6-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="463a6-117">None supported</span></span><br/>                                                              |
| <span data-ttu-id="463a6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="463a6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="463a6-119">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="463a6-119">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="463a6-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="463a6-120">Namespace</span></span><br/>                | <span data-ttu-id="463a6-121">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="463a6-121">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="463a6-122">MOF</span><span class="sxs-lookup"><span data-stu-id="463a6-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="463a6-123"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="463a6-123"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="463a6-124">DLL</span><span class="sxs-lookup"><span data-stu-id="463a6-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="463a6-125"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="463a6-125"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="463a6-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="463a6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="463a6-127">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="463a6-127">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





