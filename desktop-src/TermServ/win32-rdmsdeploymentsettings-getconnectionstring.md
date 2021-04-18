---
title: Метод ConnectionString класса Win32_RDMSDeploymentSettings
description: Извлекает строку подключения к базе данных на уровне развертывания.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Метод ConnectionString службы удаленных рабочих столов
- Метод ConnectionString службы удаленных рабочих столов, Win32_RDMSDeploymentSettings класс
- Win32_RDMSDeploymentSettings класса службы удаленных рабочих столов, метод ConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490974"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="82e25-106">Метод ConnectionString \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="82e25-106">GetConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="82e25-107">Извлекает строку подключения к базе данных на уровне развертывания.</span><span class="sxs-lookup"><span data-stu-id="82e25-107">Retrieves the deployment-level database connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="82e25-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="82e25-108">Syntax</span></span>


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="82e25-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="82e25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82e25-110">*Строка* \[ подключения заполняет\]</span><span class="sxs-lookup"><span data-stu-id="82e25-110">*ConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82e25-111">Строка подключения</span><span class="sxs-lookup"><span data-stu-id="82e25-111">The connection string</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82e25-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82e25-112">Return value</span></span>

<span data-ttu-id="82e25-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="82e25-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="82e25-114">Требования</span><span class="sxs-lookup"><span data-stu-id="82e25-114">Requirements</span></span>



| <span data-ttu-id="82e25-115">Требование</span><span class="sxs-lookup"><span data-stu-id="82e25-115">Requirement</span></span> | <span data-ttu-id="82e25-116">Значение</span><span class="sxs-lookup"><span data-stu-id="82e25-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="82e25-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82e25-117">Minimum supported client</span></span><br/> | <span data-ttu-id="82e25-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="82e25-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="82e25-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82e25-119">Minimum supported server</span></span><br/> | <span data-ttu-id="82e25-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="82e25-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="82e25-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="82e25-121">Namespace</span></span><br/>                | <span data-ttu-id="82e25-122">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="82e25-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="82e25-123">MOF</span><span class="sxs-lookup"><span data-stu-id="82e25-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82e25-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="82e25-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="82e25-125">DLL</span><span class="sxs-lookup"><span data-stu-id="82e25-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82e25-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82e25-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="82e25-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82e25-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82e25-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="82e25-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





