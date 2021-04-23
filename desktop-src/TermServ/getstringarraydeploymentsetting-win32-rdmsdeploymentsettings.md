---
title: Метод Жетстрингаррайдеплойментсеттинг класса Win32_RDMSDeploymentSettings
description: Извлекает параметры развертывания для коллекции виртуальных рабочих столов.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингаррайдеплойментсеттинг
- Службы удаленных рабочих столов метода Жетстрингаррайдеплойментсеттинг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетстрингаррайдеплойментсеттинг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135403"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="e7146-106">Метод Жетстрингаррайдеплойментсеттинг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="e7146-106">GetStringArrayDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="e7146-107">Извлекает параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e7146-107">Retrieves the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7146-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7146-108">Syntax</span></span>


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
);
```



## <a name="parameters"></a><span data-ttu-id="e7146-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7146-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7146-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e7146-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e7146-111">The alias of the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="e7146-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e7146-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7146-113">Получает массив строк, содержащий параметры развертывания.</span><span class="sxs-lookup"><span data-stu-id="e7146-113">Receives an array of strings that contains the deployment settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e7146-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e7146-114">Requirements</span></span>



| <span data-ttu-id="e7146-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e7146-115">Requirement</span></span> | <span data-ttu-id="e7146-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e7146-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7146-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e7146-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7146-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e7146-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e7146-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e7146-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7146-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e7146-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e7146-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e7146-121">Namespace</span></span><br/>                | <span data-ttu-id="e7146-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="e7146-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e7146-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e7146-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e7146-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e7146-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e7146-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e7146-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7146-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7146-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e7146-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7146-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7146-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e7146-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





