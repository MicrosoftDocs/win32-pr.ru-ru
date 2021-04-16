---
description: Задает параметры общего ресурса.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Метод Сетшареинфо класса Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656065"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a><span data-ttu-id="fac24-103">Метод Сетшареинфо \_ класса Win32 клустершаре</span><span class="sxs-lookup"><span data-stu-id="fac24-103">SetShareInfo method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="fac24-104">Задает параметры общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="fac24-104">Sets the parameters of the shared resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac24-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac24-105">Syntax</span></span>


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="fac24-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fac24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac24-107">*MaximumAllowed* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fac24-107">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac24-108">Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.</span><span class="sxs-lookup"><span data-stu-id="fac24-108">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="fac24-109">*Описание* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fac24-109">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac24-110">Описывает ресурс, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="fac24-110">Describes the resource being shared.</span></span>

</dd> <dt>

<span data-ttu-id="fac24-111">*Доступ к* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="fac24-111">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fac24-112">Дескриптор безопасности для разрешений уровня пользователя.</span><span class="sxs-lookup"><span data-stu-id="fac24-112">Security descriptor for user-level permissions.</span></span> <span data-ttu-id="fac24-113">Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса.</span><span class="sxs-lookup"><span data-stu-id="fac24-113">A security descriptor contains information about the permission, owner, and access capabilities of the resource.</span></span> <span data-ttu-id="fac24-114">Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="fac24-114">For more information, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fac24-115">Требования</span><span class="sxs-lookup"><span data-stu-id="fac24-115">Requirements</span></span>



| <span data-ttu-id="fac24-116">Требование</span><span class="sxs-lookup"><span data-stu-id="fac24-116">Requirement</span></span> | <span data-ttu-id="fac24-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fac24-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac24-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac24-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fac24-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fac24-119">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="fac24-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac24-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fac24-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fac24-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="fac24-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fac24-122">Namespace</span></span><br/>                | <span data-ttu-id="fac24-123">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fac24-123">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fac24-124">MOF</span><span class="sxs-lookup"><span data-stu-id="fac24-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac24-125"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fac24-125"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fac24-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fac24-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac24-127"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac24-127"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac24-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac24-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac24-129">**\_Клустершаре Win32**</span><span class="sxs-lookup"><span data-stu-id="fac24-129">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

