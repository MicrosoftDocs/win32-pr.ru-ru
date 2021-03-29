---
title: Идврителокалфонтфилелоадер Жетфилепасленгсфромкэй, метод
description: Получает длину абсолютного пути к файлу из ключа ссылки на файл шрифта.
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- Непосредственная запись метода Жетфилепасленгсфромкэй
- Прямая запись метода Жетфилепасленгсфромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетфилепасленгсфромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 091c3cd5f1e13c40d364a3db005793f1dd0bf5f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668876"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>Метод Идврителокалфонтфилелоадер:: Жетфилепасленгсфромкэй

Получает длину абсолютного пути к файлу из ключа ссылки на файл шрифта.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фонтфилереференцекэй* \[ окне\]
</dt> <dd>

Тип: **константа \* void**

Ключ ссылки на файл шрифта, однозначно определяющий файл локального шрифта в области используемого загрузчика шрифтов.

</dd> <dt>

*фонтфилереференцекэйсизе* 
</dt> <dd>

Тип: **UINT32**

Размер ключа ссылки на файл шрифта в байтах.

</dd> <dt>

*филепасленгс* \[ заполняет\]
</dt> <dd>

Тип: **UINT32 \***

Длина строки пути к файлу, не включая завершающий символ **null** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Библиотека<br/> | <dl> <dt>Дврите. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**идврителокалфонтфилелоадер**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





