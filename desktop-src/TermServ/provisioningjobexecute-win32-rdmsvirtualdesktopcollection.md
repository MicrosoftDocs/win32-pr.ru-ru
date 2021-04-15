---
title: Метод Провисионингжобексекуте класса Win32_RDMSVirtualDesktopCollection
description: Запускает задание подготовки виртуальных рабочих столов.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингжобексекуте
- Службы удаленных рабочих столов метода Провисионингжобексекуте, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионингжобексекуте
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492762"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="aefe6-106">Метод Провисионингжобексекуте \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="aefe6-106">ProvisioningJobExecute method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="aefe6-107">Запускает задание подготовки виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="aefe6-107">Runs a virtual desktop provisioning job.</span></span>

## <a name="syntax"></a><span data-ttu-id="aefe6-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aefe6-108">Syntax</span></span>


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a><span data-ttu-id="aefe6-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="aefe6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aefe6-110">*Жобинпутксмл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="aefe6-110">*JobInputXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aefe6-111">Строка, содержащая сведения об инициализации в формате XML.</span><span class="sxs-lookup"><span data-stu-id="aefe6-111">A string that contains the provisioning information in XML format.</span></span>

</dd> <dt>

<span data-ttu-id="aefe6-112">*Жобгуид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="aefe6-112">*JobGuid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aefe6-113">**Идентификатор GUID** , однозначно определяющий выполняемое задание подготовки.</span><span class="sxs-lookup"><span data-stu-id="aefe6-113">The **GUID** that uniquely identifies the provisioning job to run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aefe6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aefe6-114">Return value</span></span>

<span data-ttu-id="aefe6-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="aefe6-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="aefe6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="aefe6-116">Requirements</span></span>



| <span data-ttu-id="aefe6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="aefe6-117">Requirement</span></span> | <span data-ttu-id="aefe6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="aefe6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="aefe6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aefe6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="aefe6-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="aefe6-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="aefe6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aefe6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="aefe6-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aefe6-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="aefe6-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aefe6-123">Namespace</span></span><br/>                | <span data-ttu-id="aefe6-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="aefe6-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="aefe6-125">MOF</span><span class="sxs-lookup"><span data-stu-id="aefe6-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aefe6-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aefe6-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="aefe6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="aefe6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aefe6-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aefe6-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="aefe6-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aefe6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aefe6-130">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="aefe6-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





