---
title: Метод Ивмдрменкрипт Encrypt (Вмдрмсдк. h)
description: Метод Encrypt шифрует буфер данных на месте.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Шифрование метода Windows Media Format
- Шифрование метода Windows Media Format, интерфейс Ивмдрменкрипт
- Интерфейс Ивмдрменкрипт интерфейса Windows Media Format, метод Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717761"
---
# <a name="iwmdrmencryptencrypt-method"></a>Метод Ивмдрменкрипт:: Encrypt

Метод **Encrypt** шифрует буфер данных на месте.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pbData* \[ в, out\]
</dt> <dd>

Данные для шифрования. Если метод завершился удачно, данные шифруются при возврате.

</dd> <dt>

*cbData* \[ окне\]
</dt> <dd>

Размер данных в байтах.

</dd> <dt>

*пвмкриптодата* \[ окне\]
</dt> <dd>

Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую дополнительные параметры. Задайте **значение NULL** , чтобы использовать значения шифрования по умолчанию.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрменкрипт**](iwmdrmencrypt.md)
</dt> <dt>

[**вмдрмкриптодата**](wmdrmcryptodata.md)
</dt> </dl>

 

 





