---
description: Помещает в объект Ивордформсинк альтернативную форму слова.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: 'Ивордформсинк: метод:P Уталтворд (Search. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 874428ed435d2336398f6e72c58b70de275565cce2e606f1fdddea54f0684742
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944414"
---
# <a name="iwordformsinkputaltword-method"></a>Ивордформсинк: метод:P Уталтворд

Помещает в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) альтернативную форму слова.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвЦинбуф* \[ окне\]
</dt> <dd>

Указатель на буфер, содержащий альтернативную форму слова.

</dd> <dt>

*КВК* \[ окне\]
</dt> <dd>

Число символов в *пвЦинбуф*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Код возврата                                                                                              | Описание                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>                     | Операция успешно завершена. <br/>                                                                                             |
| <dl> <dt>**Языковая \_ \_крупное \_ слово S**</dt> </dl> | Значение *КВК* больше, чем значение *улмакстокенсизе* , указанное в [**истеммер:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init). <br/> |



 

## <a name="remarks"></a>Remarks

Этот метод вызывается из метода [**женератевордформс**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) реализации [**истеммер**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) . Все альтернативные формы для слова, за исключением последнего, помещаются в объект [**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) путем вызова **Ивордформсинк::P уталтворд**. Последняя альтернативная форма слова, которая всегда является исходной формой слова, обрабатывается путем вызова [**ивордформсинк::P утворд**](iwordformsink-putword.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                |
| Заголовок<br/>                   | <dl> <dt>Поиск. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивордформсинк**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
