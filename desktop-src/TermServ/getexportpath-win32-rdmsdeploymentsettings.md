---
title: Метод Жетекспортпас класса Win32_RDMSDeploymentSettings
description: Извлекает путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.
ms.assetid: 8df79e31-b960-46ae-b49c-8052b356e1a8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетекспортпас
- Службы удаленных рабочих столов метода Жетекспортпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетекспортпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baf96d1d71554f1b8ea310759d36d0918a511cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672510"
---
# <a name="getexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="7a00e-106">Метод Жетекспортпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="7a00e-106">GetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="7a00e-107">Извлекает путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="7a00e-107">Retrieves the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a00e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a00e-108">Syntax</span></span>


```mof
uint32 GetExportPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="7a00e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7a00e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a00e-110">*DirectoryPath* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7a00e-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7a00e-111">Получает путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="7a00e-111">Receives the directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a00e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7a00e-112">Return value</span></span>

<span data-ttu-id="7a00e-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="7a00e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a00e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7a00e-114">Requirements</span></span>



| <span data-ttu-id="7a00e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7a00e-115">Requirement</span></span> | <span data-ttu-id="7a00e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7a00e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a00e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a00e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7a00e-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7a00e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="7a00e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a00e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7a00e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7a00e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="7a00e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a00e-121">Namespace</span></span><br/>                | <span data-ttu-id="7a00e-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="7a00e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="7a00e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="7a00e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a00e-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a00e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a00e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7a00e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a00e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a00e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="7a00e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a00e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a00e-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="7a00e-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





