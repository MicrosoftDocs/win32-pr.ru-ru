---
description: Метод Initialize подготавливает объект Ибитебуффер для использования. Этот метод должен быть вызван до вызова любых других методов в интерфейсе Ибитебуффер.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: 'Метод Ибитебуффер:: Initialize (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417634"
---
# <a name="ibytebufferinitialize-method"></a>Метод Ибитебуффер:: Initialize

\[Метод **Initialize** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий. Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]

Метод **Initialize** подготавливает объект [**ибитебуффер**](ibytebuffer.md) для использования. Этот метод должен быть вызван до вызова любых других методов в интерфейсе **ибитебуффер** .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*лсизе* \[ окне\]
</dt> <dd>

Начальный размер (в байтах) данных, которые должен содержать поток.

</dd> <dt>

*pData* \[ окне\]
</dt> <dd>

Если не **равно NULL**, начальные данные для записи в поток.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает на Успешный вызов.

## <a name="remarks"></a>Remarks

При использовании нового потока [**ибитебуффер**](ibytebuffer.md) Вызывайте этот метод перед использованием любого из других методов **ибитебуффер** .

## <a name="examples"></a>Примеры

В следующем примере показана инициализация объекта [**ибитебуффер**](ibytebuffer.md) .


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Скардссп. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардссп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

