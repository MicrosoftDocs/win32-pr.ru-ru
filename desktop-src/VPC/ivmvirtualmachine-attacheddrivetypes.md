---
title: Свойство Аттачеддриветипес Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Массив, указывающий тип диска, подключенного к каждому расположению в виртуальной машине.
ms.assetid: 6896c9cd-5448-4fbb-8c8e-eef306a5cea1
keywords:
- Аттачеддриветипес свойство Virtual PC
- Аттачеддриветипес свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Аттачеддриветипес
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AttachedDriveTypes
- IVMVirtualMachine.get_AttachedDriveTypes
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5f01802b7fa7e3a4f1ccbfc1b5c4bf70e06614
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137215"
---
# <a name="ivmvirtualmachineattacheddrivetypes-property"></a><span data-ttu-id="49a25-106">Свойство Ивмвиртуалмачине:: Аттачеддриветипес</span><span class="sxs-lookup"><span data-stu-id="49a25-106">IVMVirtualMachine::AttachedDriveTypes property</span></span>

<span data-ttu-id="49a25-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="49a25-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="49a25-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="49a25-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="49a25-109">Извлекает массив, указывающий тип диска, подключенного к каждому расположению виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="49a25-109">Retrieves an array indicating the type of drive attached to each location in the virtual machine (VM).</span></span>

<span data-ttu-id="49a25-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="49a25-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a25-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49a25-111">Syntax</span></span>


```C++
HRESULT get_AttachedDriveTypes(
  [out, retval] VARIANT *driveTypes
);
```



## <a name="property-value"></a><span data-ttu-id="49a25-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="49a25-112">Property value</span></span>

<span data-ttu-id="49a25-113">Вариант типа VT **\_ Array** \| **VT \_** , содержащий записи типа **VT \_ UI1**.</span><span class="sxs-lookup"><span data-stu-id="49a25-113">A variant of type **VT\_ARRAY** \| **VT\_VARIANT** containing entries of type **VT\_UI1**.</span></span> <span data-ttu-id="49a25-114">Массив содержит значение [**вмдриветипе**](vmdrivetype.md) для каждого устройства, подключенного к каждому расположению шины.</span><span class="sxs-lookup"><span data-stu-id="49a25-114">The array contains the [**VMDriveType**](vmdrivetype.md) value of each device connected to every bus location.</span></span> <span data-ttu-id="49a25-115">Массив упорядочивается по идентификатору \[  \] \[ *deviceID* буснумбер \] .</span><span class="sxs-lookup"><span data-stu-id="49a25-115">The array is ordered by \[*busNumber*\]\[*deviceID*\].</span></span>

## <a name="error-codes"></a><span data-ttu-id="49a25-116">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="49a25-116">Error codes</span></span>



| <span data-ttu-id="49a25-117">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="49a25-117">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="49a25-118">Значение</span><span class="sxs-lookup"><span data-stu-id="49a25-118">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="49a25-119"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="49a25-119"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="49a25-120">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49a25-120">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="49a25-121"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="49a25-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="49a25-122">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="49a25-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="49a25-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a25-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="49a25-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="49a25-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="49a25-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="49a25-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="49a25-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="49a25-126">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="49a25-127">Требования</span><span class="sxs-lookup"><span data-stu-id="49a25-127">Requirements</span></span>



| <span data-ttu-id="49a25-128">Требование</span><span class="sxs-lookup"><span data-stu-id="49a25-128">Requirement</span></span> | <span data-ttu-id="49a25-129">Значение</span><span class="sxs-lookup"><span data-stu-id="49a25-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a25-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49a25-130">Minimum supported client</span></span><br/> | <span data-ttu-id="49a25-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="49a25-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="49a25-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49a25-132">Minimum supported server</span></span><br/> | <span data-ttu-id="49a25-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="49a25-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="49a25-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="49a25-134">End of client support</span></span><br/>    | <span data-ttu-id="49a25-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="49a25-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="49a25-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="49a25-136">Product</span></span><br/>                  | <span data-ttu-id="49a25-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="49a25-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="49a25-138">Header</span><span class="sxs-lookup"><span data-stu-id="49a25-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="49a25-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="49a25-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="49a25-140">IID</span><span class="sxs-lookup"><span data-stu-id="49a25-140">IID</span></span><br/>                      | <span data-ttu-id="49a25-141">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="49a25-141">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="49a25-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49a25-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a25-143">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="49a25-143">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

