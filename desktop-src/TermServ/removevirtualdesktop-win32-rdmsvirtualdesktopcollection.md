---
title: Метод Ремовевиртуалдесктоп класса Win32_RDMSVirtualDesktopCollection
description: Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.
ms.assetid: 287ebbb2-86db-4b4a-8dbb-ac5472789e72
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремовевиртуалдесктоп
- Службы удаленных рабочих столов метода Ремовевиртуалдесктоп, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Ремовевиртуалдесктоп
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.RemoveVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a468de22d571fa52d37c2ad51d40d492af35384a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533914"
---
# <a name="removevirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="c7792-106">Метод Ремовевиртуалдесктоп \_ класса Win32 рдмсвиртуалдесктопколлектион</span><span class="sxs-lookup"><span data-stu-id="c7792-106">RemoveVirtualDesktop method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="c7792-107">Удаляет виртуальный рабочий стол из коллекции виртуальных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="c7792-107">Removes a virtual desktop from the virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7792-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c7792-108">Syntax</span></span>


```mof
uint32 RemoveVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="c7792-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7792-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7792-110">*VMName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c7792-110">*VMName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7792-111">Имя виртуальной машины, на которой размещен виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="c7792-111">The name of the virtual machine that hosts the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7792-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7792-112">Return value</span></span>

<span data-ttu-id="c7792-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="c7792-113">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7792-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c7792-114">Requirements</span></span>



| <span data-ttu-id="c7792-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c7792-115">Requirement</span></span> | <span data-ttu-id="c7792-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c7792-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7792-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7792-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7792-118">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c7792-118">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c7792-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7792-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7792-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c7792-120">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c7792-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c7792-121">Namespace</span></span><br/>                | <span data-ttu-id="c7792-122">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="c7792-122">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c7792-123">MOF</span><span class="sxs-lookup"><span data-stu-id="c7792-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c7792-124"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c7792-124"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c7792-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c7792-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7792-126"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7792-126"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c7792-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7792-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7792-128">**\_Рдмсвиртуалдесктопколлектион Win32**</span><span class="sxs-lookup"><span data-stu-id="c7792-128">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





