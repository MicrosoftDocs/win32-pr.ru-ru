---
title: Свойство Ивмвиртуалмачине дисплея (Впккоминтерфацес. h)
description: Извлекает экран видео для виртуальной машины.
ms.assetid: ca5a433d-4613-4b6d-9de7-d9c6a2038e38
keywords:
- Показать свойство Virtual PC
- Отобразить свойство Virtual PC, интерфейс Ивмвиртуалмачине
- Интерфейс Ивмвиртуалмачине Virtual PC, свойство дисплея
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Display
- IVMVirtualMachine.get_Display
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 175150ba76074918d497efd2c9f65a53af46b8bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491298"
---
# <a name="ivmvirtualmachinedisplay-property"></a><span data-ttu-id="c14ce-106">Ивмвиртуалмачине::D свойство воспроизведения</span><span class="sxs-lookup"><span data-stu-id="c14ce-106">IVMVirtualMachine::Display property</span></span>

<span data-ttu-id="c14ce-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c14ce-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c14ce-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c14ce-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c14ce-109">Извлекает экран видео для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c14ce-109">Retrieves the video display for the virtual machine.</span></span>

<span data-ttu-id="c14ce-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c14ce-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c14ce-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c14ce-111">Syntax</span></span>


```C++
HRESULT get_Display(
  [out, retval] IVMDisplay **display
);
```



## <a name="property-value"></a><span data-ttu-id="c14ce-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c14ce-112">Property value</span></span>

<span data-ttu-id="c14ce-113">Объект [**ивмдисплай**](ivmdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="c14ce-113">The [**IVMDisplay**](ivmdisplay.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c14ce-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c14ce-114">Error codes</span></span>



| <span data-ttu-id="c14ce-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c14ce-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c14ce-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c14ce-116">Meaning</span></span>                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="c14ce-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c14ce-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c14ce-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c14ce-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="c14ce-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c14ce-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c14ce-120">Параметр имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="c14ce-120">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="c14ce-121"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c14ce-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c14ce-122">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="c14ce-122">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="c14ce-123"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c14ce-123"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c14ce-124">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c14ce-124">An unexpected error has occurred.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c14ce-125">Требования</span><span class="sxs-lookup"><span data-stu-id="c14ce-125">Requirements</span></span>



| <span data-ttu-id="c14ce-126">Требование</span><span class="sxs-lookup"><span data-stu-id="c14ce-126">Requirement</span></span> | <span data-ttu-id="c14ce-127">Значение</span><span class="sxs-lookup"><span data-stu-id="c14ce-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c14ce-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c14ce-128">Minimum supported client</span></span><br/> | <span data-ttu-id="c14ce-129">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c14ce-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c14ce-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c14ce-130">Minimum supported server</span></span><br/> | <span data-ttu-id="c14ce-131">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c14ce-131">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c14ce-132">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c14ce-132">End of client support</span></span><br/>    | <span data-ttu-id="c14ce-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c14ce-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c14ce-134">Продукт</span><span class="sxs-lookup"><span data-stu-id="c14ce-134">Product</span></span><br/>                  | <span data-ttu-id="c14ce-135">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c14ce-135">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c14ce-136">Header</span><span class="sxs-lookup"><span data-stu-id="c14ce-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c14ce-137"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c14ce-137"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c14ce-138">IID</span><span class="sxs-lookup"><span data-stu-id="c14ce-138">IID</span></span><br/>                      | <span data-ttu-id="c14ce-139">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="c14ce-139">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="c14ce-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c14ce-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c14ce-141">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="c14ce-141">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

