---
title: IDXCoreAdapter::QueryState
description: Извлекает текущее состояние указанного элемента на адаптере.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 61fc5c601904011de8f343777a95385a16ec3d7e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719137"
---
# <a name="idxcoreadapterquerystate-method"></a>Метод Идкскореадаптер:: Куеристате

Извлекает текущее состояние указанного элемента на адаптере. Перед вызовом **куеристате** для типа свойства вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE QueryState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t outputBufferSize,
  _Out_writes_bytes_(outputBufferSize) void *outputBuffer) = 0;

template <class T1, class T2>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _In_reads_bytes_opt_(sizeof(T1)) const T1 *inputStateDetails,
  _Out_writes_bytes_(sizeof(T2)) T2 *outputBuffer);

template <class T>
HRESULT QueryState( 
  DXCoreAdapterState state,
  _Out_writes_bytes_(sizeof(T)) T *outputBuffer);
```

## <a name="parameters"></a>Параметры

### <a name="state"></a>state

Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**

Тип элемента состояния на адаптере, состояние которого вы хотите получить. Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>инпутстатедетаилссизе

Тип: **size_t**

Размер (в байтах) буфера сведений о входном состоянии, который вы (необязательно) выделяете и предоставляете в *инпутстатедетаилс*.

### <a name="inputstatedetails-in"></a>Инпутстатедетаилс [in]

Тип: **void const \***

Необязательный указатель на постоянный буфер сведений о состоянии ввода, который вы выделили в приложении, содержащий все сведения о запросе, необходимые для типа состояния, указанного в поле *штат*. Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="outputbuffersize"></a>аутпутбуфферсизе

Тип: **size_t**

Размер (в байтах) выходного буфера, который вы выделили и предоставляющих в *outputBuffer*.

### <a name="outputbuffer-out"></a>outputBuffer [out]

Тип: **void \***

Указатель на выходной буфер, выделенный в приложении, и который заполняется функцией. Дополнительные сведения о требованиях к выходному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Адаптер больше не находится в допустимом состоянии.|
|DXGI_ERROR_INVALID_CALL|Тип состояния, указанный в *состоянии* , не распознается данной операционной системой (ОС). Вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).|
|DXGI_ERROR_UNSUPPORTED|Тип состояния, указанный в *состоянии* , не поддерживается адаптером. Вызовите [искуеристатесуппортед](./nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) , чтобы убедиться, что запрос типа состояния доступен для этого адаптера и операционной системы (ОС).|
|E_INVALIDARG|Недостаточный размер буфера предоставляется для *outputBuffer* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).|
|E_POINTER|`nullptr` был предоставлен для *outputBuffer* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).|

## <a name="remarks"></a>Комментарии

Дополнительные сведения о каждом типе состояния адаптера и используемых входных и выходных данных см. в разделе [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) . Эта функция обнуляет буфер *outputBuffer* перед заполнением.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)