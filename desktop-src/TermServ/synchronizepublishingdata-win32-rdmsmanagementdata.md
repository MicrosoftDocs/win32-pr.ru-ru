---
title: Метод Синчронизепублишингдата класса Win32_RDMSManagementData
description: Синхронизирует указанный набор данных публикации для служб управления удаленный рабочий стол (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Синчронизепублишингдата
- Службы удаленных рабочих столов метода Синчронизепублишингдата, класс Win32_RDMSManagementData
- Класс Win32_RDMSManagementData службы удаленных рабочих столов, метод Синчронизепублишингдата
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415432"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a><span data-ttu-id="f0c81-106">Метод Синчронизепублишингдата \_ класса Win32 рдмсманажементдата</span><span class="sxs-lookup"><span data-stu-id="f0c81-106">SynchronizePublishingData method of the Win32\_RDMSManagementData class</span></span>

<span data-ttu-id="f0c81-107">Синхронизирует указанный набор данных публикации для служб управления удаленный рабочий стол (RDMS).</span><span class="sxs-lookup"><span data-stu-id="f0c81-107">Synchronizes the specified set of publishing data for Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="f0c81-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f0c81-108">Syntax</span></span>


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a><span data-ttu-id="f0c81-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0c81-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0c81-110">*Контекст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f0c81-110">*Context* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0c81-111">Сведения о контексте публикуемых данных для синхронизации.</span><span class="sxs-lookup"><span data-stu-id="f0c81-111">The context information of the publishing data to synchronize.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0c81-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0c81-112">Return value</span></span>

<span data-ttu-id="f0c81-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="f0c81-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0c81-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f0c81-114">Requirements</span></span>



| <span data-ttu-id="f0c81-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f0c81-115">Requirement</span></span> | <span data-ttu-id="f0c81-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f0c81-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0c81-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0c81-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f0c81-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f0c81-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f0c81-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0c81-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f0c81-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f0c81-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f0c81-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f0c81-121">Namespace</span></span><br/>                | <span data-ttu-id="f0c81-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="f0c81-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f0c81-123">MOF</span><span class="sxs-lookup"><span data-stu-id="f0c81-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f0c81-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f0c81-125">DLL</span><span class="sxs-lookup"><span data-stu-id="f0c81-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0c81-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0c81-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f0c81-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0c81-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0c81-128">**\_Рдмсманажементдата Win32**</span><span class="sxs-lookup"><span data-stu-id="f0c81-128">**Win32\_RDMSManagementData**</span></span>](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





