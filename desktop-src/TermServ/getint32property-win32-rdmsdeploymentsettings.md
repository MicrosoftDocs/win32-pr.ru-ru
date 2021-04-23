---
title: Метод GetInt32Property класса Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681944"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="73bf7-106">Метод GetInt32Property \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="73bf7-106">GetInt32Property method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="73bf7-107">Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="73bf7-107">Retrieves an integer property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="73bf7-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73bf7-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="73bf7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="73bf7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73bf7-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="73bf7-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="73bf7-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="73bf7-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73bf7-113">Целое число, получающее полученное значение.</span><span class="sxs-lookup"><span data-stu-id="73bf7-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="73bf7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73bf7-114">Requirements</span></span>



| <span data-ttu-id="73bf7-115">Требование</span><span class="sxs-lookup"><span data-stu-id="73bf7-115">Requirement</span></span> | <span data-ttu-id="73bf7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73bf7-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73bf7-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="73bf7-117">Minimum supported client</span></span><br/> | <span data-ttu-id="73bf7-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="73bf7-118">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="73bf7-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="73bf7-119">Minimum supported server</span></span><br/> | <span data-ttu-id="73bf7-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73bf7-120">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="73bf7-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="73bf7-121">Namespace</span></span><br/>                | <span data-ttu-id="73bf7-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="73bf7-122">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="73bf7-123">Header</span><span class="sxs-lookup"><span data-stu-id="73bf7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="73bf7-124"><dt>Microsoft. Diagnostics. аппаналисис. h</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-124"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="73bf7-125">MOF</span><span class="sxs-lookup"><span data-stu-id="73bf7-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73bf7-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-126"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="73bf7-127">DLL</span><span class="sxs-lookup"><span data-stu-id="73bf7-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73bf7-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73bf7-128"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="73bf7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73bf7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73bf7-130">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="73bf7-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





