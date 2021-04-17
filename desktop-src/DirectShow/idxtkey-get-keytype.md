---
description: Метод Get \_ KeyType Извлекает тип ключа.
ms.assetid: 902cbd46-529a-45d8-afa2-a8dd9439769a
title: 'Метод Идксткэй:: get_KeyType (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_KeyType
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7341815169549f24db55518e021b9e5096286a65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675327"
---
# <a name="idxtkeyget_keytype-method"></a>Метод Идксткэй:: Get \_ KeyType

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_KeyType`Метод получает тип ключа.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_KeyType(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает одно из следующих значений перечисления.



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

 

 




