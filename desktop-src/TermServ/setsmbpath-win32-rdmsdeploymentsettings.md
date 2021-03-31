---
title: Метод Сетсмбпас класса Win32_RDMSDeploymentSettings
description: Обновляет UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.
ms.assetid: 0b0b5b17-7b52-41e5-b9c6-c5f3e51c7853
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсмбпас
- Службы удаленных рабочих столов метода Сетсмбпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетсмбпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSMBPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d40598a3217ff1ca7c6082b3af09097352962309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988935"
---
# <a name="setsmbpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="78e0c-106">Метод Сетсмбпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="78e0c-106">SetSMBPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="78e0c-107">Обновляет UNC-путь к общему ресурсу SMB, в котором развернуты виртуальные машины коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="78e0c-107">Updates the UNC path to the SMB share to which virtual machines of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="78e0c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="78e0c-108">Syntax</span></span>


```mof
uint32 SetSMBPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="78e0c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="78e0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78e0c-110">*DirectoryPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="78e0c-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78e0c-111">Новый путь к общему ресурсу SMB в формате UNC.</span><span class="sxs-lookup"><span data-stu-id="78e0c-111">The new path to the SMB share, in UNC format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78e0c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="78e0c-112">Return value</span></span>

<span data-ttu-id="78e0c-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="78e0c-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="78e0c-114">Требования</span><span class="sxs-lookup"><span data-stu-id="78e0c-114">Requirements</span></span>



| <span data-ttu-id="78e0c-115">Требование</span><span class="sxs-lookup"><span data-stu-id="78e0c-115">Requirement</span></span> | <span data-ttu-id="78e0c-116">Значение</span><span class="sxs-lookup"><span data-stu-id="78e0c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="78e0c-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="78e0c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78e0c-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="78e0c-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="78e0c-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="78e0c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78e0c-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="78e0c-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="78e0c-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="78e0c-121">Namespace</span></span><br/>                | <span data-ttu-id="78e0c-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="78e0c-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="78e0c-123">MOF</span><span class="sxs-lookup"><span data-stu-id="78e0c-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78e0c-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78e0c-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="78e0c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="78e0c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78e0c-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78e0c-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="78e0c-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="78e0c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78e0c-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="78e0c-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





