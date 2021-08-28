---
title: Метод Ивмдрменкриптскаттер Енкриптскаттер (Вмдрмсдк. h)
description: Метод Енкриптскаттер выполняет расшифровку и шифрование данных.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Формат Windows Media, Енкриптскаттер метод
- Енкриптскаттер метод Windows Media Format, интерфейс Ивмдрменкриптскаттер
- Интерфейс Ивмдрменкриптскаттер Windows Media Format, метод Енкриптскаттер
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fae3f8a40bc5468898424dcf33bf947235a632db44f4dada7f2c96b2a3a064b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839714"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a>Метод Ивмдрменкриптскаттер:: Енкриптскаттер

Метод **енкриптскаттер** выполняет расшифровку и шифрование данных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кблоккс* \[ окне\]
</dt> <dd>

Число элементов в массиве *ргблоккс* .

</dd> <dt>

*ргблоккс* \[ окне\]
</dt> <dd>

Массив из одной или нескольких [**структур \_ \_ \_ блоков с шифрованием WMDRM**](wmdrm-encrypt-scatter-block.md) . Каждый элемент описывает блок данных для расшифровки и шифрования.

</dd> <dt>

*пвмкриптодата* \[ окне\]
</dt> <dd>

Указатель на структуру [**вмдрмкриптодата**](wmdrmcryptodata.md) , содержащую параметры шифрования. Задайте для параметра **значение NULL** , чтобы использовать параметры по умолчанию.

</dd> <dt>

*кбаутпут* \[ окне\]
</dt> <dd>

Размер буфера выходных данных, переданного как *пбаутпут*.

</dd> <dt>

*пбаутпут* \[ заполняет\]
</dt> <dd>

Выходной буфер.

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

[**инитенкриптскаттер**](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[**Интерфейс Ивмдрменкриптскаттер**](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





