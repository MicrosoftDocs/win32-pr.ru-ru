---
title: Метод Жетбасевхдпас класса Win32_RDMSDeploymentSettings
description: Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов. | Метод Жетбасевхдпас класса Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетбасевхдпас
- Службы удаленных рабочих столов метода Жетбасевхдпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетбасевхдпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000161"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a><span data-ttu-id="b20d0-107">Метод Жетбасевхдпас \_ класса Win32 рдмсдеплойментсеттингс</span><span class="sxs-lookup"><span data-stu-id="b20d0-107">GetBaseVHDPath method of the Win32\_RDMSDeploymentSettings class</span></span>

<span data-ttu-id="b20d0-108">Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="b20d0-108">Retrieves the base path to the directory to which VHDs of the virtual desktop collection are deployed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b20d0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b20d0-109">Syntax</span></span>


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a><span data-ttu-id="b20d0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b20d0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b20d0-111">*DirectoryPath* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b20d0-111">*DirectoryPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b20d0-112">Получает путь развертывания VHD.</span><span class="sxs-lookup"><span data-stu-id="b20d0-112">Receives the VHD deployment path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b20d0-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b20d0-113">Return value</span></span>

<span data-ttu-id="b20d0-114">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="b20d0-114">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b20d0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b20d0-115">Requirements</span></span>



| <span data-ttu-id="b20d0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b20d0-116">Requirement</span></span> | <span data-ttu-id="b20d0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b20d0-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b20d0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b20d0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b20d0-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b20d0-119">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="b20d0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b20d0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b20d0-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b20d0-121">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="b20d0-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b20d0-122">Namespace</span></span><br/>                | <span data-ttu-id="b20d0-123">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="b20d0-123">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="b20d0-124">MOF</span><span class="sxs-lookup"><span data-stu-id="b20d0-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b20d0-125"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b20d0-125"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="b20d0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b20d0-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b20d0-127"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b20d0-127"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="b20d0-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b20d0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b20d0-129">**\_Рдмсдеплойментсеттингс Win32**</span><span class="sxs-lookup"><span data-stu-id="b20d0-129">**Win32\_RDMSDeploymentSettings**</span></span>](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





