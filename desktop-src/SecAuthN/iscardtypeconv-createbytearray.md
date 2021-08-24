---
description: Создает типичный массив байтов C/C++.
ms.assetid: 915e8cca-2a0f-409e-a6df-54fa73bdc305
title: 'Метод Искардтипеконв:: Креатебитеаррай (Скарддат. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.CreateByteArray
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 297fc58d3a1457e48a16eb4330b11b506813eae23218484d3dbacce637f194c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013754"
---
# <a name="iscardtypeconvcreatebytearray-method"></a>Метод Искардтипеконв:: Креатебитеаррай

\[Метод **креатебитеаррай** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. [Модули смарт-карт](/previous-versions/windows/desktop/secsmart/smart-card-modules) предоставляют аналогичные функции.\]

Метод **креатебитеаррай** создает типичный массив байтов C/C++.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateByteArray(
  [in]  DWORD  dwAllocSize,
  [out] LPBYTE *ppbyArray
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*дваллоксизе* \[ окне\]
</dt> <dd>

Размер (в байтах) памяти, выделяемой для массива.

</dd> <dt>

*ппбяррай* \[ заполняет\]
</dt> <dd>

Указатель на массив байтов, который необходимо вернуть.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает одно из следующих возможных значений:



| Код возврата                                                                                   | Описание                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Выделенная память успешно распределена.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Возникла проблема с одним или несколькими параметрами, передаваемыми в функцию.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно свободной памяти для удовлетворения запроса.<br/>                                            |



 

## <a name="remarks"></a>Remarks

Чтобы создать универсальный буфер байтов, сопоставленный с объектом **IStream** ([**ибитебуффер**](ibytebuffer.md)), вызовите [**креатебитебуффер**](iscardtypeconv-createbytebuffer.md).

Чтобы создать набор SAFEARRAY автоматизации для неподписанных символов (байт), вызовите [**креатесафеаррай**](iscardtypeconv-createsafearray.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скарддат. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скарддат. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ искардтипеконв определен как 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>См. также

<dl> <dt>

[**искардтипеконв**](iscardtypeconv.md)
</dt> <dt>

[Возвращаемые значения смарт-карты](authentication-return-values.md)
</dt> <dt>

[**креатебитебуффер**](iscardtypeconv-createbytebuffer.md)
</dt> <dt>

[**креатесафеаррай**](iscardtypeconv-createsafearray.md)
</dt> </dl>

 

 
