---
title: Свойство Item Ивмсериалпортколлектион (Впккоминтерфацес. h)
description: Извлекает объект последовательного порта, соответствующий указанному индексу.
ms.assetid: 24ce1404-d7aa-4125-b1f9-9c54418ea205
keywords:
- Свойство элемента Virtual PC
- Свойство элемента Virtual PC, интерфейс Ивмсериалпортколлектион
- Интерфейс Ивмсериалпортколлектион Virtual PC, свойство Item
topic_type:
- apiref
api_name:
- IVMSerialPortCollection.Item
- IVMSerialPortCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be44cc92507954848c369273ae27de49df8d0ad8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691861"
---
# <a name="ivmserialportcollectionitem-property"></a><span data-ttu-id="c0322-106">Свойство Ивмсериалпортколлектион:: Item</span><span class="sxs-lookup"><span data-stu-id="c0322-106">IVMSerialPortCollection::Item property</span></span>

<span data-ttu-id="c0322-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="c0322-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="c0322-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="c0322-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="c0322-109">Извлекает объект последовательного порта, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="c0322-109">Retrieves the serial port object that corresponds to the specified index.</span></span>

<span data-ttu-id="c0322-110">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c0322-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0322-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0322-111">Syntax</span></span>


```C++
HRESULT get_Item(
  [in]          long          index,
  [out, retval] IVMSerialPort **serialPort
);
```



## <a name="property-value"></a><span data-ttu-id="c0322-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c0322-112">Property value</span></span>

<span data-ttu-id="c0322-113">Объект [**ивмсериалпорт**](ivmserialport.md) .</span><span class="sxs-lookup"><span data-stu-id="c0322-113">The [**IVMSerialPort**](ivmserialport.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0322-114">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="c0322-114">Error codes</span></span>



| <span data-ttu-id="c0322-115">Имя/значение</span><span class="sxs-lookup"><span data-stu-id="c0322-115">Name/value</span></span>                                                                                                                                                    | <span data-ttu-id="c0322-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c0322-116">Meaning</span></span>                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0322-117"><dt>С \_ ОК</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0322-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="c0322-118">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="c0322-118">The operation was successful.</span></span> <br/>                                                      |
| <dl> <span data-ttu-id="c0322-119"><dt>Д \_ </dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="c0322-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>         | <span data-ttu-id="c0322-120">Параметр *serialPort* имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="c0322-120">The *serialPort* parameter is NULL.</span></span> <br/>                                                |
| <dl> <span data-ttu-id="c0322-121"><dt> \_ E \_ бадиндекс</dt> <dt>0x8002000B</dt></span><span class="sxs-lookup"><span data-stu-id="c0322-121"><dt>DISP\_E\_BADINDEX</dt> <dt>0x8002000B</dt></span></span> </dl>  | <span data-ttu-id="c0322-122">Индекс запрошенного элемента не соответствует элементу в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="c0322-122">The index of the requested item does not correspond to an item in this collection.</span></span> <br/> |
| <dl> <span data-ttu-id="c0322-123"><dt>Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c0322-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="c0322-124">Конфигурация неизвестна.</span><span class="sxs-lookup"><span data-stu-id="c0322-124">The configuration is unknown.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="c0322-125"><dt> \_ E \_ Exception</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="c0322-125"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="c0322-126">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c0322-126">An unexpected error has occurred.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="c0322-127">Требования</span><span class="sxs-lookup"><span data-stu-id="c0322-127">Requirements</span></span>



| <span data-ttu-id="c0322-128">Требование</span><span class="sxs-lookup"><span data-stu-id="c0322-128">Requirement</span></span> | <span data-ttu-id="c0322-129">Значение</span><span class="sxs-lookup"><span data-stu-id="c0322-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0322-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0322-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c0322-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c0322-131">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0322-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0322-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c0322-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c0322-133">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="c0322-134">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c0322-134">End of client support</span></span><br/>    | <span data-ttu-id="c0322-135">Windows 7</span><span class="sxs-lookup"><span data-stu-id="c0322-135">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="c0322-136">Продукт</span><span class="sxs-lookup"><span data-stu-id="c0322-136">Product</span></span><br/>                  | <span data-ttu-id="c0322-137">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="c0322-137">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="c0322-138">Header</span><span class="sxs-lookup"><span data-stu-id="c0322-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0322-139"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0322-139"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="c0322-140">IID</span><span class="sxs-lookup"><span data-stu-id="c0322-140">IID</span></span><br/>                      | <span data-ttu-id="c0322-141">IID \_ ивмсериалпортколлектион определен как dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="c0322-141">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="c0322-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c0322-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0322-143">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="c0322-143">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="c0322-144">**ивмсериалпортколлектион**</span><span class="sxs-lookup"><span data-stu-id="c0322-144">**IVMSerialPortCollection**</span></span>](ivmserialportcollection.md)
</dt> </dl>

 

