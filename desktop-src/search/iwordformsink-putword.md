---
description: Помещает исходную форму Word в объект Ивордформсинк.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'Ивордформсинк: метод:P Утворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692185"
---
# <a name="iwordformsinkputword-method"></a>Ивордформсинк: метод:P Утворд

Помещает исходную форму Word в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвЦинбуф* \[ окне\]
</dt> <dd>

Указатель на буфер, содержащий последнюю альтернативную форму слова, которое всегда является исходным словом.

</dd> <dt>

*КВК* \[ окне\]
</dt> <dd>

Число символов в *пвЦинбуф*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                          | Описание                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Операция успешно завершена. <br/> |



 

## <a name="remarks"></a>Комментарии

**Путворд** вызывается из метода [**женератевордформс**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) реализации [**истеммер**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Этот метод обрабатывает исходную форму слова и вызывается последним. Все предыдущие формы для слова помещаются в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) путем вызова [**Ивордформсинк::P уталтворд**](iwordformsink-putphrase.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Поиск. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
