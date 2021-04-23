---
title: Метод Провисионинженумератежобс класса Win32_RDMSVirtualDesktopCollection
description: Перечисляет задания подготовки виртуальных рабочих столов для этой службы.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионинженумератежобс
- Службы удаленных рабочих столов метода Провисионинженумератежобс, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионинженумератежобс
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535384"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="72a9e-106">Метод Провисионинженумератежобс \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="72a9e-106">ProvisioningEnumerateJobs method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="72a9e-107">Перечисляет задания подготовки виртуальных рабочих столов для этой службы.</span><span class="sxs-lookup"><span data-stu-id="72a9e-107">Enumerates virtual desktop provisioning jobs for this service.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a9e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72a9e-108">Syntax</span></span>


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a><span data-ttu-id="72a9e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="72a9e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72a9e-110">*JobType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72a9e-110">*JobType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a9e-111">Целое число, указывающее тип задания для перечисления.</span><span class="sxs-lookup"><span data-stu-id="72a9e-111">An integer that specifies the type of job to enumerate.</span></span>

<span data-ttu-id="72a9e-112">Этому параметру можно присвоить одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="72a9e-112">This parameter can be set to one of the following values:</span></span>

<dt>

<span data-ttu-id="72a9e-113">0</span><span class="sxs-lookup"><span data-stu-id="72a9e-113">0</span></span>
</dt> <dd>

<span data-ttu-id="72a9e-114">Выполняемые задания</span><span class="sxs-lookup"><span data-stu-id="72a9e-114">Running jobs</span></span>

</dd> <dt>

<span data-ttu-id="72a9e-115">1</span><span class="sxs-lookup"><span data-stu-id="72a9e-115">1</span></span>
</dt> <dd>

<span data-ttu-id="72a9e-116">Завершенные задания</span><span class="sxs-lookup"><span data-stu-id="72a9e-116">Completed jobs</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="72a9e-117">*Коллектионалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="72a9e-117">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72a9e-118">Псевдоним коллекции виртуальных рабочих столов для перечисления.</span><span class="sxs-lookup"><span data-stu-id="72a9e-118">The alias of the virtual desktop collection to enumerate.</span></span> <span data-ttu-id="72a9e-119">Значение по умолчанию для этого параметра равно FALSE, что указывает на то, что все выполняемые задания должны быть перечислены.</span><span class="sxs-lookup"><span data-stu-id="72a9e-119">The default value for this parameter is FALSE, which specifies that all running jobs are to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="72a9e-120">*Жобгуидс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="72a9e-120">*JobGuids* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72a9e-121">Массив, содержащий **идентификаторы GUID** заданий подготовки для перечисления.</span><span class="sxs-lookup"><span data-stu-id="72a9e-121">An array that contains the **GUIDs** of provisioning jobs to enumerate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72a9e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="72a9e-122">Return value</span></span>

<span data-ttu-id="72a9e-123">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="72a9e-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a9e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="72a9e-124">Requirements</span></span>



| <span data-ttu-id="72a9e-125">Требование</span><span class="sxs-lookup"><span data-stu-id="72a9e-125">Requirement</span></span> | <span data-ttu-id="72a9e-126">Значение</span><span class="sxs-lookup"><span data-stu-id="72a9e-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a9e-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="72a9e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="72a9e-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="72a9e-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="72a9e-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="72a9e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="72a9e-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72a9e-130">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="72a9e-131">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="72a9e-131">Namespace</span></span><br/>                | <span data-ttu-id="72a9e-132">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="72a9e-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="72a9e-133">MOF</span><span class="sxs-lookup"><span data-stu-id="72a9e-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72a9e-134"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="72a9e-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="72a9e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="72a9e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72a9e-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72a9e-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="72a9e-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72a9e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a9e-138">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="72a9e-138">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





