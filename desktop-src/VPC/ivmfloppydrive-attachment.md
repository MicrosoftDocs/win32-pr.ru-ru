---
title: Свойство вложения Ивмфлоппидриве (Впккоминтерфацес. h)
description: Возвращает тип носителя, подключенного к дисководу гибких дисков в виртуальной машине.
ms.assetid: 0b7e43ac-de56-4c4b-82e6-75877aea06f2
keywords:
- Свойство вложения Virtual PC
- Свойство вложения Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, свойство вложения
topic_type:
- apiref
api_name:
- IVMFloppyDrive.Attachment
- IVMFloppyDrive.get_Attachment
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44814148baf27672f30b8e3c5015d841aaaba4b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691858"
---
# <a name="ivmfloppydriveattachment-property"></a><span data-ttu-id="f1571-106">Свойство Ивмфлоппидриве:: вложение</span><span class="sxs-lookup"><span data-stu-id="f1571-106">IVMFloppyDrive::Attachment property</span></span>

<span data-ttu-id="f1571-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1571-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f1571-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="f1571-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f1571-109">Возвращает тип носителя, подключенного к дисководу гибких дисков виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f1571-109">Retrieves the type of media attached to the floppy drive in the virtual machine (VM).</span></span>

<span data-ttu-id="f1571-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f1571-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1571-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f1571-111">Syntax</span></span>


```C++
HRESULT get_Attachment(
  [out, retval] VMFloppyDriveAttachmentType *driveAttachment
);
```



## <a name="property-value"></a><span data-ttu-id="f1571-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f1571-112">Property value</span></span>

<span data-ttu-id="f1571-113">Тип носителя.</span><span class="sxs-lookup"><span data-stu-id="f1571-113">The type of media.</span></span> <span data-ttu-id="f1571-114">Список значений см. в разделе [**вмфлоппидривеаттачменттипе**](vmfloppydriveattachmenttype.md).</span><span class="sxs-lookup"><span data-stu-id="f1571-114">For a list of values, see [**VMFloppyDriveAttachmentType**](vmfloppydriveattachmenttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="f1571-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="f1571-115">Error codes</span></span>



| <span data-ttu-id="f1571-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="f1571-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="f1571-117">Значение</span><span class="sxs-lookup"><span data-stu-id="f1571-117">Meaning</span></span>                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1571-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f1571-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="f1571-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f1571-119">The operation was successful.</span></span><br/>                                  |
| <dl> <span data-ttu-id="f1571-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="f1571-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="f1571-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f1571-121">The parameter is **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="f1571-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="f1571-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="f1571-123">Конфигурация для этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="f1571-123">The configuration for this VM is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="f1571-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f1571-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="f1571-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="f1571-125">An unexpected error has occurred.</span></span><br/>                              |



## <a name="requirements"></a><span data-ttu-id="f1571-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f1571-126">Requirements</span></span>



| <span data-ttu-id="f1571-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f1571-127">Requirement</span></span> | <span data-ttu-id="f1571-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f1571-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1571-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1571-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f1571-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f1571-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f1571-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1571-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f1571-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="f1571-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f1571-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f1571-133">End of client support</span></span><br/>    | <span data-ttu-id="f1571-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f1571-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f1571-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="f1571-135">Product</span></span><br/>                  | <span data-ttu-id="f1571-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f1571-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f1571-137">Header</span><span class="sxs-lookup"><span data-stu-id="f1571-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1571-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1571-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f1571-139">IID</span><span class="sxs-lookup"><span data-stu-id="f1571-139">IID</span></span><br/>                      | <span data-ttu-id="f1571-140">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="f1571-140">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f1571-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f1571-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1571-142">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="f1571-142">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

