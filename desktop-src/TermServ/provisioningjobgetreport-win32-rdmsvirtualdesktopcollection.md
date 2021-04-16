---
title: Метод Провисионингжобжетрепорт класса Win32_RDMSVirtualDesktopCollection
description: Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингжобжетрепорт
- Службы удаленных рабочих столов метода Провисионингжобжетрепорт, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионингжобжетрепорт
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672715"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="4e5a9-106">Метод Провисионингжобжетрепорт \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="4e5a9-106">ProvisioningJobGetReport method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="4e5a9-107">Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-107">Gets a report about the status of a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e5a9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e5a9-108">Syntax</span></span>


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a><span data-ttu-id="4e5a9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e5a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e5a9-110">*Жобгуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4e5a9-110">*JobGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5a9-111">**Идентификатор GUID** , однозначно определяющий задание подготовки.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-111">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="4e5a9-112">*Жобрепортксмл* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4e5a9-112">*JobReportXml* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4e5a9-113">Строка, содержащая отчет в формате XML.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-113">A string that contains the report in XML format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e5a9-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e5a9-114">Return value</span></span>

<span data-ttu-id="4e5a9-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="4e5a9-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e5a9-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4e5a9-116">Requirements</span></span>



| <span data-ttu-id="4e5a9-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4e5a9-117">Requirement</span></span> | <span data-ttu-id="4e5a9-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4e5a9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e5a9-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4e5a9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4e5a9-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4e5a9-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4e5a9-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4e5a9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4e5a9-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4e5a9-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4e5a9-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4e5a9-123">Namespace</span></span><br/>                | <span data-ttu-id="4e5a9-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="4e5a9-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4e5a9-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4e5a9-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4e5a9-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4e5a9-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4e5a9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4e5a9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e5a9-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e5a9-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4e5a9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4e5a9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e5a9-130">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="4e5a9-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





