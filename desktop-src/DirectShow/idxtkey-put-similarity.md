---
description: Метод "разместить \_ подобие" задает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.
ms.assetid: f033b226-f36d-4288-b17e-e173546caee1
title: 'Идксткэй: метод ut_Similarity:p (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2f2aec52b987a1d4f146f2261d44a289ddac59f3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675808"
---
# <a name="idxtkeyput_similarity-method"></a>Идксткэй: \_ метод сходства:p UT

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`put_Similarity`Метод задает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_Similarity(
  [in] int newVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Задает значение подобия. Допустимый диапазон: от 0 до 100.

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
</dt> <dt>

[**Идксткэй::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




