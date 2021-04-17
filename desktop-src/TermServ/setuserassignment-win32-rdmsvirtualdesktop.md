---
title: Метод Сетусерассигнмент класса Win32_RDMSVirtualDesktop
description: Назначает пользователю виртуальный рабочий стол.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетусерассигнмент
- Службы удаленных рабочих столов метода Сетусерассигнмент, класс Win32_RDMSVirtualDesktop
- Класс Win32_RDMSVirtualDesktop службы удаленных рабочих столов, метод Сетусерассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672831"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="4d4f1-106">Метод Сетусерассигнмент \_ класса Win32 рдмсвиртуалдесктоп</span><span class="sxs-lookup"><span data-stu-id="4d4f1-106">SetUserAssignment method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="4d4f1-107">Назначает пользователю виртуальный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="4d4f1-107">Assigns a virtual desktop to a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d4f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d4f1-108">Syntax</span></span>


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a><span data-ttu-id="4d4f1-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d4f1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d4f1-110">*Имя пользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d4f1-110">*UserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d4f1-111">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4f1-111">The username of the user.</span></span>

</dd> <dt>

<span data-ttu-id="4d4f1-112">*Доменпользователя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4d4f1-112">*UserDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d4f1-113">Доменное имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="4d4f1-113">The domain name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d4f1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d4f1-114">Return value</span></span>

<span data-ttu-id="4d4f1-115">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="4d4f1-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d4f1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="4d4f1-116">Requirements</span></span>



| <span data-ttu-id="4d4f1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="4d4f1-117">Requirement</span></span> | <span data-ttu-id="4d4f1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="4d4f1-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d4f1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4d4f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="4d4f1-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4d4f1-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="4d4f1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4d4f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="4d4f1-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d4f1-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="4d4f1-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4d4f1-123">Namespace</span></span><br/>                | <span data-ttu-id="4d4f1-124">Корневой \\ \\ rdms CIMv2</span><span class="sxs-lookup"><span data-stu-id="4d4f1-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="4d4f1-125">MOF</span><span class="sxs-lookup"><span data-stu-id="4d4f1-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d4f1-126"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d4f1-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d4f1-127">DLL</span><span class="sxs-lookup"><span data-stu-id="4d4f1-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d4f1-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d4f1-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="4d4f1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4d4f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d4f1-130">**\_Рдмсвиртуалдесктоп Win32**</span><span class="sxs-lookup"><span data-stu-id="4d4f1-130">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





