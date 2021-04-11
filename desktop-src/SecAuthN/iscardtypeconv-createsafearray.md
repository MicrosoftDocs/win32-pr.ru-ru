---
description: Создает SAFEARRAY автоматизации для неподписанных символов (в байтах).
ms.assetid: 67cc8cd1-95be-4498-ac25-6c418089af27
title: 'Метод Искардтипеконв:: Креатесафеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateSafeArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 6bc27a3f50f0740eca178787fd021f76c9b6729e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143420"
---
# <a name="iscardtypeconvcreatesafearray-method"></a>Метод Искардтипеконв:: Креатесафеаррай

\[Метод **креатесафеаррай** доступен для использования в операционных системах, указанных в разделе требования. Он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздней версии, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **креатесафеаррай** создает SAFEARRAY автоматизации для неподписанных символов (в байтах).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSafeArray(
  [in]  UINT        nAllocSize,
  [out] LPSAFEARRAY *ppArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*наллоксизе* \[ окне\]
</dt> <dd>

Размер в байтах памяти, выделяемой для массива.

</dd> <dt>

*ппаррай* \[ заполняет\]
</dt> <dd>

Указатель на возвращаемый объект SAFEARRAY.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Выделенная память успешно распределена.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно свободной памяти для удовлетворения запроса.<br/>                                            |



 

## <a name="remarks"></a>Комментарии

Чтобы создать типичный массив байтов C/C++, вызовите [**креатебитеаррай**](iscardtypeconv-createbytearray.md).

Чтобы создать универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)), вызовите [**креатебитебуффер**](iscardtypeconv-createbytebuffer.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искардтипеконв**](iscardtypeconv.md)
</dt> <dt>

[Возвращаемые значения смарт-карты](authentication-return-values.md)
</dt> <dt>

[**креатебитеаррай**](iscardtypeconv-createbytearray.md)
</dt> <dt>

[**креатебитебуффер**](iscardtypeconv-createbytebuffer.md)
</dt> </dl>

 

 
