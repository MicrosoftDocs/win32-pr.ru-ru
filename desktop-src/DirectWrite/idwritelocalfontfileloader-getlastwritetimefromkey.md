---
title: Идврителокалфонтфилелоадер Жетластвритетимефромкэй, метод
description: Получает время последней записи файла из ключа ссылки на файл шрифта.
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- Непосредственная запись метода Жетластвритетимефромкэй
- Прямая запись метода Жетластвритетимефромкэй, интерфейс Идврителокалфонтфилелоадер
- Прямая запись интерфейса Идврителокалфонтфилелоадер, метод Жетластвритетимефромкэй
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689025"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>Метод Идврителокалфонтфилелоадер:: Жетластвритетимефромкэй

Получает время последней записи файла из ключа ссылки на файл шрифта.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
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

*LastWriteTime* \[ заполняет\]
</dt> <dd>

Тип: **fileTime \***

Время последнего изменения файла шрифта.

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

 

 





