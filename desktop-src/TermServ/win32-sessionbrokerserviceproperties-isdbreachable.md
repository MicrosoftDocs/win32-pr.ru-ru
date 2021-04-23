---
title: Метод Исдбреачабле класса Win32_SessionBrokerServiceProperties
description: Проверяет доступность базы данных.
ms.assetid: c9774d6d-1b78-4ec1-bae2-80d41d4c9b06
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Исдбреачабле
- Службы удаленных рабочих столов метода Исдбреачабле, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Исдбреачабле
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.IsDbReachable
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3a59b8b0eba80dd832b3967b5e626642684f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490581"
---
# <a name="isdbreachable-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="d08b8-106">Метод Исдбреачабле \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="d08b8-106">IsDbReachable method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="d08b8-107">Проверяет доступность базы данных.</span><span class="sxs-lookup"><span data-stu-id="d08b8-107">Checks if the database is reachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08b8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d08b8-108">Syntax</span></span>


```mof
uint32 IsDbReachable(
  [in] string connStringToDb,
  [in] string connSecondaryStringToDb,
  [in] string activeBrokerName
);
```



## <a name="parameters"></a><span data-ttu-id="d08b8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d08b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08b8-110">*коннстрингтодб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d08b8-110">*connStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b8-111">Строка подключения к базе данных.</span><span class="sxs-lookup"><span data-stu-id="d08b8-111">The connection string to the database.</span></span>

</dd> <dt>

<span data-ttu-id="d08b8-112">*коннсекондаристрингтодб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d08b8-112">*connSecondaryStringToDb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b8-113">Вторичная строка подключения к центральной базе данных.</span><span class="sxs-lookup"><span data-stu-id="d08b8-113">Secondary connection string to the central database.</span></span>

<span data-ttu-id="d08b8-114">**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d08b8-114">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> <dt>

<span data-ttu-id="d08b8-115">*активеброкернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d08b8-115">*activeBrokerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08b8-116">Имя активного брокера.</span><span class="sxs-lookup"><span data-stu-id="d08b8-116">Active broker name.</span></span>

<span data-ttu-id="d08b8-117">**Windows server 2012 R2 и Windows server 2012:** Этот параметр недоступен до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="d08b8-117">**Windows Server 2012 R2 and Windows Server 2012:** This parameter is not available before Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d08b8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="d08b8-118">Requirements</span></span>



| <span data-ttu-id="d08b8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="d08b8-119">Requirement</span></span> | <span data-ttu-id="d08b8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="d08b8-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08b8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d08b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="d08b8-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d08b8-122">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d08b8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d08b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="d08b8-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d08b8-124">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="d08b8-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d08b8-125">Namespace</span></span><br/>                | <span data-ttu-id="d08b8-126">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d08b8-126">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d08b8-127">MOF</span><span class="sxs-lookup"><span data-stu-id="d08b8-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d08b8-128"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d08b8-128"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d08b8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="d08b8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08b8-130"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d08b8-130"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d08b8-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d08b8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d08b8-132">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="d08b8-132">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





