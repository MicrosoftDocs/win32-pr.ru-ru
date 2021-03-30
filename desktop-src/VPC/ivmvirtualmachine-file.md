---
title: Свойство файла Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Получает полный путь к VMC файлу для конфигурации виртуальной машины.
ms.assetid: fc215068-e908-417c-bd68-214539a0a14e
keywords:
- Свойство файла Virtual PC
- Свойство файла Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство File
topic_type:
- apiref
api_name:
- IVMVirtualMachine.File
- IVMVirtualMachine.get_File
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71ac3bc68d167a7057d76adc1ce84a29291b7c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802687"
---
# <a name="ivmvirtualmachinefile-property"></a><span data-ttu-id="553a7-106">Ивмвиртуалмачине:: File, свойство</span><span class="sxs-lookup"><span data-stu-id="553a7-106">IVMVirtualMachine::File property</span></span>

<span data-ttu-id="553a7-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="553a7-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="553a7-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="553a7-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="553a7-109">Получает полный путь к VMC файлу для конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="553a7-109">Retrieves the fully qualified path of the .vmc file for the virtual machine configuration.</span></span>

<span data-ttu-id="553a7-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="553a7-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="553a7-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="553a7-111">Syntax</span></span>


```C++
HRESULT get_File(
  [out, retval] BSTR *virtualMachineXMLFile
);
```



## <a name="property-value"></a><span data-ttu-id="553a7-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="553a7-112">Property value</span></span>

<span data-ttu-id="553a7-113">Полное имя \* файла ". VMC", описывающего эту конфигурацию виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="553a7-113">The fully qualified name of the "\*.vmc" file that describes this virtual machine configuration.</span></span>

## <a name="error-codes"></a><span data-ttu-id="553a7-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="553a7-114">Error codes</span></span>



| <span data-ttu-id="553a7-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="553a7-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="553a7-116">Значение</span><span class="sxs-lookup"><span data-stu-id="553a7-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="553a7-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="553a7-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="553a7-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="553a7-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="553a7-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="553a7-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="553a7-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="553a7-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="553a7-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="553a7-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="553a7-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="553a7-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="553a7-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="553a7-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="553a7-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="553a7-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="553a7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="553a7-125">Requirements</span></span>



| <span data-ttu-id="553a7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="553a7-126">Requirement</span></span> | <span data-ttu-id="553a7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="553a7-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="553a7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="553a7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="553a7-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="553a7-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="553a7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="553a7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="553a7-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="553a7-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="553a7-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="553a7-132">End of client support</span></span><br/>    | <span data-ttu-id="553a7-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="553a7-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="553a7-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="553a7-134">Product</span></span><br/>                  | <span data-ttu-id="553a7-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="553a7-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="553a7-136">Header</span><span class="sxs-lookup"><span data-stu-id="553a7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="553a7-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="553a7-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="553a7-138">IID</span><span class="sxs-lookup"><span data-stu-id="553a7-138">IID</span></span><br/>                      | <span data-ttu-id="553a7-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="553a7-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="553a7-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="553a7-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553a7-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="553a7-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

