---
title: Метод Инсталлброкердатабасе класса Win32_SessionBrokerServiceProperties
description: Устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном сервере SQL Server.
ms.assetid: 9cc6fa4a-f1eb-49eb-bec4-acaff73190e8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Инсталлброкердатабасе
- Службы удаленных рабочих столов метода Инсталлброкердатабасе, класс Win32_SessionBrokerServiceProperties
- Класс Win32_SessionBrokerServiceProperties службы удаленных рабочих столов, метод Инсталлброкердатабасе
topic_type:
- apiref
api_name:
- Win32_SessionBrokerServiceProperties.InstallBrokerDatabase
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da560bd4746c41864b3c56438f841efebe71ecd7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801300"
---
# <a name="installbrokerdatabase-method-of-the-win32_sessionbrokerserviceproperties-class"></a><span data-ttu-id="6d886-106">Метод Инсталлброкердатабасе \_ класса Win32 сессионброкерсервицепропертиес</span><span class="sxs-lookup"><span data-stu-id="6d886-106">InstallBrokerDatabase method of the Win32\_SessionBrokerServiceProperties class</span></span>

<span data-ttu-id="6d886-107">Устанавливает базу данных посредника подключений к удаленному рабочему столу на центральном сервере SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6d886-107">Installs an RD connection broker database on a central SQL server.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d886-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d886-108">Syntax</span></span>


```mof
uint32 InstallBrokerDatabase(
  [in] string newDbFilePath,
  [in] string connStringToCentralDBMaster,
  [in] string centralRdcmsDbName
);
```



## <a name="parameters"></a><span data-ttu-id="6d886-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d886-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d886-110">*невдбфилепас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d886-110">*newDbFilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d886-111">путь к файлу новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="6d886-111">new database file path.</span></span>

</dd> <dt>

<span data-ttu-id="6d886-112">*коннстрингтоцентралдбмастер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d886-112">*connStringToCentralDBMaster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d886-113">Строка подключения к главному хозяину базы данных.</span><span class="sxs-lookup"><span data-stu-id="6d886-113">Connection string to the central database master.</span></span>

</dd> <dt>

<span data-ttu-id="6d886-114">*централрдкмсдбнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6d886-114">*centralRdcmsDbName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d886-115">Имя центральной базы данных.</span><span class="sxs-lookup"><span data-stu-id="6d886-115">Name of the central database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d886-116">Требования</span><span class="sxs-lookup"><span data-stu-id="6d886-116">Requirements</span></span>



| <span data-ttu-id="6d886-117">Требование</span><span class="sxs-lookup"><span data-stu-id="6d886-117">Requirement</span></span> | <span data-ttu-id="6d886-118">Значение</span><span class="sxs-lookup"><span data-stu-id="6d886-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d886-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6d886-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6d886-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6d886-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6d886-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6d886-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6d886-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6d886-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="6d886-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d886-123">Namespace</span></span><br/>                | <span data-ttu-id="6d886-124">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="6d886-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="6d886-125">MOF</span><span class="sxs-lookup"><span data-stu-id="6d886-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6d886-126"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6d886-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="6d886-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6d886-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d886-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d886-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d886-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d886-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d886-130">**\_Сессионброкерсервицепропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="6d886-130">**Win32\_SessionBrokerServiceProperties**</span></span>](win32-sessionbrokerserviceproperties.md)
</dt> </dl>

 

 





