---
title: Метод Адддесктопассигнмент класса Win32_RDMSDesktopAssignment
description: Добавьте назначение рабочего стола.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Адддесктопассигнмент
- Службы удаленных рабочих столов метода Адддесктопассигнмент, класс Win32_RDMSDesktopAssignment
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов, метод Адддесктопассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891750"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a><span data-ttu-id="ca0f1-106">Метод Адддесктопассигнмент \_ класса Win32 рдмсдесктопассигнмент</span><span class="sxs-lookup"><span data-stu-id="ca0f1-106">AddDesktopAssignment method of the Win32\_RDMSDesktopAssignment class</span></span>

<span data-ttu-id="ca0f1-107">Добавление назначения рабочего стола</span><span class="sxs-lookup"><span data-stu-id="ca0f1-107">Add a desktop assignment</span></span>

## <a name="syntax"></a><span data-ttu-id="ca0f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca0f1-108">Syntax</span></span>


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a><span data-ttu-id="ca0f1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca0f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca0f1-110">*Коллектионалиас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0f1-110">*CollectionAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0f1-111">Псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="ca0f1-111">The collection alias.</span></span>

</dd> <dt>

<span data-ttu-id="ca0f1-112">*Десктопнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0f1-112">*DesktopName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0f1-113">Имя рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="ca0f1-113">The name of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="ca0f1-114">*Доменпользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0f1-114">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0f1-115">Доменное имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca0f1-115">The user account domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ca0f1-116">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ca0f1-116">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca0f1-117">Имя учетной записи пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca0f1-117">The user account name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ca0f1-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ca0f1-118">Requirements</span></span>



| <span data-ttu-id="ca0f1-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ca0f1-119">Requirement</span></span> | <span data-ttu-id="ca0f1-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ca0f1-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca0f1-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca0f1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ca0f1-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ca0f1-122">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ca0f1-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca0f1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ca0f1-124">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="ca0f1-124">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="ca0f1-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca0f1-125">Namespace</span></span><br/>                | <span data-ttu-id="ca0f1-126">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="ca0f1-126">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ca0f1-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ca0f1-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca0f1-128"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca0f1-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca0f1-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ca0f1-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca0f1-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca0f1-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ca0f1-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca0f1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca0f1-132">**\_Рдмсдесктопассигнмент Win32**</span><span class="sxs-lookup"><span data-stu-id="ca0f1-132">**Win32\_RDMSDesktopAssignment**</span></span>](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





