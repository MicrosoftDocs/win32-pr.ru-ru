---
title: Метод Рдвундовмпермиссионс класса Win32_RdvhManagement
description: Отмена разрешений, установленных Рдвсетупвмпермиссионс на указанной виртуальной машине.
ms.assetid: 3331430e-7427-42f7-ab09-27fece8dc3ca
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Рдвундовмпермиссионс
- Службы удаленных рабочих столов метода Рдвундовмпермиссионс, класс Win32_RdvhManagement
- Класс Win32_RdvhManagement службы удаленных рабочих столов, метод Рдвундовмпермиссионс
topic_type:
- apiref
api_name:
- Win32_RdvhManagement.RdvUndoVMPermissions
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1dc8892435522dcd2c7457fe4b74a0d9671740
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492759"
---
# <a name="rdvundovmpermissions-method-of-the-win32_rdvhmanagement-class"></a><span data-ttu-id="044e5-106">Метод Рдвундовмпермиссионс \_ класса Win32 рдвхманажемент</span><span class="sxs-lookup"><span data-stu-id="044e5-106">RdvUndoVMPermissions method of the Win32\_RdvhManagement class</span></span>

<span data-ttu-id="044e5-107">Отмена разрешений, установленных [**рдвсетупвмпермиссионс**](rdvsetupvmpermissions-win32-rdvhmanagement.md) на указанной виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="044e5-107">Reverts permissions set by [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md) on the specified virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="044e5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="044e5-108">Syntax</span></span>


```mof
uint32 RdvUndoVMPermissions(
  [in] string VmName
);
```



## <a name="parameters"></a><span data-ttu-id="044e5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="044e5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="044e5-110">*VmName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="044e5-110">*VmName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="044e5-111">Имя виртуальной машины для отмены разрешений.</span><span class="sxs-lookup"><span data-stu-id="044e5-111">Name of the virtual machine to undo permissions on.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="044e5-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="044e5-112">Return value</span></span>

<span data-ttu-id="044e5-113">Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.</span><span class="sxs-lookup"><span data-stu-id="044e5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="044e5-114">Список этих значений см. в разделе [службы удаленных рабочих столов коды ошибок поставщика WMI](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="044e5-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="044e5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="044e5-115">Requirements</span></span>



| <span data-ttu-id="044e5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="044e5-116">Requirement</span></span> | <span data-ttu-id="044e5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="044e5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="044e5-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="044e5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="044e5-119">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="044e5-119">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="044e5-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="044e5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="044e5-121">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="044e5-121">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="044e5-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="044e5-122">Namespace</span></span><br/>                | <span data-ttu-id="044e5-123">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="044e5-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="044e5-124">MOF</span><span class="sxs-lookup"><span data-stu-id="044e5-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="044e5-125"><dt>Тсвмхост. mof</dt></span><span class="sxs-lookup"><span data-stu-id="044e5-125"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="044e5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="044e5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="044e5-127"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="044e5-127"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="044e5-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="044e5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="044e5-129">**\_Рдвхманажемент Win32**</span><span class="sxs-lookup"><span data-stu-id="044e5-129">**Win32\_RdvhManagement**</span></span>](win32-rdvhmanagement.md)
</dt> </dl>

 

 





