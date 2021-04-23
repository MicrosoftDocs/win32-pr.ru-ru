---
title: Свойство _NewEnum Ивмдвддривеколлектион (Впккоминтерфацес. h)
description: Извлекает перечислитель для коллекции компакт-дисков и дисков DVD.
ms.assetid: e911628b-2a92-41e5-9271-556a297d747d
keywords:
- _NewEnum свойств Virtual PC
- _NewEnum свойств Virtual PC, интерфейс Ивмдвддривеколлектион
- Ивмдвддривеколлектион интерфейс Virtual PC, свойство _NewEnum
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection._NewEnum
- IVMDVDDriveCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfd0de3aaf6b25808d1afa591b0c2099599e6bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988607"
---
# <a name="ivmdvddrivecollection_newenum-property"></a><span data-ttu-id="accba-106">Свойство Ивмдвддривеколлектион:: \_ NewEnum</span><span class="sxs-lookup"><span data-stu-id="accba-106">IVMDVDDriveCollection::\_NewEnum property</span></span>

<span data-ttu-id="accba-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="accba-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="accba-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="accba-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="accba-109">Извлекает перечислитель для коллекции компакт-дисков и дисков DVD.</span><span class="sxs-lookup"><span data-stu-id="accba-109">Retrieves an enumerator for the CD/DVD collection.</span></span>

<span data-ttu-id="accba-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="accba-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="accba-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="accba-111">Syntax</span></span>


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## <a name="property-value"></a><span data-ttu-id="accba-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="accba-112">Property value</span></span>

<span data-ttu-id="accba-113">Перечислитель [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .</span><span class="sxs-lookup"><span data-stu-id="accba-113">The [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) enumerator.</span></span>

## <a name="error-codes"></a><span data-ttu-id="accba-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="accba-114">Error codes</span></span>



| <span data-ttu-id="accba-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="accba-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="accba-116">Значение</span><span class="sxs-lookup"><span data-stu-id="accba-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="accba-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="accba-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="accba-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="accba-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="accba-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="accba-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="accba-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="accba-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="accba-121"><dt>Д \_ Сбой</dt> <dt>0x80004005</dt></span><span class="sxs-lookup"><span data-stu-id="accba-121"><dt>E\_FAIL</dt> <dt>0x80004005</dt></span></span> </dl>            | <span data-ttu-id="accba-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="accba-122">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="accba-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="accba-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="accba-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="accba-124">An unexpected error occurred.</span></span><br/>     |



## <a name="requirements"></a><span data-ttu-id="accba-125">Требования</span><span class="sxs-lookup"><span data-stu-id="accba-125">Requirements</span></span>



| <span data-ttu-id="accba-126">Требование</span><span class="sxs-lookup"><span data-stu-id="accba-126">Requirement</span></span> | <span data-ttu-id="accba-127">Значение</span><span class="sxs-lookup"><span data-stu-id="accba-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="accba-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="accba-128">Minimum supported client</span></span><br/> | <span data-ttu-id="accba-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="accba-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="accba-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="accba-130">Minimum supported server</span></span><br/> | <span data-ttu-id="accba-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="accba-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="accba-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="accba-132">End of client support</span></span><br/>    | <span data-ttu-id="accba-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="accba-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="accba-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="accba-134">Product</span></span><br/>                  | <span data-ttu-id="accba-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="accba-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="accba-136">Header</span><span class="sxs-lookup"><span data-stu-id="accba-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="accba-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="accba-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="accba-138">IID</span><span class="sxs-lookup"><span data-stu-id="accba-138">IID</span></span><br/>                      | <span data-ttu-id="accba-139">IID \_ ивмдвддривеколлектион определен как bc86e297-e55f-4742-9614-ad11d3131f68</span><span class="sxs-lookup"><span data-stu-id="accba-139">IID\_IVMDVDDriveCollection is defined as bc86e297-e55f-4742-9614-ad11d3131f68</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="accba-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="accba-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="accba-141">**ивмдвддривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="accba-141">**IVMDVDDriveCollection**</span></span>](ivmdvddrivecollection.md)
</dt> </dl>

 

