---
title: Свойство Коннектиммедиатели Ивмсериалпорт (Впккоминтерфацес. h)
description: Определяет, должен ли быть открыт последовательный порт без ожидания получения команды модема.
ms.assetid: 5ac22906-0fe2-477d-98af-7c05ce274cc5
keywords:
- Коннектиммедиатели свойство Virtual PC
- Коннектиммедиатели свойство Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, свойство Коннектиммедиатели
topic_type:
- apiref
api_name:
- IVMSerialPort.ConnectImmediately
- IVMSerialPort.get_ConnectImmediately
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7661b9cf3b118427b1ecb2b6f450913e35e35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802458"
---
# <a name="ivmserialportconnectimmediately-property"></a><span data-ttu-id="694e6-106">Свойство Ивмсериалпорт:: Коннектиммедиатели</span><span class="sxs-lookup"><span data-stu-id="694e6-106">IVMSerialPort::ConnectImmediately property</span></span>

<span data-ttu-id="694e6-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="694e6-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="694e6-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="694e6-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="694e6-109">Определяет, должен ли быть открыт последовательный порт без ожидания получения команды модема.</span><span class="sxs-lookup"><span data-stu-id="694e6-109">Determines whether the serial port should be opened without waiting for a modem command to be received.</span></span>

<span data-ttu-id="694e6-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="694e6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="694e6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="694e6-111">Syntax</span></span>


```C++
HRESULT get_ConnectImmediately(
  [out, retval] VARIANT_BOOL *vmConnectImmediately
);
```



## <a name="property-value"></a><span data-ttu-id="694e6-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="694e6-112">Property value</span></span>

<span data-ttu-id="694e6-113">**Вариант \_ Значение TRUE** , если последовательный порт должен быть открыт без ожидания получения команды модема; **Вариант \_** В противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="694e6-113">**VARIANT\_TRUE** if the serial port should be opened without waiting for a modem command to be received; **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="694e6-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="694e6-114">Error codes</span></span>



| <span data-ttu-id="694e6-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="694e6-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="694e6-116">Значение</span><span class="sxs-lookup"><span data-stu-id="694e6-116">Meaning</span></span>                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="694e6-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="694e6-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="694e6-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="694e6-118">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="694e6-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="694e6-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="694e6-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="694e6-120">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="694e6-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="694e6-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="694e6-122">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="694e6-122">The configuration for this virtual machine is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="694e6-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="694e6-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="694e6-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="694e6-124">An unexpected error has occurred.</span></span><br/>                        |



## <a name="remarks"></a><span data-ttu-id="694e6-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="694e6-125">Remarks</span></span>

<span data-ttu-id="694e6-126">Это свойство допустимо, только если свойство [**Type**](ivmserialport-type.md) Port имеет значение **вмсериалпорт \_ хостпорт**.</span><span class="sxs-lookup"><span data-stu-id="694e6-126">This property is valid only if the port [**Type**](ivmserialport-type.md) property is **vmSerialPort\_HostPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="694e6-127">Требования</span><span class="sxs-lookup"><span data-stu-id="694e6-127">Requirements</span></span>



| <span data-ttu-id="694e6-128">Требование</span><span class="sxs-lookup"><span data-stu-id="694e6-128">Requirement</span></span> | <span data-ttu-id="694e6-129">Значение</span><span class="sxs-lookup"><span data-stu-id="694e6-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="694e6-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="694e6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="694e6-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="694e6-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="694e6-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="694e6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="694e6-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="694e6-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="694e6-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="694e6-134">End of client support</span></span><br/>    | <span data-ttu-id="694e6-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="694e6-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="694e6-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="694e6-136">Product</span></span><br/>                  | <span data-ttu-id="694e6-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="694e6-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="694e6-138">Header</span><span class="sxs-lookup"><span data-stu-id="694e6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="694e6-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="694e6-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="694e6-140">IID</span><span class="sxs-lookup"><span data-stu-id="694e6-140">IID</span></span><br/>                      | <span data-ttu-id="694e6-141">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="694e6-141">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="694e6-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="694e6-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="694e6-143">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="694e6-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

