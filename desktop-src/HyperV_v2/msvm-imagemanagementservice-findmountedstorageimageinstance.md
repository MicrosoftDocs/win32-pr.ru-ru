---
description: Находит \_ объект Маунтедсторажеимаже мсвм для указанного пути к образу диска.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Метод Финдмаунтедсторажеимажеинстанце класса Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542471"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="0100f-103">Метод Финдмаунтедсторажеимажеинстанце \_ класса) мсвм</span><span class="sxs-lookup"><span data-stu-id="0100f-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="0100f-104">Находит объект [**\_ маунтедсторажеимаже мсвм**](msvm-mountedstorageimage.md) для указанного пути к образу диска.</span><span class="sxs-lookup"><span data-stu-id="0100f-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="0100f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0100f-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="0100f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0100f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0100f-107">*Селектионкритерион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0100f-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0100f-108">Полный путь, указывающий расположение файла образа диска.</span><span class="sxs-lookup"><span data-stu-id="0100f-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="0100f-109">*Критерионтипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0100f-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0100f-110">Тип критерия, который нужно найти при поиске образа диска.</span><span class="sxs-lookup"><span data-stu-id="0100f-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="0100f-111">**неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="0100f-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="0100f-112">**Путь** (2)</span><span class="sxs-lookup"><span data-stu-id="0100f-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="0100f-113">*Изображение* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0100f-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0100f-114">Ссылка на [**\_ маунтедсторажеимаже мсвм**](msvm-mountedstorageimage.md) (может иметь значение null, если образ не подключен).</span><span class="sxs-lookup"><span data-stu-id="0100f-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0100f-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0100f-115">Return value</span></span>

<span data-ttu-id="0100f-116">Этот метод возвращает одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="0100f-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="0100f-117">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="0100f-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-118">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="0100f-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-119">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="0100f-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-120">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="0100f-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-121">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="0100f-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-122">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="0100f-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-123">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="0100f-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-124">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="0100f-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-125">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="0100f-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-126">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="0100f-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-127">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="0100f-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-128">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="0100f-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-129">**Файл не найден** (32779)</span><span class="sxs-lookup"><span data-stu-id="0100f-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="0100f-130">**Объект не найден** (32789)</span><span class="sxs-lookup"><span data-stu-id="0100f-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="0100f-131">Требования</span><span class="sxs-lookup"><span data-stu-id="0100f-131">Requirements</span></span>



| <span data-ttu-id="0100f-132">Требование</span><span class="sxs-lookup"><span data-stu-id="0100f-132">Requirement</span></span> | <span data-ttu-id="0100f-133">Значение</span><span class="sxs-lookup"><span data-stu-id="0100f-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0100f-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0100f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0100f-135">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0100f-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="0100f-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0100f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0100f-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="0100f-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="0100f-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0100f-138">Namespace</span></span><br/>                | <span data-ttu-id="0100f-139">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0100f-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0100f-140">MOF</span><span class="sxs-lookup"><span data-stu-id="0100f-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0100f-141"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0100f-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0100f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="0100f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0100f-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0100f-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0100f-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0100f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0100f-145">**Мсвм \_ )**</span><span class="sxs-lookup"><span data-stu-id="0100f-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




