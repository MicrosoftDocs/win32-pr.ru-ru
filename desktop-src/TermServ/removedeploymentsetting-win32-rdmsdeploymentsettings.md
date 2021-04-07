---
title: Метод Ремоведеплойментсеттинг класса Win32_RDMSDeploymentSettings
description: Удаляет параметры развертывания для коллекции виртуальных рабочих столов.
ms.assetid: 68e102a3-8f3f-4997-bdf0-c2ae3640ed42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремоведеплойментсеттинг
- Службы удаленных рабочих столов метода Ремоведеплойментсеттинг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Ремоведеплойментсеттинг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.RemoveDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 336b93f86d6b96074341dde4851813b26eb66fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892658"
---
# <a name="removedeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="0058a-106">Метод Ремоведеплойментсеттинг \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="0058a-106">RemoveDeploymentSetting method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="0058a-107">Удаляет параметры развертывания для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0058a-107">Deletes the deployment settings for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="0058a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0058a-108">Syntax</span></span>


```mof
uint32 RemoveDeploymentSetting(
  [in] string Key
);
```



## <a name="parameters"></a><span data-ttu-id="0058a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0058a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0058a-110">*Ключ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0058a-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0058a-111">Псевдоним коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="0058a-111">The alias of the virtual desktop collection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0058a-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0058a-112">Requirements</span></span>



| <span data-ttu-id="0058a-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0058a-113">Requirement</span></span> | <span data-ttu-id="0058a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0058a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0058a-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0058a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0058a-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0058a-116">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="0058a-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0058a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0058a-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0058a-118">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="0058a-119">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0058a-119">Namespace</span></span><br/>                | <span data-ttu-id="0058a-120">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="0058a-120">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="0058a-121">MOF</span><span class="sxs-lookup"><span data-stu-id="0058a-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0058a-122"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0058a-122"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="0058a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="0058a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0058a-124"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0058a-124"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="0058a-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0058a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0058a-126">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="0058a-126">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





