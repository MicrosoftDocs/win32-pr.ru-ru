---
title: IDXCoreAdapter::SetState
description: Задает состояние указанного элемента на адаптере.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8cbeacdb8c6020441b5dd74a9f9233a6c112b4f6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719136"
---
# <a name="idxcoreadaptersetstate-method"></a>Метод Идкскореадаптер:: SetState

Задает состояние указанного элемента на адаптере. Перед вызовом **SetState** для типа свойства вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE SetState( 
  DXCoreAdapterState state,
  size_t inputStateDetailsSize,
  _In_reads_bytes_opt_(inputStateDetailsSize) const void *inputStateDetails,
  size_t inputDataSize,
  _In_reads_bytes_(inputDataSize) const void *inputData) = 0;

template <class T1, class T2>
HRESULT SetState( 
  DXCoreAdapterState state,
  const T1 *inputStateDetails,
  const T2 *inputData);
```

## <a name="parameters"></a>Параметры

### <a name="state"></a>state

Тип: **[дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md)**

Тип элемента состояния на адаптере, состояние которого вы хотите задать. Дополнительные сведения о каждом типе состояния адаптера см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputstatedetailssize"></a>инпутстатедетаилссизе

Тип: **size_t**

Размер (в байтах) буфера сведений о входном состоянии, который вы (необязательно) выделяете и предоставляете в *инпутстатедетаилс*.

### <a name="inputstatedetails-in"></a>Инпутстатедетаилс [in]

Тип: **void const \***

Необязательный указатель на постоянный буфер сведений о состоянии ввода, который вы выделили в приложении, содержащий все сведения о запросе, необходимые для типа состояния, указанного в поле *штат*. Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

### <a name="inputdatasize"></a>инпутдатасизе

Тип: **size_t**

Размер (в байтах) входного буфера, который вы выделили и предоставляющих в *inputData*.

### <a name="inputdata-in"></a>inputData [in]

Тип: **void \***

Указатель на входной буфер, выделенный в приложении, содержащий сведения о состоянии, которые необходимо задать для элемента состояния, тип которого указан в поле *штат*. Дополнительные сведения о требованиях к входному буферу для данного типа состояния см. в таблице в [дкскореадаптерстате](./ne-dxcore_interface-dxcoreadapterstate.md) .

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_DEVICE_REMOVED|Адаптер больше не находится в допустимом состоянии.|
|DXGI_ERROR_INVALID_CALL|Тип состояния, указанный в *состоянии* , не распознается данной операционной системой (ОС). Вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).|
|DXGI_ERROR_UNSUPPORTED|Тип состояния, указанный в *состоянии* , не поддерживается адаптером. Вызовите [иссетстатесуппортед](./nf-dxcore_interface-idxcoreadapter-issetstatesupported.md) , чтобы убедиться, что задание типа состояния доступно для этого адаптера и операционной системы (ОС).|
|E_INVALIDARG|Недостаточный размер буфера предоставляется для *inputData* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).|
|E_POINTER|`nullptr` был предоставлен для *inputData* (или для *инпутстатедетаилс* , где необходим буфер сведений о состоянии входа).|

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)