---
description: Метод «вставить \_ KeyType» указывает тип ключа.
ms.assetid: 4a6201e6-1939-4da6-8c9f-1c34b9713ecb
title: 'Идксткэй: метод ut_KeyType:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8e5e501c1f678adb857e39d579fbd958127652a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675318"
---
# <a name="idxtkeyput_keytype-method"></a>Идксткэй::p \_ метода UT KeyType

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_KeyType`Метод задает тип ключа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_KeyType(
  [in] int newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Указывает тип ключа. Этот параметр должен быть одним из следующих значений перечисления.



| Значение             | Описание                                           |
|-------------------|-------------------------------------------------------|
| ДКСТКЭЙ \_ RGB       | Ключ чрома. (Ключ для значения RGB.)                       |
| ДКСТКЭЙ \_ нонред    | Ключ нонред. (Делает прозрачными синие и зеленые области.) |
| \_светимость дксткэй | Ключ освещенности.                                        |
| ДКСТКЭЙ \_ Alpha     | Ключ по значению альфа.                                   |
| оттенок ДКСТКЭЙ \_       | Ключ с оттенокм.                                           |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> </dl>

 

 




