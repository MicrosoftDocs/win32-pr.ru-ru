---
title: Метод дешифровки Ивмдрмдекрипт (Вмдрмсдк. h)
description: Метод дешифровки расшифровывает буфер данных на месте.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Расшифровка метода Windows Media Format
- Метод расшифровки формата Windows Media Format, интерфейс Ивмдрмдекрипт
- Интерфейс Ивмдрмдекрипт интерфейса Windows Media Format, метод дешифрации
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be82ec976da39103698b93a09b3d5235c8c8ee712783ca8284dc7b18c6a8a27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027752"
---
# <a name="iwmdrmdecryptdecrypt-method"></a>Ивмдрмдекрипт: метод:D екрипт

Метод **дешифровки** расшифровывает буфер данных на месте.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pbData* \[ в, out\]
</dt> <dd>

Данные для расшифровки. Если метод завершился удачно, эти данные расшифровываются при возврате.

</dd> <dt>

*cbData* \[ окне\]
</dt> <dd>

Размер данных в байтах.

</dd> <dt>

*пвмкриптодата* \[ окне\]
</dt> <dd>

Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую дополнительные параметры. Может иметь **значение NULL** , если содержимое было зашифровано с помощью параметров по умолчанию.

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

[**Интерфейс Ивмдрмдекрипт**](iwmdrmdecrypt.md)
</dt> <dt>

[**вмдрмкриптодата**](wmdrmcryptodata.md)
</dt> </dl>

 

 





