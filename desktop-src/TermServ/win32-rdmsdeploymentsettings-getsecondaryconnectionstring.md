---
title: Метод Жетсекондариконнектионстринг класса Win32_RDMSDeploymentSettings
description: Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетсекондариконнектионстринг
- Службы удаленных рабочих столов метода Жетсекондариконнектионстринг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетсекондариконнектионстринг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340640"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="a77d7-106">Метод Жетсекондариконнектионстринг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="a77d7-106">GetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="a77d7-107">Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.</span><span class="sxs-lookup"><span data-stu-id="a77d7-107">Retrieves the deployment-level database secondary connection string, which may be used to support password expiration.</span></span>

## <a name="syntax"></a><span data-ttu-id="a77d7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a77d7-108">Syntax</span></span>


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="a77d7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a77d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a77d7-110">*Секондариконнектионстринг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="a77d7-110">*SecondaryConnectionString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a77d7-111">Строка подключения для извлечения</span><span class="sxs-lookup"><span data-stu-id="a77d7-111">The connection string to retrieve</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a77d7-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a77d7-112">Return value</span></span>

<span data-ttu-id="a77d7-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a77d7-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a77d7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a77d7-114">Requirements</span></span>



| <span data-ttu-id="a77d7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="a77d7-115">Requirement</span></span> | <span data-ttu-id="a77d7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a77d7-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a77d7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a77d7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a77d7-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a77d7-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="a77d7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a77d7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a77d7-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="a77d7-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="a77d7-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a77d7-121">Namespace</span></span><br/>                | <span data-ttu-id="a77d7-122">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="a77d7-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="a77d7-123">MOF</span><span class="sxs-lookup"><span data-stu-id="a77d7-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a77d7-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a77d7-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="a77d7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a77d7-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a77d7-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a77d7-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="a77d7-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a77d7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a77d7-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="a77d7-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





