---
title: Интерфейс Ивмсериалпортколлектион (Впккоминтерфацес. h)
description: Определяет коллекцию последовательных портов в пределах виртуальной машины. Чтобы получить объект Ивмсериалпортколлектион, используйте свойство Сериалпортс Ивмвиртуалмачине.
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- Виртуальный ПК с интерфейсом Ивмсериалпортколлектион
- Ивмсериалпортколлектион интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802453"
---
# <a name="ivmserialportcollection-interface"></a><span data-ttu-id="79818-106">Интерфейс Ивмсериалпортколлектион</span><span class="sxs-lookup"><span data-stu-id="79818-106">IVMSerialPortCollection interface</span></span>

<span data-ttu-id="79818-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="79818-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="79818-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="79818-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="79818-109">Определяет коллекцию последовательных портов в пределах виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="79818-109">Defines the collection of serial ports within the virtual machine.</span></span> <span data-ttu-id="79818-110">Чтобы получить объект **ивмсериалпортколлектион** , используйте свойство [**Ивмвиртуалмачине:: сериалпортс**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="79818-110">To obtain an **IVMSerialPortCollection** object, use the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="79818-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="79818-111">Members</span></span>

<span data-ttu-id="79818-112">Интерфейс **ивмсериалпортколлектион** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="79818-112">The **IVMSerialPortCollection** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="79818-113">**Ивмсериалпортколлектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="79818-113">**IVMSerialPortCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="79818-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="79818-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="79818-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="79818-115">Properties</span></span>

<span data-ttu-id="79818-116">Интерфейс **ивмсериалпортколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="79818-116">The **IVMSerialPortCollection** interface has these properties.</span></span>



| <span data-ttu-id="79818-117">Свойство</span><span class="sxs-lookup"><span data-stu-id="79818-117">Property</span></span>                                                         | <span data-ttu-id="79818-118">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="79818-118">Access type</span></span>          | <span data-ttu-id="79818-119">Описание</span><span class="sxs-lookup"><span data-stu-id="79818-119">Description</span></span>                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="79818-120">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="79818-120">**\_NewEnum**</span></span>](ivmserialportcollection--newenum.md)<br/> | <span data-ttu-id="79818-121">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="79818-121">Read-only</span></span><br/> | <span data-ttu-id="79818-122">Перечислитель для коллекции.</span><span class="sxs-lookup"><span data-stu-id="79818-122">An enumerator for the collection.</span></span><br/>                               |
| [<span data-ttu-id="79818-123">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="79818-123">**Count**</span></span>](ivmserialportcollection-count.md)<br/>        | <span data-ttu-id="79818-124">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="79818-124">Read-only</span></span><br/> | <span data-ttu-id="79818-125">Число последовательных портов в этой коллекции.</span><span class="sxs-lookup"><span data-stu-id="79818-125">The number of serial ports in this collection.</span></span><br/>                  |
| [<span data-ttu-id="79818-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="79818-126">**Item**</span></span>](ivmserialportcollection-item.md)<br/>          | <span data-ttu-id="79818-127">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="79818-127">Read-only</span></span><br/> | <span data-ttu-id="79818-128">Объект последовательного порта, соответствующий указанному индексу.</span><span class="sxs-lookup"><span data-stu-id="79818-128">The serial port object that corresponds to the specified index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="79818-129">Требования</span><span class="sxs-lookup"><span data-stu-id="79818-129">Requirements</span></span>



| <span data-ttu-id="79818-130">Требование</span><span class="sxs-lookup"><span data-stu-id="79818-130">Requirement</span></span> | <span data-ttu-id="79818-131">Значение</span><span class="sxs-lookup"><span data-stu-id="79818-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="79818-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79818-132">Minimum supported client</span></span><br/> | <span data-ttu-id="79818-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="79818-133">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="79818-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79818-134">Minimum supported server</span></span><br/> | <span data-ttu-id="79818-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="79818-135">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="79818-136">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="79818-136">End of client support</span></span><br/>    | <span data-ttu-id="79818-137">Windows 7</span><span class="sxs-lookup"><span data-stu-id="79818-137">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="79818-138">Продукт</span><span class="sxs-lookup"><span data-stu-id="79818-138">Product</span></span><br/>                  | <span data-ttu-id="79818-139">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="79818-139">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="79818-140">Header</span><span class="sxs-lookup"><span data-stu-id="79818-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="79818-141"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="79818-141"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="79818-142">IID</span><span class="sxs-lookup"><span data-stu-id="79818-142">IID</span></span><br/>                      | <span data-ttu-id="79818-143">IID \_ ивмсериалпортколлектион определен как dd3c6175-1f04-4341-9f85-104074880289</span><span class="sxs-lookup"><span data-stu-id="79818-143">IID\_IVMSerialPortCollection is defined as dd3c6175-1f04-4341-9f85-104074880289</span></span><br/>    |



## <a name="see-also"></a><span data-ttu-id="79818-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79818-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79818-145">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="79818-145">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> <dt>

[<span data-ttu-id="79818-146">**Ивмвиртуалмачине:: Сериалпортс**</span><span class="sxs-lookup"><span data-stu-id="79818-146">**IVMVirtualMachine::SerialPorts**</span></span>](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

