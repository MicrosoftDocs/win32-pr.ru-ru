---
title: Идврителокалфонтфилелоадер Жетфилепасфромкэй, метод
description: Получает абсолютный путь к файлу шрифта из ключа ссылки на файл шрифта.
ms.assetid: a61cfe80-100d-4813-b04f-a39f626893dd
keywords:
- Непосредственная запись метода Жетфилепасфромкэй
- Прямая запись метода Жетфилепасфромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетфилепасфромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14fb3070ddc2f0d82554c86f005343faa3c087fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688938"
---
# <a name="idwritelocalfontfileloadergetfilepathfromkey-method"></a>Метод Идврителокалфонтфилелоадер:: Жетфилепасфромкэй

Получает абсолютный путь к файлу шрифта из ключа ссылки на файл шрифта.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetFilePathFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       WCHAR  *filePath,
              UINT32 filePathSize
) = 0;
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*фонтфилереференцекэй* \[ окне\]
</dt> <dd>

Тип: **константа \* void**

Ключ ссылки на файл шрифта, однозначно определяющий файл локального шрифта в пределах используемого загрузчика шрифтов.

</dd> <dt>

*фонтфилереференцекэйсизе* 
</dt> <dd>

Тип: **UINT32**

Размер ключа ссылки на файл шрифта в байтах.

</dd> <dt>

*путь к файлу* \[ заполняет\]
</dt> <dd>

Тип: **WCHAR \***

Массив символов, который получает путь к локальному файлу.

</dd> <dt>

*филепассизе* 
</dt> <dd>

Тип: **UINT32**

Длина массива символов пути к файлу.

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

 

 





