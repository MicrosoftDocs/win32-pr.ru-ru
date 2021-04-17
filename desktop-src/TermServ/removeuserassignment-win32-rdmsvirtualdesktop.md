---
title: Метод Ремовеусерассигнмент класса Win32_RDMSVirtualDesktop
description: Удаляет назначение пользователя из виртуального рабочего стола.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовеусерассигнмент
- Службы удаленных рабочих столов метода Ремовеусерассигнмент, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Ремовеусерассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681920"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="1d0ab-106">Метод Ремовеусерассигнмент \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="1d0ab-106">RemoveUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="1d0ab-107">Удаляет назначение пользователя из виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="1d0ab-107">Removes the user assignment from the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d0ab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1d0ab-108">Syntax</span></span>


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="1d0ab-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d0ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d0ab-110">*VMName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1d0ab-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d0ab-111">Имя виртуальной машины виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="1d0ab-111">The virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d0ab-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d0ab-112">Return value</span></span>

<span data-ttu-id="1d0ab-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="1d0ab-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d0ab-114">Требования</span><span class="sxs-lookup"><span data-stu-id="1d0ab-114">Requirements</span></span>



| <span data-ttu-id="1d0ab-115">Требование</span><span class="sxs-lookup"><span data-stu-id="1d0ab-115">Requirement</span></span> | <span data-ttu-id="1d0ab-116">Значение</span><span class="sxs-lookup"><span data-stu-id="1d0ab-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0ab-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d0ab-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1d0ab-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="1d0ab-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1d0ab-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d0ab-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1d0ab-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1d0ab-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1d0ab-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1d0ab-121">Namespace</span></span><br/>                | <span data-ttu-id="1d0ab-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="1d0ab-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1d0ab-123">MOF</span><span class="sxs-lookup"><span data-stu-id="1d0ab-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d0ab-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d0ab-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d0ab-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1d0ab-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d0ab-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d0ab-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1d0ab-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1d0ab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d0ab-128">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="1d0ab-128">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





