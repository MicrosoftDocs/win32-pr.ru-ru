---
title: Метод Сетконнектионстринг класса Win32_RDMSDeploymentSettings
description: Задает строку подключения к базе данных на уровне развертывания.
ms.assetid: c8902ab9-72a6-4d69-ab22-f6074205deb4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетконнектионстринг
- Службы удаленных рабочих столов метода Сетконнектионстринг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетконнектионстринг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ccb3f618f6a08dcb95bb7dc04c1494be6a7b5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415321"
---
# <a name="setconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="e148e-106">Метод Сетконнектионстринг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="e148e-106">SetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="e148e-107">Задает строку подключения к базе данных на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="e148e-107">Sets the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e148e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e148e-108">Syntax</span></span>


```mof
uint32 SetConnectionString(
  [in] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="e148e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e148e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e148e-110">*Строка* \[ подключения окне\]</span><span class="sxs-lookup"><span data-stu-id="e148e-110">*ConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e148e-111">Строка подключения для установки</span><span class="sxs-lookup"><span data-stu-id="e148e-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e148e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e148e-112">Return value</span></span>

<span data-ttu-id="e148e-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e148e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e148e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e148e-114">Requirements</span></span>



| <span data-ttu-id="e148e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e148e-115">Requirement</span></span> | <span data-ttu-id="e148e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e148e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e148e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e148e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e148e-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e148e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e148e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e148e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e148e-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e148e-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="e148e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e148e-121">Namespace</span></span><br/>                | <span data-ttu-id="e148e-122">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="e148e-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e148e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e148e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e148e-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e148e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e148e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e148e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e148e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e148e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e148e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e148e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e148e-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e148e-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





