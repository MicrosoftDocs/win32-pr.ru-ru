---
title: Метод Сетсекондариконнектионстринг класса Win32_RDMSDeploymentSettings
description: Задает вторичную строку подключения базы данных уровня развертывания.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекондариконнектионстринг
- Службы удаленных рабочих столов метода Сетсекондариконнектионстринг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетсекондариконнектионстринг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f8060a6f2676b5599bf44672e79ebf48e64e354
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801978"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="3e944-106">Метод Сетсекондариконнектионстринг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="3e944-106">SetSecondaryConnectionString method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="3e944-107">Задает вторичную строку подключения базы данных уровня развертывания.</span><span class="sxs-lookup"><span data-stu-id="3e944-107">Sets the deployment level database secondary connection string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e944-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e944-108">Syntax</span></span>


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a><span data-ttu-id="3e944-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e944-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e944-110">*Секондариконнектионстринг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="3e944-110">*SecondaryConnectionString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e944-111">Строка подключения для установки</span><span class="sxs-lookup"><span data-stu-id="3e944-111">The connection string to set</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e944-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3e944-112">Return value</span></span>

<span data-ttu-id="3e944-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="3e944-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e944-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3e944-114">Requirements</span></span>



| <span data-ttu-id="3e944-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3e944-115">Requirement</span></span> | <span data-ttu-id="3e944-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e944-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e944-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e944-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e944-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3e944-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="3e944-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e944-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e944-120">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="3e944-120">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="3e944-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3e944-121">Namespace</span></span><br/>                | <span data-ttu-id="3e944-122">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="3e944-122">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="3e944-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3e944-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e944-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e944-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e944-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e944-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e944-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e944-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="3e944-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e944-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e944-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="3e944-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





