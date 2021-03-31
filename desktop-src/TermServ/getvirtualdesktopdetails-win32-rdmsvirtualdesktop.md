---
title: Метод Жетвиртуалдесктопдетаилс класса Win32_RDMSVirtualDesktop
description: Получение дополнительных сведений о виртуальном рабочем столе.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвиртуалдесктопдетаилс
- Службы удаленных рабочих столов метода Жетвиртуалдесктопдетаилс, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Жетвиртуалдесктопдетаилс
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491337"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="182bc-106">Метод Жетвиртуалдесктопдетаилс \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="182bc-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="182bc-107">Получение дополнительных сведений о виртуальном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="182bc-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="182bc-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="182bc-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="182bc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="182bc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="182bc-110">*Рамсизеинмб* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="182bc-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182bc-111">Получает объем ОЗУ, назначенный виртуальному рабочему столу, в байтах.</span><span class="sxs-lookup"><span data-stu-id="182bc-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="182bc-112">*Ремотефксенаблед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="182bc-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182bc-113">Получает значение, указывающее, включено ли RemoteFX на виртуальном рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="182bc-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="182bc-114">**Значение true** , если RemoteFX включен. в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="182bc-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="182bc-115">*OSVersion* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="182bc-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="182bc-116">Получает версию ОС виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="182bc-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="182bc-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="182bc-117">Return value</span></span>

<span data-ttu-id="182bc-118">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="182bc-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="182bc-119">Требования</span><span class="sxs-lookup"><span data-stu-id="182bc-119">Requirements</span></span>



| <span data-ttu-id="182bc-120">Требование</span><span class="sxs-lookup"><span data-stu-id="182bc-120">Requirement</span></span> | <span data-ttu-id="182bc-121">Значение</span><span class="sxs-lookup"><span data-stu-id="182bc-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="182bc-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="182bc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="182bc-123">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="182bc-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="182bc-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="182bc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="182bc-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="182bc-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="182bc-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="182bc-126">Namespace</span></span><br/>                | <span data-ttu-id="182bc-127">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="182bc-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="182bc-128">MOF</span><span class="sxs-lookup"><span data-stu-id="182bc-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="182bc-129"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="182bc-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="182bc-130">DLL</span><span class="sxs-lookup"><span data-stu-id="182bc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="182bc-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="182bc-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="182bc-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="182bc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="182bc-133">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="182bc-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





