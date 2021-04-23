---
title: Метод Счедулепатч класса Win32_RDMSVirtualDesktopCollection
description: Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Счедулепатч
- Службы удаленных рабочих столов метода Счедулепатч, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Счедулепатч
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490314"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="de1c9-106">Метод Счедулепатч \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="de1c9-106">SchedulePatch method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="de1c9-107">Планирует задание подготовки обновлений программного обеспечения, устанавливающее обновления программного обеспечения на виртуальных машинах в коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="de1c9-107">Schedules a software update provisioning job that installs software updates on the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="de1c9-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="de1c9-108">Syntax</span></span>


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a><span data-ttu-id="de1c9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="de1c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de1c9-110">Время *начала* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de1c9-110">*StartTime* \[in\]</span></span>
</dt> <dd>

> [!Note]  
> <span data-ttu-id="de1c9-111">Система не выполнит выход пользователей виртуальных машин до тех пор, пока не будет указано значение параметра *форцелогоффтиме* .</span><span class="sxs-lookup"><span data-stu-id="de1c9-111">The system will not log off users of the virtual machines until the time specified in the *ForceLogOffTime* parameter.</span></span>

 

<span data-ttu-id="de1c9-112">Дата и время установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="de1c9-112">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="de1c9-113">*Форцелогоффтиме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de1c9-113">*ForceLogOffTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1c9-114">Дата и время, когда система будет выходить из системы пользователей виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="de1c9-114">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="de1c9-115">*Жобинпутксмл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="de1c9-115">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de1c9-116">Строка в формате XML, содержащая сведения о задании обновления программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="de1c9-116">An XML formatted string that contains the software update job information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de1c9-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de1c9-117">Return value</span></span>

<span data-ttu-id="de1c9-118">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="de1c9-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="de1c9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="de1c9-119">Requirements</span></span>



| <span data-ttu-id="de1c9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="de1c9-120">Requirement</span></span> | <span data-ttu-id="de1c9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="de1c9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="de1c9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="de1c9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="de1c9-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="de1c9-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="de1c9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="de1c9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="de1c9-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="de1c9-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="de1c9-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="de1c9-126">Namespace</span></span><br/>                | <span data-ttu-id="de1c9-127">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="de1c9-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="de1c9-128">MOF</span><span class="sxs-lookup"><span data-stu-id="de1c9-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="de1c9-129"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="de1c9-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="de1c9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="de1c9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de1c9-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de1c9-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="de1c9-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="de1c9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de1c9-133">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="de1c9-133">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





