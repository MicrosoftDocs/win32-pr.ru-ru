---
description: Получает системные сертификаты в системе узла.
ms.assetid: d470a57d-85b9-4d31-bb2c-9b6f21e2860d
title: Метод Жетсистемцертификатес класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.GetSystemCertificates
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5464d420b7fc019a0829d7255dafb1716e5e9f5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540346"
---
# <a name="getsystemcertificates-method-of-the-msvm_replicationservice-class"></a><span data-ttu-id="b99fb-103">Метод Жетсистемцертификатес \_ класса Репликатионсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="b99fb-103">GetSystemCertificates method of the Msvm\_ReplicationService class</span></span>

<span data-ttu-id="b99fb-104">Получает системные сертификаты в системе узла.</span><span class="sxs-lookup"><span data-stu-id="b99fb-104">Retrieves the system certificates on a host system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b99fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b99fb-105">Syntax</span></span>


```mof
uint32 GetSystemCertificates(
  [out] string EncodedCertificates[]
);
```



## <a name="parameters"></a><span data-ttu-id="b99fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b99fb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b99fb-107">*Енкодедцертификатес* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b99fb-107">*EncodedCertificates* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b99fb-108">В случае успеха получает сертификаты, доступные в личном хранилище для локального компьютера.</span><span class="sxs-lookup"><span data-stu-id="b99fb-108">If successful, receives the certificates available from the Personal store for the local machine.</span></span> <span data-ttu-id="b99fb-109">Каждая запись представляет собой строку сертификата в кодировке Base 64.</span><span class="sxs-lookup"><span data-stu-id="b99fb-109">Each entry is a base 64 encoded certificate string.</span></span> <span data-ttu-id="b99fb-110">Эту строку можно преобразовать в массив байтов, создав объект X509Certificate2.</span><span class="sxs-lookup"><span data-stu-id="b99fb-110">This string can be converted to a byte array by constructing an X509Certificate2 object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b99fb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b99fb-111">Return value</span></span>

<span data-ttu-id="b99fb-112">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b99fb-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b99fb-113">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="b99fb-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-114">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="b99fb-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-115">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="b99fb-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-116">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="b99fb-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-117">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="b99fb-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-118">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="b99fb-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-119">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="b99fb-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-120">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="b99fb-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-121">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="b99fb-121">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-122">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="b99fb-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-123">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="b99fb-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-124">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="b99fb-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-125">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="b99fb-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="b99fb-126">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="b99fb-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="b99fb-127">Требования</span><span class="sxs-lookup"><span data-stu-id="b99fb-127">Requirements</span></span>



| <span data-ttu-id="b99fb-128">Требование</span><span class="sxs-lookup"><span data-stu-id="b99fb-128">Requirement</span></span> | <span data-ttu-id="b99fb-129">Значение</span><span class="sxs-lookup"><span data-stu-id="b99fb-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b99fb-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b99fb-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b99fb-131">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="b99fb-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b99fb-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b99fb-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b99fb-133">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="b99fb-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b99fb-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b99fb-134">Namespace</span></span><br/>                | <span data-ttu-id="b99fb-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="b99fb-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b99fb-136">MOF</span><span class="sxs-lookup"><span data-stu-id="b99fb-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b99fb-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b99fb-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b99fb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b99fb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b99fb-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b99fb-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b99fb-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b99fb-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b99fb-141">**Мсвм \_ репликатионсервице**</span><span class="sxs-lookup"><span data-stu-id="b99fb-141">**Msvm\_ReplicationService**</span></span>](msvm-replicationservice.md)
</dt> </dl>

 

 




