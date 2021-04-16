---
title: Метод Сетекспортпас класса Win32_RDMSDeploymentSettings
description: Обновляет путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.
ms.assetid: e52b79c8-6724-4264-93d5-4a2a14c89b6b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетекспортпас
- Службы удаленных рабочих столов метода Сетекспортпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетекспортпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetExportPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32dbc844aecf86d4c62fada6c5cd68d514a69272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672635"
---
# <a name="setexportpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c3778-106">Метод Сетекспортпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="c3778-106">SetExportPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c3778-107">Обновляет путь к каталогу, в котором развернуты виртуальные машины для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c3778-107">Updates the directory path to which virtual machines are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3778-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3778-108">Syntax</span></span>


```mof
uint32 SetExportPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="c3778-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c3778-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3778-110">*DirectoryPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c3778-110">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3778-111">Новый путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="c3778-111">The new directory path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3778-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c3778-112">Return value</span></span>

<span data-ttu-id="c3778-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c3778-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3778-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c3778-114">Requirements</span></span>



| <span data-ttu-id="c3778-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c3778-115">Requirement</span></span> | <span data-ttu-id="c3778-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c3778-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3778-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3778-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c3778-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3778-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c3778-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3778-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c3778-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c3778-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c3778-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3778-121">Namespace</span></span><br/>                | <span data-ttu-id="c3778-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="c3778-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c3778-123">MOF</span><span class="sxs-lookup"><span data-stu-id="c3778-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3778-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3778-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3778-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c3778-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3778-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3778-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c3778-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3778-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3778-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="c3778-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





