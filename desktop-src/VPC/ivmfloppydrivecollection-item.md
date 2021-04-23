---
title: Свойство Item Ивмфлоппидривеколлектион (Впккоминтерфацес. h)
description: Объект флоппи-дисковода, соответствующий указанному индексу.
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмфлоппидривеколлектион
- Интерфейс Ивмфлоппидривеколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137487"
---
# <a name="ivmfloppydrivecollectionitem-property"></a><span data-ttu-id="58b3f-106">Свойство Ивмфлоппидривеколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="58b3f-106">IVMFloppyDriveCollection::Item property</span></span>

<span data-ttu-id="58b3f-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="58b3f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="58b3f-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="58b3f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="58b3f-109">Извлекает объект флоппи-дисковода, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="58b3f-109">Retrieves the floppy object that corresponds to the specified index.</span></span>

<span data-ttu-id="58b3f-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="58b3f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="58b3f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="58b3f-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a><span data-ttu-id="58b3f-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="58b3f-112">Property value</span></span>

<span data-ttu-id="58b3f-113">Объект [**ивмфлоппидриве**](ivmfloppydrive.md) .</span><span class="sxs-lookup"><span data-stu-id="58b3f-113">The [**IVMFloppyDrive**](ivmfloppydrive.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="58b3f-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="58b3f-114">Error codes</span></span>



| <span data-ttu-id="58b3f-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="58b3f-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="58b3f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="58b3f-116">Meaning</span></span>                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="58b3f-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="58b3f-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="58b3f-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="58b3f-118">The operation was successful.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="58b3f-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="58b3f-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="58b3f-120">Параметр *флоппидриве* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="58b3f-120">The *floppyDrive* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="58b3f-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="58b3f-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="58b3f-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="58b3f-122">The index of the requested item does not correspond to an item in this collection.</span></span><br/> |
| <dl> <span data-ttu-id="58b3f-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="58b3f-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="58b3f-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="58b3f-124">The configuration is unknown.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="58b3f-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="58b3f-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="58b3f-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="58b3f-126">An unexpected error has occurred.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="58b3f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="58b3f-127">Requirements</span></span>



| <span data-ttu-id="58b3f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="58b3f-128">Requirement</span></span> | <span data-ttu-id="58b3f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="58b3f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="58b3f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58b3f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="58b3f-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="58b3f-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="58b3f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58b3f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="58b3f-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="58b3f-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="58b3f-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="58b3f-134">End of client support</span></span><br/>    | <span data-ttu-id="58b3f-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="58b3f-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="58b3f-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="58b3f-136">Product</span></span><br/>                  | <span data-ttu-id="58b3f-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="58b3f-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="58b3f-138">Header</span><span class="sxs-lookup"><span data-stu-id="58b3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="58b3f-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="58b3f-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="58b3f-140">IID</span><span class="sxs-lookup"><span data-stu-id="58b3f-140">IID</span></span><br/>                      | <span data-ttu-id="58b3f-141">IID \_ ивмфлоппидривеколлектион определен как 8ba70a25-F698-4ee5-85CE-3cc93a925516</span><span class="sxs-lookup"><span data-stu-id="58b3f-141">IID\_IVMFloppyDriveCollection is defined as 8ba70a25-f698-4ee5-85ce-3cc93a925516</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="58b3f-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="58b3f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58b3f-143">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="58b3f-143">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> <dt>

[<span data-ttu-id="58b3f-144">**ивмфлоппидривеколлектион**</span><span class="sxs-lookup"><span data-stu-id="58b3f-144">**IVMFloppyDriveCollection**</span></span>](ivmfloppydrivecollection.md)
</dt> </dl>

 

