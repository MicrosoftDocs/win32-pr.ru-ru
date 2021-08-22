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
ms.openlocfilehash: 9ebb49b2857c23bb11b5e4d091dece820bb833b2b4e77224558f2d7972885445
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027742"
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



 

## <a name="remarks"></a>Remarks

Отсутствует.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмдрменкрипт**](iwmdrmencrypt.md)
</dt> <dt>

[**вмдрмкриптодата**](wmdrmcryptodata.md)
</dt> </dl>

 

 





