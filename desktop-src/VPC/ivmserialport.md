---
title: Интерфейс Ивмсериалпорт (Впккоминтерфацес. h)
description: Определяет последовательный порт внутри виртуальной машины.
ms.assetid: a6568885-bfdf-4559-8886-02ca59096ca0
keywords:
- Виртуальный ПК с интерфейсом Ивмсериалпорт
- Ивмсериалпорт интерфейс Virtual PC, описание
topic_type:
- apiref
api_name:
- IVMSerialPort
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6edc758ffecca9a0d4788e5586c902cf0b21dd5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534781"
---
# <a name="ivmserialport-interface"></a><span data-ttu-id="4abf4-105">Интерфейс Ивмсериалпорт</span><span class="sxs-lookup"><span data-stu-id="4abf4-105">IVMSerialPort interface</span></span>

<span data-ttu-id="4abf4-106">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="4abf4-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="4abf4-107">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4abf4-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="4abf4-108">Определяет последовательный порт внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4abf4-108">Defines a serial port inside a virtual machine.</span></span> <span data-ttu-id="4abf4-109">Этот интерфейс позволяет настраивать последовательные порты внутри виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4abf4-109">This interface allows you to configure serial ports inside a virtual machine.</span></span> <span data-ttu-id="4abf4-110">Объект **ивмсериалпорт** можно получить из объекта [**ивмсериалпортколлектион**](ivmserialportcollection.md) , возвращенного из свойства [**ивмвиртуалмачине:: сериалпортс**](ivmvirtualmachine-serialports.md) .</span><span class="sxs-lookup"><span data-stu-id="4abf4-110">You can retrieve an **IVMSerialPort** object from the [**IVMSerialPortCollection**](ivmserialportcollection.md) object returned from the [**IVMVirtualMachine::SerialPorts**](ivmvirtualmachine-serialports.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="4abf4-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="4abf4-111">Members</span></span>

<span data-ttu-id="4abf4-112">Интерфейс **ивмсериалпорт** наследует от интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="4abf4-112">The **IVMSerialPort** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="4abf4-113">**Ивмсериалпорт** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4abf4-113">**IVMSerialPort** also has these types of members:</span></span>

-   [<span data-ttu-id="4abf4-114">Методы</span><span class="sxs-lookup"><span data-stu-id="4abf4-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="4abf4-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="4abf4-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4abf4-116">Методы</span><span class="sxs-lookup"><span data-stu-id="4abf4-116">Methods</span></span>

<span data-ttu-id="4abf4-117">Интерфейс **ивмсериалпорт** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4abf4-117">The **IVMSerialPort** interface has these methods.</span></span>



| <span data-ttu-id="4abf4-118">Метод</span><span class="sxs-lookup"><span data-stu-id="4abf4-118">Method</span></span>                                       | <span data-ttu-id="4abf4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="4abf4-119">Description</span></span>                                                      |
|:---------------------------------------------|:-----------------------------------------------------------------|
| [<span data-ttu-id="4abf4-120">**\_ID**</span><span class="sxs-lookup"><span data-stu-id="4abf4-120">**\_ID**</span></span>](ivmserialport--id.md)            | <span data-ttu-id="4abf4-121">Извлекает внутренний идентификатор последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="4abf4-121">Retrieves the internal identifier of the serial port.</span></span><br/> |
| [<span data-ttu-id="4abf4-122">**Configure**</span><span class="sxs-lookup"><span data-stu-id="4abf4-122">**Configure**</span></span>](ivmserialport-configure.md) | <span data-ttu-id="4abf4-123">Настраивает последовательный порт.</span><span class="sxs-lookup"><span data-stu-id="4abf4-123">Configures the serial port.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="4abf4-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="4abf4-124">Properties</span></span>

<span data-ttu-id="4abf4-125">Интерфейс **ивмсериалпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4abf4-125">The **IVMSerialPort** interface has these properties.</span></span>



| <span data-ttu-id="4abf4-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="4abf4-126">Property</span></span>                                                                  | <span data-ttu-id="4abf4-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="4abf4-127">Access type</span></span>          | <span data-ttu-id="4abf4-128">Описание</span><span class="sxs-lookup"><span data-stu-id="4abf4-128">Description</span></span>                                                                                                       |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4abf4-129">**коннектиммедиатели**</span><span class="sxs-lookup"><span data-stu-id="4abf4-129">**ConnectImmediately**</span></span>](ivmserialport-connectimmediately.md)<br/> | <span data-ttu-id="4abf4-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4abf4-130">Read-only</span></span><br/> | <span data-ttu-id="4abf4-131">Указывает, должен ли быть открыт последовательный порт без ожидания получения команды модема.</span><span class="sxs-lookup"><span data-stu-id="4abf4-131">Indicates whether the serial port should be opened without waiting for a modem command to be received.</span></span><br/> |
| [<span data-ttu-id="4abf4-132">**Имя**</span><span class="sxs-lookup"><span data-stu-id="4abf4-132">**Name**</span></span>](ivmserialport-name.md)<br/>                             | <span data-ttu-id="4abf4-133">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4abf4-133">Read-only</span></span><br/> | <span data-ttu-id="4abf4-134">Имя последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="4abf4-134">The name of the serial port.</span></span><br/>                                                                           |
| [<span data-ttu-id="4abf4-135">**Тип**</span><span class="sxs-lookup"><span data-stu-id="4abf4-135">**Type**</span></span>](ivmserialport-type.md)<br/>                             | <span data-ttu-id="4abf4-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="4abf4-136">Read-only</span></span><br/> | <span data-ttu-id="4abf4-137">Тип последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="4abf4-137">The type of the serial port.</span></span><br/>                                                                           |



 

## <a name="requirements"></a><span data-ttu-id="4abf4-138">Требования</span><span class="sxs-lookup"><span data-stu-id="4abf4-138">Requirements</span></span>



| <span data-ttu-id="4abf4-139">Требование</span><span class="sxs-lookup"><span data-stu-id="4abf4-139">Requirement</span></span> | <span data-ttu-id="4abf4-140">Значение</span><span class="sxs-lookup"><span data-stu-id="4abf4-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4abf4-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4abf4-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4abf4-142">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="4abf4-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4abf4-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4abf4-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4abf4-144">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="4abf4-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="4abf4-145">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4abf4-145">End of client support</span></span><br/>    | <span data-ttu-id="4abf4-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4abf4-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="4abf4-147">Продукт</span><span class="sxs-lookup"><span data-stu-id="4abf4-147">Product</span></span><br/>                  | <span data-ttu-id="4abf4-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="4abf4-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="4abf4-149">Header</span><span class="sxs-lookup"><span data-stu-id="4abf4-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="4abf4-150"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="4abf4-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="4abf4-151">IID</span><span class="sxs-lookup"><span data-stu-id="4abf4-151">IID</span></span><br/>                      | <span data-ttu-id="4abf4-152">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="4abf4-152">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



 

