---
title: Метод Ивмвиртуалмачине Старткоммуникатиончаннел (Впккоминтерфацес. h)
description: Настройка коммуникационного канала между узлом и гостевой операционной системой.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Метод Старткоммуникатиончаннел Virtual PC
- Метод Старткоммуникатиончаннел Virtual PC, интерфейс Ивмвиртуалмачине
- Ивмвиртуалмачине интерфейс Virtual PC, метод Старткоммуникатиончаннел
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492216"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a><span data-ttu-id="94ebb-106">Метод Ивмвиртуалмачине:: Старткоммуникатиончаннел</span><span class="sxs-lookup"><span data-stu-id="94ebb-106">IVMVirtualMachine::StartCommunicationChannel method</span></span>

<span data-ttu-id="94ebb-107">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="94ebb-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="94ebb-108">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="94ebb-109">Настройка коммуникационного канала между узлом и гостевой операционной системой.</span><span class="sxs-lookup"><span data-stu-id="94ebb-109">Sets up a communication channel between host and guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="94ebb-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94ebb-110">Syntax</span></span>


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a><span data-ttu-id="94ebb-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="94ebb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94ebb-112">*инхостендпоинттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-112">*inHostEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ebb-113">Этот параметр должен быть **вмендпоинт \_ помощью канала NamedPipe** (0).</span><span class="sxs-lookup"><span data-stu-id="94ebb-113">This parameter must be **vmEndpoint\_NamedPipe** (0).</span></span>

</dd> <dt>

<span data-ttu-id="94ebb-114">*инхостендпоинтнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-114">*inHostEndPointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ebb-115">Уникальное имя канала.</span><span class="sxs-lookup"><span data-stu-id="94ebb-115">The unique pipe name.</span></span> <span data-ttu-id="94ebb-116">Эта строка должна иметь следующую форму: " \\ \\ . \\ pipe \\ *pipeName*".</span><span class="sxs-lookup"><span data-stu-id="94ebb-116">This string must have the following form: "\\\\.\\pipe\\*pipename*".</span></span> <span data-ttu-id="94ebb-117">*PipeName* часть имени может содержать любой символ, кроме обратной косой черты, включая цифры и специальные символы.</span><span class="sxs-lookup"><span data-stu-id="94ebb-117">The *pipename* part of the name can include any character other than a backslash, including numbers and special characters.</span></span> <span data-ttu-id="94ebb-118">Длина строки имени канала может доставлять до 256 символов.</span><span class="sxs-lookup"><span data-stu-id="94ebb-118">The entire pipe name string can be up to 256 characters long.</span></span> <span data-ttu-id="94ebb-119">Имена каналов не чувствительны к регистру.</span><span class="sxs-lookup"><span data-stu-id="94ebb-119">Pipe names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="94ebb-120">*ингуестендпоинттипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-120">*inGuestEndpointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ebb-121">Этот параметр должен быть **вмендпоинт \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="94ebb-121">This parameter must be **vmEndpoint\_TCPIP** (1).</span></span>

</dd> <dt>

<span data-ttu-id="94ebb-122">*ингуестендпоинтнаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-122">*inGuestEndpointName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94ebb-123">Номер порта, на котором прослушивается TCP-сервер в гостевой системе.</span><span class="sxs-lookup"><span data-stu-id="94ebb-123">The port number on which the TCP server in the guest is listening.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94ebb-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94ebb-124">Return value</span></span>

<span data-ttu-id="94ebb-125">Этот метод может возвращать одно из этих значений.</span><span class="sxs-lookup"><span data-stu-id="94ebb-125">This method can return one of these values.</span></span>



| <span data-ttu-id="94ebb-126">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="94ebb-126">Return code/value</span></span>                                                                                                                                                                                  | <span data-ttu-id="94ebb-127">Описание</span><span class="sxs-lookup"><span data-stu-id="94ebb-127">Description</span></span>                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94ebb-128"><dt>**С \_ ОК**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-128"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                        | <span data-ttu-id="94ebb-129">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="94ebb-129">The operation was successful.</span></span><br/>                                                                                                                    |
| <dl> <span data-ttu-id="94ebb-130"><dt>**Д \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-130"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                       | <span data-ttu-id="94ebb-131">Параметр *инхостендпоинттипе* не является **вмендпоинт \_ помощью канала NamedPipe** (0), или параметр *ингуестендпоинттипе* не является **вмендпоинт \_ tcpip** (1).</span><span class="sxs-lookup"><span data-stu-id="94ebb-131">The *inHostEndpointType* parameter is not **vmEndpoint\_NamedPipe** (0) or the *inGuestEndpointType* parameter is not **vmEndpoint\_TCPIP** (1).</span></span><br/> |
| <dl> <span data-ttu-id="94ebb-132"><dt>**Д \_**</dt> <dt>0x80004003</dt> указателя</span><span class="sxs-lookup"><span data-stu-id="94ebb-132"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                          | <span data-ttu-id="94ebb-133">Параметр *инхостендпоинтнаме* или *Ингуестендпоинтнаме* имеет значение **null** или не является допустимым значением.</span><span class="sxs-lookup"><span data-stu-id="94ebb-133">The *inHostEndPointName* or *inGuestEndpointName* parameter is **NULL** or not a valid value.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="94ebb-134"><dt>**\_ E \_ Exception**</dt> <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-134"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                                  | <span data-ttu-id="94ebb-135">Произошла непредвиденная ошибка.</span><span class="sxs-lookup"><span data-stu-id="94ebb-135">An unexpected error has occurred.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="94ebb-136"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ недопустимого \_ маркера)**</dt> <dt>0x80070006</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_HANDLE)**</dt> <dt>0x80070006</dt></span></span> </dl>        | <span data-ttu-id="94ebb-137">Недопустимый маркер.</span><span class="sxs-lookup"><span data-stu-id="94ebb-137">A handle is not valid.</span></span><br/>                                                                                                                           |
| <dl> <span data-ttu-id="94ebb-138"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (Error \_ OUTOFMEMORY)**</dt> <dt>0x8007000E</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl>            | <span data-ttu-id="94ebb-139">Недостаточно памяти для выполнения этого запроса.</span><span class="sxs-lookup"><span data-stu-id="94ebb-139">There is not enough memory available to complete this request.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="94ebb-140"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ не \_ готова)**</dt> <dt>0x80070015</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-140"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_READY)**</dt> <dt>0x80070015</dt></span></span> </dl>             | <span data-ttu-id="94ebb-141">Базовая система, используемая для предоставления сетевых служб в данный момент инициализируется.</span><span class="sxs-lookup"><span data-stu-id="94ebb-141">The underlying system it uses to provide network services is currently being initialized.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="94ebb-142"><dt>**Значение HRESULT \_ ИЗ \_ Win32 (ошибка \_ уже \_ существует)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>        | <span data-ttu-id="94ebb-143">Имя канала уже используется.</span><span class="sxs-lookup"><span data-stu-id="94ebb-143">The pipe name is already in use.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="94ebb-144"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ канал ошибки \_ занят)**</dt> <dt>0x800700e7</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PIPE\_BUSY)**</dt> <dt>0x800700e7</dt></span></span> </dl>             | <span data-ttu-id="94ebb-145">Один или несколько каналов работают и могут стать доступными в ближайшее время.</span><span class="sxs-lookup"><span data-stu-id="94ebb-145">One or more channels are running down and may become available shortly.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="94ebb-146"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ \_ достигнуто максимальное число сеансов с ошибками)**</dt> <dt>0x80070161</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_MAX\_SESSIONS\_REACHED)**</dt> <dt>0x80070161</dt></span></span> </dl> | <span data-ttu-id="94ebb-147">Максимальное число доступных каналов связи — используется.</span><span class="sxs-lookup"><span data-stu-id="94ebb-147">The maximum numbers of communication channels available are in-use.</span></span> <span data-ttu-id="94ebb-148">В данный момент невозможно запустить другой канал.</span><span class="sxs-lookup"><span data-stu-id="94ebb-148">Another channel cannot be started at this time.</span></span><br/>                              |
| <dl> <span data-ttu-id="94ebb-149"><dt>**Значение HRESULT \_ ИЗ \_ Win32 ( \_ \_ несоответствие редакции ошибки)**</dt> <dt>0x8007051a</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-149"><dt>**HRESULT\_FROM\_WIN32(ERROR\_REVISION\_MISMATCH)**</dt> <dt>0x8007051a</dt></span></span> </dl>     | <span data-ttu-id="94ebb-150">Существует несоответствие между версией узла и гостевыми подсистемами.</span><span class="sxs-lookup"><span data-stu-id="94ebb-150">There is a mismatch between the version of the host and guest subsystems.</span></span> <span data-ttu-id="94ebb-151">Дополнительные сведения см. в журнале событий Windows.</span><span class="sxs-lookup"><span data-stu-id="94ebb-151">See the Windows Event Log for more detail.</span></span><br/>                             |
| <dl> <span data-ttu-id="94ebb-152"><dt>**Виртуальная машина \_ \_Виртуальная машина E \_ не \_ работает**</dt> <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-152"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                             | <span data-ttu-id="94ebb-153">Виртуальная машина не запущена.</span><span class="sxs-lookup"><span data-stu-id="94ebb-153">The VM is not running.</span></span><br/>                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="94ebb-154">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94ebb-154">Remarks</span></span>

<span data-ttu-id="94ebb-155">Текущая реализация поддерживает только интерфейс именованных каналов на узле и интерфейс TCP/IP в гостевой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="94ebb-155">The current implementation supports only named pipe interface on the host and TCP/IP interface on the guest operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ebb-156">Требования</span><span class="sxs-lookup"><span data-stu-id="94ebb-156">Requirements</span></span>



| <span data-ttu-id="94ebb-157">Требование</span><span class="sxs-lookup"><span data-stu-id="94ebb-157">Requirement</span></span> | <span data-ttu-id="94ebb-158">Значение</span><span class="sxs-lookup"><span data-stu-id="94ebb-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="94ebb-159">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94ebb-159">Minimum supported client</span></span><br/> | <span data-ttu-id="94ebb-160">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="94ebb-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94ebb-161">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94ebb-161">Minimum supported server</span></span><br/> | <span data-ttu-id="94ebb-162">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="94ebb-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="94ebb-163">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="94ebb-163">End of client support</span></span><br/>    | <span data-ttu-id="94ebb-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="94ebb-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="94ebb-165">Продукт</span><span class="sxs-lookup"><span data-stu-id="94ebb-165">Product</span></span><br/>                  | <span data-ttu-id="94ebb-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="94ebb-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="94ebb-167">Header</span><span class="sxs-lookup"><span data-stu-id="94ebb-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="94ebb-168"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ebb-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="94ebb-169">IID</span><span class="sxs-lookup"><span data-stu-id="94ebb-169">IID</span></span><br/>                      | <span data-ttu-id="94ebb-170">IID \_ ивмвиртуалмачине определен как f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="94ebb-170">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="94ebb-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94ebb-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ebb-172">**ивмвиртуалмачине**</span><span class="sxs-lookup"><span data-stu-id="94ebb-172">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="94ebb-173">**вмендпоинттипе**</span><span class="sxs-lookup"><span data-stu-id="94ebb-173">**VMEndpointType**</span></span>](vmendpointtype.md)
</dt> </dl>

 

