---
title: Свойство типа Ивмсериалпорт (Впккоминтерфацес. h)
description: Возвращает тип последовательного порта.
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- Тип свойства Virtual PC
- Тип свойства Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, тип Property
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490953"
---
# <a name="ivmserialporttype-property"></a><span data-ttu-id="b46c4-106">Свойство Ивмсериалпорт:: Type</span><span class="sxs-lookup"><span data-stu-id="b46c4-106">IVMSerialPort::Type property</span></span>

<span data-ttu-id="b46c4-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b46c4-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b46c4-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b46c4-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b46c4-109">Возвращает тип последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="b46c4-109">Retrieves the type of the serial port.</span></span>

<span data-ttu-id="b46c4-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b46c4-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="b46c4-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b46c4-111">Syntax</span></span>


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a><span data-ttu-id="b46c4-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b46c4-112">Property value</span></span>

<span data-ttu-id="b46c4-113">Тип последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="b46c4-113">The type of serial port.</span></span> <span data-ttu-id="b46c4-114">Список значений см. в разделе [**вмсериалпорттипе**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="b46c4-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="b46c4-115">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b46c4-115">Error codes</span></span>



| <span data-ttu-id="b46c4-116">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="b46c4-116">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="b46c4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b46c4-117">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="b46c4-118"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b46c4-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="b46c4-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b46c4-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="b46c4-120"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="b46c4-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="b46c4-121">Параметр имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b46c4-121">The parameter is NULL.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b46c4-122"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="b46c4-122"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="b46c4-123">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b46c4-123">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b46c4-124"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b46c4-124"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="b46c4-125">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b46c4-125">An unexpected error has occurred.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="b46c4-126">Требования</span><span class="sxs-lookup"><span data-stu-id="b46c4-126">Requirements</span></span>



| <span data-ttu-id="b46c4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="b46c4-127">Requirement</span></span> | <span data-ttu-id="b46c4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="b46c4-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b46c4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b46c4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b46c4-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b46c4-130">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b46c4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b46c4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b46c4-132">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b46c4-132">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b46c4-133">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b46c4-133">End of client support</span></span><br/>    | <span data-ttu-id="b46c4-134">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b46c4-134">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b46c4-135">Продукт</span><span class="sxs-lookup"><span data-stu-id="b46c4-135">Product</span></span><br/>                  | <span data-ttu-id="b46c4-136">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b46c4-136">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b46c4-137">Header</span><span class="sxs-lookup"><span data-stu-id="b46c4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b46c4-138"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b46c4-138"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b46c4-139">IID</span><span class="sxs-lookup"><span data-stu-id="b46c4-139">IID</span></span><br/>                      | <span data-ttu-id="b46c4-140">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="b46c4-140">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="b46c4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b46c4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46c4-142">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="b46c4-142">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

