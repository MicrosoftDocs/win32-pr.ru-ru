---
title: Метод Провисионингжобканцел класса Win32_RDMSVirtualDesktopCollection
description: Отмена задания подготовки виртуальных рабочих столов.
ms.assetid: 933ea0f3-b916-4e70-89de-597f9eb23976
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингжобканцел
- Службы удаленных рабочих столов метода Провисионингжобканцел, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионингжобканцел
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobCancel
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f414bcdc264d682817898bae98fcf60a716452
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672716"
---
# <a name="provisioningjobcancel-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="803b2-106">Метод Провисионингжобканцел \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="803b2-106">ProvisioningJobCancel method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="803b2-107">Отмена задания подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="803b2-107">Cancels a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="803b2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="803b2-108">Syntax</span></span>


```mof
uint32 ProvisioningJobCancel(
  [in] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="803b2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="803b2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="803b2-110">*Жобгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="803b2-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="803b2-111">**Идентификатор GUID** , однозначно определяющий задание подготовки для отмены.</span><span class="sxs-lookup"><span data-stu-id="803b2-111">The **GUID** that uniquely identifies the provisioning job to cancel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="803b2-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="803b2-112">Return value</span></span>

<span data-ttu-id="803b2-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="803b2-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="803b2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="803b2-114">Requirements</span></span>



| <span data-ttu-id="803b2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="803b2-115">Requirement</span></span> | <span data-ttu-id="803b2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="803b2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="803b2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="803b2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="803b2-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="803b2-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="803b2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="803b2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="803b2-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="803b2-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="803b2-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="803b2-121">Namespace</span></span><br/>                | <span data-ttu-id="803b2-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="803b2-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="803b2-123">MOF</span><span class="sxs-lookup"><span data-stu-id="803b2-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="803b2-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="803b2-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="803b2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="803b2-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="803b2-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="803b2-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="803b2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="803b2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="803b2-128">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="803b2-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





