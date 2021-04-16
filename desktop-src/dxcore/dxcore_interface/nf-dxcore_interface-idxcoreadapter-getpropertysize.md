---
title: IDXCoreAdapter::GetPropertySize
description: Для указанного свойства адаптера получает размер буфера в байтах, необходимого для вызова метода [Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md).
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ff077d3c4c827a55f7fd9b10dfe93f1271649f72
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105719126"
---
# <a name="idxcoreadaptergetpropertysize-method"></a>Метод Идкскореадаптер:: Жетпропертисизе

Для указанного свойства адаптера получает размер буфера в байтах, необходимого для вызова метода [Property](./nf-dxcore_interface-idxcoreadapter-getproperty.md). Перед вызовом **жетпропертисизе** для типа свойства вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetPropertySize(
  DXCoreAdapterProperty property,
  _Out_ size_t *bufferSize) = 0;
```

## <a name="parameters"></a>Параметры

### <a name="property"></a>свойство;

Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Тип свойства, размер которого требуется получить в байтах.

### <a name="buffersize-out"></a>bufferSize [out]

Тип: **size_t \***

Указатель на значение **size_t** . Функция отменяет ссылку на указатель и задает для него значение размера (в байтах) выходного буфера, который необходимо выделить, и передать в качестве аргумента *PropertyData* в вызове метода [IsReference.](./nf-dxcore_interface-idxcoreadapter-getproperty.md)

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_INVALID_CALL|Тип свойства, указанный в *свойстве* , не распознается данной операционной системой (ОС). Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).|
|DXGI_ERROR_UNSUPPORTED|Тип свойства, указанный в *свойстве* , не поддерживается адаптером. Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).|
|E_POINTER|`nullptr` был предоставлен для *bufferSize*.|

## <a name="remarks"></a>Комментарии

Вы можете вызвать **жетпропертисизе** на адаптере, который больше не является допустимым &mdash; , функция не завершится ошибкой.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)