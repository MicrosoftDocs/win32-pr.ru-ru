---
description: 'Метод revert отменяет все изменения, внесенные в поток транзакций с момента последнего вызова Ибитебуффер:: Commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Метод Ибитебуффер:: revert (Скардссп. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46e535560332c43d250b0a26183036342c8cca29144e3d2d1803582387af6bd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101264"
---
# <a name="ibytebufferrevert-method"></a>Метод Ибитебуффер:: revert

\[Метод **revert** доступен для использования в операционных системах, указанных в разделе требования. он недоступен для использования в Windows Server 2003 с пакетом обновления 1 (SP1) и более поздних версий, Windows Vista, Windows Server 2008 и последующих версиях операционной системы. Интерфейс [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) предоставляет аналогичные функциональные возможности.\]

Метод **revert** отменяет все изменения, внесенные в поток транзакций с момента последнего вызова [**Ибитебуффер:: Commit**](ibytebuffer-commit.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает, что вызов был успешным, и поток был восстановлен до предыдущей версии.

## <a name="remarks"></a>Remarks

Этот метод отклоняет изменения, внесенные в поток транзакций с момента последней операции фиксации.

## <a name="examples"></a>Примеры

В следующем примере показан возврат транзакционного потока к последней операции фиксации.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Окончание поддержки клиента<br/>    | Windows XP<br/>                                                                   |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Скардссп. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Скардссп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ибитебуффер определен как E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

