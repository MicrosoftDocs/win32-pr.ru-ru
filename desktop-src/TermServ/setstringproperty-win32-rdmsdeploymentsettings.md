---
title: Метод Сетстрингпроперти класса Win32_RDMSDeploymentSettings (Цертенролл. h)
description: Обновляет строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.
ms.assetid: 500ab1cb-7336-47a8-adee-790976ea30fe
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетстрингпроперти
- Службы удаленных рабочих столов метода Сетстрингпроперти, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетстрингпроперти
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 138f6d91ed428caabf8da69e3d958675f879dd15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136515"
---
# <a name="setstringproperty-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="60b42-106">Метод Сетстрингпроперти \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="60b42-106">SetStringProperty method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="60b42-107">Обновляет строковое свойство для параметров развертывания коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="60b42-107">Updates a string property for the deployment settings of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60b42-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60b42-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="60b42-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="60b42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b42-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60b42-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b42-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="60b42-111">The alias to the virtual desktop collection.</span></span>

</dd> <dt>

<span data-ttu-id="60b42-112">*Значение* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60b42-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b42-113">Новое значение свойства.</span><span class="sxs-lookup"><span data-stu-id="60b42-113">The new property value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="60b42-114">Требования</span><span class="sxs-lookup"><span data-stu-id="60b42-114">Requirements</span></span>



| <span data-ttu-id="60b42-115">Требование</span><span class="sxs-lookup"><span data-stu-id="60b42-115">Requirement</span></span> | <span data-ttu-id="60b42-116">Значение</span><span class="sxs-lookup"><span data-stu-id="60b42-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="60b42-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="60b42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="60b42-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="60b42-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="60b42-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="60b42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="60b42-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="60b42-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="60b42-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="60b42-121">Namespace</span></span><br/>                | <span data-ttu-id="60b42-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="60b42-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="60b42-123">Header</span><span class="sxs-lookup"><span data-stu-id="60b42-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="60b42-124"><dt>Цертенролл. h</dt></span><span class="sxs-lookup"><span data-stu-id="60b42-124"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="60b42-125">MOF</span><span class="sxs-lookup"><span data-stu-id="60b42-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b42-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b42-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b42-127">DLL</span><span class="sxs-lookup"><span data-stu-id="60b42-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b42-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b42-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="60b42-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60b42-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b42-130">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="60b42-130">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





