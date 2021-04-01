---
title: Свойство Ивмфлоппидривеколлектион Count (Впккоминтерфацес. h)
description: Число дисководов гибких дисков в этой коллекции.
ms.assetid: d430e5ae-9782-4f88-a5a4-744e79545c7a
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмфлоппидривеколлектион
- Ивмфлоппидривеколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Count
- IVMFloppyDriveCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21b00c13795a633c664cea2c4476d58b346f9108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071985"
---
# <a name="ivmfloppydrivecollectioncount-property"></a><span data-ttu-id="3699a-106">Свойство Ивмфлоппидривеколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="3699a-106">IVMFloppyDriveCollection::Count property</span></span>

<span data-ttu-id="3699a-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="3699a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3699a-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="3699a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3699a-109">Возвращает число дисководов гибких дисков в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="3699a-109">Retrieves the number of floppy drives in this collection.</span></span>

<span data-ttu-id="3699a-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3699a-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3699a-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3699a-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="3699a-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3699a-112">Property value</span></span>

<span data-ttu-id="3699a-113">Число дисководов гибких носителей.</span><span class="sxs-lookup"><span data-stu-id="3699a-113">The number of floppy media drives.</span></span>

## <a name="error-codes"></a><span data-ttu-id="3699a-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="3699a-114">Error codes</span></span>



| <span data-ttu-id="3699a-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="3699a-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="3699a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3699a-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3699a-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3699a-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="3699a-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3699a-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="3699a-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="3699a-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="3699a-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="3699a-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="3699a-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3699a-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="3699a-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="3699a-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="3699a-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3699a-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="3699a-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="3699a-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3699a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="3699a-125">Requirements</span></span>



| <span data-ttu-id="3699a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="3699a-126">Requirement</span></span> | <span data-ttu-id="3699a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="3699a-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3699a-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3699a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3699a-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3699a-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3699a-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3699a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3699a-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="3699a-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3699a-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="3699a-132">End of client support</span></span><br/>    | <span data-ttu-id="3699a-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3699a-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3699a-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="3699a-134">Product</span></span><br/>                  | <span data-ttu-id="3699a-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3699a-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3699a-136">Header</span><span class="sxs-lookup"><span data-stu-id="3699a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3699a-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="3699a-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3699a-138">IID</span><span class="sxs-lookup"><span data-stu-id="3699a-138">IID</span></span><br/>                      | <span data-ttu-id="3699a-139">IID \_ ивмфлоппидривеколлектион определен как 8ba70a25-F698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="3699a-139">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="3699a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3699a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3699a-141">**ивмфлоппидривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="3699a-141">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

