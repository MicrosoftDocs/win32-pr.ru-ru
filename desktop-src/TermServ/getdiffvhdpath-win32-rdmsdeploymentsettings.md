---
title: Метод Жетдиффвхдпас класса Win32_RDMSDeploymentSettings
description: Возвращает путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.
ms.assetid: 4340c817-2276-48a1-a856-b4c9e91ea981
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетдиффвхдпас
- Службы удаленных рабочих столов метода Жетдиффвхдпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетдиффвхдпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetDiffVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7391315013cf8487d93b32f645933d14f06db2d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414929"
---
# <a name="getdiffvhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="5fdd4-106">Метод Жетдиффвхдпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="5fdd4-106">GetDiffVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="5fdd4-107">Возвращает путь к каталогу, в котором развернуты разностные диски для коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="5fdd4-107">Retrieves the directory path to which the differencing disks are deployed for a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fdd4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fdd4-108">Syntax</span></span>


```mof
uint32 GetDiffVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="5fdd4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fdd4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fdd4-110">*DirectoryPath* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="5fdd4-110">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fdd4-111">Получает новый путь разностного диска.</span><span class="sxs-lookup"><span data-stu-id="5fdd4-111">Receives the new differencing disk path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fdd4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5fdd4-112">Return value</span></span>

<span data-ttu-id="5fdd4-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="5fdd4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fdd4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="5fdd4-114">Requirements</span></span>



| <span data-ttu-id="5fdd4-115">Требование</span><span class="sxs-lookup"><span data-stu-id="5fdd4-115">Requirement</span></span> | <span data-ttu-id="5fdd4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="5fdd4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fdd4-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fdd4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5fdd4-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="5fdd4-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="5fdd4-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fdd4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5fdd4-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5fdd4-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="5fdd4-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5fdd4-121">Namespace</span></span><br/>                | <span data-ttu-id="5fdd4-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="5fdd4-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="5fdd4-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5fdd4-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fdd4-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fdd4-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fdd4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5fdd4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fdd4-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fdd4-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="5fdd4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5fdd4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fdd4-128">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="5fdd4-128">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





