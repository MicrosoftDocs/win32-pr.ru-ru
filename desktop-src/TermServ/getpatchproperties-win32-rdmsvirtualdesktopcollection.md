---
title: Метод Жетпатчпропертиес класса Win32_RDMSVirtualDesktopCollection
description: Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпатчпропертиес
- Службы удаленных рабочих столов метода Жетпатчпропертиес, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Жетпатчпропертиес
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534571"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="8fc2a-106">Метод Жетпатчпропертиес \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="8fc2a-106">GetPatchProperties method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="8fc2a-107">Извлекает свойства задания подготовки обновлений программного обеспечения для виртуальных машин в коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-107">Retrieves the properties of a software update provisioning job for the virtual machines in a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc2a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8fc2a-108">Syntax</span></span>


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a><span data-ttu-id="8fc2a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8fc2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc2a-110">Время *начала* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fc2a-110">*StartTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc2a-111">Дата и время установки обновлений.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-111">The date and time to install the updates.</span></span>

</dd> <dt>

<span data-ttu-id="8fc2a-112">*Форцелогоффтиме* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fc2a-112">*ForceLogOffTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc2a-113">Дата и время, когда система будет выходить из системы пользователей виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-113">The date and time on which the system will log off users of the virtual machines.</span></span>

</dd> <dt>

<span data-ttu-id="8fc2a-114">*Жобгуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fc2a-114">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc2a-115">**Идентификатор GUID** , который однозначно определяет задание подготовки.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-115">A **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="8fc2a-116">*Состояние* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="8fc2a-116">*State* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8fc2a-117">Состояние задания подготовки.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-117">The state of the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc2a-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8fc2a-118">Return value</span></span>

<span data-ttu-id="8fc2a-119">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="8fc2a-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fc2a-120">Требования</span><span class="sxs-lookup"><span data-stu-id="8fc2a-120">Requirements</span></span>



| <span data-ttu-id="8fc2a-121">Требование</span><span class="sxs-lookup"><span data-stu-id="8fc2a-121">Requirement</span></span> | <span data-ttu-id="8fc2a-122">Значение</span><span class="sxs-lookup"><span data-stu-id="8fc2a-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fc2a-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8fc2a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8fc2a-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="8fc2a-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="8fc2a-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8fc2a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8fc2a-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="8fc2a-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="8fc2a-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8fc2a-127">Namespace</span></span><br/>                | <span data-ttu-id="8fc2a-128">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="8fc2a-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="8fc2a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="8fc2a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8fc2a-130"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8fc2a-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="8fc2a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8fc2a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8fc2a-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8fc2a-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="8fc2a-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8fc2a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc2a-134">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="8fc2a-134">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





