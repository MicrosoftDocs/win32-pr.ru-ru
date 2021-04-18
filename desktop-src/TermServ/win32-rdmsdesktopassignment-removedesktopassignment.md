---
title: Метод Ремоведесктопассигнмент класса Win32_RDMSDesktopAssignment
description: Удаляет назначение рабочего стола.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Ремоведесктопассигнмент
- Службы удаленных рабочих столов метода Ремоведесктопассигнмент, класс Win32_RDMSDesktopAssignment
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов, метод Ремоведесктопассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682106"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="6b6d3-106">Метод Ремоведесктопассигнмент \_ класса Win32 рдмсдесктопассигнмент</span><span class="sxs-lookup"><span data-stu-id="6b6d3-106">RemoveDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="6b6d3-107">Удаляет назначение рабочего стола</span><span class="sxs-lookup"><span data-stu-id="6b6d3-107">Removes a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="6b6d3-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b6d3-108">Syntax</span></span>


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="6b6d3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b6d3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b6d3-110">*Коллектионалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6d3-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6d3-111">Псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="6b6d3-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="6b6d3-112">*Десктопнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6d3-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6d3-113">Имя рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="6b6d3-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="6b6d3-114">*Доменпользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6d3-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6d3-115">Доменное имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b6d3-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="6b6d3-116">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6b6d3-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b6d3-117">Имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="6b6d3-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b6d3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="6b6d3-118">Requirements</span></span>



| <span data-ttu-id="6b6d3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="6b6d3-119">Requirement</span></span> | <span data-ttu-id="6b6d3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="6b6d3-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b6d3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b6d3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="6b6d3-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="6b6d3-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="6b6d3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b6d3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="6b6d3-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="6b6d3-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="6b6d3-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b6d3-125">Namespace</span></span><br/>                | <span data-ttu-id="6b6d3-126">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b6d3-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="6b6d3-127">MOF</span><span class="sxs-lookup"><span data-stu-id="6b6d3-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b6d3-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b6d3-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b6d3-129">DLL</span><span class="sxs-lookup"><span data-stu-id="6b6d3-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b6d3-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b6d3-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="6b6d3-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b6d3-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b6d3-132">**\_Рдмсдесктопассигнмент Win32**</span><span class="sxs-lookup"><span data-stu-id="6b6d3-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





