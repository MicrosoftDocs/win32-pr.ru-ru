---
title: Свойство Сериалпортс Ивмвиртуалмачине (Впккоминтерфацес. h)
description: Возвращает перечисляемую коллекцию последовательных портов.
ms.assetid: 502fe4f1-c58c-460c-8431-41fddd753d18
keywords:
- Сериалпортс свойство Virtual PC
- Сериалпортс свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, свойство Сериалпортс
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SerialPorts
- IVMVirtualMachine.get_SerialPorts
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18119c649014a020dd2a2d4e2fdeb7c2bbaae87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534961"
---
# <a name="ivmvirtualmachineserialports-property"></a><span data-ttu-id="91a56-106">Свойство Ивмвиртуалмачине:: Сериалпортс</span><span class="sxs-lookup"><span data-stu-id="91a56-106">IVMVirtualMachine::SerialPorts property</span></span>

<span data-ttu-id="91a56-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="91a56-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="91a56-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="91a56-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="91a56-109">Возвращает перечисляемую коллекцию последовательных портов.</span><span class="sxs-lookup"><span data-stu-id="91a56-109">Retrieves an enumerable collection of serial ports.</span></span>

<span data-ttu-id="91a56-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91a56-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a56-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91a56-111">Syntax</span></span>


```C++
HRESULT get_SerialPorts(
  [out, retval] IVMSerialPortCollection **serialPortCollection
);
```



## <a name="property-value"></a><span data-ttu-id="91a56-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91a56-112">Property value</span></span>

<span data-ttu-id="91a56-113">Объект [**ивмсериалпортколлектион**](ivmserialportcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="91a56-113">An [**IVMSerialPortCollection**](ivmserialportcollection.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="91a56-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="91a56-114">Error codes</span></span>



| <span data-ttu-id="91a56-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="91a56-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="91a56-116">Значение</span><span class="sxs-lookup"><span data-stu-id="91a56-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="91a56-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="91a56-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="91a56-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="91a56-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="91a56-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="91a56-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="91a56-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="91a56-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91a56-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="91a56-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="91a56-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="91a56-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="91a56-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="91a56-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="91a56-125">Требования</span><span class="sxs-lookup"><span data-stu-id="91a56-125">Requirements</span></span>



| <span data-ttu-id="91a56-126">Требование</span><span class="sxs-lookup"><span data-stu-id="91a56-126">Requirement</span></span> | <span data-ttu-id="91a56-127">Значение</span><span class="sxs-lookup"><span data-stu-id="91a56-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a56-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91a56-128">Minimum supported client</span></span><br/> | <span data-ttu-id="91a56-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="91a56-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="91a56-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91a56-130">Minimum supported server</span></span><br/> | <span data-ttu-id="91a56-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="91a56-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="91a56-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="91a56-132">End of client support</span></span><br/>    | <span data-ttu-id="91a56-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="91a56-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="91a56-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="91a56-134">Product</span></span><br/>                  | <span data-ttu-id="91a56-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="91a56-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="91a56-136">Header</span><span class="sxs-lookup"><span data-stu-id="91a56-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a56-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="91a56-138">IID</span><span class="sxs-lookup"><span data-stu-id="91a56-138">IID</span></span><br/>                      | <span data-ttu-id="91a56-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="91a56-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="91a56-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91a56-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91a56-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="91a56-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

