---
title: Метод Синчронизеаллпублишингдата класса Win32_RDMSManagementData
description: Синхронизирует все данные публикации для служб удаленный рабочий стол Management Services (RDMS).
ms.assetid: 3a2135c3-26d6-4b6e-9680-f2d07f33ec05
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Синчронизеаллпублишингдата
- Службы удаленных рабочих столов метода Синчронизеаллпублишингдата, класс Win32_RDMSManagementData
- Класс Win32_RDMSManagementData службы удаленных рабочих столов, метод Синчронизеаллпублишингдата
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizeAllPublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4db541954e1595c7b2fc8340f05a9415ad39b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802110"
---
# <a name="synchronizeallpublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="8fce3-106">Метод Синчронизеаллпублишингдата \_ класса Win32 рдмсманажементдата</span><span class="sxs-lookup"><span data-stu-id="8fce3-106">SynchronizeAllPublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="8fce3-107">Синхронизирует все данные публикации для служб удаленный рабочий стол Management Services (RDMS).</span><span class="sxs-lookup"><span data-stu-id="8fce3-107">Synchronizes all publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fce3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fce3-108">Syntax</span></span>


```mof
uint32 SynchronizeAllPublishingData();
```



## <a name="parameters"></a><span data-ttu-id="8fce3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fce3-109">Parameters</span></span>

<span data-ttu-id="8fce3-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8fce3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8fce3-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fce3-111">Return value</span></span>

<span data-ttu-id="8fce3-112">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="8fce3-112">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fce3-113">Требования</span><span class="sxs-lookup"><span data-stu-id="8fce3-113">Requirements</span></span>



| <span data-ttu-id="8fce3-114">Требование</span><span class="sxs-lookup"><span data-stu-id="8fce3-114">Requirement</span></span> | <span data-ttu-id="8fce3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="8fce3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fce3-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fce3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8fce3-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8fce3-117">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8fce3-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fce3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8fce3-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fce3-119">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8fce3-120">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fce3-120">Namespace</span></span><br/>                | <span data-ttu-id="8fce3-121">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="8fce3-121">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8fce3-122">MOF</span><span class="sxs-lookup"><span data-stu-id="8fce3-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fce3-123"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fce3-123"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fce3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8fce3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fce3-125"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fce3-125"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8fce3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fce3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fce3-127">**\_Рдмсманажементдата Win32**</span><span class="sxs-lookup"><span data-stu-id="8fce3-127">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





