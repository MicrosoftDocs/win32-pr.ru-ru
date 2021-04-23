---
title: Метод Провисионингпрепжоб класса Win32_RDMSVirtualDesktopCollection
description: Создает задание подготовки виртуальных рабочих столов.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингпрепжоб
- Службы удаленных рабочих столов метода Провисионингпрепжоб, интерфейс Win32_RDMSVirtualDesktopCollection
- Службы удаленных рабочих столов интерфейса Win32_RDMSVirtualDesktopCollection, метод Провисионингпрепжоб
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988570"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="e8664-106">Метод Провисионингпрепжоб \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="e8664-106">ProvisioningPrepJob method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="e8664-107">Создает задание подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="e8664-107">Creates a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8664-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8664-108">Syntax</span></span>


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="e8664-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e8664-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8664-110">*Коллектионалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-111">Псевдоним коллекции, в которой размещен виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="e8664-111">The alias of the collection that hosts the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-112">*VMHostName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-112">*VMHostName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-113">Имя узла виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8664-113">The virtual machine host name.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-114">*VMName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-114">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-115">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8664-115">The name of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-116">*Експорттолокатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-116">*ExportToLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-117">Полный путь к расположению для экспорта задания подготовки.</span><span class="sxs-lookup"><span data-stu-id="e8664-117">The full path the location to export the provisioning job.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-118">*бсиспреп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-118">*bSysPrep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-119">Указывает, представляет ли задание подготовки развертывание Sysprep.</span><span class="sxs-lookup"><span data-stu-id="e8664-119">Indicates whether the provisioning job represents a Sysprep deployment.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-120">*MachineName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-120">*MachineName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-121">Имя компьютера, на котором размещена виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="e8664-121">The machine name of the computer that hosts the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-122">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-122">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-123">Имя пользователя администратора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8664-123">The user name of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-124">*Пароль* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e8664-124">*Password* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-125">Пароль администратора виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e8664-125">The password of the administrator of the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="e8664-126">*Жобгуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e8664-126">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8664-127">**Идентификатор GUID** , однозначно определяющий задание подготовки.</span><span class="sxs-lookup"><span data-stu-id="e8664-127">The **GUID** that uniquely identifies the provisioning job.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8664-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e8664-128">Return value</span></span>

<span data-ttu-id="e8664-129">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="e8664-129">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8664-130">Требования</span><span class="sxs-lookup"><span data-stu-id="e8664-130">Requirements</span></span>



| <span data-ttu-id="e8664-131">Требование</span><span class="sxs-lookup"><span data-stu-id="e8664-131">Requirement</span></span> | <span data-ttu-id="e8664-132">Значение</span><span class="sxs-lookup"><span data-stu-id="e8664-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8664-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8664-133">Minimum supported client</span></span><br/> | <span data-ttu-id="e8664-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e8664-134">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="e8664-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8664-135">Minimum supported server</span></span><br/> | <span data-ttu-id="e8664-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8664-136">Windows Server 2008</span></span><br/>                                                              |
| <span data-ttu-id="e8664-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8664-137">Namespace</span></span><br/>                | <span data-ttu-id="e8664-138">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="e8664-138">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="e8664-139">MOF</span><span class="sxs-lookup"><span data-stu-id="e8664-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8664-140"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8664-140"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8664-141">DLL</span><span class="sxs-lookup"><span data-stu-id="e8664-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8664-142"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8664-142"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="e8664-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e8664-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8664-144">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="e8664-144">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





