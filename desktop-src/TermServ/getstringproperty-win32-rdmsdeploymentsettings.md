---
title: Метод Жетстрингпроперти класса Win32_RDMSDeploymentSettings
description: Извлекает строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.
ms.assetid: 468ffdea-57a9-4478-adae-3629e4522762
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингпроперти
- Службы удаленных рабочих столов метода Жетстрингпроперти, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f26a570becbbae6b0d768c399acd3dd2954ecdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415201"
---
# <a name="getstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7a1b4-106">Метод Жетстрингпроперти \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="7a1b4-106">GetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7a1b4-107">Извлекает строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7a1b4-107">Retrieves a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1b4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a1b4-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="7a1b4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a1b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a1b4-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7a1b4-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1b4-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7a1b4-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="7a1b4-112">*Значение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a1b4-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a1b4-113">Строка, принимающая извлеченное значение.</span><span class="sxs-lookup"><span data-stu-id="7a1b4-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a1b4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7a1b4-114">Requirements</span></span>



| <span data-ttu-id="7a1b4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7a1b4-115">Requirement</span></span> | <span data-ttu-id="7a1b4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7a1b4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1b4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a1b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1b4-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7a1b4-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7a1b4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a1b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1b4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a1b4-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7a1b4-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a1b4-121">Namespace</span></span><br/>                | <span data-ttu-id="7a1b4-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="7a1b4-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7a1b4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7a1b4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a1b4-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a1b4-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a1b4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1b4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a1b4-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1b4-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7a1b4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a1b4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1b4-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="7a1b4-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





