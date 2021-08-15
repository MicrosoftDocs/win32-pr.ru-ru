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
ms.openlocfilehash: 5dbd14b2791441f5c09a7242d6f8c1e343413f8c3cd94fc0519ac6487857b7d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399134"
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

## <a name="remarks"></a>Remarks

> [!Note]  
> Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.

 

> [!Note]  
> чтобы получить кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (sp1).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Кедит. h</dt> </dl>      |
| Библиотека<br/> | <dl> <dt>Стрмиидс. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Идксткэй**](idxtkey.md)
</dt> <dt>

[**Идксткэй::p UT \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




