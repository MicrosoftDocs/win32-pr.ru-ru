---
title: Метод Ивмдрменкриптскаттер Инитенкриптскаттер (Вмдрмсдк. h)
description: Метод Инитенкриптскаттер инициализирует интерфейс Ивмдрменкриптскаттер для использования.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Формат Windows Media, Инитенкриптскаттер метод
- Инитенкриптскаттер метод Windows Media Format, интерфейс Ивмдрменкриптскаттер
- Интерфейс Ивмдрменкриптскаттер Windows Media Format, метод Инитенкриптскаттер
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e83cce80b218d4cc8482d013537b7fae562312f242bc3549f4fa5069b1c677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027762"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a>Метод Ивмдрменкриптскаттер:: Инитенкриптскаттер

Метод **инитенкриптскаттер** инициализирует интерфейс **ивмдрменкриптскаттер** для использования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кстреамс* \[ окне\]
</dt> <dd>

Число элементов в массиве *ргинфос* . Это также число потоков, включенных в зашифрованные данные.

</dd> <dt>

*ргинфос* \[ окне\]
</dt> <dd>

Массив из одной или нескольких [**структур \_ \_ \_ сведений о шифрующей**](wmdrm-encrypt-scatter-info.md) подразделении WMDRM. Каждый элемент содержит сведения о шифровании для потока. Число элементов в этом массиве должно быть равно значению параметра *кстреамс*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**енкриптскаттер**](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[**Интерфейс Ивмдрменкриптскаттер**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





