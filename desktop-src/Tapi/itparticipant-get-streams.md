---
description: Метод Get \_ Streams создает коллекцию потоков, связанных с текущим участником.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'Метод ИтпартиЦипант:: get_Streams (Ипмсп. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675485"
---
# <a name="itparticipantget_streams-method"></a>Метод ИтпартиЦипант:: Get \_ Streams

\[**получить \_ Потоки** недоступны для использования в Windows Vista, Windows Server 2008 и последующих версиях операционной системы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Метод **Get \_ Streams** создает коллекцию потоков, связанных с текущим участником. Этот метод предоставляется для клиентских приложений автоматизации, например, написанных на Visual Basic. Приложения C и C++ должны использовать метод [**енумератестреамс**](itparticipant-enumeratestreams.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвариант* \[ заполняет\]
</dt> <dd>

Указатель на **вариант** , содержащий [**итколлектион**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) указателей интерфейса [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать одно из этих значений.



| Значение                                                                                         | Значение                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Метод успешно выполнен.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения операции.<br/> |
| <dl> <dt>**\_указатель E**</dt> </dl>     | Параметр *пвариант* не является допустимым указателем.<br/>     |



 

## <a name="remarks"></a>Комментарии

TAPI вызывает метод **AddRef** в интерфейсе [**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) , возвращенном **итпартиЦипант:: Get \_ Streams**. Приложение должно вызвать **выпуск** в интерфейсе **итстреам** , чтобы освободить ресурсы, связанные с ним.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|--------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                                |
| Header<br/>       | <dl> <dt>Ипмсп. h</dt> </dl>   |
| Библиотека<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итпартиЦипант**](itparticipant.md)
</dt> <dt>

[**енумератестреамс**](itparticipant-enumeratestreams.md)
</dt> <dt>

[**иенумстреам**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[**итколлектион**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**итстреам**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

