---
title: Метод Сетстрингаррайдеплойментсеттинг класса Win32_RDMSDeploymentSettings
description: Обновляет параметры развертывания для коллекции виртуальных рабочих столов.
ms.assetid: 386594bd-a793-4e5d-ad2c-217951bee9f6
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетстрингаррайдеплойментсеттинг
- Службы удаленных рабочих столов метода Сетстрингаррайдеплойментсеттинг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетстрингаррайдеплойментсеттинг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb5ecc6d1238b739f8fe19d02e96ba427ed09b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803767"
---
# <a name="setstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="fa6d4-106">Метод Сетстрингаррайдеплойментсеттинг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="fa6d4-106">SetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="fa6d4-107">Обновляет параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fa6d4-107">Updates the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa6d4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fa6d4-108">Syntax</span></span>


```mof
uint32 SetStringArrayDeploymentSetting(
  [in] string Key,
  [in] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="fa6d4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa6d4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa6d4-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa6d4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6d4-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="fa6d4-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="fa6d4-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fa6d4-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa6d4-113">Массив строк, содержащий новые параметры развертывания.</span><span class="sxs-lookup"><span data-stu-id="fa6d4-113">An array of strings that contains the new deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa6d4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fa6d4-114">Requirements</span></span>



| <span data-ttu-id="fa6d4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fa6d4-115">Requirement</span></span> | <span data-ttu-id="fa6d4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fa6d4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa6d4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fa6d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fa6d4-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fa6d4-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="fa6d4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fa6d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fa6d4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fa6d4-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="fa6d4-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fa6d4-121">Namespace</span></span><br/>                | <span data-ttu-id="fa6d4-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="fa6d4-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="fa6d4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fa6d4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fa6d4-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fa6d4-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="fa6d4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fa6d4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fa6d4-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa6d4-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="fa6d4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fa6d4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa6d4-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="fa6d4-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





