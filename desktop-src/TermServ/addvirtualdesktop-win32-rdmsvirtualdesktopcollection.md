---
title: Метод Аддвиртуалдесктоп класса Win32_RDMSVirtualDesktopCollection
description: Добавляет виртуальный рабочий стол в коллекцию виртуальных рабочих столов.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Аддвиртуалдесктоп
- Службы удаленных рабочих столов метода Аддвиртуалдесктоп, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Аддвиртуалдесктоп
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533884"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="9081e-106">Метод Аддвиртуалдесктоп \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="9081e-106">AddVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="9081e-107">Добавляет виртуальный рабочий стол в коллекцию виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="9081e-107">Adds a virtual desktop to the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9081e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9081e-108">Syntax</span></span>


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="9081e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9081e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9081e-110">*VMName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9081e-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9081e-111">Имя виртуальной машины, на которой размещен виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="9081e-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9081e-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9081e-112">Return value</span></span>

<span data-ttu-id="9081e-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="9081e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9081e-114">Требования</span><span class="sxs-lookup"><span data-stu-id="9081e-114">Requirements</span></span>



| <span data-ttu-id="9081e-115">Требование</span><span class="sxs-lookup"><span data-stu-id="9081e-115">Requirement</span></span> | <span data-ttu-id="9081e-116">Значение</span><span class="sxs-lookup"><span data-stu-id="9081e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9081e-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9081e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9081e-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9081e-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9081e-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9081e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9081e-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9081e-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9081e-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="9081e-121">Namespace</span></span><br/>                | <span data-ttu-id="9081e-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="9081e-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9081e-123">MOF</span><span class="sxs-lookup"><span data-stu-id="9081e-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9081e-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9081e-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9081e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9081e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9081e-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9081e-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9081e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9081e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9081e-128">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="9081e-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





