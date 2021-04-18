---
description: Метод Фрипропс освобождает ресурсы, выделенные методом Ипропертисеттер::. Вызовите этот метод после вызова метода "PROPS", передав ему структуры, возвращаемые методами PROPS.
ms.assetid: 5920d63d-d8eb-4fd5-b0d6-9d175e8e2c86
title: 'Метод Ипропертисеттер:: Фрипропс (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.FreeProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3cc90d094d3213b5b68f61585296bcb21ebbf5a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675025"
---
# <a name="ipropertysetterfreeprops-method"></a>Метод Ипропертисеттер:: Фрипропс

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`FreeProps`Метод освобождает ресурсы, выделенные методом [**ипропертисеттер:: "PROPS**](ipropertysetter-getprops.md) ". Вызовите этот метод после вызова метода " **PROPS**", передав ему структуры, возвращаемые методами **PROPS**.

## <a name="syntax"></a>Синтаксис


```C++
void FreeProps(
  [in] LONG         cParams,
  [in] DEXTER_PARAM *paParam,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кпарамс* \[ окне\]
</dt> <dd>

Число элементов в массиве *папарам* .

</dd> <dt>

*папарам* \[ окне\]
</dt> <dd>

Указатель на массив структур [**\_ param Декстер**](dexter-param.md) .

</dd> <dt>

*павалуе* \[ окне\]
</dt> <dd>

Указатель на массив структур [**\_ значений Декстер**](dexter-value.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

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

[**Интерфейс Ипропертисеттер**](ipropertysetter.md)
</dt> <dt>

[Коды ошибок и успешности](error-and-success-codes.md)
</dt> </dl>

 

 




