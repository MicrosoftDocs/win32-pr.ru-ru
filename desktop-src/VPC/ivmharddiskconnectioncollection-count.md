---
title: Свойство Ивмхарддискконнектионколлектион Count (Впккоминтерфацес. h)
description: Возвращает число подключений к жестким дискам в этой коллекции.
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Число свойств Virtual PC
- Число свойств Virtual PC, интерфейс Ивмхарддискконнектионколлектион
- Ивмхарддискконнектионколлектион интерфейс Virtual PC, свойство Count
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f34bbf4d07d7c5967ccfc38e16a743105de8e69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802465"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a><span data-ttu-id="0ea09-106">Свойство Ивмхарддискконнектионколлектион:: count</span><span class="sxs-lookup"><span data-stu-id="0ea09-106">IVMHardDiskConnectionCollection::Count property</span></span>

<span data-ttu-id="0ea09-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0ea09-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0ea09-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0ea09-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0ea09-109">Возвращает число подключений к жестким дискам в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="0ea09-109">Retrieves the number of hard disk connections in this collection.</span></span>

<span data-ttu-id="0ea09-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ea09-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ea09-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ea09-111">Syntax</span></span>


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="0ea09-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0ea09-112">Property value</span></span>

<span data-ttu-id="0ea09-113">Число подключений к жестким дискам.</span><span class="sxs-lookup"><span data-stu-id="0ea09-113">The number of hard disk connections.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0ea09-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0ea09-114">Error codes</span></span>



| <span data-ttu-id="0ea09-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="0ea09-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0ea09-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0ea09-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0ea09-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0ea09-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0ea09-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0ea09-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0ea09-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="0ea09-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0ea09-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0ea09-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0ea09-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="0ea09-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="0ea09-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="0ea09-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="0ea09-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0ea09-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0ea09-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0ea09-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0ea09-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0ea09-125">Requirements</span></span>



| <span data-ttu-id="0ea09-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0ea09-126">Requirement</span></span> | <span data-ttu-id="0ea09-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0ea09-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ea09-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0ea09-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0ea09-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0ea09-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                         |
| <span data-ttu-id="0ea09-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0ea09-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0ea09-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0ea09-131">None supported</span></span><br/>                                                                          |
| <span data-ttu-id="0ea09-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0ea09-132">End of client support</span></span><br/>    | <span data-ttu-id="0ea09-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0ea09-133">Windows 7</span></span><br/>                                                                               |
| <span data-ttu-id="0ea09-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="0ea09-134">Product</span></span><br/>                  | <span data-ttu-id="0ea09-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0ea09-135">Windows Virtual PC</span></span><br/>                                                                      |
| <span data-ttu-id="0ea09-136">Header</span><span class="sxs-lookup"><span data-stu-id="0ea09-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ea09-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ea09-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl>      |
| <span data-ttu-id="0ea09-138">IID</span><span class="sxs-lookup"><span data-stu-id="0ea09-138">IID</span></span><br/>                      | <span data-ttu-id="0ea09-139">IID \_ ивмхарддискконнектионколлектион определен как b9f2caf4-0aeb-4085-B105-ceddb90dbf62</span><span class="sxs-lookup"><span data-stu-id="0ea09-139">IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ea09-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ea09-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea09-141">**ивмхарддискконнектионколлектион**</span><span class="sxs-lookup"><span data-stu-id="0ea09-141">**IVMHardDiskConnectionCollection**</span></span>](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

