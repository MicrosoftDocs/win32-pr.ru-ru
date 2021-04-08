---
title: Свойство Дривенумбер Ивмфлоппидриве (Впккоминтерфацес. h)
description: Возвращает отсчитываемый от нуля индекс контроллера, к которому подключен флоппи-дисковод.
ms.assetid: 79a40cad-d280-4c67-9214-0532569e47e4
keywords:
- Дривенумбер свойство Virtual PC
- Дривенумбер свойство Virtual PC, интерфейс Ивмфлоппидриве
- Ивмфлоппидриве интерфейс Virtual PC, свойство Дривенумбер
topic_type:
- apiref
api_name:
- IVMFloppyDrive.DriveNumber
- IVMFloppyDrive.get_DriveNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb2f2aeacaf3067515e9e44c58422cd4c9f31fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892077"
---
# <a name="ivmfloppydrivedrivenumber-property"></a><span data-ttu-id="0c1e6-106">Ивмфлоппидриве: свойство Ривенумбер:D</span><span class="sxs-lookup"><span data-stu-id="0c1e6-106">IVMFloppyDrive::DriveNumber property</span></span>

<span data-ttu-id="0c1e6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="0c1e6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="0c1e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="0c1e6-109">Возвращает отсчитываемый от нуля индекс контроллера, к которому подключен флоппи-дисковод.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-109">Retrieves the zero-based index of the controller to which the floppy drive is attached.</span></span>

<span data-ttu-id="0c1e6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c1e6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0c1e6-111">Syntax</span></span>


```C++
HRESULT get_DriveNumber(
  [out, retval] long *driveNumber
);
```



## <a name="property-value"></a><span data-ttu-id="0c1e6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0c1e6-112">Property value</span></span>

<span data-ttu-id="0c1e6-113">Отсчитываемый от нуля индекс контроллера.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-113">The zero-based index of the controller.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0c1e6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="0c1e6-114">Error codes</span></span>



| <span data-ttu-id="0c1e6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="0c1e6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="0c1e6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="0c1e6-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="0c1e6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0c1e6-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="0c1e6-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="0c1e6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="0c1e6-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="0c1e6-121"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e6-121"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="0c1e6-122">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="0c1e6-122">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="0c1e6-123">Требования</span><span class="sxs-lookup"><span data-stu-id="0c1e6-123">Requirements</span></span>



| <span data-ttu-id="0c1e6-124">Требование</span><span class="sxs-lookup"><span data-stu-id="0c1e6-124">Requirement</span></span> | <span data-ttu-id="0c1e6-125">Значение</span><span class="sxs-lookup"><span data-stu-id="0c1e6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c1e6-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c1e6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0c1e6-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c1e6-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c1e6-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c1e6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0c1e6-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="0c1e6-129">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="0c1e6-130">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="0c1e6-130">End of client support</span></span><br/>    | <span data-ttu-id="0c1e6-131">Windows 7</span><span class="sxs-lookup"><span data-stu-id="0c1e6-131">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="0c1e6-132">Продукт</span><span class="sxs-lookup"><span data-stu-id="0c1e6-132">Product</span></span><br/>                  | <span data-ttu-id="0c1e6-133">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="0c1e6-133">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="0c1e6-134">Header</span><span class="sxs-lookup"><span data-stu-id="0c1e6-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c1e6-135"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c1e6-135"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="0c1e6-136">IID</span><span class="sxs-lookup"><span data-stu-id="0c1e6-136">IID</span></span><br/>                      | <span data-ttu-id="0c1e6-137">IID \_ ивмфлоппидриве определен как 661abee6-112a-4ed9-babf-3c874969f10e</span><span class="sxs-lookup"><span data-stu-id="0c1e6-137">IID\_IVMFloppyDrive is defined as 661abee6-112a-4ed9-babf-3c874969f10e</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0c1e6-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c1e6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c1e6-139">**ивмфлоппидриве**</span><span class="sxs-lookup"><span data-stu-id="0c1e6-139">**IVMFloppyDrive**</span></span>](ivmfloppydrive.md)
</dt> </dl>

 

