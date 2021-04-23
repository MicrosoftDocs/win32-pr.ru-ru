---
title: Метод Сетсбдбконнектионстрингс класса Win32_SessionBrokerServiceProperties
description: Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.
ms.assetid: a9a20eca-22d9-495c-b976-2952c97be67e
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсбдбконнектионстрингс
- Службы удаленных рабочих столов метода Сетсбдбконнектионстрингс, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Сетсбдбконнектионстрингс
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.SetSBDbConnectionStrings
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4aa02cabe89e434fb8b24b308bbe2ec51fa5f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490578"
---
# <a name="setsbdbconnectionstrings-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="0bf42-106">Метод Сетсбдбконнектионстрингс \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="0bf42-106">SetSBDbConnectionStrings method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="0bf42-107">Сохраняет строки подключения к базе данных (первичные и вторичные) в реестре.</span><span class="sxs-lookup"><span data-stu-id="0bf42-107">Saves DB connection strings, both primary and secondary, in the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="0bf42-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0bf42-108">Syntax</span></span>


```mof
uint32 SetSBDbConnectionStrings(
  [in] string connStringToCentralDBRdcms,
  [in] string secondaryConnStringToCentralDBRdcms
);
```



## <a name="parameters"></a><span data-ttu-id="0bf42-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bf42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bf42-110">*коннстрингтоцентралдбрдкмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf42-110">*connStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf42-111">Основная строка подключения.</span><span class="sxs-lookup"><span data-stu-id="0bf42-111">The primary connection string.</span></span>

</dd> <dt>

<span data-ttu-id="0bf42-112">*секондариконнстрингтоцентралдбрдкмс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0bf42-112">*secondaryConnStringToCentralDBRdcms* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bf42-113">Вторичная строка подключения.</span><span class="sxs-lookup"><span data-stu-id="0bf42-113">The secondary connection string.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0bf42-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0bf42-114">Requirements</span></span>



| <span data-ttu-id="0bf42-115">Требование</span><span class="sxs-lookup"><span data-stu-id="0bf42-115">Requirement</span></span> | <span data-ttu-id="0bf42-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0bf42-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0bf42-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bf42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0bf42-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0bf42-118">None supported</span></span><br/>                                                              |
| <span data-ttu-id="0bf42-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bf42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0bf42-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0bf42-120">Windows Server 2016</span></span><br/>                                                         |
| <span data-ttu-id="0bf42-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0bf42-121">Namespace</span></span><br/>                | <span data-ttu-id="0bf42-122">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="0bf42-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="0bf42-123">MOF</span><span class="sxs-lookup"><span data-stu-id="0bf42-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0bf42-124"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0bf42-124"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0bf42-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0bf42-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0bf42-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0bf42-126"><dt>RDMS.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0bf42-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bf42-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bf42-128">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="0bf42-128">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





