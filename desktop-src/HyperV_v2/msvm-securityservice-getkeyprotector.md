---
description: Извлекает предохранитель ключа для виртуальной системы.
ms.assetid: fd827da8-b2fc-4c57-bb7d-7da46db8e8be
title: Метод Жеткэйпротектор класса Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.GetKeyProtector
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 49f2479660d0402c7b3d428c76f9fe454ecf64cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350652"
---
# <a name="getkeyprotector-method-of-the-msvm_securityservice-class"></a><span data-ttu-id="f26b5-103">Метод Жеткэйпротектор \_ класса SecurityService мсвм</span><span class="sxs-lookup"><span data-stu-id="f26b5-103">GetKeyProtector method of the Msvm\_SecurityService class</span></span>

<span data-ttu-id="f26b5-104">Извлекает предохранитель ключа для виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f26b5-104">Retrieves the key protector for a virtual system.</span></span>

## <a name="syntax"></a><span data-ttu-id="f26b5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f26b5-105">Syntax</span></span>


```mof
uint32 GetKeyProtector(
  [in]  string SecuritySettingData,
  [out] uint8  KeyProtector[]
);
```



## <a name="parameters"></a><span data-ttu-id="f26b5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f26b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f26b5-107">*Секуритисеттингдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f26b5-107">*SecuritySettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f26b5-108">Строка содержит встроенный экземпляр класса [**мсвм \_ секуритисеттингдата**](msvm-securitysettingdata.md) , представляющий параметры безопасности виртуальной системы.</span><span class="sxs-lookup"><span data-stu-id="f26b5-108">String contains an embedded instance of the [**Msvm\_SecuritySettingData**](msvm-securitysettingdata.md) class representing the security settings of a virtual system.</span></span>

</dd> <dt>

<span data-ttu-id="f26b5-109">*Кэйпротектор* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f26b5-109">*KeyProtector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f26b5-110">Получает необработанный массив байтов, содержащий предохранитель ключа, который используется в данный момент.</span><span class="sxs-lookup"><span data-stu-id="f26b5-110">Receives the raw byte array that contains the key protector currently in use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f26b5-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f26b5-111">Return value</span></span>

<span data-ttu-id="f26b5-112">При успешном выполнении возвращает 0 или 4096.</span><span class="sxs-lookup"><span data-stu-id="f26b5-112">On success, returns a 0 or 4096.</span></span> <span data-ttu-id="f26b5-113">В противном случае возвращает ошибку.</span><span class="sxs-lookup"><span data-stu-id="f26b5-113">Otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="f26b5-114">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="f26b5-114">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-115">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="f26b5-115">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-116">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="f26b5-116">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-117">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="f26b5-117">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-118">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="f26b5-118">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-119">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="f26b5-119">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-120">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="f26b5-120">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-121">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="f26b5-121">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-122">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="f26b5-122">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-123">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="f26b5-123">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-124">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="f26b5-124">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-125">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="f26b5-125">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f26b5-126">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="f26b5-126">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f26b5-127">Требования</span><span class="sxs-lookup"><span data-stu-id="f26b5-127">Requirements</span></span>



| <span data-ttu-id="f26b5-128">Требование</span><span class="sxs-lookup"><span data-stu-id="f26b5-128">Requirement</span></span> | <span data-ttu-id="f26b5-129">Значение</span><span class="sxs-lookup"><span data-stu-id="f26b5-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f26b5-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f26b5-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f26b5-131">\[Только для настольных приложений Windows 10 версии 1703\]</span><span class="sxs-lookup"><span data-stu-id="f26b5-131">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f26b5-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f26b5-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f26b5-133">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="f26b5-133">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="f26b5-134">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f26b5-134">Namespace</span></span><br/>                | <span data-ttu-id="f26b5-135">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="f26b5-135">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f26b5-136">MOF</span><span class="sxs-lookup"><span data-stu-id="f26b5-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f26b5-137"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f26b5-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f26b5-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f26b5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f26b5-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f26b5-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f26b5-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f26b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f26b5-141">**Мсвм \_ SecurityService**</span><span class="sxs-lookup"><span data-stu-id="f26b5-141">**Msvm\_SecurityService**</span></span>](msvm-securityservice.md)
</dt> </dl>

 

 




