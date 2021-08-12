---
title: IDXCoreAdapter::GetProperty
description: Извлекает значение указанного свойства адаптера.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 8adb48994580125d153c36394c4db65cb38f4a08306814d1638e5c27eb3d4868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279404"
---
# <a name="idxcoreadaptergetproperty-method"></a>Идкскореадаптер:: метод Property

Извлекает значение указанного свойства адаптера. Перед вызовом метода **Property** для типа свойства вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС). Кроме того, перед вызовом метода **Property** вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить необходимый размер буфера, в котором будет получено значение свойства.

## <a name="syntax"></a>Синтаксис

```cpp
virtual HRESULT STDMETHODCALLTYPE GetProperty(
  DXCoreAdapterProperty property,
  size_t bufferSize,
  _Out_writes_bytes_(bufferSize) void *propertyData) = 0;

template <class T>
HRESULT GetProperty( 
  DXCoreAdapterProperty property,
  _Out_writes_bytes_(sizeof(T)) T *propertyData);
```

## <a name="parameters"></a>Параметры

### <a name="property"></a>свойство;

Тип: **[дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Тип свойства, значение которого необходимо получить. Дополнительные сведения о каждом свойстве адаптера см. в таблице в [дкскореадаптерпроперти](./ne-dxcore_interface-dxcoreadapterproperty.md) .

### <a name="buffersize"></a>bufferSize

Тип: **size_t**

Размер (в байтах) выходного буфера, который вы выделили и предоставляющих в *PropertyData*.

### <a name="propertydata-out"></a>propertyData [out]

Тип: **void \***

Указатель на выходной буфер, выделенный в приложении, и который заполняется функцией. Вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить размер буфера *PropertyData* для заданного свойства адаптера.

## <a name="returns"></a>Возвращаемое значение

Тип: **[HRESULT](../../com/structure-of-com-error-codes.md)**

Если функция завершается с ошибкой, она возвращает **S_OK**. В противном случае возвращается [](../../com/structure-of-com-error-codes.md) [код ошибки](../../com/com-error-codes-10.md)HRESULT.

|Возвращаемое значение|Описание|
|-|-|
|DXGI_ERROR_INVALID_CALL|Тип свойства, указанный в *свойстве* , не распознается данной операционной системой (ОС). Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).|
|DXGI_ERROR_UNSUPPORTED|Тип свойства, указанный в *свойстве* , не поддерживается адаптером. Вызовите [испропертисуппортед](./nf-dxcore_interface-idxcoreadapter-ispropertysupported.md) , чтобы убедиться, что тип свойства доступен для этого адаптера и операционной системы (ОС).|
|E_INVALIDARG|Недостаточный размер буфера указан в *PropertyData*. Вызовите [жетпропертисизе](./nf-dxcore_interface-idxcoreadapter-getpropertysize.md) , чтобы определить размер буфера *PropertyData* для заданного свойства адаптера.|
|E_POINTER|`nullptr` был предоставлен для *PropertyData*.|

## <a name="remarks"></a>Remarks

Вы можете вызвать метод **Property** для адаптера, который больше не является допустимым &mdash; . в результате эта функция не будет завершаться ошибкой. Эта функция обнуляет буфер *PropertyData* перед заполнением.

## <a name="see-also"></a>См. также раздел

[Идкскореадаптер](./nn-dxcore_interface-idxcoreadapter.md), [дкскоре Reference](../dxcore-reference.md), [Использование дкскоре для перечисления адаптеров](../dxcore-enum-adapters.md)