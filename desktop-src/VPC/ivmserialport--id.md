---
title: Метод _ID Ивмсериалпорт (Впккоминтерфацес. h)
description: Внутренний идентификатор последовательного порта.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID метод Virtual PC
- _ID метод Virtual PC, интерфейс Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, метод _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135826"
---
# <a name="ivmserialport_id-method"></a><span data-ttu-id="e20c2-106">Метод Ивмсериалпорт:: \_ ID</span><span class="sxs-lookup"><span data-stu-id="e20c2-106">IVMSerialPort::\_ID method</span></span>

<span data-ttu-id="e20c2-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="e20c2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e20c2-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e20c2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e20c2-109">Извлекает внутренний идентификатор последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="e20c2-109">Retrieves the internal identifier of the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e20c2-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e20c2-110">Syntax</span></span>


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a><span data-ttu-id="e20c2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="e20c2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e20c2-112">*portID* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e20c2-112">*portID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e20c2-113">Идентификатор последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="e20c2-113">The serial port identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e20c2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e20c2-114">Return value</span></span>

<span data-ttu-id="e20c2-115">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="e20c2-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e20c2-116">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e20c2-116">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="e20c2-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e20c2-117">Description</span></span>                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="e20c2-118"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e20c2-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="e20c2-119">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e20c2-119">The operation was successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="e20c2-120"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="e20c2-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="e20c2-121">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e20c2-121">The parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="e20c2-122"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e20c2-122"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="e20c2-123">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="e20c2-123">An unexpected error has occurred.</span></span><br/>                        |
| <dl> <span data-ttu-id="e20c2-124"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="e20c2-124"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="e20c2-125">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e20c2-125">The configuration for this virtual machine is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e20c2-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e20c2-126">Remarks</span></span>

<span data-ttu-id="e20c2-127">Это свойство не может использоваться в языках скриптов.</span><span class="sxs-lookup"><span data-stu-id="e20c2-127">This property is not usable by scripting languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e20c2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="e20c2-128">Requirements</span></span>



| <span data-ttu-id="e20c2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="e20c2-129">Requirement</span></span> | <span data-ttu-id="e20c2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="e20c2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e20c2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e20c2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="e20c2-132">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="e20c2-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e20c2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e20c2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="e20c2-134">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e20c2-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e20c2-135">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e20c2-135">End of client support</span></span><br/>    | <span data-ttu-id="e20c2-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e20c2-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e20c2-137">Продукт</span><span class="sxs-lookup"><span data-stu-id="e20c2-137">Product</span></span><br/>                  | <span data-ttu-id="e20c2-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e20c2-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e20c2-139">Header</span><span class="sxs-lookup"><span data-stu-id="e20c2-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20c2-140"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20c2-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e20c2-141">IID</span><span class="sxs-lookup"><span data-stu-id="e20c2-141">IID</span></span><br/>                      | <span data-ttu-id="e20c2-142">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="e20c2-142">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="e20c2-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e20c2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20c2-144">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="e20c2-144">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

