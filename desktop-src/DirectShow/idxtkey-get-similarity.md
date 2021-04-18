---
description: Метод "получить \_ подобие" извлекает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.
ms.assetid: ddf82759-fe71-4e06-b73c-c450b7cce43d
title: 'Метод Идксткэй:: get_Similarity (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.get_Similarity
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e53898a1f9c5175fdf7a42ba6de68e3173f02afe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675323"
---
# <a name="idxtkeyget_similarity-method"></a>Метод Идксткэй:: Get \_ подобия

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`get_Similarity`Метод извлекает диапазон цветовых данных, которые становятся прозрачными. При более высоких значениях более широкий диапазон похожих цветов является прозрачным. Это свойство применяется только в том случае, если тип ключа — ДКСТКЭЙ \_ RGB или дксткэй \_ нонред.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_Similarity(
  [out, retval] int *pVal
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Pval* \[ out, retval\]
</dt> <dd>

Получает значение подобия.

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

[**Идксткэй:: Get \_ KeyType**](idxtkey-get-keytype.md)
</dt> </dl>

 

 




