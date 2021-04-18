---
title: Структура ORPC_DBG_BUFFER
description: '\_ \_ Структура буфера ОРПК dbg — это формат буфера, используемый для МАРШАЛИРОВАНИЯ данных RPC в методы интерфейса иорпкдебугнотифи.'
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER структуры COM
- COM PORPC_DBG_BUFFER указателя структуры
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691795"
---
# <a name="orpc_dbg_buffer-structure"></a><span data-ttu-id="50fd2-105">\_ \_ Структура буфера ОРПК dbg</span><span class="sxs-lookup"><span data-stu-id="50fd2-105">ORPC\_DBG\_BUFFER structure</span></span>

<span data-ttu-id="50fd2-106">Структура **\_ \_ буфера ОРПК dbg** — это формат буфера, используемый для маршалирования данных RPC в методы интерфейса [**иорпкдебугнотифи**](iorpcdebugnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="50fd2-106">The **ORPC\_DBG\_BUFFER** structure is the buffer format used to marshalled RPC data to the methods of the [**IOrpcDebugNotify**](iorpcdebugnotify.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="50fd2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="50fd2-107">Syntax</span></span>


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a><span data-ttu-id="50fd2-108">Члены</span><span class="sxs-lookup"><span data-stu-id="50fd2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="50fd2-109">**алвайсорсометимес**</span><span class="sxs-lookup"><span data-stu-id="50fd2-109">**alwaysOrSometimes**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-110">Значение, управляющее порождением отладчика.</span><span class="sxs-lookup"><span data-stu-id="50fd2-110">A value that controls debugger spawning.</span></span> <span data-ttu-id="50fd2-111">**алвайсорсометимес** может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50fd2-111">**alwaysOrSometimes** can be one of the following values:</span></span>



| <span data-ttu-id="50fd2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-112">Value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="50fd2-113">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-113">Meaning</span></span>                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <span data-ttu-id="50fd2-114"><dt>**ОРПК \_ ОТЛАДКа \_ всегда**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-114"><dt>**ORPC\_DEBUG\_ALWAYS**</dt> <dt>0x00000000</dt></span></span> </dl>                              | <span data-ttu-id="50fd2-115">Если этот параметр задан, COM всегда будет вызывать уведомление клиента или сервера для получателя.</span><span class="sxs-lookup"><span data-stu-id="50fd2-115">If set, COM will always raise the client or server notification on the receiver.</span></span><br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <span data-ttu-id="50fd2-116"><dt>**ОРПК \_ ОТЛАДКа, \_ Если \_ перехватчик \_ включен**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-116"><dt>**ORPC\_DEBUG\_IF\_HOOK\_ENABLED**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="50fd2-117">Если этот параметр задан, COM будет создавать уведомление клиента или сервера для получателя только в том случае, если отладка COM была включена путем вызова [**дллдебугобжектрпчук**](dlldebugobjectrpchook.md) в этом процессе с параметром **фтраце** , для которого задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-117">If set, COM will only raise the client or server notification on the receiver if COM debugging has been enabled by calling [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) in that process with **fTrace** set to **TRUE**.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="50fd2-118">**вермажор**</span><span class="sxs-lookup"><span data-stu-id="50fd2-118">**verMajor**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-119">Основной номер версии спецификации формата данных.</span><span class="sxs-lookup"><span data-stu-id="50fd2-119">The major version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-120">**верминор**</span><span class="sxs-lookup"><span data-stu-id="50fd2-120">**verMinor**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-121">Дополнительный номер версии спецификации формата данных.</span><span class="sxs-lookup"><span data-stu-id="50fd2-121">The minor version number of the data format specification.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-122">**кбремаининг**</span><span class="sxs-lookup"><span data-stu-id="50fd2-122">**cbRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-123">Число байтов, включая **кбремаининг**, которые следуют в этой структуре.</span><span class="sxs-lookup"><span data-stu-id="50fd2-123">The number of bytes, inclusive of **cbRemaining**, that follow in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-124">**гуидсемантик**</span><span class="sxs-lookup"><span data-stu-id="50fd2-124">**guidSemantic**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-125">Идентификатор GUID, определяющий, какие члены объединения представлены ниже.</span><span class="sxs-lookup"><span data-stu-id="50fd2-125">A GUID that determines which members of the union are present below.</span></span> <span data-ttu-id="50fd2-126">**гуидсемантик** может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50fd2-126">**guidSemantic** can take one of the following values:</span></span>



| <span data-ttu-id="50fd2-127">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-127">Value</span></span>                                                                                                           | <span data-ttu-id="50fd2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-128">Meaning</span></span>                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50fd2-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-129"><dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt></span></span> </dl> | <span data-ttu-id="50fd2-130">Определяет, должен ли отладчик выполнять одно пошаговое выполнение.</span><span class="sxs-lookup"><span data-stu-id="50fd2-130">Determines if single stepping is to be performed by the debugger.</span></span> <span data-ttu-id="50fd2-131">Ниже приведен только элемент **фстопоносерсиде** объединения.</span><span class="sxs-lookup"><span data-stu-id="50fd2-131">Only the **fStopOnOtherSide** member of the union is present below.</span></span><br/>                                             |
| <dl> <span data-ttu-id="50fd2-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-132"><dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="50fd2-133">Определяет, передаются ли в приемник операции с упакованными данными RPC и отладочные коды операций отладки.</span><span class="sxs-lookup"><span data-stu-id="50fd2-133">Determines if RPC marshalled data and debugging opcodes are passed to the receiver.</span></span> <span data-ttu-id="50fd2-134">Ниже представлены все члены объединения, за исключением **фстопоносерсиде**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-134">All of the members of the union are present below with the exception of **fStopOnOtherSide**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50fd2-135">**фстопоносерсиде**</span><span class="sxs-lookup"><span data-stu-id="50fd2-135">**fStopOnOtherSide**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-136">Если **значение — true**, отладчик выполняет одиночное пошаговое выполнение, и он должен выйти из сервера и продолжить выполнение после достижения другой стороны.</span><span class="sxs-lookup"><span data-stu-id="50fd2-136">If **TRUE**, single stepping is performed by the debugger and it should step out of the server and continue execution once the other side is reached.</span></span> <span data-ttu-id="50fd2-137">В противном случае выполнение одного шага не выполняется, и исполнение отладчика останавливается на другой стороне.</span><span class="sxs-lookup"><span data-stu-id="50fd2-137">Otherwise, single stepping is not performed and debugger execution stops on the other side.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-138">**вдебуггингопкоде**</span><span class="sxs-lookup"><span data-stu-id="50fd2-138">**wDebuggingOpCode**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-139">Значение, которое позволяет указать один из ряда операций.</span><span class="sxs-lookup"><span data-stu-id="50fd2-139">A value that allows for one of a series of operations to be specified.</span></span> <span data-ttu-id="50fd2-140">**вдебуггингопкоде** может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50fd2-140">**wDebuggingOpCode** can take one of the following values:</span></span>



| <span data-ttu-id="50fd2-141">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-141">Value</span></span>                                                                             | <span data-ttu-id="50fd2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-142">Meaning</span></span>                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="50fd2-143"><dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-143"><dt>0x0000</dt></span></span> </dl> | <span data-ttu-id="50fd2-144">Нет операции.</span><span class="sxs-lookup"><span data-stu-id="50fd2-144">No operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="50fd2-145"><dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-145"><dt>0x0001</dt></span></span> </dl> | <span data-ttu-id="50fd2-146">Если задано значение, то семантика одного шага будет идентична **фстопоносерсиде** , если задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-146">If set, single step semantics are identical to **fStopOnOtherSide** when set to **TRUE**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50fd2-147">**цекстент**</span><span class="sxs-lookup"><span data-stu-id="50fd2-147">**cExtent**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-148">Заполнение.</span><span class="sxs-lookup"><span data-stu-id="50fd2-148">Padding.</span></span> <span data-ttu-id="50fd2-149">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="50fd2-149">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-150">**padding**</span><span class="sxs-lookup"><span data-stu-id="50fd2-150">**padding**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-151">Заполнение.</span><span class="sxs-lookup"><span data-stu-id="50fd2-151">Padding.</span></span> <span data-ttu-id="50fd2-152">Не используйте.</span><span class="sxs-lookup"><span data-stu-id="50fd2-152">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-153">**CB**</span><span class="sxs-lookup"><span data-stu-id="50fd2-153">**cb**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-154">Размер (в байтах) данных в **ргбдата**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-154">The size, in bytes of the data in **rgbData**.</span></span>

</dd> <dt>

<span data-ttu-id="50fd2-155">**гуидекстент**</span><span class="sxs-lookup"><span data-stu-id="50fd2-155">**guidExtent**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-156">**Идентификатор GUID** , определяющий тип данных в **ргбдата**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-156">A **GUID** that determines the type of data in **rgbData**.</span></span> <span data-ttu-id="50fd2-157">**гуидекстент** может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="50fd2-157">**guidExtent** can take one of the following values:</span></span>



| <span data-ttu-id="50fd2-158">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-158">Value</span></span>                                                                                                           | <span data-ttu-id="50fd2-159">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-159">Meaning</span></span>                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="50fd2-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-160"><dt>53199051-57EB-11ce-A964-00AA006C3706</dt></span></span> </dl> | <span data-ttu-id="50fd2-161">**ргбдата** является упакованным указателем интерфейса.</span><span class="sxs-lookup"><span data-stu-id="50fd2-161">**rgbData** is a marshalled interface pointer.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="50fd2-162">**ргбдата**</span><span class="sxs-lookup"><span data-stu-id="50fd2-162">**rgbData**</span></span>
</dt> <dd>

<span data-ttu-id="50fd2-163">Буфер **байтов** , используемый для передачи УПАКОВАННЫХ com-данных RPC между клиентскими и серверными отладчиками.</span><span class="sxs-lookup"><span data-stu-id="50fd2-163">A **BYTE** buffer used to pass RPC marshalled COM data between the client and server debuggers.</span></span> <span data-ttu-id="50fd2-164">Содержимое **ргбдата** определяется **идентификатором GUID** в **гуидекстент**.</span><span class="sxs-lookup"><span data-stu-id="50fd2-164">The contents of **rgbData** are determined by the **GUID** in **guidExtent**.</span></span>



| <span data-ttu-id="50fd2-165">Значение Гуидекстент</span><span class="sxs-lookup"><span data-stu-id="50fd2-165">guidExtent Value</span></span>                     | <span data-ttu-id="50fd2-166">содержимое Ргбдата</span><span class="sxs-lookup"><span data-stu-id="50fd2-166">rgbData contents</span></span>                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50fd2-167">53199051-57EB-11ce-A964-00AA006C3706</span><span class="sxs-lookup"><span data-stu-id="50fd2-167">53199051-57EB-11ce-A964-00AA006C3706</span></span> | <span data-ttu-id="50fd2-168">Упакованный указатель интерфейса, полученный в результате вызова [**комаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="50fd2-168">A marshalled interface pointer that results from calling [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface).</span></span> <span data-ttu-id="50fd2-169">Упакованный указатель преобразуется в соответствующий указатель интерфейса с помощью [**каунмаршалинтерфаце**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span><span class="sxs-lookup"><span data-stu-id="50fd2-169">The marshalled pointer is converted into its corresponding interface pointer using [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="50fd2-170">Комментарии</span><span class="sxs-lookup"><span data-stu-id="50fd2-170">Remarks</span></span>

<span data-ttu-id="50fd2-171">Члены этой структуры имеют однобайтовый выравнивание и всегда передаются с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="50fd2-171">This members of this structure have 1-byte alignment and are always transmitted in little-endian byte order.</span></span>

## <a name="requirements"></a><span data-ttu-id="50fd2-172">Требования</span><span class="sxs-lookup"><span data-stu-id="50fd2-172">Requirements</span></span>



| <span data-ttu-id="50fd2-173">Требование</span><span class="sxs-lookup"><span data-stu-id="50fd2-173">Requirement</span></span> | <span data-ttu-id="50fd2-174">Значение</span><span class="sxs-lookup"><span data-stu-id="50fd2-174">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="50fd2-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="50fd2-175">Minimum supported client</span></span><br/> | <span data-ttu-id="50fd2-176">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50fd2-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="50fd2-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="50fd2-177">Minimum supported server</span></span><br/> | <span data-ttu-id="50fd2-178">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="50fd2-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="50fd2-179">Заголовок</span><span class="sxs-lookup"><span data-stu-id="50fd2-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="50fd2-180"><dt>Н/Д</dt></span><span class="sxs-lookup"><span data-stu-id="50fd2-180"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50fd2-181">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="50fd2-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50fd2-182">**ОРПК \_ dbg \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="50fd2-182">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="50fd2-183">**\_аргументы инициализации \_ ОРПК**</span><span class="sxs-lookup"><span data-stu-id="50fd2-183">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="50fd2-184">**дллдебугобжектрпчук**</span><span class="sxs-lookup"><span data-stu-id="50fd2-184">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> <dt>

[<span data-ttu-id="50fd2-185">**иорпкдебугнотифи**</span><span class="sxs-lookup"><span data-stu-id="50fd2-185">**IOrpcDebugNotify**</span></span>](iorpcdebugnotify.md)
</dt> </dl>

 

 





