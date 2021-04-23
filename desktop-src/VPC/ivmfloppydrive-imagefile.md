---
title: Свойство ImageFile Ивмфлоппидриве (Впккоминтерфацес. h)
description: Извлекает полный путь к файлу изображения, к которому подключен гибкий диск.
ms.assetid: fc87e438-e5d4-494d-8ac2-27a4312ee81d
keywords:
- Свойство ImageFile Virtual PC
- Свойство ImageFile Virtual PC, интерфейс Ивмфлоппидриве
- Интерфейс Ивмфлоппидриве Virtual PC, свойство ImageFile
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ImageFile
- IVMFloppyDrive.get_ImageFile
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa18c4a1da3137613e0106f828f59805e5615384
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071836"
---
# <a name="ivmfloppydriveimagefile-property"></a><span data-ttu-id="00f12-106">Свойство Ивмфлоппидриве:: ImageFile</span><span class="sxs-lookup"><span data-stu-id="00f12-106">IVMFloppyDrive::ImageFile property</span></span>

<span data-ttu-id="00f12-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="00f12-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="00f12-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="00f12-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="00f12-109">Извлекает полный путь к файлу изображения, к которому подключен гибкий диск.</span><span class="sxs-lookup"><span data-stu-id="00f12-109">Retrieves the full path of the image file to which the floppy drive is attached.</span></span>

<span data-ttu-id="00f12-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="00f12-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="00f12-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00f12-111">Syntax</span></span>


```C++
HRESULT get_ImageFile(
  [out, retval] BSTR *imageFile
);
```



## <a name="property-value"></a><span data-ttu-id="00f12-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="00f12-112">Property value</span></span>

<span data-ttu-id="00f12-113">Полный путь к файлу изображения.</span><span class="sxs-lookup"><span data-stu-id="00f12-113">The full path of the image file.</span></span>

## <a name="error-codes"></a><span data-ttu-id="00f12-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="00f12-114">Error codes</span></span>



| <span data-ttu-id="00f12-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="00f12-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="00f12-116">Значение</span><span class="sxs-lookup"><span data-stu-id="00f12-116">Meaning</span></span>                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="00f12-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="00f12-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="00f12-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="00f12-118">The operation was successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="00f12-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="00f12-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="00f12-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="00f12-120">The parameter is **NULL**.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="00f12-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="00f12-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="00f12-122">Конфигурация этой виртуальной машины недопустима или не найдена.</span><span class="sxs-lookup"><span data-stu-id="00f12-122">The configuration for this virtual machine is not valid or cannot be found.</span></span><br/> |
| <dl> <span data-ttu-id="00f12-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="00f12-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="00f12-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="00f12-124">An unexpected error has occurred.</span></span><br/>                                           |



## <a name="requirements"></a><span data-ttu-id="00f12-125">Требования</span><span class="sxs-lookup"><span data-stu-id="00f12-125">Requirements</span></span>



| <span data-ttu-id="00f12-126">Требование</span><span class="sxs-lookup"><span data-stu-id="00f12-126">Requirement</span></span> | <span data-ttu-id="00f12-127">Значение</span><span class="sxs-lookup"><span data-stu-id="00f12-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="00f12-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00f12-128">Minimum supported client</span></span><br/> | <span data-ttu-id="00f12-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="00f12-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="00f12-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00f12-130">Minimum supported server</span></span><br/> | <span data-ttu-id="00f12-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="00f12-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="00f12-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="00f12-132">End of client support</span></span><br/>    | <span data-ttu-id="00f12-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="00f12-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="00f12-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="00f12-134">Product</span></span><br/>                  | <span data-ttu-id="00f12-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="00f12-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="00f12-136">Header</span><span class="sxs-lookup"><span data-stu-id="00f12-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f12-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f12-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="00f12-138">IID</span><span class="sxs-lookup"><span data-stu-id="00f12-138">IID</span></span><br/>                      | <span data-ttu-id="00f12-139">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="00f12-139">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="00f12-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="00f12-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00f12-141">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="00f12-141">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

