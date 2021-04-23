---
title: Метод Сетбасевхдпас класса Win32_RDMSDeploymentSettings
description: Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов. | Метод Сетбасевхдпас класса Win32_RDMSDeploymentSettings
ms.assetid: 1ea4cd93-ef17-4ec9-82f9-382c549f189c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетбасевхдпас
- Службы удаленных рабочих столов метода Сетбасевхдпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетбасевхдпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7907640a9641cff3c94475318bf499415b25184
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674585"
---
# <a name="setbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="c9328-107">Метод Сетбасевхдпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="c9328-107">SetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="c9328-108">Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c9328-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9328-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c9328-109">Syntax</span></span>


```mof
uint32 SetBaseVHDPath(
  [in] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="c9328-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c9328-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9328-111">*DirectoryPath* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c9328-111">*DirectoryPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9328-112">Новый путь развертывания виртуального жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="c9328-112">The new VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9328-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c9328-113">Return value</span></span>

<span data-ttu-id="c9328-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c9328-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9328-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c9328-115">Requirements</span></span>



| <span data-ttu-id="c9328-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c9328-116">Requirement</span></span> | <span data-ttu-id="c9328-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c9328-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9328-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c9328-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c9328-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c9328-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c9328-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c9328-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c9328-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c9328-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c9328-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c9328-122">Namespace</span></span><br/>                | <span data-ttu-id="c9328-123">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="c9328-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c9328-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c9328-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9328-125"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9328-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9328-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c9328-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9328-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9328-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c9328-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c9328-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9328-129">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="c9328-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





