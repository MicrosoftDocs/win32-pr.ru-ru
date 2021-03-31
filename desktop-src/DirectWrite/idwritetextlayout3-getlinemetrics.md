---
title: IDWriteTextLayout3 Жетлинеметрикс, метод
description: Извлекает свойства каждой строки.
ms.assetid: 352ca3e3-7b08-823c-0881-0b051d4ce574
keywords:
- Непосредственная запись метода Жетлинеметрикс
- Прямая запись метода Жетлинеметрикс, интерфейс IDWriteTextLayout3
- Прямая запись интерфейса IDWriteTextLayout3, метод Жетлинеметрикс
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d10a06cbf123b71e1308b45c747ac8a840a5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491409"
---
# <a name="idwritetextlayout3getlinemetrics-method"></a>Метод IDWriteTextLayout3:: Жетлинеметрикс

Извлекает свойства каждой строки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLineMetrics(
  [out] DWRITE_LINE_METRICS1 *lineMetrics,
        UINT32               maxLineCount,
  [out] UINT32               *actualLineCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*линеметрикс* \[ заполняет\]
</dt> <dd>

Массив, который заполняется сведениями о строке.

</dd> <dt>

*макслинекаунт* 
</dt> <dd>

Максимальный размер массива Линеметрикс.

</dd> <dt>

*актуаллинекаунт* \[ заполняет\]
</dt> <dd>

Фактический размер требуемого массива Линеметрикс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Если размер Макслинекаунт не достаточен \_ \_ для недостаточного размера \_ буфера, что эквивалентно значению HRESULT \_ из \_ Win32 (ошибка \_ недостаточна для \_ буфера), возвращается значение, а для актуаллинекаунт задается необходимое количество строк.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только Windows 8.1 Классические приложения\]<br/>                                            |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2012 R2 \[\]<br/>                                 |
| Минимальный поддерживаемый телефон<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 и среда выполнения Windows приложения\]<br/> |
| Библиотека<br/>                  | <dl> <dt>Дврите. lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IDWriteTextLayout3**](idwritetextlayout3.md)
</dt> </dl>

 

 





