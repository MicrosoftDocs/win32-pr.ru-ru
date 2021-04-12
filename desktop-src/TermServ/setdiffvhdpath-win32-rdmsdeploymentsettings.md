---
title: Метод Сетдиффвхдпас класса Win32_RDMSDeploymentSettings
description: Обновляет путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.
ms.assetid: 665ffbf9-0250-4956-9bce-f5a6714b47e4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетдиффвхдпас
- Службы удаленных рабочих столов метода Сетдиффвхдпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетдиффвхдпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e52d206c9e0cbff19f26e38a2a02f04ea0acc03d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415436"
---
# <a name="setdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="e6379-106">Метод Сетдиффвхдпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="e6379-106">SetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="e6379-107">Обновляет путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e6379-107">Updates the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6379-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6379-108">Syntax</span></span>


```mof
uint32 SetDiffVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="e6379-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6379-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6379-110">*DirectoryPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6379-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6379-111">Новый путь к разностному диску.</span><span class="sxs-lookup"><span data-stu-id="e6379-111">The new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6379-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6379-112">Return value</span></span>

<span data-ttu-id="e6379-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e6379-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6379-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e6379-114">Requirements</span></span>



| <span data-ttu-id="e6379-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e6379-115">Requirement</span></span> | <span data-ttu-id="e6379-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e6379-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6379-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6379-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e6379-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e6379-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e6379-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6379-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e6379-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e6379-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="e6379-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e6379-121">Namespace</span></span><br/>                | <span data-ttu-id="e6379-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="e6379-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e6379-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e6379-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6379-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e6379-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6379-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e6379-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6379-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6379-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e6379-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6379-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6379-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="e6379-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





