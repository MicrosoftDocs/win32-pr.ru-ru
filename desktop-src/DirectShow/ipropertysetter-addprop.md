---
description: Метод Аддпроп добавляет свойство в установщик свойств с массивом пар "время — значение", определяющим значение свойства за определенный период времени.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Метод Ипропертисеттер:: Аддпроп (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675027"
---
# <a name="ipropertysetteraddprop-method"></a>Метод Ипропертисеттер:: Аддпроп

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`AddProp`Метод добавляет свойство в установщик свойств с массивом пар "время — значение", определяющим значение свойства за определенный период времени.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Параметр* \[ окне\]
</dt> <dd>

[**Декстер \_ Структура PARAM**](dexter-param.md) , указывающая свойство. Элемент **nзначения** структуры должен равняться размеру массива, заданного в параметре *павалуе* .

</dd> <dt>

*павалуе* \[ окне\]
</dt> <dd>

Указатель на массив структур [**\_ значений Декстер**](dexter-value.md) , содержащих пары "время — значение". Массив должен быть в порядке возрастания времени. Время задается относительно времени начала действия или перехода.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Первая структура [**\_ значения Декстер**](dexter-value.md) должна задавать время ссылки, равное нулю, и флаг интерполяции (**двинтерп**) **\_ перехода декстерф** или метод возвращает ошибку.

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

 

 




