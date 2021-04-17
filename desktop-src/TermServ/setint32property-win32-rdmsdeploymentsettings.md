---
title: Метод SetInt32Property класса Win32_RDMSDeploymentSettings
description: Обновляет целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.
ms.assetid: c5e6dbd5-7db7-4409-bf53-c2680e4a5319
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода SetInt32Property
- Службы удаленных рабочих столов метода SetInt32Property, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fecdc42031514d5219fc03172b951602ad021ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682071"
---
# <a name="setint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="cea54-106">Метод SetInt32Property \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="cea54-106">SetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="cea54-107">Обновляет целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cea54-107">Updates an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cea54-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cea54-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="cea54-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="cea54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea54-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cea54-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea54-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="cea54-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="cea54-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cea54-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cea54-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="cea54-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cea54-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cea54-114">Requirements</span></span>



| <span data-ttu-id="cea54-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cea54-115">Requirement</span></span> | <span data-ttu-id="cea54-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cea54-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea54-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cea54-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cea54-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="cea54-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="cea54-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cea54-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cea54-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cea54-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="cea54-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="cea54-121">Namespace</span></span><br/>                | <span data-ttu-id="cea54-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="cea54-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="cea54-123">MOF</span><span class="sxs-lookup"><span data-stu-id="cea54-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cea54-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cea54-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="cea54-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cea54-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cea54-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cea54-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="cea54-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cea54-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cea54-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="cea54-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





