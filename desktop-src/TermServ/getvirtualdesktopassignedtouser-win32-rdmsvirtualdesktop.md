---
title: Метод Жетвиртуалдесктопассигнедтаусер класса Win32_RDMSVirtualDesktop
description: Извлекает виртуальный рабочий стол, назначенный указанному пользователю.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетвиртуалдесктопассигнедтаусер
- Службы удаленных рабочих столов метода Жетвиртуалдесктопассигнедтаусер, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Жетвиртуалдесктопассигнедтаусер
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcbbbed20b6b571e8867689ac901344af8e23b93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672505"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="d5688-106">Метод Жетвиртуалдесктопассигнедтаусер \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="d5688-106">GetVirtualDesktopAssignedToUser method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="d5688-107">Извлекает виртуальный рабочий стол, назначенный указанному пользователю.</span><span class="sxs-lookup"><span data-stu-id="d5688-107">Retrieves the virtual desktop that is assigned to the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5688-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5688-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a><span data-ttu-id="d5688-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5688-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5688-110">*Коллектионалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5688-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5688-111">Псевдоним коллекции виртуальных рабочих столов, содержащей виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="d5688-111">The alias of the virtual desktop collection that contain the virtual desktop.</span></span>

</dd> <dt>

<span data-ttu-id="d5688-112">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5688-112">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5688-113">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5688-113">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="d5688-114">*Доменпользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5688-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5688-115">Доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="d5688-115">The domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="d5688-116">*VMName* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d5688-116">*VMName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5688-117">Получает имя виртуальной машины для виртуального рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="d5688-117">Receives the virtual machine name of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5688-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5688-118">Return value</span></span>

<span data-ttu-id="d5688-119">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="d5688-119">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5688-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d5688-120">Requirements</span></span>



| <span data-ttu-id="d5688-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d5688-121">Requirement</span></span> | <span data-ttu-id="d5688-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d5688-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5688-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5688-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d5688-124">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d5688-124">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="d5688-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5688-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d5688-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5688-126">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="d5688-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d5688-127">Namespace</span></span><br/>                | <span data-ttu-id="d5688-128">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="d5688-128">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="d5688-129">MOF</span><span class="sxs-lookup"><span data-stu-id="d5688-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5688-130"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5688-130"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5688-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d5688-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5688-132"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5688-132"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="d5688-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5688-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5688-134">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="d5688-134">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





