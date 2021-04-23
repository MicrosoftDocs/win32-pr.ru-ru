---
title: Метод Жетпровисионингпропертиес класса Win32_RDMSCollectionProperties
description: Извлекает свойства подготовки коллекции виртуальных рабочих столов.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетпровисионингпропертиес
- Службы удаленных рабочих столов метода Жетпровисионингпропертиес, класс Win32_RDMSCollectionProperties
- Класс Win32_RDMSCollectionProperties службы удаленных рабочих столов, метод Жетпровисионингпропертиес
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681978"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a><span data-ttu-id="68f3c-106">Метод Жетпровисионингпропертиес \_ класса Win32 рдмсколлектионпропертиес</span><span class="sxs-lookup"><span data-stu-id="68f3c-106">GetProvisioningProperties method of the Win32\_RDMSCollectionProperties class</span></span>

<span data-ttu-id="68f3c-107">Извлекает свойства подготовки коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68f3c-107">Retrieves the provisioning properties of the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="68f3c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68f3c-108">Syntax</span></span>


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a><span data-ttu-id="68f3c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="68f3c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68f3c-110">*Пулвхдтипе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-110">*PoolVhdType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-111">Указывает формат виртуального жесткого диска (виртуальный жесткий диск) пула виртуальных машин в коллекции.</span><span class="sxs-lookup"><span data-stu-id="68f3c-111">Specifies the VHD (virtual hard disk) format of the virtual machine pool in the collection.</span></span>

<dt>

<span data-ttu-id="68f3c-112">Клонировать</span><span class="sxs-lookup"><span data-stu-id="68f3c-112">Clone</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-113">Клонированный виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="68f3c-113">A cloned VHD.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-114">диффдиск</span><span class="sxs-lookup"><span data-stu-id="68f3c-114">DiffDisk</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-115">Разностный виртуальный жесткий диск.</span><span class="sxs-lookup"><span data-stu-id="68f3c-115">A differencing VHD.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="68f3c-116">*Мастервмлокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-116">*MasterVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-117">Получает путь к образу главной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="68f3c-117">Receives the path to the master VM image.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-118">*NamePrefix* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-118">*NamePrefix* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-119">Получает префикс имени, добавляемый к началу имен виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="68f3c-119">Receives the name prefix to append to the beginning of virtual machine names.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-120">*Наместартиндекс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-120">*NameStartIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-121">Начальный индекс.</span><span class="sxs-lookup"><span data-stu-id="68f3c-121">Start index.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-122">*Локалвмлокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-122">*LocalVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-123">Получает локальный путь к виртуальным машинам на серверах Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="68f3c-123">Receives the local path to the virtual machines on the Hyper-V servers.</span></span> <span data-ttu-id="68f3c-124">Если этот параметр имеет значение **null** или если он пуст, будет использоваться каталог виртуальной машины по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68f3c-124">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-125">*Локалголдвмлокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-125">*LocalGoldVmLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-126">Получает локальный путь к золотому образу VHD, если для параметра *пулвхдтпе* задано значение "диффдиск".</span><span class="sxs-lookup"><span data-stu-id="68f3c-126">Receives the local path to the golden VHD image when the *PoolVhdTpe* parameter is set to "DiffDisk".</span></span> <span data-ttu-id="68f3c-127">Если этот параметр имеет значение **null** или если он пуст, будет использоваться каталог виртуальной машины по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="68f3c-127">If this parameter is set to **NULL** or if it is empty, the default virtual machine directory will be used.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-128">*Рунфромсмб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-128">*RunFromSMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-129">Получает значение, указывающее, следует ли запускать коллекцию из общего ресурса SMB.</span><span class="sxs-lookup"><span data-stu-id="68f3c-129">Receives a value that indicates whether to run the collection from an Server Message Block (SMB) share.</span></span> <span data-ttu-id="68f3c-130">**Значение true** , чтобы запускать виртуальные машины из общего ресурса СБМ; ином **Значение false**.</span><span class="sxs-lookup"><span data-stu-id="68f3c-130">**TRUE** to run the virtual machines from an SBM share; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-131">*Смблокатион* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-131">*SMBLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-132">Получает путь к общему ресурсу SMB, если включен общий доступ к SMB.</span><span class="sxs-lookup"><span data-stu-id="68f3c-132">Receives the path to the SMB share if SMB sharing is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-133">*Смбстреаминг* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-133">*SMBStreaming* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-134">Получает значение, указывающее, включена ли потоковая передача SMB.</span><span class="sxs-lookup"><span data-stu-id="68f3c-134">Receives a value that indicates whether SMB streaming is enabled.</span></span> <span data-ttu-id="68f3c-135">**Значение true** , если общий доступ к SMB включен; ином **Значение false**.</span><span class="sxs-lookup"><span data-stu-id="68f3c-135">**TRUE** if SMB sharing is enabled; otherwise; **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-136">*Вмдомаин* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-136">*VmDomain* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-137">Получает доменное имя виртуальных машин в коллекции.</span><span class="sxs-lookup"><span data-stu-id="68f3c-137">Receives the domain name of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-138">*Вмау* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-138">*VmOU* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-139">Получает Active Directory подразделение виртуальных машин в коллекции.</span><span class="sxs-lookup"><span data-stu-id="68f3c-139">Receives the Active Directory organization unit (OU) of the virtual machines in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="68f3c-140">*ProductKey* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="68f3c-140">*ProductKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="68f3c-141">Получает ключи продукта операционной системы для виртуальных машин в коллекции.</span><span class="sxs-lookup"><span data-stu-id="68f3c-141">Receives the OS product keys for the virtual machines in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68f3c-142">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="68f3c-142">Return value</span></span>

<span data-ttu-id="68f3c-143">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="68f3c-143">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="68f3c-144">Требования</span><span class="sxs-lookup"><span data-stu-id="68f3c-144">Requirements</span></span>



| <span data-ttu-id="68f3c-145">Требование</span><span class="sxs-lookup"><span data-stu-id="68f3c-145">Requirement</span></span> | <span data-ttu-id="68f3c-146">Значение</span><span class="sxs-lookup"><span data-stu-id="68f3c-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="68f3c-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68f3c-147">Minimum supported client</span></span><br/> | <span data-ttu-id="68f3c-148">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68f3c-148">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="68f3c-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68f3c-149">Minimum supported server</span></span><br/> | <span data-ttu-id="68f3c-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68f3c-150">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="68f3c-151">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68f3c-151">Namespace</span></span><br/>                | <span data-ttu-id="68f3c-152">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="68f3c-152">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="68f3c-153">MOF</span><span class="sxs-lookup"><span data-stu-id="68f3c-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68f3c-154"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68f3c-154"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="68f3c-155">DLL</span><span class="sxs-lookup"><span data-stu-id="68f3c-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68f3c-156"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68f3c-156"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="68f3c-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68f3c-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68f3c-158">**\_Рдмсколлектионпропертиес Win32**</span><span class="sxs-lookup"><span data-stu-id="68f3c-158">**Win32\_RDMSCollectionProperties**</span></span>](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





