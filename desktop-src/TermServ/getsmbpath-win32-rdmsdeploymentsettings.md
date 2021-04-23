---
title: Метод Жетсмбпас класса Win32_RDMSDeploymentSettings
description: Возвращает UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.
ms.assetid: 0a5d3c11-6a77-48f7-a3ea-6f82725ff01f
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетсмбпас
- Службы удаленных рабочих столов метода Жетсмбпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетсмбпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa1738faf82a6405018495dd762ba9585daa3e1b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104416165"
---
# <a name="getsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="6366e-106">Метод Жетсмбпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="6366e-106">GetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="6366e-107">Возвращает UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="6366e-107">Retrieves the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6366e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6366e-108">Syntax</span></span>


```mof
uint32 GetSMBPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="6366e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6366e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6366e-110">*DirectoryPath* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="6366e-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6366e-111">Получает путь в формате UNC к общему ресурсу SMB.</span><span class="sxs-lookup"><span data-stu-id="6366e-111">Receives a UNC formatted path to the SMB share.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6366e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6366e-112">Return value</span></span>

<span data-ttu-id="6366e-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="6366e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6366e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="6366e-114">Requirements</span></span>



| <span data-ttu-id="6366e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="6366e-115">Requirement</span></span> | <span data-ttu-id="6366e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="6366e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6366e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6366e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6366e-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6366e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6366e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6366e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6366e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6366e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="6366e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6366e-121">Namespace</span></span><br/>                | <span data-ttu-id="6366e-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="6366e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6366e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="6366e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6366e-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6366e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6366e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6366e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6366e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6366e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6366e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6366e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6366e-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="6366e-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





