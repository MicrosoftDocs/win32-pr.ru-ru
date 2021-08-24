---
title: Ивмдрмдевице Клеандатасторе, метод
description: Метод Клеандатасторе запускает процесс очистки хранилища данных DRM на устройстве.
ms.assetid: aad99137-6d2b-4612-8014-9783035af929
keywords:
- Метод Клеандатасторе Windows Media диспетчер устройств
- Метод Клеандатасторе Windows Media диспетчер устройств, интерфейс Ивмдрмдевице
- Интерфейс Ивмдрмдевице Windows Media диспетчер устройств, метод Клеандатасторе
topic_type:
- apiref
api_name:
- IWMDRMDevice.CleanDataStore
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9decc999d1ecb6c97359d1c4c169b84e7f67da88f5fa25bfe2cb17b2c31f9fd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766644"
---
# <a name="iwmdrmdevicecleandatastore-method"></a>Метод Ивмдрмдевице:: Клеандатасторе

Метод **клеандатасторе** запускает процесс очистки хранилища данных DRM на устройстве.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CleanDataStore(
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Флаги для критериев очистки хранилища.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ВМДДРМСП. idl</dt> </dl> |
| Библиотека<br/> | <dl> <dt>Мссачлп. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмдрмдевице**](iwmdrmdevice.md)
</dt> </dl>

 

 





