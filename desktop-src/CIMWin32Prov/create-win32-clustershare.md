---
description: Создает новый экземпляр Win32 \_ клустершаре.
ms.assetid: a6fde28d-f19e-4a31-8f0d-35927c75a030
ms.tgt_platform: multiple
title: Метод Create класса Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7cbf7c42b8523bcd12b19e9b474ecc50bd031939
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142751"
---
# <a name="create-method-of-the-win32_clustershare-class"></a><span data-ttu-id="f8970-103">Метод Create \_ класса Win32 клустершаре</span><span class="sxs-lookup"><span data-stu-id="f8970-103">Create method of the Win32\_ClusterShare class</span></span>

<span data-ttu-id="f8970-104">Создает новый экземпляр [**Win32 \_ клустершаре**](win32-clustershare.md) .</span><span class="sxs-lookup"><span data-stu-id="f8970-104">Creates a new [**Win32\_ClusterShare**](win32-clustershare.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8970-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8970-105">Syntax</span></span>


```mof
static uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a><span data-ttu-id="f8970-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8970-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8970-107">*Путь* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8970-107">*Path* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-108">Локальный путь к общей папке Windows.</span><span class="sxs-lookup"><span data-stu-id="f8970-108">Local path of the Windows share.</span></span>

<span data-ttu-id="f8970-109">Например, "C: \\ Program Files".</span><span class="sxs-lookup"><span data-stu-id="f8970-109">Example, "C:\\Program Files".</span></span>

</dd> <dt>

<span data-ttu-id="f8970-110">*Имя* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8970-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-111">Псевдоним для пути, настроенного в качестве общего ресурса в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="f8970-111">The alias to a path set up as a share on a computer system running Windows.</span></span>

<span data-ttu-id="f8970-112">Например, "Public".</span><span class="sxs-lookup"><span data-stu-id="f8970-112">Example, "public".</span></span>

</dd> <dt>

<span data-ttu-id="f8970-113">*Тип* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8970-113">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-114">Тип ресурса, к которому предоставляется общий доступ.</span><span class="sxs-lookup"><span data-stu-id="f8970-114">Type of resource being shared.</span></span> <span data-ttu-id="f8970-115">К типам относятся: дисковые накопители, очереди печати, межпроцессное взаимодействие (IPC) и общие устройства.</span><span class="sxs-lookup"><span data-stu-id="f8970-115">Types include: disk drives, print queues, interprocess communications (IPC), and general devices.</span></span>

<dt>

<span data-ttu-id="f8970-116">0 (0x0)</span><span class="sxs-lookup"><span data-stu-id="f8970-116">0 (0x0)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-117">Диск</span><span class="sxs-lookup"><span data-stu-id="f8970-117">Disk Drive</span></span>

</dd> <dt>

<span data-ttu-id="f8970-118">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="f8970-118">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-119">Очередь печати</span><span class="sxs-lookup"><span data-stu-id="f8970-119">Print Queue</span></span>

</dd> <dt>

<span data-ttu-id="f8970-120">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="f8970-120">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-121">Устройство</span><span class="sxs-lookup"><span data-stu-id="f8970-121">Device</span></span>

</dd> <dt>

<span data-ttu-id="f8970-122">3 (0x3)</span><span class="sxs-lookup"><span data-stu-id="f8970-122">3 (0x3)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-123">IPC</span><span class="sxs-lookup"><span data-stu-id="f8970-123">IPC</span></span>

</dd> <dt>

<span data-ttu-id="f8970-124">2147483648 (0x80000000)</span><span class="sxs-lookup"><span data-stu-id="f8970-124">2147483648 (0x80000000)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-125">Администратор диска</span><span class="sxs-lookup"><span data-stu-id="f8970-125">Disk Drive Admin</span></span>

</dd> <dt>

<span data-ttu-id="f8970-126">2147483649 (0x80000001)</span><span class="sxs-lookup"><span data-stu-id="f8970-126">2147483649 (0x80000001)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-127">Администратор очереди печати</span><span class="sxs-lookup"><span data-stu-id="f8970-127">Print Queue Admin</span></span>

</dd> <dt>

<span data-ttu-id="f8970-128">2147483650 (0x80000002)</span><span class="sxs-lookup"><span data-stu-id="f8970-128">2147483650 (0x80000002)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-129">Администратор устройства</span><span class="sxs-lookup"><span data-stu-id="f8970-129">Device Admin</span></span>

</dd> <dt>

<span data-ttu-id="f8970-130">2147483651 (0x80000003)</span><span class="sxs-lookup"><span data-stu-id="f8970-130">2147483651 (0x80000003)</span></span>
</dt> <dd>

<span data-ttu-id="f8970-131">Администратор IPC</span><span class="sxs-lookup"><span data-stu-id="f8970-131">IPC Admin</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="f8970-132">*MaximumAllowed* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f8970-132">*MaximumAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-133">Максимальное число пользователей, которым разрешено использовать этот ресурс одновременно.</span><span class="sxs-lookup"><span data-stu-id="f8970-133">Limit on the maximum number of users allowed to use this resource concurrently.</span></span>

</dd> <dt>

<span data-ttu-id="f8970-134">*Описание* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f8970-134">*Description* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-135">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f8970-135">Description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="f8970-136">*Пароль* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f8970-136">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-137">TBD</span><span class="sxs-lookup"><span data-stu-id="f8970-137">TBD</span></span>

</dd> <dt>

<span data-ttu-id="f8970-138">*Доступ к* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="f8970-138">*Access* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f8970-139">Необязательный встроенный экземпляр класса [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) , который содержит дескриптор безопасности для нового общего ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8970-139">Optional embedded instance of a [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class that contains the security descriptor for the new share.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f8970-140">Требования</span><span class="sxs-lookup"><span data-stu-id="f8970-140">Requirements</span></span>



| <span data-ttu-id="f8970-141">Требование</span><span class="sxs-lookup"><span data-stu-id="f8970-141">Requirement</span></span> | <span data-ttu-id="f8970-142">Значение</span><span class="sxs-lookup"><span data-stu-id="f8970-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8970-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f8970-143">Minimum supported client</span></span><br/> | <span data-ttu-id="f8970-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f8970-144">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="f8970-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f8970-145">Minimum supported server</span></span><br/> | <span data-ttu-id="f8970-146">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f8970-146">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="f8970-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f8970-147">Namespace</span></span><br/>                | <span data-ttu-id="f8970-148">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f8970-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f8970-149">MOF</span><span class="sxs-lookup"><span data-stu-id="f8970-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f8970-150"><dt>Cimwin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f8970-150"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f8970-151">DLL</span><span class="sxs-lookup"><span data-stu-id="f8970-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f8970-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8970-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8970-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8970-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8970-154">**\_Клустершаре Win32**</span><span class="sxs-lookup"><span data-stu-id="f8970-154">**Win32\_ClusterShare**</span></span>](win32-clustershare.md)
</dt> </dl>

 

