---
title: Функция обратного вызова Жеттсаудиоендпоинтенумераторфорсессион
description: Возвращает ссылку на перечислитель конечной точки аудио для указанного идентификатора сеанса.
ms.assetid: 9dd95ef7-f83f-43be-a8b2-e2b0e4a47a42
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов функции обратного вызова Жеттсаудиоендпоинтенумераторфорсессион
topic_type:
- apiref
api_name:
- GetTSAudioEndpointEnumeratorForSession
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d6c09896fc4b35fcb0b6a01a7d592421dd5d5654
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682083"
---
# <a name="gettsaudioendpointenumeratorforsession-callback-function"></a>Функция обратного вызова Жеттсаудиоендпоинтенумераторфорсессион

Возвращает ссылку на перечислитель конечной точки аудио для указанного идентификатора сеанса. Потребители этого перечислителя конечной точки аудио, такие как MMDevAPI.dll, вызывают эту функцию, чтобы получить перечислитель конечных точек аудио в службы удаленных рабочих столовном сеансе.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetTSAudioEndpointEnumeratorForSession(
  _In_  DWORD               SessionId,
  _Out_ IMMDeviceEnumerator **ppEndpointEnumerator
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Идентификатор сеанса* \[ окне\]
</dt> <dd>

Идентификатор сеанса службы удаленных рабочих столов.

</dd> <dt>

*ппендпоинтенумератор* \[ заполняет\]
</dt> <dd>

Адрес указателя на интерфейс [**иммдевицеенумератор**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, возвращается значение **S \_ ОК**.

## <a name="remarks"></a>Комментарии

Эта функция не определена в файле заголовка. Эту функцию следует реализовать и экспортировать в пользовательский перечислитель конечной точки и использовать сигнатуру, приведенную в блоке синтаксиса ранее в этом разделе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>         |
| Минимальная версия сервера<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Реализация пользовательского перечислителя конечной точки аудио](implementing-an-audio-endpoint-enumerator.md)
</dt> <dt>

[**иммдевицеенумератор**](/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
</dt> </dl>

 

