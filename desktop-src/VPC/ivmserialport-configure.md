---
title: Метод Configure Ивмсериалпорт (Впккоминтерфацес. h)
description: Настраивает последовательный порт.
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- Настройка метода Virtual PC
- Настройка метода Virtual PC, интерфейса Ивмсериалпорт
- Интерфейс Ивмсериалпорт Virtual PC, метод configure
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99440263dbf52282b6f3c2756ff7dd76151ff73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071694"
---
# <a name="ivmserialportconfigure-method"></a><span data-ttu-id="50112-106">Метод Ивмсериалпорт:: Configure</span><span class="sxs-lookup"><span data-stu-id="50112-106">IVMSerialPort::Configure method</span></span>

<span data-ttu-id="50112-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="50112-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="50112-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="50112-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="50112-109">Настраивает последовательный порт.</span><span class="sxs-lookup"><span data-stu-id="50112-109">Configures the serial port.</span></span>

## <a name="syntax"></a><span data-ttu-id="50112-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50112-110">Syntax</span></span>


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a><span data-ttu-id="50112-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="50112-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50112-112">*portType* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50112-112">*portType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50112-113">Тип последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="50112-113">The type of serial port.</span></span> <span data-ttu-id="50112-114">Список значений см. в разделе [**вмсериалпорттипе**](vmserialporttype.md).</span><span class="sxs-lookup"><span data-stu-id="50112-114">For a list of values, see [**VMSerialPortType**](vmserialporttype.md).</span></span>

</dd> <dt>

<span data-ttu-id="50112-115">*портнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50112-115">*portName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50112-116">Имя последовательного порта.</span><span class="sxs-lookup"><span data-stu-id="50112-116">The name of the serial port.</span></span> <span data-ttu-id="50112-117">Например, "COM1" для **вмсериалпорт \_ хостпорт**, "C: \\SerialPort.txt" для **вмсериалпорт \_ TextFile** или " \\ \\ *ServerName* \\ pipe \\ *pipeName*" для **вмсериалпорт \_ помощью канала NamedPipe**.</span><span class="sxs-lookup"><span data-stu-id="50112-117">For example, "COM1" for **vmSerialPort\_HostPort**, "C:\\SerialPort.txt" for **vmSerialPort\_TextFile**, or "\\\\*servername*\\pipe\\*pipename*" for **vmSerialPort\_NamedPipe**.</span></span>

</dd> <dt>

<span data-ttu-id="50112-118">*вмконнектиммедиатели* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="50112-118">*vmConnectImmediately* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50112-119">**Значение true** , если последовательный порт узла должен быть открыт сразу же после запуска виртуальной машины; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="50112-119">**TRUE** if the host serial port should be opened immediately when the virtual machine is started and **FALSE** otherwise.</span></span> <span data-ttu-id="50112-120">Игнорируется, если *portType* не **вмсериалпорт \_ хостпорт**.</span><span class="sxs-lookup"><span data-stu-id="50112-120">Ignored if *portType* is not **vmSerialPort\_HostPort**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50112-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="50112-121">Return value</span></span>

<span data-ttu-id="50112-122">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="50112-122">This method can return one of these values.</span></span>



| <span data-ttu-id="50112-123">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="50112-123">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="50112-124">Описание</span><span class="sxs-lookup"><span data-stu-id="50112-124">Description</span></span>                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50112-125"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="50112-125"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="50112-126">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="50112-126">The operation was successful.</span></span><br/>                                                                                          |
| <dl> <span data-ttu-id="50112-127"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="50112-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="50112-128">Недопустимый параметр *portType* .</span><span class="sxs-lookup"><span data-stu-id="50112-128">The *portType* parameter is not valid.</span></span><br/>                                                                                 |
| <dl> <span data-ttu-id="50112-129"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="50112-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="50112-130">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="50112-130">An unexpected error has occurred.</span></span><br/>                                                                                      |
| <dl> <span data-ttu-id="50112-131"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="50112-131"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="50112-132">Параметр *портнаме* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="50112-132">The *portName* parameter is **NULL**.</span></span><br/>                                                                                  |
| <dl> <span data-ttu-id="50112-133"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (Error \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="50112-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>      | <span data-ttu-id="50112-134">Недостаточно памяти для выполнения этого запроса.</span><span class="sxs-lookup"><span data-stu-id="50112-134">There is not enough memory available to complete this request.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="50112-135"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ переполнение буфера ошибки)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="50112-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="50112-136">Путь, указанный в параметре *портнаме* , слишком длинный.</span><span class="sxs-lookup"><span data-stu-id="50112-136">The path specified by the *portName* parameter is too long.</span></span> <span data-ttu-id="50112-137">Длина пути должна быть меньше **максимального \_ пути** (260).</span><span class="sxs-lookup"><span data-stu-id="50112-137">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="50112-138"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимое \_ имя)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="50112-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="50112-139">Параметр *портнаме* содержит недопустимый символ (один из " \* ? <>/ \| ": ").</span><span class="sxs-lookup"><span data-stu-id="50112-139">The *portName* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="50112-140"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ Bad \_ PATHNAME)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="50112-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="50112-141">Параметр *портнаме* указывает пустой или относительный путь.</span><span class="sxs-lookup"><span data-stu-id="50112-141">The *portName* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="50112-142">Требуется абсолютный путь.</span><span class="sxs-lookup"><span data-stu-id="50112-142">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="50112-143"><dt>**Виртуальная машина \_ \_Неизвестный \_ 0xA0040207 виртуальной машины**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="50112-143"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>                            | <span data-ttu-id="50112-144">Недопустимая конфигурация для этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="50112-144">The configuration for this virtual machine is not valid.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="50112-145"><dt>**Виртуальная машина \_ E \_ преф \_ недопустимое \_ значение**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="50112-145"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>                   | <span data-ttu-id="50112-146">Указанный порт уже используется.</span><span class="sxs-lookup"><span data-stu-id="50112-146">The specified port is already in use.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="50112-147">Требования</span><span class="sxs-lookup"><span data-stu-id="50112-147">Requirements</span></span>



| <span data-ttu-id="50112-148">Требование</span><span class="sxs-lookup"><span data-stu-id="50112-148">Requirement</span></span> | <span data-ttu-id="50112-149">Значение</span><span class="sxs-lookup"><span data-stu-id="50112-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50112-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50112-150">Minimum supported client</span></span><br/> | <span data-ttu-id="50112-151">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="50112-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="50112-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50112-152">Minimum supported server</span></span><br/> | <span data-ttu-id="50112-153">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="50112-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="50112-154">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="50112-154">End of client support</span></span><br/>    | <span data-ttu-id="50112-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="50112-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="50112-156">Продукт</span><span class="sxs-lookup"><span data-stu-id="50112-156">Product</span></span><br/>                  | <span data-ttu-id="50112-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="50112-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="50112-158">Header</span><span class="sxs-lookup"><span data-stu-id="50112-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="50112-159"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="50112-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="50112-160">IID</span><span class="sxs-lookup"><span data-stu-id="50112-160">IID</span></span><br/>                      | <span data-ttu-id="50112-161">IID \_ ивмсериалпорт определен как 2ce4460d-1d3f-4458-bf8b-44084b816815</span><span class="sxs-lookup"><span data-stu-id="50112-161">IID\_IVMSerialPort is defined as 2ce4460d-1d3f-4458-bf8b-44084b816815</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="50112-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50112-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50112-163">**ивмсериалпорт**</span><span class="sxs-lookup"><span data-stu-id="50112-163">**IVMSerialPort**</span></span>](ivmserialport.md)
</dt> </dl>

 

