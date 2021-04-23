---
title: Метод Рдвсетупвмпермиссионс класса Win32_RdvhManagement
description: Устанавливает разрешения на виртуальную машину для текущего пользователя.
ms.assetid: 6ac45983-d468-4a3b-875f-48717ba23ed0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвсетупвмпермиссионс
- Службы удаленных рабочих столов метода Рдвсетупвмпермиссионс, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвсетупвмпермиссионс
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvSetupVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd8028a33bc772f9dd37f25a1dc22074baf771b6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490605"
---
# <a name="rdvsetupvmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="a380a-106">Метод Рдвсетупвмпермиссионс \_ класса Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="a380a-106">RdvSetupVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="a380a-107">Устанавливает разрешения на виртуальную машину для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="a380a-107">Sets the permissions on a virtual machine for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a380a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a380a-108">Syntax</span></span>


```mof
uint32 RdvSetupVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="a380a-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a380a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a380a-110">*VmName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a380a-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a380a-111">Имя виртуальной машины, для которой нужно задать разрешения.</span><span class="sxs-lookup"><span data-stu-id="a380a-111">The name of the virtual machine to set permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a380a-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a380a-112">Return value</span></span>

<span data-ttu-id="a380a-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="a380a-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a380a-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a380a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a380a-115">Требования</span><span class="sxs-lookup"><span data-stu-id="a380a-115">Requirements</span></span>



| <span data-ttu-id="a380a-116">Требование</span><span class="sxs-lookup"><span data-stu-id="a380a-116">Requirement</span></span> | <span data-ttu-id="a380a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="a380a-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a380a-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a380a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a380a-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a380a-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="a380a-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a380a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a380a-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a380a-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a380a-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a380a-122">Namespace</span></span><br/>                | <span data-ttu-id="a380a-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="a380a-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="a380a-124">MOF</span><span class="sxs-lookup"><span data-stu-id="a380a-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a380a-125"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a380a-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a380a-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a380a-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a380a-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a380a-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a380a-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a380a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a380a-129">**\_Рдвхманажемент Win32**</span><span class="sxs-lookup"><span data-stu-id="a380a-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





